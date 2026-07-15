
## **Mobs personnalisés sur la carte (radar de foule)**

JourneyMap classe les entités pour le radar selon leur type et leur catégorie d'entité Minecraft, et non selon l'interface personnalisée que vous implémentez.

- Les entités hostiles, passives, ambiantes et PNJ sont reconnues automatiquement à partir de leur classe d'entité vanille (par exemple `PathfinderMob`, `Animal`, `WaterAnimal`, `Villager` et les interfaces de marqueurs `Enemy` et `Npc`).
- Une entité qui a actuellement une cible d'attaque est affichée comme hostile, même si elle est normalement passive.
- Les entités invisibles pour le joueur (y compris les joueurs furtifs) sont cachées sur le radar.
- Si vous souhaitez fournir vos propres icônes de foule, voir [Jeux d'icônes de foule personnalisés](custom-mob-icons.md).

!!! note "Note"

    Si votre mod utilise une classe d'entité inhabituelle que JourneyMap ne récupère pas automatiquement, vous pouvez l'enregistrer via l'API JourneyMap (voir ci-dessous) en utilisant l'événement d'enregistrement d'entité.

## **Créer des suggestions de waypoints dans le chat**

Les joueurs peuvent ajouter des waypoints en cliquant sur un texte spécialement formaté dans le chat.  (Pratique pour donner des quêtes, des messages de bienvenue, etc.)

Par exemple:

`NPC says: "Here's where I buried my loot:" [name:treasure, x:1212, y:70, z:456, dim:0]`

Le texte du chat lui-même n'est pas modifié, mais est transformé en lien pour les joueurs disposant de JourneyMap.  Le texte de survol indique qu'il est possible de cliquer sur celui-ci pour créer un point de cheminement ou d'appuyer sur la touche Maj pour l'afficher sur la carte en plein écran.

Un emplacement est constitué de deux ou plusieurs paires `name:value` entre crochets, séparées par des virgules.  Les coordonnées `x` et `z` sont obligatoires ; `y`, `dim` et `name` sont facultatifs.  L'ordre des paires n'a pas d'importance.  Voir [Partage des waypoints](../client/waypoints.md#location-format) sur la page Waypoints du client pour le format complet.

!!! note "Note"

    Si `dim` est omis, la dimension du joueur est supposée.

## **Afficher des formes personnalisées, du texte ou des points de cheminement sur la carte**

L'[JourneyMap API](https://github.com/TeamJM/journeymap-api) donne aux auteurs de mods la possibilité de gérer des waypoints personnalisés et de dessiner des superpositions (polygones, marqueurs et images) sur la mini-carte, la carte plein écran et la carte Web.

Ajoutez l'API en tant que dépendance, implémentez une classe de plugin et inscrivez-vous aux événements qui vous intéressent.  Le référentiel API comprend un exemple de mod qui démontre une intégration fonctionnelle.

## **Quoi de neuf pour les intégrateurs dans la version 6.0**

JourneyMap 6.0 est livré avec une API retravaillée.  Points forts pour les auteurs de mods :

- **API v2** - l'API réside désormais sous le package `journeymap.api.v2`.  Mettez à jour vos importations et l'enregistrement du plugin en conséquence.
- **Plus d'événements** - les nouveaux événements client et serveur couvrent le cycle de vie des points de cheminement (création, mise à jour, suppression), les groupes de points de cheminement, le transfert de groupe, le radar d'entité, le rendu plein écran, les menus contextuels et les points de cheminement globaux et les groupes de points de cheminement côté serveur.  Inscrivez-vous via les registres d'événements v2.
- **Enregistrement InfoSlot basé sur les composants** - les modules complémentaires enregistrent des emplacements d'informations personnalisés via l'événement de registre.  Les étiquettes des emplacements sont désormais des `Component` du chat Minecraft plutôt que des chaînes simples.
- **Données personnalisées saisies sur les points de cheminement et les groupes de points de cheminement** - les points de cheminement et les groupes prennent en charge les données personnalisées saisies et saisies afin que les modules complémentaires puissent attacher leurs propres valeurs sans entrer en collision les uns avec les autres ou avec JourneyMap.  Les anciens accesseurs de données personnalisés à valeur unique sont obsolètes.
- **ShapeProperties.StrokePosition** - Les superpositions de formes peuvent définir l'endroit où le trait est dessiné par rapport au bord (à l'intérieur, au centre ou à l'extérieur).
- **Icônes EntityDTO** - les chemins des icônes d'entité sont exposés en tant qu'emplacements de ressources Minecraft, ce qui facilite le pointage vers vos propres textures d'icônes.

!!! note "Note"

    Cette page est un aperçu.  Pour connaître les noms exacts des classes et des méthodes, consultez la source de l'API et l'exemple de mod dans le [référentiel voyagemap-api](https://github.com/TeamJM/journeymap-api), qui fait autorité et suit chaque version.

## **En cas de doute, parlez-nous !**

Entrez en contact avec l’équipe JourneyMap @Developers sur le public [JourneyMap Discord server](https://discord.gg/eP8gE69).
