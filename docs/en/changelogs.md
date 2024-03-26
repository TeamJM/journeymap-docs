# **Changelogs**

This page shows all the changelogs from JourneyMap 5.9.0 to 5.9.24 which is the latest version of JourneyMap so far.

## **JourneyMap 5.9.24**

- Fixed: unintentional bug that prevent map updates with the performance release effecting some, but not all versions released.

## **JourneyMap 5.9.23**

- Fixed: Changed the performance update to be even better.
- Fixed: Version numbers that had p1 which was breaking for fabric mods that depended on journeymap.

## **JourneyMap 5.9.22**

- Fixed: Minimap rotation causing the screen hud to rotate, this fix also fixes some other weird issues with minimap.
- Fixed: Added a 3s delay to deathpoint creation.

## **JourneyMap 5.9.21**

- Fixed: [ModCompat] ViveCraft key bindings.
- Fixed: Minimap rendering logic bug.
- Fixed: Removed some unnecessary class allocations that can have a severe impact on performance.

## **JourneyMap 5.9.20**

- Fixed: Waypoint Manager and Options Screen scrolling. (another fix)

## **JourneyMap 5.9.19**

- Fixed: Minimap Position Screen.
- Fixed: Options Screen scrolling and position.

## **JourneyMap 5.9.18**

- Fixed: Minimap Position Screen.
- Fixed: Options Screen scrolling and position.

## **JourneyMap 5.9.17**

- Fixed: Addressed some mod interaction issues.
- Support for 1.20.3 and 1.20.4

## **JourneyMap 5.9.16**

- Fixed: [Fabric] Screen Layering breaking fabric onclose event.
- Fixed: Sending packets while client is not ready.

## **JourneyMap 5.9.15**

- Fixed: Fullscreen map issues on Mac Retina displays.
- Fixed: Server disconnect when packet is sent too early.
- Fixed: Disabling Day/Night cycle prevents radar updates.

## **JourneyMap 5.9.14**

- Fixed: Discord chat bot mod compatibility issue.
- Fixed: Rare minimap texture failure.
- Fixed: Info Slot tooltip not getting translated.
- Support for NeoForge and 1.20.2

## **JourneyMap 5.9.13**

- Fixed: [Fabric] Waypoint icons not displaying through some objects.
- Fixed: Old waypoint migration issues.
- Fixed: AutoMap breaking if a malformed region file is found.
- Fixed: Tamed horses not getting colored correctly on map.
- Fixed: Stained Glass block and pane transparency.
- Langs: Added Italian and Taiwan and updated Korean language files.

## **JourneyMap 5.9.12**

- Fixed: Waypoint command from console.
- Fixed: Block 0,0,0 preventing map opening.
- Fixed: Fullscreen not following correctly when moving from cave to overworld.
- Fixed: Some global server properties not working in dimensions.

## **JourneyMap 5.9.11**

- Fixed: [Fabric] Weird rendering issus when waypoints are showing.
- Fixed: Mouse keybinds work for in-game actions.

## **JourneyMap 5.9.10**

- Fixed: Oculus compatibility issue with waypoint icons.

## **JourneyMap 5.9.9**

- Fixed: Polygons moving when on follow mode.
- Fixed: Options screen going weird on minimap preview.
- Fixed: Multiworld option not working correctly in some instances.
- Fixed: Creating waypoint from fullscreen context ignores first key.

## **JourneyMap 5.9.8**

- Fixed: [Fabric] Fixed issue with right click in recipe window.
- Fixed: Textbox fields are once again selectable with mouse.
- Fixed: [Forge] Waypoint distance not updating past 128m.

## **JourneyMap 5.9.7**

- Fixed: [Quilt] Quilt loader 0.18+ webmap fixes.
- Fixed: API Markers text offsets.
- Fixed: Fake player skin timeout issue.
- Fixed: Default water coloring if mods mess with it.
- Updated to 1.20

## **JourneyMap 5.9.6**

- Fixed: [Fabric] Waypoint chatting disconnecting from server.
- Fixed: Potential issue with fake players breaking getting player heads.

## **JourneyMap 5.9.5**

- Added: Support for Cobblemon resource pack icons. use entity_icon instead of pokemon in the path.
- Updated: Cleaned up lang jsons.
- Fixed: Cave and Surface Render distance sliders.

## **JourneyMap 5.9.4**

- Updated: Long dimension names over 25 characters are compressed.
- Mod Compat: ChinjufuMod leaves not rendering correctly.
- Fixed: MapSaver rendering weird blank images.
- Fixed: Slopes at 0 and below.

