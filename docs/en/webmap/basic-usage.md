# **Webmap Basic Usage**

Once the [Webmap addon is installed](installing.md), you enable it from
JourneyMap's options and open it in any web browser.

![Webmap](../img/webmap.png){: .center}

## **Enabling the Webmap**

1. Open JourneyMap's options (press `O`, or open the fullscreen map and
   click Options).
2. Go to the **Webmap** category.
3. Turn on **Enable Web Map**.

If the **Announce Mod** advanced option is enabled (the default),
JourneyMap posts the Webmap address in chat once when you join a world.
The resolved port is also written to the game log.

See [Settings](settings.md) for the port option and how port selection
works.

## **Opening the Webmap**

Open a web browser and go to:

```text
http://localhost:8080/
```

Replace `8080` with the port shown in chat if it differs (for example
if port 8080 was already in use).

To view the map from another device on the same network, replace
`localhost` with the local IP address of the computer running
Minecraft, for example `http://192.168.1.20:8080/`.

## **Controls**

- **Pan** - click and drag.
- **Zoom** - mouse wheel.
- **Map type** - switch between day, night, topo, and cave maps.
- **Dimension** - switch between the dimensions you have explored.
- **Waypoints** - your waypoints are shown on the web map.
