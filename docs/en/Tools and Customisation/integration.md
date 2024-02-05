## **Custom Mobs on the map (mob radar)**

- Be sure your EntityCreatures implement at least one of these Minecraft core interfaces: IAnimal, IMob, INpc, or IWaterMob.
- If you want to provide your own mob icons, see [Custom Mob Icon Sets](custom-mob-icons.md).
- EntityCreatures with a hostile target will be shown as hostile.  
- EntityCreatures set invisible (sneaking) will be hidden on the radar.

## **Create waypoint suggestions in chat**

Players can add waypoints by clicking on specially-formatted text in chat.  (Handy for giving quests, welcome messages, etc.)

For example:

`NPC says: "Here's where I buried my loot:" [name:"treasure", x:1212, y:70, z:456, dim:0]`

The chat text itself is not changed, but is turned into a link for players with JourneyMap.  Hover text shows it can be clicked to create a waypoint, or shift-clicked to show on the full screen map.

!!! note "Note"

    ''name'' and ''dim'' are optional. If ''dim'' is omitted, the dimension of the player is assumed.

## **Display custom shapes, text, or waypoints on the map**

There is a [JourneyMap API](https://github.com/TeamJM/journeymap-api) (for Minecraft 1.9.4 and later versions) which gives you the ability to manage custom waypoints and add overlays on the minimap, fullscreen map, or webmap.

## **When in doubt, talk to us!**

Get in touch with the JourneyMap @Developers team on the public [JourneyMap Discord server](https://discord.gg/eP8gE69).
