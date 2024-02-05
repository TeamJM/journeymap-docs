# **Translate the docs**

If you want to contribute towards JourneyMap, a good way to do that is to translate the docs and the mod. This can help people that do not speak or not know how to read English, be able to read the JourneyMap docs or play the JourneyMap mod in their own language.

Instructions on how to translate the mod can be found [here](translate-mod.md)

## **Getting Setup**

To get started on translating the wiki, you will need to have a local environment ready for testing your translations. This can be done by following the steps shown in the [README](https://github.com/TeamJM/journeymap-docs#installing).

You will have to make a few changes to the `mkdocs.yml` file in the config folder. This can be done by:

1. Opening the `mkdocs.yml` file in the config folder
2. Scroll down until you see the variable name `languages` and input a new line like this:

```diff title="mkdocs.yml"
      languages:
         - locale: en
           default: true
           name: English
           build: true
+
+        - locale: fr
+          default: false
+          name: Français
+          build: true

```

3\. You will also have to add translations to the navigation elements for French. To do this, please copy and paste the `nav_translations` section from the English to the French section. Here is an example:

```diff title="mkdocs.yml"
          - locale: fr
            default: false
            name: Français
            build: true
+           nav_translations:
+             Home: Home
+             About: About
+             Credits: Credits
+             Licensing: Licensing
+             Support: Support
+             Client Docs: Client Docs
+             Installing: Installing
+             Basic Usage: Basic Usage
+             Full-Screen Map: Full-Screen Map
+             Settings: Settings
+             Overview: Overview
+             Grid: Grid
+             Minimap: Minimap
+             Minimap Position: Minimap Position
+             Full-Screen Map: Full-Screen Map
+             Webmap: Webmap
+             Waypoint: Waypoint
+             Waypoint Beacons: Waypoint Beacons
+             Cartography: Cartography
+             Advanced Options: Advanced Options
+             Waypoints: Waypoints
+             Server Docs: Server Docs
+             Installing: Installing
+             Basic Usage: Basic Usage
+             Commands: Commands
+             Waypoint: Waypoint
+             Settings: Settings
+             Overview: Overview
+             Global Properties: Global Properties
+             Default Dimension Properties: Default Dimension Properties
+             Dimension - minecraft:overworld: Dimension - minecraft:overworld
+             Dimension - minecraft:the_nether: Dimension - minecraft:the_nether
+             Dimension - minecraft:the_end: Dimension - minecraft:the_end
+             Multiplayer: Multiplayer
+             Endpoints: Endpoints
+             Waypoint: Waypoint
+             Tools & Customisation: Tools & Customisation
+             Custom Mob Icons: Custom Mob Icons
+             Integrate your mod: Integrate your mod
+             JourneyMap Tools: JourneyMap Tools
+             Map a multiplayer server: Map a multiplayer server
+             Topographic: Topographic
+             UI Themes: UI Themes
+             Contributing: Contributing
+             Translate the mod: Translate the mod
+             Translate the docs: Translate the docs
+             Changelogs: Changelogs
```

This codeblock includes English translations. In this case, you would need to translate the English words after the colon into French. I have left them English as an example.

!!! note "Note"

    The instructions above only apply if you are translating to French. Please apply these instructions to the relative language you are translating to.

## **Creating a new folder**

Now that you have set yourself up, you can now start translating the actual docs. To start, you will need to create a new folder in the docs directory with your 2-letter [ISO-639-1](https://en.wikipedia.org/wiki/ISO_639-1) language code. Here is an example of how to do this if you are translating the docs to French:

```text
├─ docs/
│    ├─ en/
│    │   ├─ About/
│    │   ├─ Client Docs/
│    │   ├─ Server Docs/
│    │   ├─ Tools and Customisation/
│    │   ├─ changelogs.md
│    │   └─ index.md
│    │
│    └─ fr/
│        ├─ About/
│        ├─ Client Docs/
│        ├─ Server Docs/
│        ├─ Tools and Customisation/
│        ├─ changelogs.md
│        └─ index.md
```

An easy way to do this is to create a folder with your 2-letter [ISO-639-1](https://en.wikipedia.org/wiki/ISO_639-1) language code and copy and paste the contents from the en directory to your newly created folder in the docs directory.

Once your folder with all the files have been created, you can start translating the docs to your language.

## **Finishing steps**

You might have come here asking yourself, what do I do once I have finished translating? Well, the final step you would do is to PR your work to the main repo for us to review and merge if all of it looks great.

**Thank you very much for your hard work!**
