## **Utilisation de Base**

!!! warning "Translation needed for 6.0"

    This page was updated for JourneyMap 6.0. Some sections shown are
    the English source pending translation. See Contributing to help
    translate the docs.

Une fois que vous avez [installé](installing.md) JourneyMap, tout ce que vous avez à faire est de rejoindre un serveur ou de charger un monde en solo.

Pour la plupart, JourneyMap fonctionne directement après l'installation. Tout ce que vous avez à faire pour commencer à cartographier votre monde est de commencer à l'explorer ! La zone autour de vous sera cartographiée automatiquement au fur et à mesure de vos déplacements, et sera visible dans chacun des trois types de cartes que JourneyMap prend en charge.

## **Mappages de Touches**

The following key mappings are available by default when you are playing on a world or multiplayer server.

- ++j++ - Show or hide the full-screen map
- ++ctrl+j++ - Show or hide the minimap. On Fabric this is ++m++ instead, because Fabric does not support modifier keys for keybinds
- ++equal++ / ++minus++ - Zoom the minimap in and out
- ++bracket-left++ - Cycle the map type shown in the minimap
- ++backslash++ - Switch between minimap presets
- ++b++ - Create [a waypoint](waypoints.md) where you are standing
- ++n++ - Open the [waypoint manager](waypoints.md)
- ++g++ - Toggle entity name labels

JourneyMap also has keybinds for toggling waypoint rendering (all waypoints, in-world only, or on-map only). These are unbound by default - assign them in Minecraft's Controls if you want them.

All keys specified in the documentation can be customized in Minecraft's own settings. Just open the menu (by default, with the ++esc++ key), click on Options and then Controls, and you will see two new categories for all of JourneyMap's keys.

## **Marqueurs**

Tous les types de cartes contiennent des marqueurs. Ces marqueurs dénotent diverses pièces d'informations - telles que la position d'une entité ou [un point de repère](waypoints.md) sur la carte.

| Icône                                                          | Description                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| ![Marqueur-Joueur](../img/markers/marker-player.png){: .center} | Votre position sur la carte. *Note : Cette icône a <br>une bordure blanche en jeu.* |
| ![Point de Repère](../img/markers/waypoint.png){: .center}    | [Un point de repère](waypoints.md). La couleur peut être définie <br>dans le gestionnaire de points de repère. |
| ![Point de Repère](../img/markers/waypoint-death.png){: .center} | [Un point de repère de mort](waypoints.md)                                        |

| Icône                                                                  | Description                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![Marqueur-Blanc](../img/markers/marker-white.png){: .center}          | Un marqueur dénotant une entité sur la carte. La couleur <br>du marqueur dénote le type d'entité. |
| ![Marqueur-Blanc-Bas](../img/markers/marker-white-down.png){: .center} | Une entité en dessous de vous.                                                                     |
| ![Marqueur-Blanc-Haut](../img/markers/marker-white-up.png){: .center}  | Une entité au-dessus de vous.                                                                      |

| Icône                                                        | Description                          |
|--------------------------------------------------------------|--------------------------------------|
| ![Marqueur-Gris](../img/markers/marker-grey.png){: .center}  | Une entité neutre, comme un animal.  |
| ![Marqueur-Vert](../img/markers/marker-green.png){: .center} | Un villageois.                        |
| ![Marqueur-Bleu](../img/markers/marker-blue.png){: .center}  | Un autre joueur.                      |
| ![Marqueur-Rouge](../img/markers/marker-red.png){: .center}  | Une entité hostile, comme un monstre. |

Les marqueurs et leur affichage peuvent être personnalisés dans le [gestionnaire de paramètres](settings/minimap.md).

## **La Minicarte**

Par défaut, la minicarte sera affichée dans le coin supérieur droit de votre écran.

![Minicarte](../img/minimap.png){: .center}

Ceci est votre minicarte. Par défaut, elle affiche la zone autour de votre personnage, ainsi que des informations de base et les positions de votre personnage, d'autres joueurs, d'animaux et de monstres.

La minicarte peut être zoomée et dézoomée à tout moment en appuyant sur l'une des touches de zoom (par défaut, les touches ++equal++ et ++minus++).

The text above and below the minimap is shown in info slots. There are four of them. By default they show:

- Slot 1: nothing (blank)
- Slot 2: the in-game time
- Slot 3: your coordinates
- Slot 4: the biome you are in

La minicarte et ses emplacements d'informations peuvent être personnalisés dans le [gestionnaire de paramètres](settings/minimap.md).

## **La Carte en Plein Écran**

En appuyant sur la touche de la carte en plein écran (par défaut, la touche J), vous pouvez ouvrir la carte en plein écran.

![Carte en Plein Écran](../img/full-screen.png){: .center}

Cette carte vous donne une vue défilable de toutes les zones de la carte que vous avez explorées jusqu'à présent, affichées telles qu'elles étaient lorsque vous les avez découvertes. Elle donne également accès aux paramètres de JourneyMap et à un certain nombre d'options d'affichage de la carte.

Pour plus d'informations sur la carte en plein écran, veuillez consulter [la page de la carte en plein écran](settings/full-screen-map.md).

## **La Webmap**

The webmap lets you view and explore your map in a web browser, including from another device such as a phone or tablet, while the game is running. As of JourneyMap 6.0 the webmap is a separate addon mod.

![Webmap](../img/webmap.png){: .center}

See the [Webmap](../webmap/installing.md) section for how to install and use it.
