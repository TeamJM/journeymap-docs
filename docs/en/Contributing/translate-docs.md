# **Translate the docs**

If you want to contribute towards JourneyMap, a good way to do that is to translate the docs and the mod. This can help people that do not speak or not know how to read English, be able to read the JourneyMap docs or play the JourneyMap mod in their own language.

Instructions on how to translate the mod can be found [here](translate-mod.md)

## **Getting Setup**

To get started on translating the wiki, you will need to have a local environment ready for testing your translations. This can be done by following the steps shown in the [README](https://github.com/TeamJM/journeymap-docs#installing).

You will have to make a few changes to the `mkdocs.yml` file in the config folder. This can be done by:

1. Opening the `mkdocs.yml` file in the config folder
2. Scroll down until you see the variable name `languages` and input a new line like this:

```diff
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

!!! note "Note"

    The instructions above only apply if you are translating to French. Please apply these intructions to the relative language you are translating to.

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
