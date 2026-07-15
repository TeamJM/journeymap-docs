# **Global Properties**

La catégorie Propriétés globales contient des paramètres qui affectent le comportement côté serveur du mod. Ce sont les valeurs par défaut
propriétés du serveur.

![Global-Properties](../../img/settings/server/global-properties.png){: .center}

## **Toggles**

L'état par défaut de chaque bascule ci-dessous est marqué d'un texte en **gras**.

| Basculer | Descriptif |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Autoriser Journeymap** | S'il faut autoriser Journeymap à fonctionner pour les non-opérateurs.                                                                                                                                 |
| **Identification mondiale** | L'activation modifiera le répertoire de sauvegarde des données de mappage de ce serveur. L'utilisation principale est d'empêcher l'écrasement des cartes et des paramètres lors de l'utilisation d'une configuration multi-mondes et lorsque les utilisateurs ne donnent pas de noms uniques aux serveurs. AVERTISSEMENT : s'il est désactivé puis activé sur un serveur actif, il réinitialisera toutes les données de mappage utilisateur. |
| **Autoriser l'affichage de l'administrateur du serveur** | Indique si les utilisateurs non opérationnels peuvent afficher l'écran d'administration du serveur en mode lecture seule.                                                                                                             |
| **Autoriser la mini-carte** | S'il faut autoriser la mini-carte client. Lorsqu'elle est désactivée, la mini-carte n'est pas disponible pour les joueurs.                                                                                            |
| Masquer l'affichage des coordonnées | Masque tous les affichages de coordonnées et empêche la modification des valeurs de coordonnées pour les waypoints. Remplace la plupart des affichages de coordonnées par le texte « Emplacement inconnu ». Remarque : Cela n'affecte pas les noms de waypoints existants. |
| **Autoriser les points de cheminement** | S'il faut autoriser les waypoints. Désactive complètement le rendu de la carte et des balises du jeu ainsi que les écrans associés.                                                                                   |
| **Autoriser les balises de point de cheminement** | S'il faut autoriser le rendu des balises dans le jeu. (ne désactive pas les waypoints de la carte) |
| **Autoriser les points de cheminement de la mort** | S'il faut autoriser la création de points de cheminement de la mort au décès de l'utilisateur.                                                                                                                        |
| Waypoints mondiaux uniquement | Lorsqu'il est activé, les joueurs peuvent uniquement afficher et activer la visibilité des waypoints globaux. La création, la modification et la suppression de waypoints personnels sont désactivées.                                    |
| Autoriser toutes les téléportations | Permet la téléportation des waypoints et du menu contextuel plein écran. La téléportation par waypoint uniquement est prioritaire !                                                                                    || Téléportation au point de cheminement uniquement | Lorsqu'il est activé, les joueurs ne peuvent se téléporter que via des waypoints. La téléportation arbitraire par clic droit sur la carte est désactivée.                                                                                |
| **Téléportation dimensionnelle** | Activez la téléportation Cross Dimension Waypoint pour les utilisateurs non opérationnels. Les utilisateurs OP peuvent toujours l'utiliser.                                                                                            |
| **Radar des joueurs** | Si les joueurs peuvent voir d'autres joueurs sur la carte.                                                                                                                                         |
| **Noms des joueurs** | Si les joueurs peuvent voir les noms des autres joueurs sur la carte.                                                                                                                                  |
| **Radar villageois** | Si les joueurs peuvent voir les villageois sur la carte.                                                                                                                                             |
| **Radar pour animaux** | Si les joueurs peuvent voir des animaux sur la carte.                                                                                                                                               |
| **Radar monstre/hostile** | Si les joueurs peuvent voir des monstres ou des entités hostiles sur la carte.                                                                                                                          |
| Masquer les opérations | Masquer les opérations sur le radar lorsque le radar étendu est activé.                                                                                                                                    |
| Masquer les spectateurs | Que ce soit pour cacher les spectateurs sur le radar.                                                                                                                                             |

## **Autres paramètres**

L'option par défaut pour chaque paramètre ci-dessous est marquée d'un texte **gras**.

