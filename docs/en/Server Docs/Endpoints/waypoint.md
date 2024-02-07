# **Waypoints**

The External Waypoint Packet Listener is a feature that allows the server to send waypoints to the client. This is useful for server admins who want to provide waypoints to players without requiring an addon mod.

## **Examples**

Below is an example of what the packet json looks like and what information the server sends to the client to process and interpret.

Packet Identifier

```text
discriminator:0
channel:journeymap:waypoint
```

Packet Buffer

```text
waypoint StringUtf  value -> waypointjson.toString();
action StringUtf  value-> "create" or "delete"
announce Boolean -> value true or false  : Announce determines if the user is notified when a waypoint is created or deleted. 
```

Packet Reader (journeymap's client code)

```text
this.waypoint = buf.readUtf();
this.action = buf.readUtf();
this.announce = buf.readBoolean();
```

**Example Create Payload**

```json
{
  "id": "home_-10,70,32",
  "name": "home",
  "icon": "journeymap:ui/img/waypoint-icon.png",
  "enable": true,
  "type": "Normal",
  "origin": "external",
  "x": -10,
  "y": 70,
  "z": 32,
  "r": 85,
  "g": 255,
  "b": 255,
  "persistent": false,
  "dimensions": [
    "minecraft:overworld"
  ]
}
```

```text
id -> <code>id = "name + "_" + x + "," + y + "," + z"</code> this format is required.<br>
name -> waypoint name<br>
icon -> <code>journeymap:ui/img/waypoint-icon.png</code> this is required<br>
enable -> required to be true<br>
type -> <code>Normal</code>  or <code>Death</code><br>
origin -> <code>external</code> or <code>external-force</code> external-force cannot be disabled/hidden on the client<br>
x -> x coord<br>
y -> y coord<br>
z -> z coord<br>
r -> red value<br>
g -> green value<br>
b -> blue value<br>
persistent -> <code>true</code> saves to disk, will load when the user restarts minecraft, or changes dimensions. <code>false</code> is not saved to disk, is removed from memory when the user exists minecraft<br>
dimensions -> list of dimensions<br>
```

**Example Delete Payload**

```json
{
  "name": "test"
}
```

name -> waypoint name is all that is required to delete the waypoint. 
Example implementation using CraftBukkit

```java
    public static void createWaypoint(Player player, String name, IntVector3 pos, WaypointType type, ChatColor color) {
        Color rgb = color.getColor();
        JsonObject obj = new JsonObject();
        obj.addProperty("id", name + '_' + pos.getX() + ',' + pos.getY() + ',' + pos.getZ());
        obj.addProperty("name", name);
        obj.addProperty("icon", "waypoint-normal.png");
        obj.addProperty("enable", true);
        obj.addProperty("type", type.type);
        obj.addProperty("origin", "external");
        obj.addProperty("x", pos.getX());
        obj.addProperty("y", pos.getY());
        obj.addProperty("z", pos.getZ());
        obj.addProperty("r", rgb.getRed());
        obj.addProperty("g", rgb.getGreen());
        obj.addProperty("b", rgb.getBlue());
        obj.addProperty("persistent", false);

        JsonArray dimensions = new JsonArray(1);
        dimensions.add("minecraft:" + player.getWorld().getName());
        obj.add("dimensions", dimensions);

        PacketDataSerializer out = new PacketDataSerializer(Unpooled.buffer());
        out.writeByte(0); // Extra Byte for Forge
        out.a(obj.toString()); // Payload
        out.a(CREATE); // Action
        out.writeBoolean(false); // Announce
        player.sendPacket(new PacketPlayOutCustomPayload(WAYPOINT_KEY, out));
    }

    public static void deleteWaypoint(Player player, String name) {
        JsonObject obj = new JsonObject();
        obj.addProperty("name", name);
        obj.addProperty("origin", "external");

        PacketDataSerializer out = new PacketDataSerializer(Unpooled.buffer());
        out.writeByte(0); // Extra Byte for Forge
        out.a(obj.toString()); // Payload
        out.a(DELETE); // Action
        out.writeBoolean(false); // Announce
        player.sendPacket(new PacketPlayOutCustomPayload(WAYPOINT_KEY, out));
    }
```

If you have the PacketDataSerializer (PacketBuffer) deobfuscated it would most likely use buffer.writeString(...) rather than buffer.a(...)
If you want to use a different buffer/write manually the internals of that method are something like:

```java
    public PacketDataSerializer writeString(String s, int byteLimit) {
        
        byte[] bytes = s.getBytes(StandardCharsets.UTF_8);
        if (bytes.length > byteLimit) {
            throw new EncoderException("String too big (was " + bytes.length + " bytes encoded, max " + byteLimit + ")");
        } else {
            
            this.writeVarInt(bytes.length);
            this.writeBytes(bytes);
            return this;
        }
    }
```
