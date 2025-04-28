# **Changelogs**

Cette page présente tous les journaux de modifications de JourneyMap de la version 5.9.0 à la 5.9.24, qui est la dernière version de JourneyMap jusqu'à présent.

## **JourneyMap 5.9.24**

- Correction : un bug involontaire empêchait la mise à jour de la carte avec la version axée sur les performances, affectant certaines, mais pas toutes les versions publiées.

## **JourneyMap 5.9.23**

- Correction : amélioration supplémentaire de la mise à jour des performances.
- Correction : les numéros de version contenant "p1" provoquaient des erreurs pour les mods Fabric dépendant de JourneyMap.

## **JourneyMap 5.9.22**

- Correction : la rotation de la minimap provoquait la rotation du HUD à l'écran, cette correction résout également d'autres problèmes étranges avec la minimap.
- Correction : ajout d'un délai de 3 secondes pour la création du point de mort.

## **JourneyMap 5.9.21**

- Correction : [ModCompat] Raccourcis de touches pour ViveCraft.
- Correction : bug dans la logique de rendu de la minimap.
- Correction : suppression de certaines allocations de classes inutiles ayant un impact important sur les performances.

## **JourneyMap 5.9.20**

- Corrigé : Défilement du Gestionnaire de points de repère et de l'Écran des Options. (une autre correction)

## **JourneyMap 5.9.19**

- Corrigé : Écran de Position de la Minicarte.
- Corrigé : Défilement et position de l'Écran des Options.

## **JourneyMap 5.9.18**

- Corrigé : Écran de Position de la Minicarte.
- Corrigé : Défilement et position de l'Écran des Options.

## **JourneyMap 5.9.17**

- Corrigé : Quelques problèmes d'interaction avec des mods.
- Support pour 1.20.3 et 1.20.4

## **JourneyMap 5.9.16**

- Corrigé : [Fabric] Superposition des écrans brisant l'événement de fermeture de fabric.
- Corrigé : Envoi de paquets alors que le client n'est pas prêt.

## **JourneyMap 5.9.15**

- Corrigé : Problèmes de carte en plein écran sur les écrans Mac Retina.
- Corrigé : Déconnexion du serveur lorsque le paquet est envoyé trop tôt.
- Corrigé : La désactivation du cycle Jour/Nuit empêche les mises à jour du radar.

## **JourneyMap 5.9.14**

- Corrigé : Problème de compatibilité avec le bot de chat Discord.
- Corrigé : Échec rare de texture de la minicarte.
- Corrigé : L'infobulle de l'emplacement d'information ne se traduit pas.
- Support pour NeoForge et 1.20.2

## **JourneyMap 5.9.13**

- Corrigé : [Fabric] Icônes de points de repère ne s'affichant pas à travers certains objets.
- Corrigé : Problèmes de migration de vieux points de repère.
- Corrigé : AutoMap se brisant si un fichier de région mal formé est trouvé.
- Corrigé : Chevaux apprivoisés ne se colorant pas correctement sur la carte.
- Corrigé : Transparence des blocs et des panneaux en verre teinté.
- Langues : Ajout de l'italien et du taiwanais et mise à jour des fichiers de langue coréenne.

## **JourneyMap 5.9.12**

- Corrigé : Commande de point de repère depuis la console.
- Corrigé : Bloc 0,0,0 empêchant l'ouverture de la carte.
- Corrigé : Plein écran ne suivant pas correctement lors du repère de la grotte au monde extérieur.
- Corrigé : Certaines propriétés globales du serveur ne fonctionnant pas dans les dimensions.

## **JourneyMap 5.9.11**

- Corrigé : [Fabric] Problèmes d'affichage étranges lorsque les points de repère sont affichés.
- Corrigé : Les raccourcis de la souris fonctionnent pour les actions en jeu.

## **JourneyMap 5.9.10**

- Corrigé : Problème de compatibilité avec Oculus concernant les icônes de points de repère.

## **JourneyMap 5.9.9**