## **JourneyMap 5.9.3**

- Fixed: Mod Villager texture exception.
- Fixed: Client Render range larger than Server causing chunks to render black.
- ModCompat: [Fabric] VulkanMod

## **JourneyMap 5.9.2**

- Mod Compat: Create Mod Curved Rails not rendering and Railway Casing color.
- Fixed: Crash when api removes non polygons.
- Fixed: Possible rare crash when creating a new UIState fails.
- Fixed: Bed block rendering.

## **JourneyMap 5.9.1**

- Fixed: Options not displaying tooltips.
- Fixed: Logs displaying what is under them in caves.
- Fixed: More tree and plants added to topo ignore.
- Fixed: Bad chunks breaking cave mapping.

## **JourneyMap 5.9.0**

- Updated: [Fabric] File extraction to support the new "quilt.mfs" file protocol for quilt loader 0.18.1.
- Updated: [Fabric] Fabric loader version backed off to 0.14.10 since 0.14.11 prevented Quilt users from using JM.
- Updated: Webmap now extracts web-content from the jar and places it in the journeymap folder.
- Fixed: Corrupt chunk cache causing mapping failures.
- Fixed: EntityIcons set via EntityRadarUpdateEvent not displaying in webmap.
- Fixed: Tree shadows showing up on topo map.
- Fixed: Automap lighting issues.
- Fixed: Entity names not showing on minimap when heading is changed.
- Fixed: Possible NPE in waypoint manager.
- Fixed: Hopefully fixed compatibility issues for later versions of Immersive Portals.
- Fixed: [1.19.x]: Frog icons
- Fixed: Some logOnce loggers having a throwable when shouldn't.
- Fixed: OptionScreens scrolling bounds.

## **JourneyMap 5.9.0 Beta 5**

- Fixed: UI screens failing due to AbstractMethod errors.
- Fixed: Random textures showing up on empty/blank tiles.

## **JourneyMap 5.9.0 Beta 4**

- Added: [1.19.3] Missing entity icons.(Sandriell)
- Fixed: Waypoint Hide Key not saving waypoint's "enabled" field.
- Fixed: Memory leak when using vanilla mechanics to deserialize chunks for automapping.
- Fixed: Mod-Compat with BBOR
- Fixed: Mod flower colors
- Fixed: Polygon text no longer displays outside of the minimap.
- Fixed: Deathpoint creation when immediate respawn rule is set.

## **JourneyMap 5.9.0 Beta 3**

- Added: Clear Unlit Caves, unlit and inner slice blocks are rendered clear instead of black. Default: False
- Updated: Icon handling for mods that use a path like twilight forest.
- Updated: languages
- Updated: Rendering cleanup.
- Fixed: Fullscreen cave layer slider for worlds with larger than vanilla logical heights.
- Fixed: Mod compat with REI. [Forge]
- Fixed: Slopes below y0.
- Fixed: Custom waypoint tp commands without slash. [1.19.1/2]
- Fixed: Possible class cast exception with waypoint groups via api.

## **JourneyMap 5.9.0 Beta 2**

- Updated: [Fabric] CurseForge Fabric releases to include Quilt Tag.
- Fixed: [Fabric] Download Url Error
- Fixed: Unknown mobs causing screen render issues.
- Fixed: Minimap performance issues when addons draw many polygons on the map
- Fixed: [Fabric] Sending packets if Journeymap is not on the remote side.
- Fixed: Forge 1.19.x Prevent server and client sending packets if the mod is not on the other side. (Requires Minimum Forge Version 1.19.1-42.0.8)
- Fixed: Forge 1.18.2 Prevent server and client sending packets if the mod is not on the other side. (Requires Minimum Forge Version 1.18.2-40.1.70)

## **JourneyMap 5.9.0 Beta 1**

- Uses journeymap-api version 1.9.
NEW: Texture Engine, no longer using buffered images.
- Added: Missing playing panda icon.
- Changed: Waypoint command takes a player, list of players, or @a for all players. It is now required to supply players, announce is still optional.
- Updated: VersionCheck to use java-http-client.
- Fixed: Vertical region grid line not displaying.
- Fixed: Log Spam if biome is null in caves.
- Fixed: ModCompat: Amecs
- Fixed: API multiple show's and removes not displaying overlays.
- Fixed: Automap stopping weirdness.
- Fixed: Textures when shader beacon is enabled but beacons are disabled.
- Fixed: Changing advanced Options causing purist theme to break.
- Fixed: Fabric: Display Update event for api usage.
- Fixed: Fabric: Resizing when layers are displayed.
