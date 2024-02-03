# **Translate the mod**

If you want to contribute towards JourneyMap, a good way to do that is to translate the docs and the mod. This can help people that do not speak or not know how to read English, be able to read the JourneyMap docs or play the JourneyMap mod in their own language.

Instructions on how to translate the docs can be found [here](translate-docs.md)

## **I. Check the current language files**

This Git repository contains the latest language files for JourneyMap: **[JourneyMap Language Files](https://github.com/TeamJM/journeymap-lang)**.

- If your language file is in the repository, view it and check it for accuracy.
- If your language file is **not** in the repository, your language has not yet been translated for JourneyMap.

## **II. Instructions for creating / using the language file**

If your language file does not yet exist:

1. Copy the en_us.json file
2. Rename it according the [Locale Code](https://minecraft.wiki/w/Language) used by Mojang
3. Ensure it is saved with UTF-8 encoding (not ASCII or an ISO format)

The .json file **must be saved in UTF-8 encoding** by using a text editor which can handle UTF-8 characters like [Notepad Plus](https://notepad-plus-plus.org/).

If your language uses a character set which needs to be handled with Unicode characters, you can type them directly into the file. There is **no longer a need** to use Unicode hexadecimal Numeric Character Reference (NCR) codes (like \u0202).

**Example**: `"jm.common.saving_map_to_file": "Saving %1$s map to file..."`

<span style="color: red">**Incorrect**</span>: <code>"jm.common.saving_map_to_file": "\u8282\u80FD %1$s \u6620\u5C04\u5230\u6587\u4EF6..."</code>

<span style="color: green">**Correct**</span>: <code>"jm.common.saving_map_to_file": 节能 %1$s 映射到文件..."</code>

## **III. How to translate the .json file**

- Open your new .json file in a text editor which can handle UTF-8 characters like [Notepad Plus](https://notepad-plus-plus.org/). You will see a series of **keys** and **phrases** separated by an equals (:) sign. For example:

`"jm.common.chat_announcement": "&sect;eJourneyMap:&sect;f %1$s"`
`"jm.common.mapgui_only_ready": "Press [&sect;b%1$s&sect;f]. (Webserver disabled.)"`

The sample lines above have the **keys** of "jm.common.chat_announcement" and "jm.common.mapgui_only_ready".

- Translate each **phrase** from the English phrase to your language, but do NOT alter the message keys. (Only change the text which come **after** the equals ("=") sign.)

**Example**: <code>"example.key": "This is a phrase."</code>

<span style="color: green">**Correct**</span>: <code>"example.key": "Esta es una frase."</code>

<span style="color: red">**Incorrect**</span>: <code>"example.llave": "Esta es una frase."</code>

- Many of the phrases contain one or more numbered **parameters**. For example: "%1$s", "%1$d", "%2$s", etc. These are placeholders which will be replaced with a value when the message is displayed. You may reorder these parameters if it is required by the grammar rules of your language. For example:

`"jm.common.player_location=Location": "%1$s , %2$s  | Elevation:  %3$s  (  %4$s  ) | Biome:  %5$s"`

When the above phrase is used by JourneyMap, the parameters will be substituted with actual location information, like so:

`Location: 23,-98 | Elevation: 32 (2) | Biome: Desert`

- If a phrase is missing from an existing language file, it will be prefixed with a "#" and have "???" as the phrase.  You should remove the "#" prefix and then provide the correct phrase.

**Example**: <code># "example.key": "???"</code>

<span style="color: green">**Correct**</span>: <code>"example.key": "Esta es una frase."</code>

- Do not add line breaks (carriage returns) or HTML to any of the phrases.

- Do not translate or remove the special character combinations used by Minecraft to change color. (&sect;b, &sect;f, &sect;e, etc.)

## **IV. How to test your translation**

1. Use a zip program like 7-Zip to open your JourneyMap*.jar mod file.
2. Navigate down to `/assets/journeymap/lang` and add your language file (if new) or replace the older one.
3. JourneyMap will use the language you select in Minecraft. Select your language in Minecraft, and JourneyMap will use your new translation.
4. Please test your translation in Minecraft as best as you can. Don't worry about trying to provoke error messages, but please try to test as much as possible, including the Fullscreen Map controls (and tooltips), Options (and tooltips), and Web Map controls to confirm they are working.

## **V. How to submit your translation**

[Follow the instructions on Github](https://github.com/TeamJM/journeymap-lang#how-to-translate-journeymap)

**Thank you very much for your hard work!**
