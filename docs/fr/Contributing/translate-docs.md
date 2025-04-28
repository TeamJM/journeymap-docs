# **Traduire la documentation**

Si vous souhaitez contribuer à JourneyMap, une bonne façon de le faire est de traduire la documentation et le mod. Cela peut aider les personnes qui ne parlent pas ou qui ne savent pas lire l'anglais à pouvoir lire la documentation de JourneyMap ou à jouer au mod JourneyMap dans leur propre langue.

Les instructions sur la manière de traduire le mod peuvent être trouvées [ici](translate-mod.md).

## **Configuration**

Pour commencer à traduire le wiki, vous devez préparer un environnement local pour tester vos traductions. Cela peut être fait en suivant les étapes indiquées dans le [README](https://github.com/TeamJM/journeymap-docs#installing).

Vous devrez apporter quelques modifications au fichier `mkdocs.yml` dans le dossier de configuration. Cela peut être fait en suivant ces étapes :

1. Ouvrez le fichier `mkdocs.yml` dans le dossier de configuration.
2. Faites défiler jusqu'à voir le nom de la variable `languages` et ajoutez une nouvelle ligne comme suit :

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

3. Vous devrez également ajouter des traductions aux éléments de navigation pour le français. Pour ce faire, veuillez copier et coller la section `nav_translations` de l'anglais vers la section française. Voici un exemple :

```diff title="mkdocs.yml"
          - locale: fr
            default: false
            name: Français
            build: true
+           nav_translations:
+             Home: Accueil
+             About: À propos
+             Credits: Crédits
+             Licensing: Licence
+             Support: Support
+             Client Docs: Documentation Client
+             Installing: Installation
+             Basic Usage: Utilisation de Base
+             Full-Screen Map: Carte Plein Écran
+             Settings: Paramètres
+             Overview: Aperçu
+             Grid: Grille
+             Minimap: Minicarte
+             Minimap Position: Position de la Minicarte
+             Full-Screen Map: Carte Plein Écran
+             Webmap: Carte Web
+             Waypoint: Point de Repère
+             Waypoint Beacons: Balises de Points de Repère
+             Cartography: Cartographie
+             Advanced Options: Options Avancées
+             Waypoints: Points de Repère
+             Server Docs: Documentation Serveur
+             Installing: Installation
+             Basic Usage: Utilisation de Base
+             Commands: Commandes
+             Waypoint: Point de Repère
+             Settings: Paramètres
+             Overview: Aperçu
+             Global Properties: Propriétés Globales
+             Default Dimension Properties: Propriétés par Défaut des Dimensions
+             Dimension - minecraft:overworld: Dimension - minecraft:overworld
+             Dimension - minecraft:the_nether: Dimension - minecraft:the_nether
+             Dimension - minecraft:the_end: Dimension - minecraft:the_end
+             Multiplayer: Multijoueur
+             Endpoints: Points de Terminaison
+             Waypoint: Point de Repère
+             Tools & Customisation: Outils et Personnalisation
+             Custom Mob Icons: Icônes de Mob Personnalisées
+             Integrate your mod: Intégrer votre mod
+             JourneyMap Tools: Outils JourneyMap
+             Map a multiplayer server: Cartographier un serveur multijoueur
+             Topographic: Topographique
+             UI Themes: Thèmes de l'Interface Utilisateur
+             Contributing: Contribuer
+             Translate the mod: Traduire le mod
+             Translate the docs: Traduire la documentation
+             Changelogs: Journaux de Modifications
```

Ce bloc de code inclut des traductions anglaises. Dans ce cas, vous devrez traduire les mots anglais après le deux-points en français. Je les ai laissés en anglais à titre d'exemple.

!!! note "Remarque"
    Les instructions ci-dessus ne s'appliquent que si vous traduisez en français. Veuillez appliquer ces instructions à la langue relative dans laquelle vous traduisez.

## **Créer un nouveau dossier**

Maintenant que vous vous êtes configuré, vous pouvez commencer à traduire la documentation proprement dite. Pour commencer, vous devrez créer un nouveau dossier dans le répertoire des documents avec votre code de langue à 2 lettres [ISO-639-1](https://en.wikipedia.org/wiki/ISO_639-1). Voici un exemple de la façon de procéder si vous traduisez la documentation en français :

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

Une manière simple de faire cela est de créer un dossier avec votre code de langue à 2 lettres [ISO-639-1](https://en.wikipedia.org/wiki/ISO_639-1) et de copier-coller le contenu du répertoire en dans votre nouveau dossier créé dans le répertoire des documents.

Une fois que votre dossier avec tous les fichiers a été créé, vous pouvez commencer à traduire la documentation dans votre langue.

## **Étapes finales**

Vous vous demandez peut-être ce que vous devez faire une fois que vous avez terminé de traduire ? Eh bien, la dernière étape consiste à faire une PR de votre travail vers le dépôt principal afin que nous puissions le réviser et le fusionner si tout semble bon.

**Merci beaucoup pour votre travail acharné !**