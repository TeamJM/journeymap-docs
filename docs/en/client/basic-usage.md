## **Basic Usage**

Once you have JourneyMap [installed](installing.md), all you need to do is join a server or load up a single-player world.

For the most part, JourneyMap works right out of the box. All you need to do to start mapping your world is to begin exploring it! The area around you will be mapped automatically as you travel, and will be visible in each of the three types of map that JourneyMap supports.

## **Key Mappings**

The following key mappings are available by default when you are playing on a world or multiplayer server.

- ++j++ - Show or hide the full-screen map
- ++ctrl+j++ - Show or hide the minimap. On Fabric this is ++m++ instead, because Fabric does not support modifier keys for keybinds
- ++equal++ / ++minus++ - Zoom the minimap in and out
- ++bracket-left++ - Cycle the map type shown in the minimap
- ++backslash++ - Switch between minimap presets
- ++b++ - Create [a waypoint](waypoints.md) where you are standing
- ++n++ - Open the [waypoint manager](waypoints.md)
- ++g++ - Toggle entity name labels

JourneyMap also has keybinds for toggling waypoint rendering (all waypoints, in-world only, or on-map only). These are unbound by default - assign them in Minecraft's Controls if you want them.

All keys specified in the documentation can be customized in Minecraft's own settings. Just open the menu (by default, with the ++esc++ key), click on Options and then Controls, and you will see two new categories for all of JourneyMap's keys.

## **Markers**

All map types contain markers. These markers denote various pieces of information - such as the position of an entity or [a waypoint](waypoints.md) on the map.

| Icon                                                          | Description                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| ![Marker-Player](../img/markers/marker-player.png){: .center} | Your position on the map. *Note: This icon has a <br>white border ingame.*     |
| ![Waypoint](../img/markers/waypoint.png){: .center}           | [A waypoint](waypoints.md). The colour can be set in <br>the waypoint manager. |
| ![Waypoint](../img/markers/waypoint-death.png){: .center}     | [A death Waypoint](waypoints.md)                                               |

| Icon                                                                  | Description                                                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| ![Marker-White](../img/markers/marker-white.png){: .center}           | A marker denoting an entity on the map. The colour <br>of the marker denotes the type of entity. |
| ![Marker-White-Down](../img/markers/marker-white-down.png){: .center} | An entity below you.                                                                             |
| ![Marker-White-Up](../img/markers/marker-white-up.png){: .center}     | An entity above you.                                                                             |

| Icon                                                        | Description                       |
|-------------------------------------------------------------|-----------------------------------|
| ![Marker-Grey](../img/markers/marker-grey.png){: .center}   | A neutral entity, like an animal. |
| ![Marker-Green](../img/markers/marker-green.png){: .center} | A villager.                       |
| ![Marker-Blue](../img/markers/marker-blue.png){: .center}   | Another player.                   |
| ![Marker-Red](../img/markers/marker-red.png){: .center}     | A hostile entity, like a monster. |

Markers and their display can be customized in the [settings manager](settings/minimap.md).

## **The Minimap**

By default, the minimap will be displayed in the top-right corner of your screen.

![Minimap](../img/minimap.png){: .center}

This is your minimap. By default, it displays the area around your character, as well as some basic information and the positions of your character, other players, animals and monsters.

The minimap can be zoomed in and out at any time by pressing either of the zoom keys (by default, the ++equal++ and ++minus++ keys).

The text above and below the minimap is shown in info slots. There are four of them. By default they show:

- Slot 1: nothing (blank)
- Slot 2: the in-game time
- Slot 3: your coordinates
- Slot 4: the biome you are in

The minimap and its info slots may be customized in the [settings manager](settings/minimap.md).

## **The Full-Screen Map**

By pressing the full-screen map key (by default, the J key), you can open the full-screen map.

![Full-Screen-Map](../img/full-screen.png){: .center}

This map gives you a scrollable view of all the areas of the map you have explored so far, displayed as it was when you discovered them. It also provides access to JourneyMap's Settings and a number of map display options.

For more information on the full-screen map, please see the [full-screen map page](settings/full-screen-map.md).

## **The Webmap**

The webmap lets you view and explore your map in a web browser, including from another device such as a phone or tablet, while the game is running. As of JourneyMap 6.0 the webmap is a separate addon mod.

![Webmap](../img/webmap.png){: .center}

See the [Webmap](../webmap/installing.md) section for how to install and use it.
