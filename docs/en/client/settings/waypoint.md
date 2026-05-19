# **Waypoint Settings**

This category allows you to change some settings relating to how [waypoints](../waypoints.md) behave and are displayed.
Waypoints also have a number of individual settings - you can find out about those
on [the waypoints page.](../waypoints.md)

![Waypoint-Settings](../../img/settings/client/waypoints.png){: .center}

## **Toggles**

The **bold** toggle settings below are enabled by default.

| Toggle                                              | Description                                                                                                                              |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **Enable Waypoint Manager**                         | Enable the Waypoint Manager. If you use another mod to manage waypoints, you should disable this.                                         |
| Show Delete Confirmation                            | Show a confirmation prompt before deleting a waypoint. This can also be toggled from the delete dialog itself.                            |
| Disable Share                                       | Disables the share button in the Waypoint Manager and in the fullscreen popup menu Chat Position.                                         |
| Disable Strikethrough text                          | Disables the strike through of the waypoint text for disabled waypoints.                                                                  |
| Use Waypoint Actions Button                         | Use a single actions dropdown per waypoint instead of the image button list. Using the single button allows for larger text display.     |
| Open Waypoint Manager in Current Dimension          | Opens the Waypoint Manager focused on the dimension you are currently in.                                                                 |
| **Create Deathpoints**                              | Automatically create a waypoint at the spot where you die.                                                                               |
| Show Player Heads                                   | Show player heads in the world at their location. Only works on a server that has JourneyMap installed with expanded radar enabled.       |
| Remove Decimals from Teleport                       | Some servers do not support teleporting to the center of a block, so this option uses whole numbers instead of adding .5 to the value.    |
| **Display Death Waypoint Label <br>on map overlay** | Whether to show the name for death waypoints on your minimap and <br>full-screen map.                                                    |
| **Double Click to Create**                          | Double clicking on the fullscreen map will create a waypoint at the location.                                                            |

!!! info "26.1 only"

    This category also has a **Show on Locator Bar** toggle, which shows
    waypoints on the vanilla locator bar above the hotbar. The locator
    bar is a Minecraft 1.21.6+ feature, so this option is only present in
    JourneyMap for Minecraft 26.1, not on the 1.21.1 line.

## **Other Settings**

The default option for each setting below is marked with **bold text.**

| Setting                                | Options                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Editor XYZ Button Layout               | <ul><li>**X, Z, Y**</li><li>X, Y, Z</li><li>Single Field</li></ul>                                                                                                                                       | Select the format for the X, Y, Z buttons in the waypoint editor. Single Field uses one field for comma separated values, useful for copying and pasting from external sources.                                                                                                                                                                                     |
| Custom Waypoint Teleport Command       | Text input: **/execute in {dim} run tp {name} {x} {y} {z}**                                                                                                                                              | Set the teleport command used when you teleport to a waypoint, using the following placeholders: <ul><li>**{name}**: Your player name</li><li>**{dim}**: The target dimension</li><li>**{x}**: The waypoint's X coordinate</li><li>**{y}**: The waypoint's Y coordinate</li><li>**{z}**: The waypoint's Z coordinate</li><li>**{wpname}**: The waypoint's name</li></ul> |
| Auto Remove Death Waypoints            | Toggle                                                                                                                                                                                                   | Automatically removes death waypoints as you approach them.                                                                                                                                                                                                                                                                                                       |
| Auto Remove Death Waypoint Distance    | **2** to 64                                                                                                                                                                                              | The distance at which a death waypoint is removed. Minimum 2, or it will be removed as soon as it is created.                                                                                                                                                                                                                                                      |
| Temporary Waypoint Remove Distance     | **2** to 64                                                                                                                                                                                              | The distance from the player at which temporary waypoints are automatically removed.                                                                                                                                                                                                                                                                              |
| Death Date Format                      | <ul><li>**MM-dd-yyyy**</li><li>MM-dd-yy</li><li>dd-MM-yyyy</li><li>dd-MM-yy</li><li>yyyy-MM-dd</li><li>yy-MM-dd</li></ul>                                                                                | The text format of the date of death, as shown in the death waypoint label. <ul><li>**dd**: Day</li><li>**MM**: Month</li><li>**yy**: Year (2 digits)</li><li>**yyyy**: Year (4 digits)</li></ul>                                                                                                                                                                  |
| Death Time Format                      | <ul><li>**HH:mm:ss**</li><li>H:mm:ss</li><li>HH:mm</li><li>H:mm</li><li>hh:mm:ss a</li><li>h:mm:ss a</li><li>hh:mm:ss</li><li>h:mm:ss</li><li>hh:mm a</li><li>h:mm a</li><li>hh:mm</li><li>h:mm</li></ul> | The text format of the time of death, as shown in the death waypoint label.                                                                                                                                                                                                                                                                                       |
