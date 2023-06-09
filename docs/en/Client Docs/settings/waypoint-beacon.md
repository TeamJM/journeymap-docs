## **Waypoint Beacon Settings**

By default, waypoints are displayed in the world using a beacon beam in the distance, which allows you to see where they are from anywhere in the world. By default, you can look towards the beam and see the waypoint’s icon and label as well. This behaviour can be customized below.

![Beacon-Settings](../../img/settings/client/waypoint-beacons.png){: .center}

## **Toggles**

The **bold** toggle settings below are enabled by default.

| Toggle                       | Description                                                                       |
|------------------------------|-----------------------------------------------------------------------------------|
| Always Map Caves             | Whether to map caves below you when you’re on the surface                         |
| Always Map Surface           | Whether to map the surface above you when you’re in caves                         |
| **Blend Foliage**            | Whether to apply biome colours to foliage                                         |
| Blend Grass                  | Whether to apply biome colours to grass                                           |
| Blend Water                  | Whether to apply biome colours to water                                           |
| **Ignore Glass Ceilings**    | Whether to remain in surface mode when under a glass ceiling                      |
| **Map Topography**           | Whether to generate a contour map that shows elevation                            |
| Show Bathymetry              | Whether to show underwater terrain on the map                                     |
| **Show Crops**               | Whether to show crops on the map                                                  |
| Show Plant Shadows           | Whether to plants and crops should cast shadows on the map                        |
| Show Plants                  | Whether to show plants on the map                                                 |
| **Show Surface Above Caves** | Whether to show a dimmed view of the surface when in cave mode                    |
| **Use Antialiasing**         | Whether to use anti-aliasing to improve the shading effect used to show elevation |
| **Use Cave Lighting**        | Whether to show lights underground - disable for a fully bright map               |
| **Use Transparency**         | Whether transparent blocks should reveal what’s below them on the map             |

## **Other Settings**

The default option for each setting below is marked with **bold text.**

| Setting              | Options                                     | Description                                                                                                                                                                           |
|----------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reveal Shape         | <ul><li>**Circle**</li><li>Square</li></ul> | Whether to reveal chunks in a circle or square - circle reveals show fewer chunks at once, and so perform better                                                                      |
| Render Delay         | Range: 0 - 10 (in seconds, default: **2**)  | How often JourneyMap should try to render the chunks around you - Higher values can result in better performance, but may result in chunks being missed when travelling at high speed |
| Cave Max Distance    | Range: 1 - 32 (in chunks, default: **3**)   | The maximum distance within which to attempt to render the map while in a cave - if you set this higher than your render distance, then this will use that instead                    |
| Surface Max Distance | Range: 1 - 32 (in chunks, default: **7**)   | The maximum distance within which to attempt to render the map while above ground -if you set this higher than your render distance, then this will use that instead                  |
