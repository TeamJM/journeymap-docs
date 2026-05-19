# **Waypoint Command**

When JourneyMap is installed on the server, server admins can create and
delete waypoints on players' clients from the chat.

All JourneyMap server commands live under the `/jm` prefix. The waypoint
command is `/jm waypoint`, with `/jm wp` as a shorter alias.

## **Permissions**

The command can be used by:

- Players at permission level 2 (GAMEMASTERS) or higher.
- Players in the JourneyMap server admin list.
- Anyone in single-player.

## **Create a waypoint**

```text
/jm waypoint create "name" <dimension> <x> <y> <z> <color> <players> [announce]
```

- `"name"` - the waypoint name, in quotes.
- `<dimension>` - the dimension id, for example `minecraft:overworld`.
- `<x> <y> <z>` - the waypoint coordinates.
- `<color>` - a Minecraft color name, for example `aqua`.
- `<players>` - the target player or players. Accepts a player name, a
  list of players, or `@a` for everyone. This argument is required.
- `[announce]` - optional. `true` notifies the player that a waypoint
  was created; defaults to `false` (created silently).

### Examples

```text
/jm waypoint create "Spawn" minecraft:overworld 1 50 12 aqua @a
/jm waypoint create "Home" minecraft:overworld 1 50 12 aqua mysticdrew
/jm waypoint create "Home" minecraft:overworld 1 50 12 aqua mysticdrew true
```

## **Create a temporary waypoint**

Add `temp` before `create` to create a temporary waypoint, which is not
saved to disk:

```text
/jm waypoint temp create "name" <dimension> <x> <y> <z> <color> <players> [announce]
```

## **Delete a waypoint**

```text
/jm waypoint delete "name" <players> [announce]
```

- `"name"` - the name of the waypoint to delete.
- `<players>` - the target player or players. Required.
- `[announce]` - optional. `true` notifies the player; defaults to
  `false`.

Only waypoints created by the command can be deleted by the command.

### Examples

```text
/jm waypoint delete "Home" @a
/jm waypoint delete "Home" mysticdrew
/jm waypoint delete "Home" mysticdrew true
```
