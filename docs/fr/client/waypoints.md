# **Waypoints**

!!! warning "Translation needed for 6.0"

    This page was updated for JourneyMap 6.0 in English. Translation
    is pending; the content shown is the English source. See
    Contributing to help translate the docs.

Waypoints let you mark specific locations on your map so you can keep
track of them or find your way back to them later.

Death waypoints are created automatically when you die, so you can
return to collect your items. Death waypoints can be disabled in the
[settings manager](settings/waypoint.md) if you prefer.

By default a waypoint is shown in the world as a colored beacon beam,
with its name and icon displayed when you look towards it. This and
many other behaviors can be changed in the
[Waypoint settings](settings/waypoint.md) and
[Waypoint Beacon settings](settings/waypoint-beacon.md).

![Waypoint](../img/waypoint.png){: .center}

## **Creating Waypoints**

You can create a waypoint in any of these ways:

- Press ++b++ in-game to create a waypoint where you are standing.
- Double-click, or press ++b++, in the [full-screen map](full-screen-map.md)
  to create a waypoint at the cursor.
- Open the Waypoint Manager and use the **New** button.

Each method opens the [Waypoint Editor](#the-waypoint-editor) so you can
name and customize the waypoint before saving it.

## **The Waypoint Manager**

The Waypoint Manager is a single place to manage all of your waypoints
and waypoint groups. Open it in either of these ways:

- Press ++n++ in-game or on the full-screen map.
- Open the [full-screen map](full-screen-map.md) and click the Waypoint
  Manager button.

![Waypoint-Manager](../img/waypoint-manager.png){: .center}

The manager has two panels: a list of [groups](#waypoint-groups) on one
side and the waypoints in the selected group on the other. A search box
filters the list as you type.

### Manager buttons

| Button             | Action                                                            |
|--------------------|-------------------------------------------------------------------|
| New                | Create a new waypoint.                                            |
| New Group          | Create a new waypoint group.                                      |
| Options            | Open the [settings manager](settings/overview.md).                |
| Dimension          | Filter the shown waypoints by dimension.                          |
| Import             | Import waypoints from a `.dat` file.                              |
| Import External    | Import waypoints from Xaero's Minimap, if detected.               |
| Export             | Export your waypoints to a file (you choose the format).          |
| Pending            | Review waypoints other players have shared with you.              |
| Close              | Close the Waypoint Manager.                                       |

### Per-waypoint actions

Each waypoint in the list has these actions:

- **Teleport** - if allowed by the server, teleport directly to the waypoint.
- **Find** - locate the waypoint on the [full-screen map](full-screen-map.md).
- **On/Off** - toggle the waypoint's visibility.
- **Edit** - open the [Waypoint Editor](#the-waypoint-editor).
- **Remove** - delete the waypoint.
- **Chat** - share the waypoint (see [Sharing Waypoints](#sharing-waypoints)).

### Selecting multiple waypoints

Use **Select All**, or select individual waypoints, to act on several at
once. With a selection active you can **Toggle Selected**,
**Share Selected**, or **Delete Selected**.

## **The Waypoint Editor**

The Waypoint Editor opens whenever you create or edit a waypoint.

![Waypoint-Edit](../img/waypoint-edit.png){: .center}

The editor provides these fields:

- **Name** - the display name for the waypoint.
- **Location** - the X, Y, and Z coordinates. You can switch between
  separate X / Y / Z fields and a single combined `X, Y, Z` field using
  the Coordinate Layout option (see below).
- **Dimensions** - toggles for the dimensions the waypoint is shown in.
- **Group** - the [group](#waypoint-groups) this waypoint belongs to.
  You can also create a new group from here.
- **Enable** - whether the waypoint is enabled and visible.
- **Color** - the waypoint color. Click the color wheel to pick a color,
  or use **Randomize** for a new random color.
- **Icon** - click the icon button to choose the waypoint's icon. See
  [Waypoint Icons](#waypoint-icons).
- **Description** - opens a popup for a longer free-text description.

Buttons:

- **Reset** - undo your unsaved edits to this waypoint.
- **Save** - save your changes.
- **Close** - close the editor without saving.

### Editor options

The **Waypoint Editor Options** button configures the editor itself
rather than a single waypoint. It includes the **Coordinate Layout**
option, which switches between separate X / Y / Z input fields and a
single combined `X, Y, Z` field.

## **Waypoint Groups**

Waypoint groups let you organize waypoints into named sets - for example
`Bases`, `Mining`, or `Villages`. A group can be enabled or disabled as
a whole, given its own icon, and marked as the default group for new
waypoints.

JourneyMap has several built-in groups: `Default` (where new waypoints
go unless you choose otherwise), `Death` (death waypoints), and `Temp`
(temporary waypoints). The `All` view shows every waypoint regardless of
group.

!!! note "More detail"

    Groups are a large feature with their own management screen. Full
    coverage lives on the [Waypoint Groups](waypoint-groups.md) page.

## **Waypoint Icons**

JourneyMap ships with a set of built-in waypoint icons, selectable from
the icon button in the Waypoint Editor. When many icons are available
(for example from a resource pack) JourneyMap shows a dedicated icon
selection menu so you can browse them.

You can add your own waypoint icons with a resource pack. See
[Waypoint Icons (Resource Packs)](../tools/waypoint-icons.md).

## **Server-Managed Waypoints**

When you play on a server that runs JourneyMap, the server can manage
waypoints itself. In that case waypoints have a **scope**:

- **Personal** - your own waypoints, visible only to you.
- **Global** - waypoints managed by the server and shared with players,
  set up by server admins.

The Waypoint Manager shows a scope selector when server-managed
waypoints are available. See
[Server Multiplayer settings](../server/multiplayer.md) for the
server-side options.

## **Teleporting to Waypoints**

If the server allows it, the **Teleport** action in the Waypoint Manager
takes you directly to a waypoint. Teleporting is controlled per
dimension by server admins, so it may be available in some dimensions
and not others. In single-player it is always available.

The teleport command JourneyMap uses can be customized, and there is an
option to strip decimal places from the coordinates it sends. See the
[Waypoint settings](settings/waypoint.md).

## **Sharing Waypoints**

You can share a waypoint or location with other players. Players who do
not have JourneyMap still see the location in chat in a readable format.

There are three ways to share:

1. In the Waypoint Manager, use the **Chat** button next to a waypoint
   (or **Share Selected** for several). The location is placed in the
   chat input for you - add a message if you like, then press Enter.
2. In the chat input, type `/jm ~` and press Enter. It is replaced with
   your current location.
3. Type a location manually in chat between square brackets (see
   [Location Format](#location-format) below).

When a properly formatted location appears in chat, **click** it to
create a waypoint, or **control-click** it to view the location on the
full-screen map.

![Waypoint-Chat](../img/waypoint-chat.png){: .center}

Waypoints shared directly with you arrive as **Pending** waypoints. Open
the **Pending** button in the Waypoint Manager to **Accept** or
**Decline** each one.

### Location Format

A location must have at least the x and z coordinates. The order of the
values does not matter:

- `[x:#, z:#]`
- `[x:#, y:#, z:#]`
- `[x:#, y:#, z:#, dim:#]`
- `[x:#, y:#, z:#, dim:#, name:text]`
- `[name:text, dim:#, x:#, z:#, y:#]`

A location is two or more `name:value` pairs separated by commas. The
supported values are:

- `x` (integer) **required**
- `y` (integer)
- `z` (integer) **required**
- `dim` (integer)
- `name` (string, no quotes, no commas)

## **Waypoint Commands**

JourneyMap's chat commands live under the `/jm` prefix.

`/jm reload` reloads the waypoint files from disk without restarting the
game. This is mainly useful after dropping waypoint files into the
waypoint folder while the game is running.

When the server runs JourneyMap, server-side waypoint commands are also
available under `/jm waypoint` (or `/jm wp`). See the
[server waypoint command](../server/commands/waypoint_command.md) page.

## **Backups and Importing**

JourneyMap protects your waypoint data in several ways:

- **Rolling backups** - JourneyMap keeps recent backups of your waypoint
  data and automatically loads the most recent good backup if the main
  file is found to be damaged.
- **Import / Export** - use the Import and Export buttons in the
  Waypoint Manager to back up your waypoints to a file or restore them.
- **Drop-in merge** - drop a waypoint `.dat` file into the waypoint
  folder and JourneyMap merges its waypoints into your existing data.
  Run `/jm reload`, or reconnect, to pick up files added while playing.
- **Import from Xaero's** - if Xaero's Minimap waypoints are detected,
  the **Import External** button imports them.

## **Show On Locator Bar**

!!! info "26.1 only"

    The locator bar is a Minecraft 1.21.6+ feature, so this option is
    only present in JourneyMap for Minecraft 26.1. It is not available
    on the 1.21.1 line.

Waypoints can be shown on Minecraft's locator bar. This is controlled by
a **Show On Locator Bar** option, available both globally and per
[group](waypoint-groups.md). Disabled waypoints are not shown on the
locator bar.

![Locator-Bar](../img/client/locator-bar.png){: .center}

## **Settings**

Waypoint behavior is configured in two settings categories:

- [Waypoint settings](settings/waypoint.md) - death waypoints, the
  teleport command, sharing, and more.
- [Waypoint Beacon settings](settings/waypoint-beacon.md) - how waypoint
  beacons and labels are drawn in the world.
