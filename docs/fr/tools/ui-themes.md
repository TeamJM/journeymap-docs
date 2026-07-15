# **UI Themes**

L'apparence des barres d'outils, des boutons et du cadre de la mini-carte de JourneyMap est définie par
un thème d'interface utilisateur. Vous pouvez changer de thème avec le bouton Thème de l'interface utilisateur (le bouton Peinture
icône de la palette) sur la carte en plein écran, et vous pouvez créer votre propre thème
avec vos propres images et couleurs.

## **Bundled themes**

JourneyMap est livré avec deux familles de thèmes :

- **Flat** - un ensemble de thèmes de style plat : Purist (par défaut), Desert
  Temple, EndCity, manoir forestier, forteresse du Nether, monument océanique et
  Forteresse. Tout cela se trouve dans le dossier thématique `flat`.
- **Victorian** - un thème plus orné, dans le dossier thématique `victorian_`.

Utilisez le bouton Thème de l'interface utilisateur pour parcourir les thèmes disponibles dans votre
version installée.

## **Theme files**

Les thèmes se trouvent dans le dossier de thèmes JourneyMap :

```text
.minecraft/journeymap/icon/theme/
```

Chaque thème est un dossier contenant un fichier de définition de thème ainsi que le
images qu'il utilise. Le fichier de définition est JSON et se termine par
`.theme2.json`. JourneyMap extrait les thèmes regroupés dans ce dossier
la première fois qu'il s'exécute, vous pouvez donc les ouvrir pour voir comment fonctionne un
le thème est construit.

!!! note "Theme schema 2"

    JourneyMap 6.0 utilise la version 2 du format de thème. Fin des fichiers de thème
    dans `.theme2.json` et contiennent une propriété `"schema": 2`. Thèmes
    écrits pour les anciennes versions de JourneyMap ne sont pas compatibles et
    il faut reconstruire.

## **Créer un thème : démarrage facile**

1. Ouvrez `.minecraft/journeymap/icon/theme/` et copiez l'un des fichiers fournis
   dossiers de thème (par exemple `victorian_`) vers un nouveau dossier avec votre
   propre nom, par exemple `MyTheme`.
2. Dans votre nouveau dossier, renommez le fichier `.theme2.json` pour qu'il corresponde, par exemple
   exemple `MyTheme.theme2.json`.
3. Ouvrez ce fichier dans un éditeur de texte et modifiez les valeurs `name`, `directory`,
   et `author` afin qu'elles correspondent à votre dossier et à votre nom. Le
   La valeur `directory` doit être le nom exact de votre dossier de thème.
4. Remplacez les images du dossier par vos propres illustrations. Gardez le
   dimensions de l'image conformes à ce que contient le fichier `.theme2.json`
   déclare, ou mettez à jour ces dimensions dans le fichier pour qu'elles correspondent à votre art.
5. Utilisez le bouton Thème de l'interface utilisateur sur la carte en plein écran pour passer à votre
   thème.
6. Pour partager votre thème, compressez le dossier du thème et donnez-le à d'autres.
   Ils le décompressent dans `.minecraft/journeymap/icon/theme/` et le sélectionnent
   avec le bouton Thème de l'interface utilisateur.

## **La structure du fichier de thème**

Un fichier `.theme2.json` est lu avec GSON. Vous modifiez les valeurs, mais vous
ne peut pas changer la structure. Le niveau supérieur comprend :

- `schema` - la version au format thème. Doit être `2`.
- `author`, `name`, `directory` - informations d'identification.
- `container` - spécifications de la barre d'outils (voir ci-dessous).
- `control` - spécifications des boutons et des bascules.
- `fullscreen` - couleurs d'arrière-plan de la carte plein écran et d'étiquette d'état.
- `icon` - la taille et la couleur par défaut des icônes du dossier `icon`.
- `minimap` - les spécifications du cadre de la mini-carte, avec `circle` et
  Sections `square`.

### Valeurs de couleur et d'image

Deux types de valeurs apparaissent dans le fichier :

- Une **valeur de couleur** est un objet avec une chaîne hexadécimale `color` (`#rrggbb`)
  et une valeur `alpha`. Utilisez `#ffffff` pour que la couleur laisse celle d'une image
  couleurs inchangées.
- Une **spécification d'image** déclare un `width` et un `height`, et peut également porter
  un `color` et un `alpha`.

### Conteneurs et contrôles

- `container.toolbar.horizontal` et `container.toolbar.vertical`
  décrire les barres d'outils. Une barre d'outils est construite à partir d'une image `begin`, d'un
  répétition d'une image `inner` (une répétition par bouton) et d'une image `end`.
  Chacun a `useThemeImages`, un nom de fichier `prefix`, `margin` et
  `padding`.
- `control.button` et `control.toggle` décrivent le bouton et la bascule
  contrôles : leurs `width`, `height`, leurs styles d'info-bulle et la couleur
  valeurs utilisées pour l'icône et le bouton dans chaque état (on, off, survol,
  désactivée).

### Minimap

`minimap.circle` et `minimap.square` décrivent le cercle et le carré
cadres de mini-carte. Chacun définit les tailles d'image du bord et du masque, le haut et
styles d'étiquette du bas, images de points cardinaux et vers lequel pointe la boussole
spectacle, ainsi que les couleurs du réticule et du cadre.

Les thèmes groupés constituent la meilleure référence pour les noms de fichiers exacts et
tailles - copiez-en une et comparez son `.theme2.json` aux images de son
dossier.

## **Image guidance**

Créez vos images à 2x les tailles déclarées dans le fichier `.theme2.json`.
Cela permet aux boutons de rester nets sur les écrans haute résolution et pour
joueurs utilisant les plus grandes échelles d'interface graphique de Minecraft.

## **Définition d'un thème par défaut dans un modpack**

Un modpack peut fournir un thème et en faire le thème par défaut pour l'ouverture des joueurs.
JourneyMap pour la première fois. Placez le dossier du thème dans
`.minecraft/journeymap/icon/theme/` comme d'habitude, puis créez ce fichier :

```text
.minecraft/journeymap/icon/theme/default.theme.config
```

Son contenu pointe vers le dossier du thème, le fichier du thème et le thème
nom :

```json
{
  "directory": "MyTheme",
  "filename": "MyTheme",
  "name": "MyTheme"
}
```

## **Partager votre thème**

Si vous créez un thème et souhaitez le partager, passez par le
[Serveur Discord JourneyMap](https://discord.gg/eP8gE69).
