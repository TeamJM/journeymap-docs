
## **Packs de ressources d'icônes de point de cheminement**

JourneyMap est livré avec un ensemble d'icônes de waypoints intégrées, mais vous pouvez ajouter
les vôtres en les expédiant dans un pack de ressources Minecraft. Choix de JourneyMap
les icônes s'affichent automatiquement et elles apparaissent dans le sélecteur d'icônes dans le
éditeur de waypoints.

Pour les icônes de foule et d'entité (un système différent), voir
[Icônes de foule personnalisées](custom-mob-icons.md).

## **Resource pack path**

Placez vos icônes de waypoint dans un pack de ressources sur ce chemin :

```text
assets/journeymap/textures/waypoint/icon/<name>.png
```

`<name>` devient le nom de l'icône dans le sélecteur d'icône de l'éditeur de waypoints,
alors utilisez quelque chose de descriptif.

En termes de code/emplacement de ressource, ce chemin est
`journeymap:textures/waypoint/icon/<name>.png`.

## **Image size**

Les icônes de waypoint doivent mesurer **16x16** pixels. Les images d'autres tailles ne le seront pas
rendre correctement. Utilisez des fichiers PNG transparents pour que l'icône se fonde avec le
marqueur de point de cheminement.

## **Example resource pack**

Un pack de ressources de démarrage est disponible pour être utilisé comme modèle :

[icons_test.zip](https://github.com/user-attachments/files/26309255/icons_test.zip)

Pour l'utiliser :

1. Ouvrez le zip dans 7-Zip, WinZip, WinRAR ou tout autre outil zip.
2. Modifiez le `description` dans `pack.mcmeta`.
3. Supprimez les fichiers d'aide inclus dans l'exemple.
4. Mettez vos images PNG 16x16 dans
   `assets/journeymap/textures/waypoint/icon` à l'intérieur du zip.
5. Renommez le zip comme vous voulez que le pack soit appelé.
6. Déposez le zip dans votre dossier `resourcepacks` et activez-le dans
   Écran des packs de ressources de Minecraft.

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

Les icônes placées directement dans `textures/waypoint/icon/` apparaissent dans le
Ensemble **JourneyMap**. Pour expédier vos icônes sous leur propre ensemble nommé, placez-les dans un
**sous-dossier** :

```text
assets/journeymap/textures/waypoint/icon/<set>/<name>.png
```

Chaque sous-dossier devient son propre onglet dans le sélecteur d'icônes. Le nom du sous-dossier
(`<set>`) est l'identifiant de l'ensemble. Les ensembles de packs de ressources apparaissent à côté
Onglets intégrés de JourneyMap - **Tous**, **JourneyMap**, **Minecraft**
(textures d'objets vanille) et **Map Deco** (marqueurs de carte).

### Nommer l'ensemble

Par défaut, l'onglet porte le nom du sous-dossier brut. Pour lui donner un
nom convivial et localisable, ajoutez cette clé de traduction au fichier de votre pack de ressources
fichiers de langue :

```text
waypoint.icon.set.<set>.name
```

Par exemple, un sous-dossier `houses` :

`assets/journeymap/lang/en_us.json`:

```json
{
  "waypoint.icon.set.houses.name": "Cool Houses"
}
```

`assets/journeymap/lang/es_es.json`:

```json
{
  "waypoint.icon.set.houses.name": "Casas Geniales"
}
```

La clé est facultative. Sans cela, l'onglet affiche le nom du sous-dossier (`houses`).

### Info-bulle pour l'ensemble

Pour afficher une info-bulle de survol sur l'onglet de l'ensemble, ajoutez une deuxième clé de traduction
à côté du nom :

```text
waypoint.icon.set.<set>.name.tooltip
```

Pour le même sous-dossier `houses` :

`assets/journeymap/lang/en_us.json`:

```json
{
  "waypoint.icon.set.houses.name": "Cool Houses",
  "waypoint.icon.set.houses.name.tooltip": "Player-built houses and bases."
}
```

`assets/journeymap/lang/es_es.json`:

```json
{
  "waypoint.icon.set.houses.name": "Casas Geniales",
  "waypoint.icon.set.houses.name.tooltip": "Casas y bases construidas por jugadores."
}
```

La clé d'info-bulle est facultative. Sans cela (ou avec une valeur vide), l'onglet
n'affiche aucune info-bulle au survol.

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

Icônes dans un ensemble placé sous l'espace de noms `journeymap` (le chemin indiqué ci-dessus)
sont teintés par la couleur du waypoint, comme les icônes intégrées de JourneyMap. Utiliser 16x16
fichiers PNG transparents, comme pour l’ensemble JourneyMap.
