## **Config File Options**

The config file is located here: ```(server folder)/configs/JourneyMapServer/(world).cfg```. The following options in the config file can be modified to suit your needs. Changes require a server restart.

See [Feature.java](https://github.com/TeamJM/journeymap-api/blob/1.12/src/main/java/journeymap/common/api/feature/Feature.java) for a brief description of each feature.

```
{
  "enabled": true,
  "policies": {
    "Action.Teleport": {
      "survival": false, "creative": true, "adventure": false, "spectator": false
    },
    "Display.Compass": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "Display.Fullscreen": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "Display.Minimap": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "Display.WaypointBeacon": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "Display.WaypointManager": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "Display.Webmap": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "MapType.Day": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "MapType.Night": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "MapType.Underground": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "MapType.Topo": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "MapType.Biome": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "Radar.HostileMob": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "Radar.NPC": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "Radar.PassiveMob": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "Radar.Player": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "Radar.Vehicle": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    },
    "Radar.Waypoint": {
      "survival": true, "creative": true, "adventure": false, "spectator": false
    }
  }
}
```
