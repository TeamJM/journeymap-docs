
!!! warning "Translation needed for 6.0"

    This page was updated for JourneyMap 6.0 in English. Translation
    is pending; the content shown is the English source. See
    Contributing to help translate the docs.

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
