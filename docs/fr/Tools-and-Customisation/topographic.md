## **Terminologie**

- **Carte topographique** : Une représentation graphique de la position, de l'échelle, de la forme, du relief et de la distribution des caractéristiques naturelles et culturelles sélectionnées d'une zone de la surface de la Terre.
- **Ligne de contour** : Une ligne tracée sur une carte topographique reliant deux points d'élévation égale au-dessus du niveau de la mer.
- **Intervalle de contour** : La distance verticale entre deux lignes de contour adjacentes.

[Source](https://quizlet.com/16183184/topographic-maps-terms-flash-cards)

## **Aperçu des Cartes Topographiques dans JourneyMap**

Les cartes topographiques de JourneyMap vous permettent de voir les contours d'élévation de votre monde. Vous pouvez personnaliser les propriétés et les couleurs de la carte topographique dans (`.minecraft/journeymap/config/5.2/journeymap.topo.config`) selon ce qui vous semble le mieux ou ce que vous souhaitez mettre en valeur.

Voici comment cela fonctionne :

**{Hauteur du monde} ÷ {Nombre de couleurs} = {Intervalle de contour}**

Ainsi, étant donné une **hauteur de monde de 256** blocs, une palette de **32 couleurs** créera 32 contours d'élévation, chacun ayant un **intervalle de contour de 8** blocs de hauteur.

- 1ère couleur : y 0-7
- 2ème couleur : y 8-15
- etc.

## **Personnalisation**

Le fichier de configuration des cartes topographiques `.minecraft/journeymap/config/5.2/journeymap.topo.config` peut être modifié avec un simple éditeur de texte. Vous pouvez y apporter des modifications, les enregistrer et voir les résultats immédiatement dans JourneyMap sans avoir besoin de redémarrer.

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