## **Overview**

As of JourneyMap 5.1.3, there is no server-side mechanism for generating a map of a multiplayer server.  However, if you are a server owner (or can get access to a copy of the server's world data folder), there is a workaround:

## **Workaround**

- Copy the server world data folder down to your local PC and load it as a Minecraft singleplayer world.
- In JourneyMap, go to **J > Options > Advanced** and set "AutoMap Poll Frequency" to the lowest value allowed (500ms). (This is the amount of time JourneyMap lets Minecraft take a break between region files. Running Automap can cause lag if you try to keep playing while it is running. Lowering the polling rate increases the lag, but reduces the total time it takes to Automap the world.)
- In JourneyMap, run **J > Actions > Automap** for all regions. Keep in mind Automap will do just the dimension you're in, and only the surface if you're on the surface. Or if you're underground, only the vertical slice (chunk), you were in when you kicked off Automap. If you want to Automap multiple slices or dimensions, move to the corresponding area and run Automap again.
- If you're intending to share the results with other players, note that any waypoints you create will go into the same folder as the map image tiles.

When it's done, the generated map image tiles and waypoints will be in `.minecraft/journeymap/data/sp/{worldname}`. To use the results when connecting to the server again, you'll need to copy that folder's contents to the one JourneyMap uses for your server connection: `.minecraft/journeymap/data/mp/{servername}`. If you want to share the results with other players, simply zip up the folder and give them these instructions.