- Corrigé : Mouvement des polygones en mode suivi.
- Corrigé : Écran des Options devenant bizarre sur l'aperçu de la minicarte.
- Corrigé : L'option Multiworld ne fonctionnant pas correctement dans certains cas.
- Corrigé : Création d'un point de repère depuis le contexte en plein écran ignorant la première touche.

## **JourneyMap 5.9.8**

- Corrigé : [Fabric] Problème avec le clic droit dans la fenêtre de recette.
- Corrigé : Les champs de texte sont à nouveau sélectionnables avec la souris.
- Corrigé : [Forge] Distance du point de repère ne se mettant pas à jour au-delà de 128m.

## **JourneyMap 5.9.7**

- Corrigé : [Quilt] Corrections de la webmap pour le chargeur Quilt 0.18+.
- Corrigé : Décalages de texte des marqueurs API.
- Corrigé : Problème de délai d'attente de la peau du joueur fictif.
- Corrigé : Coloration de l'eau par défaut si les mods la modifient.
- Mis à jour pour la version 1.20

## **JourneyMap 5.9.6**

- Corrigé : [Fabric] Discussion de points de repère déconnectant du serveur.
- Corrigé : Problème potentiel avec les joueurs fictifs cassant l'obtention des têtes de joueurs.

## **JourneyMap 5.9.5**

- Ajouté : Support pour les icônes du pack de ressources Cobblemon. Utiliser entity_icon au lieu de pokemon dans le chemin.
- Mis à jour : Nettoyage des jsons de langues.
- Corrigé : Curseurs de distance de rendu de la grotte et de la surface.

## **JourneyMap 5.9.4**

- Mis à jour : Les noms de dimensions de plus de 25 caractères sont compressés.
- Compatibilité de mod : Les feuilles de ChinjufuMod ne se rendent pas correctement.
- Corrigé : MapSaver rendant des images blanches étranges.
- Corrigé : Pentes à 0 et en dessous.

## **JourneyMap 5.9.3**

- Corrigé : Exception de texture de villageois de mod.
- Corrigé : Plage de rendu du client plus grande que celle du serveur provoquant un rendu noir des blocs.
- Compatibilité de mod : [Fabric] VulkanMod

## **JourneyMap 5.9.2**

- Compatibilité de mod : Les rails courbés du mod Create ne se rendent pas et couleur du boîtier ferroviaire.
- Corrigé : Crash lorsque l'api supprime des non-polygones.
- Corrigé : Crash rare possible lors de l'échec de la création d'un nouveau UIState.
- Corrigé : Rendu du bloc de lit.

## **JourneyMap 5.9.1**

- Corrigé : Les options n'affichant pas les infobulles.
- Corrigé : Les troncs affichant ce qui est sous eux dans les grottes.
- Corrigé : Plus d'arbres et de plantes ajoutés à l'ignorance topo.
- Corrigé : Mauvaises régions cassant la cartographie des grottes.

## **JourneyMap 5.9.0**

- Mis à jour : [Fabric] Extraction de fichiers pour supporter le nouveau protocole de fichier "quilt.mfs" pour le chargeur quilt 0.18.1.
- Mis à jour : [Fabric] Version du chargeur de fabric réduite à 0.14.10 puisque 0.14.11 empêchait les utilisateurs de Quilt d'utiliser JM.
- Mis à jour : La webmap extrait maintenant le contenu web du jar et le place dans le dossier journeymap.
- Corrigé : Cache de blocs corrompu causant des échecs de cartographie.
- Corrigé : EntityIcons définis via EntityRadarUpdateEvent ne s'affichant pas dans la webmap.
- Corrigé : Ombres d'arbres apparaissant sur la carte topo.
- Corrigé : Problèmes d'éclairage d'automap.
- Corrigé : Noms d'entités ne s'affichant pas sur la minicarte lorsque la direction est changée.
- Corrigé : NPE possible dans le gestionnaire de points de repère.
- Corrigé : Espérons avoir corrigé les problèmes de compatibilité pour les versions ultérieures de Immersive Portals.
- Corrigé : [1.19.x] : Icônes de grenouilles
- Corrigé : Certains loggers logOnce ayant un throwable quand ils ne devraient pas.
- Corrigé : Limites de défilement des écrans d'options.

