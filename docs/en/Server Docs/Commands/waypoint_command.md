# **Waypoint Commands**

Commands allows you to create and delete waypoints from the chat.

Note: <u>It will not be ported to older versions</u>

- Command: waypoint
- Alias: wp

**Create Waypoint**

```text
fields in [] are optional -> 
[player] is the target player, if no player is specified, it will show an error.
[announce] is whether the player has a notification that a waypoint is being created, if it is not specified, defaults to false it is created silently.
- /waypoint create "name" dimension x y z color [player] [announce]
- /waypoint delete "name" [player] [announce]
```

**Examples**

```text
-   /waypoint create "Spawn" minecraft:overworld 1 50 12 aqua
-   /waypoint create "Home" minecraft:overworld 1 50 12 aqua mysticdrew
-   /waypoint create "Home" minecraft:overworld 1 50 12 aqua true~~  currently bugged in v5.8.x
-   /waypoint create "Home" minecraft:overworld 1 50 12 aqua mysticdrew true
```

**Delete Waypoint**

Note: <u>Only deletes waypoints created by command</u>

```text
/waypoint delete "WaypointName"
/waypoint delete "WaypointName" true
/waypoint delete "WaypointName" mysticdrew
/waypoint delete "WaypointName" mysticdrew true
```

**As of JourneyMap 5.9.0**

All waypoint commands require use of the player field. It takes a player or a list of players or `@a` for both create and delete.
