## **Custom Mobs on the map (mob radar)**

JourneyMap categorizes entities for the radar by their Minecraft entity type and category, not by any custom interface you implement.

- Hostile, passive, ambient, and NPC entities are recognized automatically from their vanilla entity class (for example `PathfinderMob`, `Animal`, `WaterAnimal`, `Villager`, and the `Enemy` and `Npc` marker interfaces).
- An entity that currently has an attack target is shown as hostile, even if it is normally passive.
- Entities that are invisible to the player (including sneaking players) are hidden on the radar.
- If you want to provide your own mob icons, see [Custom Mob Icon Sets](custom-mob-icons.md).

!!! note "Note"

    If your mod uses an unusual entity class that JourneyMap does not pick up automatically, you can register it through the JourneyMap API (see below) using the entity registration event.

## **Create waypoint suggestions in chat**

Players can add waypoints by clicking on specially-formatted text in chat.  (Handy for giving quests, welcome messages, etc.)

For example:

`NPC says: "Here's where I buried my loot:" [name:treasure, x:1212, y:70, z:456, dim:0]`

The chat text itself is not changed, but is turned into a link for players with JourneyMap.  Hover text shows it can be clicked to create a waypoint, or shift-clicked to show on the full screen map.

A location is two or more `name:value` pairs inside square brackets, separated by commas.  The `x` and `z` coordinates are required; `y`, `dim`, and `name` are optional.  The order of the pairs does not matter.  See [Sharing Waypoints](../client/waypoints.md#location-format) on the client Waypoints page for the full format.

!!! note "Note"

    If `dim` is omitted, the dimension of the player is assumed.

## **Display custom shapes, text, or waypoints on the map**

The [JourneyMap API](https://github.com/TeamJM/journeymap-api) gives mod authors the ability to manage custom waypoints and draw overlays (polygons, markers, and images) on the minimap, fullscreen map, and webmap.

Add the API as a dependency, implement a plugin class, and register for the events you care about.  The API repository includes an example mod that demonstrates a working integration.

## **What is new for integrators in 6.0**

JourneyMap 6.0 ships a reworked API.  Highlights for mod authors:

- **API v2** - the API now lives under the `journeymap.api.v2` package.  Update your imports and plugin registration accordingly.
- **More events** - new client and server events cover waypoint lifecycle (create, update, delete), waypoint groups, group transfer, the entity radar, fullscreen rendering, popup menus, and server-side global waypoints and waypoint groups.  Register through the v2 event registries.
- **Component-based InfoSlot registration** - addons register custom info slots through the registry event.  Slot labels are now Minecraft chat `Component`s rather than plain strings.
- **Keyed custom data on waypoints and waypoint groups** - waypoints and groups support typed, keyed custom data so addons can attach their own values without colliding with each other or with JourneyMap.  The older single-value custom data accessors are deprecated.
- **ShapeProperties.strokePosition** - shape overlays can set where the stroke is drawn relative to the edge (inside, centered, or outside).
- **EntityDTO icons** - entity icon paths are exposed as Minecraft resource locations, making it easier to point at your own icon textures.

!!! note "Note"

    This page is an overview.  For exact class and method names, see the API source and the example mod in the [journeymap-api repository](https://github.com/TeamJM/journeymap-api), which is the authoritative reference and tracks each release.

## **When in doubt, talk to us!**

Get in touch with the JourneyMap @Developers team on the public [JourneyMap Discord server](https://discord.gg/eP8gE69).
