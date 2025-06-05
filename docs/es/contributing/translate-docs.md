# **Traducir los documentos**

Si desea contribuir a JourneyMap, una buena forma de hacerlo es traducir los documentos y el mod. Esto puede ayudar a las personas que no hablan o no saben leer inglés a poder leer los documentos de JourneyMap o jugar el mod JourneyMap en su propio idioma.

Las instrucciones sobre cómo traducir el mod se pueden encontrar [aquí](translate-mod.md)

## **Obteniendo configuración**

Para comenzar a traducir el wiki, necesitará tener un entorno local listo para probar sus traducciones. Esto se puede hacer siguiendo los pasos que se muestran en [README](https://github.com/TeamJM/journeymap-docs#installing).

Tendrá que realizar algunos cambios en el archivo `mkdocs.yml` en la carpeta de configuración. Esto se puede hacer mediante:

1. Abrir el archivo `mkdocs.yml` en la carpeta de configuración
2. Desplácese hacia abajo hasta que vea el nombre de la variable "idiomas" e ingrese una nueva línea como esta:

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

3\. También tendrás que agregar traducciones a los elementos de navegación para francés. Para hacer esto, copie y pegue la sección `nav_translations` de la sección de inglés a francés. Aquí hay un ejemplo:

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

Este bloque de código incluye traducciones al inglés. En este caso, necesitarás traducir las palabras en inglés después de los dos puntos al francés. Les he dejado el inglés como ejemplo.

!!! note "Nota"

 Las instrucciones anteriores sólo se aplican si está traduciendo al francés. Aplique estas instrucciones al idioma relativo al que está traduciendo.

## **Creando una nueva carpeta**

Ahora que ya está configurado, puede comenzar a traducir los documentos reales. Para comenzar, deberá crear una nueva carpeta en el directorio de documentos con su código de idioma de dos letras [ISO-639-1](https://en.wikipedia.org/wiki/ISO_639-1). A continuación se muestra un ejemplo de cómo hacer esto si está traduciendo los documentos al francés:

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

Una manera fácil de hacer esto es crear una carpeta con su código de idioma de dos letras [ISO-639-1](https://en.wikipedia.org/wiki/ISO_639-1) y copiar y pegar el contenido de la carpeta. en directorio a su carpeta recién creada en el directorio de documentos.

Una vez que se haya creado su carpeta con todos los archivos, puede comenzar a traducir los documentos a su idioma.

## **Pasos finales**

Seguramente habrás llegado hasta aquí preguntándote ¿qué hago una vez que haya terminado de traducir? Bueno, el último paso que deberías hacer es enviar tu trabajo al repositorio principal para que lo revisemos y lo fusionemos si todo se ve bien.

**¡Muchas gracias por tu arduo trabajo!**
