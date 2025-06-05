# **Traduce el mod**

Si desea contribuir a JourneyMap, una buena forma de hacerlo es traducir los documentos y el mod. Esto puede ayudar a las personas que no hablan o no saben leer inglés a poder leer los documentos de JourneyMap o jugar el mod JourneyMap en su propio idioma.

Las instrucciones sobre cómo traducir los documentos se pueden encontrar [aquí](translate-docs.md)

## **I. Verifique los archivos de idioma actuales**

Este repositorio de Git contiene los archivos de idioma más recientes para JourneyMap: **[Archivos de idioma de JourneyMap](https://github.com/TeamJM/journeymap-lang)**.

- Si su archivo de idioma está en el repositorio, véalo y verifique su exactitud.
- Si su archivo de idioma **no** está en el repositorio, su idioma aún no se ha traducido para JourneyMap.

## **II. Instrucciones para crear/usar el archivo de idioma**

Si su archivo de idioma aún no existe:

1. Copie el archivo en_us.json
2. Cambie el nombre según el [Código local](https://minecraft.wiki/w/Language) utilizado por Mojang
3. Asegúrese de que esté guardado con codificación UTF-8 (no ASCII ni formato ISO)

El archivo .json **debe guardarse en codificación UTF-8** mediante el uso de un editor de texto que pueda manejar caracteres UTF-8 como [Notepad Plus](https://notepad-plus-plus.org/).

Si su idioma utiliza un conjunto de caracteres que debe manejarse con caracteres Unicode, puede escribirlos directamente en el archivo. **Ya no es necesario** utilizar códigos de referencia de caracteres numéricos (NCR) hexadecimales Unicode (como \u0202).

**Ejemplo**: `"jm.common.saving_map_to_file": "Saving %1$s map to file..."`

<span style="color: red">**Incorrecto**</span>: <code>"jm.common.saving_map_to_file": "\u8282\u80FD %1$s \u6620\u5C04\u5230\u6587\u4EF6..."</code>

<span style="color: green">**Correcto**</span>: <code>"jm.common.saving_map_to_file": 节能 %1$s 映射到文件..."</code>

## **III. Cómo traducir el archivo .json**

- Abra su nuevo archivo .json en un editor de texto que pueda manejar caracteres UTF-8 como [Notepad Plus](https://notepad-plus-plus.org/). Verás una serie de **claves** y **frases** separadas por un signo igual (:). Por ejemplo:

`"jm.common.chat_announcement": "&sect;eJourneyMap:&sect;f %1$s"`
`"jm.common.mapgui_only_ready": "Press [&sect;b%1$s&sect;f]. (Webserver disabled.)"`

Las líneas de ejemplo anteriores tienen las **claves** de"jm.common.chat_announcement" y "jm.common.mapgui_only_ready".

- Traduce cada **frase** de la frase en inglés a tu idioma, pero NO alteres las claves del mensaje. (Solo cambie el texto que viene **después** del signo igual ("=").)

**Ejemplo**: <code>"example.key": "This is a phrase."</code>

<span style="color: green">**Correcto**</span>: <code>"example.key": "Esta es una frase."</code>

<span style="color: red">**Incorrecto**</span>: <code>"example.llave": "Esta es una frase."</code>

- Muchas de las frases contienen uno o más **parámetros** numerados. Por ejemplo: "%1$s", "%1$d", "%2$s", etc. Estos son marcadores de posición que se reemplazarán con un valor cuando se muestre el mensaje. Puede reordenar estos parámetros si así lo requieren las reglas gramaticales de su idioma. Por ejemplo:

`"jm.common.player_location=Location": "%1$s , %2$s  | Elevation:  %3$s  (  %4$s  ) | Biome:  %5$s"`

Cuando JourneyMap utiliza la frase anterior, los parámetros se sustituirán con información de ubicación real, así:

`Location: 23,-98 | Elevation: 32 (2) | Biome: Desert`

- Si falta una frase en un archivo de idioma existente, tendrá el prefijo "#" y "???" como la frase. Debe eliminar el prefijo "#" y luego proporcionar la frase correcta.

**Ejemplo**: <code># "example.key": "???"</code>

<span style="color: green">**Correcto**</span>: <code>"example.key": "Esta es una frase."</code>

- No agregues saltos de línea (retornos de carro) ni HTML a ninguna de las frases.

- No traduzcas ni elimines las combinaciones de caracteres especiales utilizadas por Minecraft para cambiar de color. (&sect;b, &sect;f, &sect;e, etc.)

## **IV. Cómo probar tu traducción**

1. Utilice un programa zip como 7-Zip para abrir su archivo mod JourneyMap*.jar.
2. Navegue hasta `/assets/journeymap/lang` y agregue su archivo de idioma (si es nuevo) o reemplace el anterior.
3. JourneyMap utilizará el idioma que selecciones en Minecraft. Seleccione su idioma en Minecraft y JourneyMap utilizará su nueva traducción.
4. Pruebe su traducción en Minecraft lo mejor que pueda. No se preocupe por intentar provocar mensajes de error, pero intente probar todo lo posible, incluidos los controles del mapa de pantalla completa (y información sobre herramientas), las opciones (y la información sobre herramientas) y los controles del mapa web para confirmar que están funcionando.

## **V. Cómo enviar su traducción**

[Siga las instrucciones en Github](https://github.com/TeamJM/journeymap-lang#how-to-translate-journeymap)

**¡Muchas gracias por tu arduo trabajo!**