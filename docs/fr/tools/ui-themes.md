# **UI Themes**

!!! warning "Translation needed for 6.0"

    This page was updated for JourneyMap 6.0 in English. Translation
    is pending; the content shown is the English source. See
    Contributing to help translate the docs.

The look of JourneyMap's toolbars, buttons, and minimap frame is set by
a UI theme. You can switch themes with the UI Theme button (the paint
palette icon) on the full-screen map, and you can create your own theme
with your own images and colors.

## **Bundled themes**

JourneyMap ships with two theme families:

- **Flat** - a set of flat-styled themes: Purist (the default), Desert
  Temple, EndCity, Forest Mansion, Nether Fortress, Ocean Monument, and
  Stronghold. These all live in the `flat` theme folder.
- **Victorian** - a more ornate theme, in the `victorian_` theme folder.

Use the UI Theme button to cycle through the themes available in your
installed version.

## **Theme files**

Themes live in the JourneyMap theme folder:

```text
.minecraft/journeymap/icon/theme/
```

Each theme is a folder containing a theme definition file plus the
images it uses. The definition file is JSON and ends in
`.theme2.json`. JourneyMap extracts the bundled themes into this folder
the first time it runs, so you can open them to see how a complete
theme is built.

!!! note "Theme schema 2"

    JourneyMap 6.0 uses version 2 of the theme format. Theme files end
    in `.theme2.json` and contain a `"schema": 2` property. Themes
    written for older versions of JourneyMap are not compatible and
    need to be rebuilt.

## **Creating a theme: easy start**

1. Open `.minecraft/journeymap/icon/theme/` and copy one of the bundled
   theme folders (for example `victorian_`) to a new folder with your
   own name, for example `MyTheme`.
2. In your new folder, rename the `.theme2.json` file to match, for
   example `MyTheme.theme2.json`.
3. Open that file in a text editor and change the `name`, `directory`,
   and `author` values so they match your folder and your name. The
   `directory` value must be the exact name of your theme folder.
4. Replace the images in the folder with your own artwork. Keep the
   image dimensions consistent with what the `.theme2.json` file
   declares, or update those dimensions in the file to match your art.
5. Use the UI Theme button on the full-screen map to switch to your
   theme.
6. To share your theme, zip up the theme folder and give it to others.
   They unzip it into `.minecraft/journeymap/icon/theme/` and select it
   with the UI Theme button.

## **The theme file structure**

A `.theme2.json` file is read with GSON. You edit the values, but you
cannot change the structure. The top level has:

- `schema` - the theme format version. Must be `2`.
- `author`, `name`, `directory` - identifying information.
- `container` - toolbar specs (see below).
- `control` - button and toggle specs.
- `fullscreen` - full-screen map background and status label colors.
- `icon` - the default size and color for icons in the `icon` folder.
- `minimap` - the minimap frame specs, with separate `circle` and
  `square` sections.

### Color and image values

Two value types appear throughout the file:

- A **color value** is an object with a `color` hex string (`#rrggbb`)
  and an `alpha` value. Use `#ffffff` for color to leave an image's own
  colors unchanged.
- An **image spec** declares a `width` and `height`, and may also carry
  a `color` and `alpha`.

### Containers and controls

- `container.toolbar.horizontal` and `container.toolbar.vertical`
  describe the toolbars. A toolbar is built from a `begin` image, a
  repeating `inner` image (one repeat per button), and an `end` image.
  Each has `useThemeImages`, a filename `prefix`, `margin`, and
  `padding`.
- `control.button` and `control.toggle` describe the button and toggle
  controls: their `width`, `height`, tooltip styles, and the color
  values used for the icon and button in each state (on, off, hover,
  disabled).

### Minimap

`minimap.circle` and `minimap.square` describe the circular and square
minimap frames. Each defines the rim and mask image sizes, the top and
bottom label styles, compass point images and which compass points to
show, and the reticle and frame colors.

The bundled themes are the best reference for exact filenames and
sizes - copy one and compare its `.theme2.json` to the images in its
folder.

## **Image guidance**

Create your images at 2x the sizes declared in the `.theme2.json` file.
This keeps buttons looking sharp on high-resolution displays and for
players using Minecraft's larger GUI scales.

## **Setting a default theme in a modpack**

A modpack can ship a theme and make it the default for players opening
JourneyMap for the first time. Place the theme folder in
`.minecraft/journeymap/icon/theme/` as usual, then create this file:

```text
.minecraft/journeymap/icon/theme/default.theme.config
```

Its contents point at the theme folder, the theme file, and the theme
name:

```json
{
  "directory": "MyTheme",
  "filename": "MyTheme",
  "name": "MyTheme"
}
```

## **Sharing your theme**

If you create a theme and would like to share it, drop by the
[JourneyMap Discord server](https://discord.gg/eP8gE69).
