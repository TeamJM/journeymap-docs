## **Mobs personnalisés sur la carte (radar de mobs)**

- Assurez-vous que vos EntityCreatures implémentent au moins une de ces interfaces principales de Minecraft : IAnimal, IMob, INpc ou IWaterMob.
- Si vous souhaitez fournir vos propres icônes de mobs, consultez [Ensembles d'icônes de mobs personnalisés](custom-mob-icons.md).
- Les EntityCreatures avec une cible hostile seront affichées comme hostiles.
- Les EntityCreatures définies comme invisibles (cachées) ne seront pas visibles sur le radar.

## **Créer des suggestions de points de passage dans le chat**

Les joueurs peuvent ajouter des points de passage en cliquant sur un texte formaté spécialement dans le chat. (Pratique pour donner des quêtes, des messages de bienvenue, etc.)

Par exemple :

`Le PNJ dit : "Voici où j'ai enterré mon butin :" [name:"trésor", x:1212, y:70, z:456, dim:0]`

Le texte du chat lui-même n'est pas modifié, mais il est transformé en lien pour les joueurs utilisant JourneyMap. Le texte survolé indique qu'il peut être cliqué pour créer un point de passage, ou shift-cliqué pour s'afficher sur la carte en plein écran.

!!! note "Remarque"

    ''name'' et ''dim'' sont facultatifs. Si ''dim'' est omis, la dimension du joueur est supposée.

## **Afficher des formes, du texte ou des points de passage personnalisés sur la carte**

Il existe une [API JourneyMap](https://github.com/TeamJM/journeymap-api) (pour Minecraft 1.9.4 et versions ultérieures) qui vous permet de gérer des points de passage personnalisés et d'ajouter des superpositions sur la minicarte, la carte en plein écran ou la carte web.

## **En cas de doute, contactez-nous !**

Prenez contact avec l'équipe JourneyMap @Developers sur le serveur public [JourneyMap Discord](https://discord.gg/eP8gE69).