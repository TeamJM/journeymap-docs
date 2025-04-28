# **Points de Repère**

Le **Listener de Paquet de Point de Repère Externe** est une fonctionnalité qui permet au serveur d'envoyer des points de repère au client. Cela est utile pour les administrateurs de serveur qui souhaitent fournir des points de repère aux joueurs sans nécessiter un mod d'extension.

## **Exemples**

Voici un exemple de ce à quoi ressemble le JSON du paquet et quelles informations le serveur envoie au client pour traitement et interprétation.

### Identifiant de Paquet

```text
discriminator:0
channel:journeymap:waypoint
```

### Tampon de Paquet

```text
waypoint StringUtf  value -> waypointjson.toString();
action StringUtf  value-> "create" ou "delete"
announce Boolean -> value true ou false  : Annonce détermine si l'utilisateur est notifié lors de la création ou de la suppression d'un point de repère. 
```

### Lecteur de Paquet (code du client de journeymap)

```text
this.waypoint = buf.readUtf();
this.action = buf.readUtf();
this.announce = buf.readBoolean();
```

## **Exemple de Charge Utile de Création**

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
id -> <code>id = "nom + "_" + x + "," + y + "," + z"</code> ce format est requis.<br>
name -> nom du point de repère<br>
icon -> <code>journeymap:ui/img/waypoint-icon.png</code> ceci est requis<br>
enable -> requis d'être true<br>
type -> <code>Normal</code>  ou <code>Death</code><br>
origin -> <code>external</code> ou <code>external-force</code> external-force ne peut pas être désactivé/caché sur le client<br>
x -> coordonnée x<br>
y -> coordonnée y<br>
z -> coordonnée z<br>
r -> valeur rouge<br>
g -> valeur verte<br>
b -> valeur bleue<br>
persistent -> <code>true</code> sauvegarde sur le disque, sera chargé lorsque l'utilisateur redémarre Minecraft, ou change de dimensions. <code>false</code> n'est pas sauvegardé sur le disque, est supprimé de la mémoire lorsque l'utilisateur quitte Minecraft<br>
dimensions -> liste des dimensions<br>
```

## **Exemple de Charge Utile de Suppression**

```json
{
  "name": "test"
}
```

Le nom du point de repère est tout ce qui est requis pour supprimer le point de repère. 

### Exemple d'implémentation utilisant CraftBukkit

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
    out.writeByte(0); // Octet supplémentaire pour Forge
    out.a(obj.toString()); // Charge utile
    out.a(CREATE); // Action
    out.writeBoolean(false); // Annonce
    player.sendPacket(new PacketPlayOutCustomPayload(WAYPOINT_KEY, out));
}

public static void deleteWaypoint(Player player, String name) {
    JsonObject obj = new JsonObject();
    obj.addProperty("name", name);
    obj.addProperty("origin", "external");

    PacketDataSerializer out = new PacketDataSerializer(Unpooled.buffer());
    out.writeByte(0); // Octet supplémentaire pour Forge
    out.a(obj.toString()); // Charge utile
    out.a(DELETE); // Action
    out.writeBoolean(false); // Annonce
    player.sendPacket(new PacketPlayOutCustomPayload(WAYPOINT_KEY, out));
}
```

Si vous avez le **PacketDataSerializer** (PacketBuffer) désobfusqué, il utiliserait probablement `buffer.writeString(...)` plutôt que `buffer.a(...)`. Si vous souhaitez utiliser un tampon différent / écrire manuellement, les détails internes de cette méthode ressemblent à :

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