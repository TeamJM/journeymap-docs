# **Paramètres avancés**

Cette section contient des paramètres avancés pour les utilisateurs expérimentés et ceux qui souhaitent modifier certains éléments internes de JourneyMap.

!!! warning "Warning"

    Les paramètres de cette section peuvent avoir des effets extrêmes sur les performances de votre client. Nous vous déconseillons de toucher à ces paramètres, sauf si vous comprenez bien ce que vous faites ou si un membre de l'équipe d'assistance JourneyMap vous demande de le faire.

Si la modification de ces paramètres fait planter votre client ou entraîne un horrible retard de votre ordinateur, ne dites pas que nous ne vous avons pas prévenu.

![Paramètres avancés](../../img/settings/client/advanced-options.png){: .center}

## **Toggles**

Les paramètres de bascule **gras** ci-dessous sont activés par défaut.

| Basculer | Descriptif |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Annoncez le module** | Annonce dans la fenêtre de discussion que JourneyMap est prêt |
| **Vérifiez les mises à jour des modules** | Désactiver cette option signifie que vous ne serez pas averti lorsqu'une nouvelle version de JourneyMap sera disponible |
| **Mise en cache de fragments de données** | Active ou désactive la mise en cache de morceaux - lorsqu'elle est désactivée, la téléportation ou la création de points de cheminement en dehors de votre plage de rendu sera par défaut au niveau de la mer y=64 |
| Vérification des erreurs GL | Active la vérification des erreurs OpenGL - l'activation peut diminuer les performances et un redémarrage est requis après avoir modifié cette valeur. S'applique uniquement aux versions OpenGL ; la version Minecraft 26.2 utilise Vulkan |
| **Masquer les entités furtives** | S'il faut cacher les créatures qui tentent de se faufiler (s'accroupir) |
| Masquer les spectateurs | Faut-il cacher les spectateurs sur le radar |
| **Tuiles LOD** | Activer le rendu des tuiles LOD (niveau de détail) lors d'un zoom arrière sur la carte - la désactivation et l'enregistrement supprimeront les fichiers de cache LOD du disque |
| **Superposition de type de carte mini-carte** | Afficher ou masquer l'icône de type de carte qui apparaît brièvement lorsque vous changez le type de carte de la mini-carte (Jour, Nuit, Grotte, Topo, Biome) |
| **Superposition de numéros prédéfinis sur la mini-carte** | Afficher ou masquer la superposition de numéros affichée lors du changement de préréglage de la mini-carte |
| ** Fondu de l'icône de la foule ** | Activer ou désactiver la décoloration des icônes de foule en fonction de la distance verticale par rapport au joueur |
| Prise en charge multi-monde | Expérimental : empêche l'écrasement de la carte dans les configurations de serveur multi-mondes - ne prend effet qu'après avoir rejoint le serveur |
| ** Fondu de l'icône du joueur ** | Activer ou désactiver la décoloration des icônes des joueurs en fonction de la distance verticale par rapport au joueur || Enregistrer les statistiques du cache | S'il faut activer les caches pour enregistrer leurs statistiques - peut légèrement nuire aux performances s'il est activé - destiné aux bêta-testeurs |
| **Rendu la mini-carte derrière les écrans** | Autoriser le rendu de la mini-carte derrière des écrans ouverts |
| Utiliser les icônes héritées | Utilisez les icônes de foule fournies avec JourneyMap au lieu de celles générées automatiquement ou celles fournies dans les packs de ressources |
| Utiliser l'adresse IP du serveur | Utiliser l'adresse IP du serveur lors de la sauvegarde des données pour conserver l'unicité des cartes ; ne prend effet qu'après avoir rejoint le serveur |

## **Autres paramètres**

L'option par défaut pour chaque paramètre ci-dessous est marquée d'un **texte en gras.**

| Paramètre | Options | Descriptif |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Niveau de journalisation | <ul><li>**INFO**</li><li>ALL</li><li>DEBUG</li><li>ERROR</li><li>FATAL</li><li>OFF</li><li>TRACE</li><li>WARN</li></ul> | Définissez le niveau de détail des journaux de JourneyMap - attention, certains niveaux de journalisation nuiront aux performances, conservez la valeur par défaut sauf indication contraire |
| Fréquence des sondages AutoMap | Plage : 500 - 10 000 (en ms) <br>La valeur par défaut est **2000** | Délai entre les tâches de région AutoMap : des valeurs inférieures réduiront le temps d'exécution d'AutoMap, mais peuvent nuire aux performances |
| Cacher les animaux | Plage : 100 - 10 000 (en ms) <br>La valeur par défaut est **3 100** | Durée Les données radar sont mises en cache avant de rechercher de nouveaux animaux – des valeurs inférieures peuvent nuire aux performances |
| Cacher les monstres | Plage : 100 - 10 000 (en ms) <br>La valeur par défaut est **3 000** | Les données radar de durée sont mises en cache avant de rechercher de nouveaux monstres – des valeurs inférieures peuvent nuire aux performances |
| Lecteur de cache | Plage : 100 - 2 000 (en ms) <br>La valeur par défaut est **1 000** | Les données d'état de durée vous concernant sont mises en cache avant d'être revérifiées - des valeurs inférieures peuvent nuire aux performances |
| Joueurs de cache | Plage : 100 - 10 000 (en ms) <br>La valeur par défaut est **2 000** | Les données radar de durée sont mises en cache avant de rechercher de nouveaux joueurs – des valeurs inférieures peuvent nuire aux performances |
| Cacher les villageois | Plage : 100 - 10 000 (en ms) <br>La valeur par défaut est **2 200** | Durée Les données radar sont mises en cache avant de rechercher de nouveaux villageois – des valeurs inférieures peuvent nuire aux performances |
| Animaux maximum | Plage : 1 - 128 <br>La valeur par défaut est **32** | Le nombre maximum de monstres passifs affichés sur le radar – des nombres plus élevés peuvent provoquer un décalage || Créatures ambiantes maximales | Plage : 1 - 128 <br>La valeur par défaut est **32** | Le nombre maximum de foules ambiantes affichées sur le radar – des nombres plus élevés peuvent provoquer un décalage |
| Nombre maximum de foules | Plage : 1 - 128 <br>La valeur par défaut est **32** | Le nombre maximum de foules hostiles affichées sur le radar – des nombres plus élevés peuvent entraîner un décalage |
| Nombre maximum de joueurs | Plage : 1 - 128 <br>La valeur par défaut est **32** | Le nombre maximum de joueurs affichés sur le radar – des nombres plus élevés peuvent entraîner un décalage |
| Villageois maximum | Plage : 1 - 128 <br>La valeur par défaut est **32** | Le nombre maximum de villageois affichés sur le radar – des nombres plus élevés peuvent entraîner un décalage |
| Portée radar latérale | Plage : 16 - 512 (en blocs) <br>La valeur par défaut est **64** | Distance latérale pour rechercher et afficher des entités sur le radar – des nombres plus élevés peuvent entraîner un décalage important |
| Portée radar verticale | Plage : 8 - 320 (en blocs) <br>La valeur par défaut est **16** | Distance verticale pour rechercher et afficher des entités sur le radar – des nombres plus élevés peuvent entraîner un décalage important |
