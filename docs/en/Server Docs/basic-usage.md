## **Overview**

You don't have to have JourneyMap Server installed to use the JourneyMap Client. It simply provides a way for server admins to restrict some features, and/or support Bukkit Multiworld and BungeeCord installations. Some features may not be available in both Forge and Bukkit server environments, however, so please read the information on this page and the changelogs for each release to get specific information on features for your server.

## **JourneyMap 5.5.5+**

To access the Server Admin Screen open the JourneyMap options screen. As an Opped user there will be a `Server Admin` button at the bottom of the screen.

All Options in the Server Admin Screen have tooltips that explain them in detail.

If the button does not appear, you may need to log out and back into your server if you were recently Opped, or the Admin disabled it in the config file.

By default, all Opped users have access to the Server Admin screen. This can be changed via a config file on the server.

The config file location for Fabric Servers: `(server_folder)/configs/journeymap_server.cfg`.

The config file location for Forge Servers: `(server_folder)/world/serverconfig/journeymap_server.cfg`.

```text
    server {
    # Players in this list have access to the Journeymap's Server Admin Panel
    # Add users by name or UUID, Prefer UUID as it is more secure!
    # Each value on a new line with the example format provided. (please delete the default values)
    S:"Journeymap Server Admins" <
    mysticdrew
    12341234132
    >
    
        # Default, all Ops have access to Server Admin UI in the Options screen.
        # If set to false, only users in the Admin List will have access.
        # If set to true, all ops and users in the Admin List will have access.
        B:"Ops Admin Access"=true
    }
```

## **Legacy Versions Below**

!!! note "Legacy"
The following only pertains to version pre JourneyMap version 5.5.5, before the Server Admin screen was added to JourneyMap.

## **Server control of Radar and Cave Mapping**

- Use server configs to selectively **disable radar** and/or **disable cave mapping **(which includes Nether/End mapping) for users.
- Exceptions can be made to allow these features for just Ops or for lists of individual users (staff, donators, etc.)
- Works with JourneyMap client 4.0.5, 5.0.0+ and the VoxelMap client
- Current functionality uses the color control codes used by VoxelMap, so players who have VoxelMap instead of JourneyMap will be similarly restricted. Conversely, if your server is already sending VoxelMap codes through an MOTD or other mechanism, it may conflict with the options provided by the JourneyMap Server mod.

!!! note "Note"

    This feature currently only works in a Forge server environment. This appears to be an issue with the way color codes are sent from a Bukkit server.  This will be fixed with a later release when the color codes are no longer used.

## **Multi-world Support for Maps and Waypoints**

- **Important note**: If your server doesn't use multiple worlds, you do not need this feature!  Set **UseWorldID=false** in the config file.
- For servers with multiple world folders (not just multiple dimensions) -- usually Bukkit not Forge -- this mod will automatically send a unique **World ID** to users with the JourneyMap client whenever the client loads a world.  This is necessary for servers which use multiple worlds, because it solves <http://www.minecraftforum.net/forums/minecraft-discussion/suggestions/79149-world-uid-for-multi-world-servers> this problem. The JourneyMap client uses the World Id to organize map images and waypoints when traversing between worlds.
- Console commands are provided for server admins to manage the World ID without needing to restart the server.

## **Server Reset**

- If you are resetting / wiping a server world map, it is not recommended to keep a previous World ID for the new world, because users will still have waypoints and map images from their old world map.
- To reset the World ID, simply delete it from the config and a new one will be generated when the server starts up.
- Note: Changing the World ID will result in the creation of a new folder on each JourneyMap 5.x client:  ```minecraft**'/journeymap/data/mp/(server_newworldid).```If the client has already received a different World ID, the user's waypoints and map images will remain in the old folder: ```minecraft**'/journeymap/data/mp/(server_oldworldid).```

## **Console/Chat Commands**

``/jmserver``

* **help** - displays a list of sub commands.
* **worldid** - displays the current world id to the user. (If the config option UseWorldID=true)

* **set** - sets the world id to a user specified string and sends it to all connected clients.
* **setrandom** - sets the world id to a random UUID string and sends to all connected clients
* **resync** - debug command, sends the current world id to all connected clients.  A need to use this is unusual.
* **help** - displays the usage for /jmserver worldid

## **Config File Options**

The config file is located here: ```(server folder)/configs/JourneyMapServer/(world).cfg```

The following options in the config file can be modified to suit your needs. Changes require a server restart:

**"UseWorldID"**

- Valid options: true, false. Default value: true
- **Important note**: If your server doesn't use multiple world folders, you do not need this feature!  Set to **false**.
- When set to false:
    - The server will not send the worldid to the client.
    - All **/jmserver worldid** subcommands will be disabled.

**"WorldID"**

- Valid options: any valid string, no spaces!
- This is the ID that is sent to JourneyMap for unique map instances.
- This value is ignored if UseWorldID is set to false

**"PlayerCaveMapping"**

- Valid options: true, false. Default value: true
- When set to false, users with the JourneyMap client will not have access to cave mapping features, including Nether and End maps.

**"OpsCaveMapping"**

- Valid options: true, false. Default value: true
- When set to true, Op users with the JourneyMap client will be allowed to use cave mapping features even if PlayerCaveMapping is disabled

**"WhitelistCaveMapping"**

- A comma-separated list of usernames that will be allowed to use cave mapping features in the JourneyMap client even if PlayerCaveMapping is disabled
- For example: WhitelistCaveMapping=techbrew,mysticdrew

**"PlayerRadar"**

- Valid options: true, false. Default value: true
- When set to false, users with the JourneyMap client will not have access to radar features.

**"OpsRadar"**

- Valid options: true, false. Default value: true
- When set to true, Op users with the JourneyMap client will be allowed to use radar features even if PlayerRadar is disabled for normal users.

**"SaveInWorldFolder"**

- ''Valid for Forge only. Bukkit servers must keep this value false!''
- Valid options: true, false. Default value: false
- When set to true, the world ID will be saved to a separate file and placed in the world folder, rather than in the config file.
- MCEdu servers must set this to true!  This ensures the world id stays with the world data when it is moved by the launcher.

**"WhitelistRadar"**

- A comma-separated list of usernames that will be allowed to use radar features in the JourneyMap client even if PlayerRadar is disabled
- For example: WhitelistRadar=techbrew,mysticdrew

## **What it is Not**

* This is not a server-side mapping mod.  No maps are created, made, hosted, shared, or even contemplated on the server.
* This is not a way to administer anything other than JourneyMap client features.
* This is neither a hot tub nor a time machine.

## **Modpack Usage**

The JourneyMap Client mod is governed by a [different modpack policy](../About/licensing.md) than the server.

The following applies to the server mod only:

You may include JourneyMapServer in the server-side configuration of a modpack, provided you agree to the following conditions:

1. Your launcher should link directly to a download here on the Curse CDN if it is capable of doing so (ATLauncher, MCUpdater, etc.).  If the launcher cannot link to the file directly, the JourneyMap Server jar file may be rehosted/bundled only for the purposes of your modpack, but not distributed in any other way.
2. You must provide a link to this page for server admins who use your modpack.  Documentation is a good thing.

## **Credits and Complaints**

JourneyMapServer was created by Mysticdrew on behalf of an overworked Techbrew.  All credit goes to Mysticdrew. Complaints should be composed using letters cut out from magazines and newspapers, then sent via snail mail to your local government official inside an envelope containing baking flour.  Be sure to include a return address and recent photo.