## **JourneyMap 5.9.0 Beta 5**

- Corrigé : Écrans UI échouant en raison d'erreurs de méthode abstraite.
- Corrigé : Textures aléatoires apparaissant sur des tuiles vides ou blanches.

## **JourneyMap 5.9.0 Beta 4**

- Ajouté : Icônes d'entités manquantes pour la version [1.19.3]. (Sandriell)
- Corrigé : La clé de masquage des points de repère ne sauvegardant pas le champ "activé" du point de repère.
- Corrigé : Fuite de mémoire lors de l'utilisation des mécaniques vanille pour désérialiser les blocs pour l'automapping.
- Corrigé : Compatibilité de mod avec BBOR
- Corrigé : Couleurs des fleurs de mod
- Corrigé : Le texte des polygones ne s'affiche plus en dehors de la minicarte.
- Corrigé : Création de point de mort lorsqu'une règle de réapparition immédiate est définie.

## **JourneyMap 5.9.0 Beta 3**

- Ajouté : Cavernes non éclairées claires, les blocs non éclairés et de tranche intérieure sont rendus transparents au lieu de noirs. Par défaut : Faux
- Mis à jour : Gestion des icônes pour les mods utilisant un chemin comme Twilight Forest.
- Mis à jour : Langues
- Mis à jour : Nettoyage du rendu.
- Corrigé : Curseur de couche de grotte en plein écran pour les mondes ayant des hauteurs logiques plus grandes que vanilla.
- Corrigé : Compatibilité de mod avec REI. [Forge]
- Corrigé : Pentes en dessous de y0.
- Corrigé : Commandes de téléportation de points de repère personnalisés sans slash. [1.19.1/2]
- Corrigé : Exception de cast de classe possible avec des groupes de points de repère via l'api.

## **JourneyMap 5.9.0 Beta 2**

- Mis à jour : [Fabric] Sorties CurseForge Fabric pour inclure l'étiquette Quilt.
- Corrigé : [Fabric] Erreur d'URL de téléchargement
- Corrigé : Mobs inconnus causant des problèmes de rendu d'écran.
- Corrigé : Problèmes de performance de la minicarte lorsque les addons dessinent de nombreux polygones sur la carte
- Corrigé : [Fabric] Envoi de paquets si Journeymap n'est pas du côté distant.
- Corrigé : Forge 1.19.x Empêche l'envoi de paquets par le serveur et le client si le mod n'est pas de l'autre côté. (Nécessite la version minimum de Forge 1.19.1-42.0.8)
- Corrigé : Forge 1.18.2 Empêche l'envoi de paquets par le serveur et le client si le mod n'est pas de l'autre côté. (Nécessite la version minimum de Forge 1.18.2-40.1.70)

## **JourneyMap 5.9.0 Beta 1**

- Utilise la version 1.9 de journeymap-api.
NOUVEAU : Moteur de texture, n'utilisant plus d'images en mémoire tampon.
- Ajouté : Icône de panda jouant manquante.
- Modifié : La commande de point de repère prend un joueur, une liste de joueurs, ou @a pour tous les joueurs. Il est désormais nécessaire de fournir des joueurs, l'annonce reste facultative.
- Mis à jour : VersionCheck pour utiliser java-http-client.
- Corrigé : Ligne de grille de région verticale ne s'affichant pas.
- Corrigé : Spam de log si le biome est nul dans les grottes.
- Corrigé : Compatibilité de mod : Amecs
- Corrigé : Plusieurs affichages et suppressions par l'API ne montrant pas les superpositions.
- Corrigé : Arrêt étrange de l'automap.
- Corrigé : Textures lorsque le balise de shader est activé mais les balises sont désactivés.
- Corrigé : Changement des options avancées causant la rupture du thème puriste.
- Corrigé : Fabric : Événement de mise à jour de l'affichage pour l'utilisation de l'API.
- Corrigé : Fabric : Redimensionnement lorsque les couches sont affichées.
