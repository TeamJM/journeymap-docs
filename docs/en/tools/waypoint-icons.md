## **Waypoint Icon Resource Packs**

JourneyMap ships with a set of built-in waypoint icons, but you can add
your own by shipping them in a Minecraft resource pack. JourneyMap picks
the icons up automatically and they appear in the icon picker in the
waypoint editor.

For mob and entity icons (a different system), see
[Custom Mob Icons](custom-mob-icons.md).

## **Resource pack path**

Place your waypoint icons inside a resource pack at this path:

```text
assets/journeymap/textures/waypoint/icon/<name>.png
```

`<name>` becomes the icon's name in the waypoint editor's icon picker,
so use something descriptive.

In code / resource location terms this path is
`journeymap:textures/waypoint/icon/<name>.png`.

## **Image size**

Waypoint icons must be **16x16** pixels. Images of other sizes will not
render correctly. Use transparent PNG files so the icon blends with the
waypoint marker.

## **Example resource pack**

A starter resource pack is available to use as a template:

[icons_test.zip](https://github.com/user-attachments/files/26309255/icons_test.zip)

To use it:

1. Open the zip in 7-Zip, WinZip, WinRAR, or any zip tool.
2. Edit the `description` in `pack.mcmeta`.
3. Delete the help files included in the example.
4. Put your 16x16 PNG images in
   `assets/journeymap/textures/waypoint/icon` inside the zip.
5. Rename the zip to whatever you want the pack to be called.
6. Drop the zip into your `resourcepacks` folder and enable it in
   Minecraft's Resource Packs screen.

## **Folder layout**

```text
my-waypoint-icons.zip
 └───assets
 │   └───journeymap
 │       └───textures
 │           └───waypoint
 │               └───icon
 │                   │   castle.png
 │                   │   mineshaft.png
 │                   │   portal.png
 └───pack.mcmeta
```

## **Custom icon sets**

Icons placed directly in `textures/waypoint/icon/` appear in the
**JourneyMap** set. To ship your icons as their own named set, put them in a
**subfolder**:

```text
assets/journeymap/textures/waypoint/icon/<set>/<name>.png
```

Each subfolder becomes its own tab in the icon picker. The subfolder name
(`<set>`) is the set's identifier. Resource-pack sets appear alongside
JourneyMap's built-in tabs - **All**, **JourneyMap**, **Minecraft**
(vanilla item textures), and **Map Deco** (map markers).

### Naming the set

By default the tab is labelled with the raw subfolder name. To give it a
friendly, localizable name, add this translation key to your resource pack's
language files:

```text
waypoint.iconset.<set>.name
```

For example, a `houses` subfolder:

`assets/journeymap/lang/en_us.json`:

```json
{
  "waypoint.iconset.houses.name": "Cool Houses"
}
```

`assets/journeymap/lang/es_es.json`:

```json
{
  "waypoint.iconset.houses.name": "Casas Geniales"
}
```

The key is optional. Without it, the tab shows the subfolder name (`houses`).

### Folder layout

```text
my-waypoint-icons.zip
 └───assets
 │   └───journeymap
 │       ├───lang
 │       │   │   en_us.json
 │       │   │   es_es.json
 │       └───textures
 │           └───waypoint
 │               └───icon
 │                   │   castle.png          (JourneyMap set)
 │                   │   portal.png          (JourneyMap set)
 │                   └───houses
 │                       │   cabin.png       (Cool Houses set)
 │                       │   manor.png       (Cool Houses set)
 └───pack.mcmeta
```

Icons in a set placed under the `journeymap` namespace (the path shown above)
are tinted by the waypoint color, like JourneyMap's built-in icons. Use 16x16
transparent PNG files, as for the JourneyMap set.
