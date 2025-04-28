## **Aperçu**

Depuis JourneyMap 5.1.3, il n'existe pas de mécanisme côté serveur pour générer une carte d'un serveur multijoueur. Cependant, si vous êtes propriétaire d'un serveur (ou si vous pouvez obtenir une copie du dossier de données du monde du serveur), voici une solution de contournement :

## **Solution de contournement**

- Copiez le dossier de données du monde du serveur sur votre PC local et chargez-le comme un monde en solo Minecraft.
- Dans JourneyMap, allez dans **J > Options > Avancé** et réglez la "Fréquence de sondage de l'AutoMap" sur la valeur la plus basse autorisée (500 ms). (C'est le temps que JourneyMap laisse à Minecraft pour faire une pause entre les fichiers de région. L'exécution de l'Automap peut provoquer un lag si vous essayez de continuer à jouer pendant son fonctionnement. Réduire le taux de sondage augmente le lag, mais réduit le temps total nécessaire pour Automap le monde.)
- Dans JourneyMap, exécutez **J > Actions > Automap** pour toutes les régions. Gardez à l'esprit que l'Automap ne fera que la dimension dans laquelle vous vous trouvez, et uniquement la surface si vous êtes à la surface. Ou, si vous êtes sous terre, uniquement la tranche verticale (chunk) dans laquelle vous étiez lorsque vous avez lancé l'Automap. Si vous souhaitez Automapper plusieurs tranches ou dimensions, déplacez-vous vers la zone correspondante et relancez l'Automap.
- Si vous envisagez de partager les résultats avec d'autres joueurs, notez que tous les points de chemin que vous créez seront enregistrés dans le même dossier que les tuiles d'image de la carte.

Une fois terminé, les tuiles d'image de carte générées et les points de chemin se trouveront dans `.minecraft/journeymap/data/sp/{nomdumonde}`. Pour utiliser les résultats lors de votre prochaine connexion au serveur, vous devrez copier le contenu de ce dossier vers celui que JourneyMap utilise pour votre connexion serveur : `.minecraft/journeymap/data/mp/{nomduserveur}`. Si vous souhaitez partager les résultats avec d'autres joueurs, il vous suffit de compresser le dossier et de leur donner ces instructions.