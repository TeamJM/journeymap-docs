## **Utilisation de Base**

Une fois que vous avez [installé](installing.md) JourneyMap, tout ce que vous avez à faire est de rejoindre un serveur ou de charger un monde en solo.

Pour la plupart, JourneyMap fonctionne directement après l'installation. Tout ce que vous avez à faire pour commencer à cartographier votre monde est de commencer à l'explorer ! La zone autour de vous sera cartographiée automatiquement au fur et à mesure de vos déplacements, et sera visible dans chacun des trois types de cartes que JourneyMap prend en charge.

## **Mappages de Touches**

Les mappages de touches suivants sont disponibles par défaut lorsque vous jouez sur un serveur mondial ou multijoueur.

- ++j++ - Afficher ou masquer la carte en plein écran
- ++ctrl+j++ - Afficher ou masquer la mini-carte. Sur Fabric, il s'agit plutôt de ++m++, car Fabric ne prend pas en charge les touches de modification pour les raccourcis clavier.
- ++equal++ / ++minus++ - Zoom avant et arrière sur la mini-carte
- ++bracket-left++ - Cycle le type de carte affiché dans la mini-carte
- ++backslash++ - Basculer entre les préréglages de la mini-carte
- ++b++ - Créez [un waypoint](waypoints.md) où vous vous trouvez
- ++n++ - Ouvrir le [gestionnaire de waypoints](waypoints.md)
- ++g++ - Basculer les étiquettes de nom d'entité

JourneyMap dispose également de raccourcis clavier pour basculer le rendu des points de cheminement (tous les points de cheminement, dans le monde uniquement ou sur la carte uniquement). Ceux-ci ne sont pas liés par défaut – attribuez-les dans les contrôles de Minecraft si vous le souhaitez.

Toutes les clés spécifiées dans la documentation peuvent être personnalisées dans les paramètres de Minecraft. Ouvrez simplement le menu (par défaut, avec la touche ++esc++), cliquez sur Options puis sur Contrôles, et vous verrez deux nouvelles catégories pour toutes les touches de JourneyMap.

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

Le texte au-dessus et au-dessous de la mini-carte est affiché dans les emplacements d'informations. Il y en a quatre. Par défaut, ils affichent :

- Emplacement 1 : rien (vide)
- Slot 2 : le temps de jeu
- Emplacement 3 : vos coordonnées
- Emplacement 4 : le biome dans lequel vous vous trouvez

La minicarte et ses emplacements d'informations peuvent être personnalisés dans le [gestionnaire de paramètres](settings/minimap.md).

## **La Carte en Plein Écran**

En appuyant sur la touche de la carte en plein écran (par défaut, la touche J), vous pouvez ouvrir la carte en plein écran.

![Carte en Plein Écran](../img/full-screen.png){: .center}

Cette carte vous donne une vue défilable de toutes les zones de la carte que vous avez explorées jusqu'à présent, affichées telles qu'elles étaient lorsque vous les avez découvertes. Elle donne également accès aux paramètres de JourneyMap et à un certain nombre d'options d'affichage de la carte.

Pour plus d'informations sur la carte en plein écran, veuillez consulter [la page de la carte en plein écran](settings/full-screen-map.md).

## **La Webmap**

La carte Web vous permet de visualiser et d'explorer votre carte dans un navigateur Web, y compris depuis un autre appareil tel qu'un téléphone ou une tablette, pendant que le jeu est en cours d'exécution. Depuis JourneyMap 6.0, la carte Web est un module complémentaire distinct.

![Webmap](../img/webmap.png){: .center}

Consultez la section [Webmap](../webmap/installing.md) pour savoir comment l'installer et l'utiliser.
