
!!! warning "Translation needed for 6.0"

    This page was updated for JourneyMap 6.0 in English. Translation
    is pending; the content shown is the English source. See
    Contributing to help translate the docs.

## **Installing**

Installing JourneyMap on the server is optional. It adds utility for
server admins: it lets them restrict some client features per dimension,
manage waypoints, and support multi-world setups. JourneyMap clients on
any loader can connect to a server running JourneyMap regardless of
which loader the server uses.

## **Fabric, NeoForge, and Forge servers**

1. Put the JourneyMap jar in your server's `mods` folder:
   `(server folder)/mods`
2. The first time you start the server after installing JourneyMap, a
   config file is generated under
   `(server folder)/journeymap/server/<version>/`.
3. Connected clients are automatically associated with the server's
   world id. Each client creates a folder to store its waypoints and
   map images: `.minecraft/journeymap/data/mp/(server_worldid)`

## **Paper servers**

!!! info "Minecraft 26.1 and 26.2 only"

    The Paper build of JourneyMap is available for the Minecraft 26.1 and
    26.2 builds of JourneyMap 6.0. It is not available for the 1.21.1 or
    1.21.11 builds.

On Paper servers, JourneyMap ships as a plugin rather than a mod. Place
the JourneyMap Paper jar in your server's `plugins` folder instead of
`mods`. The config and per-world behavior are otherwise the same as the
mod-loader builds.

## **Server commands**

JourneyMap's server commands live under the `/jm` prefix. The main one
is the waypoint command, `/jm waypoint` (alias `/jm wp`), documented on
the [Waypoint Command](commands/waypoint_command.md) page.
