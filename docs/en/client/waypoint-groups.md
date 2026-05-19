# **Waypoint Groups**

Waypoint groups let you organize your waypoints into named sets, such as
`Bases`, `Mining`, or `Villages`. Groups are managed from the
[Waypoint Manager](waypoints.md#the-waypoint-manager); the group list is
the panel on one side of the manager.

![Waypoint-Manager](../img/waypoint-manager.png){: .center}

## **Native groups**

JourneyMap has several built-in groups that always exist:

| Group   | Purpose                                                                 |
|---------|-------------------------------------------------------------------------|
| Default | New waypoints go here unless you pick another group.                    |
| Death   | Death waypoints created when you die.                                   |
| Temp    | Temporary waypoints.                                                    |
| All     | A virtual view that shows every waypoint regardless of its group.       |

When you play on a server that manages waypoints, a **Global** group is
also shown for the waypoints the server shares with players.

Native groups are **locked**: their names cannot be changed. They can
still be configured in other ways (see below).

## **Creating a group**

Use the **New Group** button in the Waypoint Manager, or the
**New Group** option in the [Waypoint Editor](waypoints.md#the-waypoint-editor),
to create a custom group. Custom groups can be renamed, edited, and
deleted freely.

## **Group actions**

Each group in the list has these actions:

- **Enable / Disable Group** - toggle every waypoint in the group on or
  off at once.
- **Edit Group** - open the Edit Group screen (see below).
- **Delete Group** - delete the group. (Native groups cannot be deleted.)

## **Editing a group**

![Group-Edit](../img/client/group-edit.png){: .center}

The **Edit Group** screen shows the group's Id, Tag, and waypoint count,
and provides these options:

| Option              | Description                                                                                                |
|---------------------|------------------------------------------------------------------------------------------------------------|
| Name                | The group's display name. Locked (native) groups cannot be renamed.                                        |
| Color Override      | When enabled, every waypoint in the group uses the group's color instead of its own.                       |
| Icon Override       | When enabled, every waypoint in the group uses the group's icon instead of its own.                        |
| Default             | Marks this group as the default group for new waypoints. Only one group can be the default at a time.       |
| Tag                 | Text prefixed onto every waypoint name in the group, both on the map and in the world. Can be left blank.   |
| Locked              | Shown for native groups whose name cannot be edited.                                                       |

### Show on Locator Bar

!!! info "26.1 only"

    The locator bar is a Minecraft 1.21.6+ feature, so this option is
    only present in JourneyMap for Minecraft 26.1. It is not available
    on the 1.21.1 line.

The Edit Group screen also has a **Show on Locator Bar** option, which
shows the group's waypoints on the vanilla locator bar above the hotbar.

## **Default group**

The group marked as **Default** is where new waypoints are placed unless
you choose a different group while creating them. Setting a new default
clears the flag from whatever group held it before, so there is always
exactly one default group.

## **Temporary waypoints**

The `Temp` group holds temporary waypoints. Waypoints can be added to or
removed from the Temp group, which is handy for short-lived markers you
do not want cluttering your permanent groups.

## **Group panel settings**

The **Edit Group Settings** screen controls how the group list itself is
displayed:

| Setting                  | Description                                              |
|--------------------------|----------------------------------------------------------|
| Hide All Group           | Hides the `All` group from the group panel.              |
| Hide Empty Custom Groups | Hides custom groups that contain no waypoints.           |
| Hide Empty Death Group   | Hides the `Death` group when there are no death points.  |
| Hide Empty Temp Group    | Hides the `Temp` group when there are no temp waypoints. |