| Paramètre | Options | Descriptif |
|---------------------------------|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Paramètres multijoueurs | <ul><li>**Tous**</li><li>Op</li><li>Aucun</li></ul> | S'il faut autoriser Tous les joueurs, les joueurs Op ou Aucun joueur à utiliser le menu des paramètres multijoueurs.                                                            |
| Radar général | <ul><li>**Tous**</li><li>Op</li><li>Aucun</li></ul> | <ul><li>All : le radar fonctionne pour tout le monde</li><li>Op : désactive complètement le radar pour tout le monde sauf les utilisateurs OP</li><li>Aucun : le radar est désactivé pour tout le monde.</li></ul> |
| Radar étendu | <ul><li>**Tous**</li><li>Op</li><li>Aucun</li></ul> | Si le radar des joueurs est activé, permet au serveur de suivre les joueurs en dehors de la portée du client. Les joueurs peuvent se voir n'importe où dans la même dimension. |
| Voir les joueurs underground | <ul><li>**Tous**</li><li>Op</li><li>Aucun</li></ul> | Radar étendu uniquement. Si les acteurs underground sont visibles sur le radar. Le Nether n'est pas affecté par ce paramètre.                                     |
| Mise à jour des ticks par joueur | <ul><li>Plage : 1 - 20 **La valeur par défaut est 5**</li></ul> | À quelle fréquence le serveur enverra des mises à jour de localisation des joueurs.                                                                                                  |
| Portée radar latérale | <ul><li>Plage : 16 - 512 **La valeur par défaut est 512**</li></ul> | Distance latérale (en blocs) pour rechercher et afficher des entités sur le radar. Des nombres plus élevés peuvent entraîner un décalage important.                                       |
| Portée radar verticale | <ul><li>Plage : 8 - 320 **La valeur par défaut est 320**</li></ul> | Distance verticale (en blocs) pour rechercher et afficher des entités sur le radar. Des nombres plus élevés peuvent entraîner un décalage important.                                      |
| Nombre maximum de joueurs | <ul><li>Plage : 1 - 128 **La valeur par défaut est 128**</li></ul> | Le nombre maximum de joueurs affichés sur Radar. Des nombres plus élevés peuvent entraîner un décalage.                                                                          |
| Villageois maximum | <ul><li>Plage : 1 - 128 **La valeur par défaut est 128**</li></ul> | Le nombre maximum de villageois affichés sur le radar. Des nombres plus élevés peuvent entraîner un décalage.                                                                        || Animaux maximum | <ul><li>Plage : 1 - 128 **La valeur par défaut est 128**</li></ul> | Le nombre maximum de monstres passifs affichés sur le radar. Des nombres plus élevés peuvent entraîner un décalage.                                                                     |
| Créatures ambiantes maximales | <ul><li>Plage : 1 - 128 **La valeur par défaut est 128**</li></ul> | Le nombre maximum de monstres ambiants affichés sur le radar. Des nombres plus élevés peuvent entraîner un décalage.                                                                     |
| Nombre maximum de foules | <ul><li>Plage : 1 - 128 **La valeur par défaut est 128**</li></ul> | Le nombre maximum de monstres hostiles affichés sur le radar. Des nombres plus élevés peuvent entraîner un décalage.                                                                     |
| Cartographie des surfaces | <ul><li>**Tous**</li><li>Op</li><li>Aucun</li></ul> | Cartographie de surface pour tous, opérations, aucun.                                                                                                                      |
| Cartographie topographique | <ul><li>**Tous**</li><li>Op</li><li>Aucun</li></ul> | Cartographie topographique pour tous, opérations, aucun.                                                                                                                   |
| Cartographie du biome | <ul><li>**Tous**</li><li>Op</li><li>Aucun</li></ul> | Cartographie du biome pour tous, opérations, aucun.                                                                                                                        |
| Cartographie des grottes | <ul><li>**Tous**</li><li>Op</li><li>Aucun</li></ul> | Cartographie des grottes pour tous, opérations, aucun.                                                                                                                         |
| Forcer la plage de rendu de surface de la carte Max | <ul><li>Plage : 0 - 32 **La valeur par défaut est 0**</li></ul> | Forcer tous les joueurs à respecter une distance maximale de rendu de surface pour la carte. 0 pour utiliser les paramètres client. Ce paramètre force uniquement le maximum, il n'augmente pas la plage de rendu. |
| Force Map Cave Render Range Max | <ul><li>Plage : 0 - 32 **La valeur par défaut est 0**</li></ul> | Forcez tous les joueurs à respecter une distance maximale de rendu de la grotte pour la carte. 0 pour utiliser les paramètres client. Ce paramètre force uniquement le maximum, il n'augmente pas la plage de rendu. |
