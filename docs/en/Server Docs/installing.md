## **Installing**

JourneyMap Server is an optional server-side utility for Forge, Fabric and Bukkit servers. As of JourneyMap 5.1.1, the server-side mod comes in the same jar as the JourneyMap client with Forge and Fabric.  

## **Textual Guide**

1. Put the JourneyMap.jar in your **server mods** folder: ```(server folder)/mods```
2. The first time you start the server after installing JourneyMap, a new config file will be generated in ```(server folder)/journeymap/server/<version>/journeymap.server.minecraft~<world>.config```
3. Clients that are connected will be automatically connected to the worldid. This results in the creation of a new folder by the client to store waypoints and map images: ```.minecraft/journeymap/data/mp/(server_worldid)```

## **Legacy Versions Below**
!!! note "Legacy"
    The following only pertains to version pre JourneyMap version 5.5.5, before the Server Admin screen was added to JourneyMap.

1. Put the JourneyMap .jar in your **server mods** folder: ```(server folder)/mods/```
2. The first time you start the server after installing **1.0RC4** or later, a new config file will be generated in ```(server folder)/configs/JourneyMapServer/(world).cfg```  **If you had previously used 1.0RC3** or earlier, you will need to update this new config file with the settings from your old config file.  We apologize for the inconvenience.
3. If you do not want to use the randomly-generated worldid, run the command: “/jmserver worldid set <name>” in the console or within the game as an admin.
4. Clients that are connected will be automatically updated to the new worldid.  This results in the creation of a new folder by the client to store waypoints and map images: ```minecraft**'/journeymap/data/mp/(server_worldid).```  **New in client 5.0.0RC4**:  If this is the first time a World ID is assigned, the client will automatically migrate existing waypoints and map images to the new folder.