# **Translate the docs**

If you want to contribute towards JourneyMap, a good way to do that is to translate the docs and the mod. This can help people that do not speak or not know how to read English, be able to read the JourneyMap docs in their own language.

Instructions on how to translate the mod can be found [here](translate-mod.md)

## **Getting Setup**

To get started on translating the wiki, you will need to have a local environment ready for testing your translations. This can be done by following the steps shown in the [README](https://github.com/TeamJM/journeymap-docs#installing).

You will also have to create a new folder in the existing config folder with the name of your language. For example, en is English, fr is French, de is Deutsh, etc. In our example below, we will show how to add translations for French.

Make sure to copy and paste the `mkdocs.yml` file from the en directory to your newly created folder. You will also have to make a few changes to the `mkdocs.yml` file. This can be done by:

1. Opening the `mkdocs.yml` file in your newly created folder
2. Replace the `docs_dir` variable to the name of your language

    ```diff
    - docs_dir: ../../docs/en
    + docs_dir: ../../docs/fr
    ```

3. Scroll down untuil you see the variable name `alternate` and input a new line like this:

    ```diff
        # Switch to English
        - name: English
        link: /en/
        lang: en
    +
    +    # Switch to French
    +    - name: French
    +     link: /fr/
    +      lang: fr
    ```

4. Scroll down again until you see the variable name `search` and change the language from en to the language you are translating to. Here is an example for French:

    ```diff
    -  lang: en
    +  lang: fr
    ```

You have now finished setting up yourself up to translate the docs.

## **Creating a new folder**

Now that you have set yourself up, you can now start translating the actual docs. To start, you will need to create a new folder in the docs directory with your language name. Here is an example of how to do this if you are translating the docs to French:

```text
├─ docs/
│    ├─ en/
│    │   ├─ About/
│    │   ├─ Client Docs/
│    │   ├─ img/
│    │   ├─ Server Docs/
│    │   ├─ Tools and Customisation/
│    │   ├─ changelogs.md
│    │   ├─ index.md
│    │   └─ translate.md
│    │
│    └─ fr/
│        ├─ About/
│        ├─ Client Docs/
│        ├─ img/
│        ├─ Server Docs/
│        ├─ Tools and Customisation/
│        ├─ changelogs.md
│        ├─ index.md
│        └─ translate.md
```

An easy way to do this is to create a folder with your language name and copy and paste the contents from the en directory to your newly created folder in the docs directory.

Once your folder with all the files have been created, you can actually start translating the docs.

## **Finishing steps**

You might have come here asking yourself, what do I do once I have finished translating? Well, the final step you would do is to PR your work to the main repo for us to review and merge if all of it looks great.

**Thank you very much for your hard work!**
