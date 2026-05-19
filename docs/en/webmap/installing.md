# **Installing the Webmap**

The Webmap lets you view your JourneyMap map in a web browser instead of
in-game. It is useful for showing the map on a second monitor, a tablet,
or any other device on your local network.

As of JourneyMap 6.0 the Webmap is a separate addon mod. It is no longer
bundled with JourneyMap itself, so you install two mods: JourneyMap and
the JourneyMap Webmap addon.

!!! info "Client-side only"

    The Webmap is a client-side addon. Adding it to a dedicated server
    does nothing - it only serves the map data that JourneyMap collects
    on your own client.

## **Requirements**

- JourneyMap installed (the Webmap is an addon and will not load without
  it).
- The same Minecraft version and mod loader as your JourneyMap install.
  The Webmap is built for Fabric, NeoForge, and Forge.

## **Downloading**

Download the JourneyMap Webmap from either:

- [CurseForge](https://www.curseforge.com/minecraft/mc-mods/journeymap-web-map)
- [Modrinth](https://modrinth.com/project/YaZ1fUTg)

Pick the file that matches your Minecraft version and mod loader.

## **Steps**

1. Install JourneyMap as usual (see [Client Docs > Installing](../client/installing.md)).
2. Download the JourneyMap Webmap addon for the same Minecraft version
   and loader.
3. Place the Webmap jar in the same `mods` folder as JourneyMap.
4. Launch the game. The Webmap is now available; see
   [Basic Usage](basic-usage.md) for how to enable and open it.

## **Source code**

The JourneyMap Webmap is open source:

- [TeamJM/journeymap-webmap](https://github.com/TeamJM/journeymap-webmap) -
  the mod itself.
- [TeamJM/webmap-client](https://github.com/TeamJM/webmap-client) - the
  JavaScript frontend served in the browser.
