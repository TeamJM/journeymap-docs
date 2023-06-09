## **Advanced Settings**

This section contains advanced settings for power users and those that may wish to tweak some of JourneyMap’s internals.

!!! warning "Warning"

    The settings in this section cam have extreme effects on the performance of your client. We don’t recommend touching these settings unless you have a good understanding of what you’re doing, or you’re directed to do so by a member of the JourneyMap support staff.

    If tweaking these settings crashes your client or causes your computer to lag horribly, don’t say we didn’t warn you.

![Advanced-Settings](../../img/settings/client/advanced.png){: .center}

## **Toggles**

The **bold** toggle settings below are enabled by default.

| Toggle                     | Description                                                                                                                                             |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Announce Mod**           | Whether to announce in chat when JourneyMap is ready to use                                                                                             |
| **Check for Mod Updates**  | Whether JourneyMap should check for updates on Curse                                                                                                    |
| **Hide Sneaking Entities** | Whether sneaking/crouching creatures should be hidden                                                                                                   |
| **High Display Quality**   | Uncheck to improve zoom performance and memory usage, but reduce <br>display quality and lower performance of minimap rotation when set to “My Heading” |
| Record Cache Statistics    | This is intended for beta testers - enable to record statistics for each cache                                                                          |

## **Other Settings**

The default option for each setting below is marked with **bold text.**

| Setting                | Options                                                                                                                 | Description                                                                                                                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Logging Level          | <ul><li>**INFO**</li><li>ALL</li><li>DEBUG</li><li>ERROR</li><li>FATAL</li><li>OFF</li><li>TRACE</li><li>WARN</li></ul> | Set how verbose JourneyMap's logs are, but note that some log levels can cause serious performance problems                                                                                                 |
| AutoMap Poll Frequency | Range: 500 - 10000 (in ms, default: **2000**)                                                                           | Delay between automap region tasks - lower values will make the map generate faster, but will cause significant performance drops while mapping                                                             |
| Browser Poll           | Range: 1000 - 10000 (in ms, default: **2000**)                                                                          | This setting isn't currently implemented and may be removed in a later version of JourneyMap                                                                                                                |
| Cache Animals          | Range: 1000 - 10000 (in ms, default: **3100**)                                                                          | How long radar data for animals is cached for - lower values will impact performance                                                                                                                        |
| Cache Mobs             | Range: 1000 - 10000 (in ms, default: **3000**)                                                                          | How long radar data for mobs is cached for - lower values will impact performance                                                                                                                           |
| Cache Player           | Range: 500 - 2000 (in ms, default: **1000**)                                                                            | How long data for your character is cached for - lower values will impact performance                                                                                                                       |
| Cache Players          | Range: 1000 - 10000 (in ms, default: **2000**)                                                                          | How long radar data for other players is cached for - lower values will impact performance                                                                                                                  |
| Map Tile Render Type   | Range: **1** - 4                                                                                                        | Change rendering strategy for map tiles if they appear blurry on your video card:<ol type="1"><li>Linear & mirrored</li><li>Linear & clamped</li><li>Nearest & mirrored</li><li>Nearest & clamped</li></ol> |
| Maximum Animals        | Range: 1 - 128 (default: **32**)                                                                                        | Maximum number of animals displayed on the radar                                                                                                                                                            |
| Maximum Mobs           | Range: 1 - 128 (default: **32**)                                                                                        | Maximum number of mobs displayed on the radar                                                                                                                                                               |
| Maximum Players        | Range: 1 - 128 (default: **32**)                                                                                        | Maximum number of players displayed on the radar                                                                                                                                                            |
| Maximum Villagers      | Range: 1 - 128 (default: **32**)                                                                                        | Maximum number of villagers displayed on the radar                                                                                                                                                          |
| Radar Range Lateral    | Range: 16 - 512 (in blocks, default: **64**)                                                                            | Lateral distance to search for entities to display on the radar - high values will cause a significant performance hit                                                                                      |
| Radar Range Vertical   | Range: 8 - 256 (in blocks, default: **16**)                                                                             | Vertical distance to search for entities to display on the radar - high values will cause a significant performance hit                                                                                     |
