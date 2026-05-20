## **Terminologie**

!!! warning "Translation needed for 6.0"

    This page was updated for JourneyMap 6.0. Some sections shown are
    the English source pending translation. See Contributing to help
    translate the docs.

- **Carte topographique** : Une représentation graphique de la position, de l'échelle, de la forme, du relief et de la distribution des caractéristiques naturelles et culturelles sélectionnées d'une zone de la surface de la Terre.
- **Ligne de contour** : Une ligne tracée sur une carte topographique reliant deux points d'élévation égale au-dessus du niveau de la mer.
- **Intervalle de contour** : La distance verticale entre deux lignes de contour adjacentes.

[Source](https://quizlet.com/16183184/topographic-maps-terms-flash-cards)

## **Aperçu des Cartes Topographiques dans JourneyMap**

JourneyMap's Topographic Maps let you see the elevation contours of your world.  You can customize the topographic map properties and colors in (`.minecraft/journeymap/config/6.0/journeymap.topo.config`) according to what looks best to you, or what you want to emphasize.

Voici comment cela fonctionne :

**{World height} / {Number of colors} = {Contour interval}**

So, given a **world height of 384** blocks, a palette of **32 colors** will create 32 elevation contours, each with a **contour interval of 12** blocks high.

- 1st color: the lowest 12 blocks
- 2nd color: the next 12 blocks
- etc.

!!! note "Custom Max Topo Height"

    By default the topographic map uses the world's full build height
    for the contour math. The [Cartography settings](../client/settings/cartography.md)
    have a **Custom Max Topo Height** option that lets you cap the
    height used, which is useful for emphasizing contours in a height
    range you care about. Any blocks above the cap are drawn in the
    top color.

## **Personnalisation**

The topographic maps config file `.minecraft/journeymap/config/6.0/journeymap.topo.config` can be edited with a simple text editor.  You can make changes to it, save it, and see the results immediately in JourneyMap without a need to restart.

Le fichier contient les propriétés suivantes :

- **showContour** : Indique si une ligne de contour doit être affichée entre les intervalles de contour. Par défaut, c'est vrai.
- **landContour** : Couleur hexadécimale (#rrggbb) des lignes de contour sur la terre. Ignoré si showContour est faux.
- **waterContour** : Couleur hexadécimale (#rrggbb) des lignes de contour sur l'eau. Ignoré si showContour est faux.
- **land** : Liste de couleurs hexadécimales entre guillemets, séparées par des virgules (#rrggbb) pour le terrain terrestre. Le nombre de couleurs détermine les intervalles de contour (voir l'Aperçu ci-dessus).
- **water** : Liste de couleurs hexadécimales entre guillemets, séparées par des virgules (#rrggbb) pour l'eau. Le nombre de couleurs détermine les intervalles de contour (voir l'Aperçu ci-dessus).
- **configVersion** : Utilisé par JourneyMap pour suivre les modifications de configuration. Vous pouvez ignorer cela et ne pas avoir besoin de le changer.

Si vous trouvez le fichier irrécupérable, ne paniquez pas. Il suffit de le supprimer et de redémarrer Minecraft, un nouveau fichier sera créé pour vous.

## **Choisir de Bonnes Couleurs**

En vérité, il est peu probable de trouver un ensemble de couleurs "taille unique" pour les cartes topographiques. La plupart des cartes réelles ont des dégradés non linéaires personnalisés pour mieux fonctionner avec les caractéristiques de terrain uniques d'une zone spécifique. Par exemple, des couleurs qui aident à voir clairement les changements d'élévation dans un endroit comme le Kansas, aux États-Unis (très plat), ne fonctionneraient pas bien dans l'État voisin du Colorado et ses montagnes Rocheuses.

Pour quelques exemples de dégradés topographiques utilisés dans le monde réel, consultez [ce site](http://soliton.vm.bytemark.co.uk/pub/cpt-city/index.html), en particulier [cette page](http://soliton.vm.bytemark.co.uk/pub/cpt-city/views/topo.html).

Pour votre commodité, l'outil [Éditeur de Couleur](https://jsfiddle.net/techbrew/4vm9as0o/embedded/result/) et l'outil [Générateur de Dégradé](https://jsfiddle.net/techbrew/umh423j0/embedded/result/) peuvent être utiles pour choisir des couleurs pour vos cartes topographiques.