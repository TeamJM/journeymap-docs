## **Overview**

You don't have to have JourneyMap Server installed to use the JourneyMap Client. It simply provides a way for server admins to restrict some features, and/or support Bukkit Multiworld and BungeeCord installations. Some features may not be available in both Forge and Bukkit server environments, however, so please read the information on this page and the changelogs for each release to get specific information on features for your server.

## **Server Admin Config**

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
