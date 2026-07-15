# **Installation de la carte Web**

La carte Web vous permet d'afficher votre carte JourneyMap dans un navigateur Web au lieu de
dans le jeu. C'est utile pour afficher la carte sur un deuxième moniteur, une tablette,
ou tout autre appareil sur votre réseau local.

Depuis JourneyMap 6.0, la carte Web est un module complémentaire distinct. Ce n'est plus
fourni avec JourneyMap lui-même, vous installez donc deux mods : JourneyMap et
le module complémentaire JourneyMap Webmap.

!!! info "Client-side only"

    La carte Web est un module complémentaire côté client. L'ajouter à un serveur dédié
    ne fait rien - il ne sert que les données cartographiques collectées par JourneyMap
    sur votre propre client.

## **Requirements**

- JourneyMap installé (la Webmap est un module complémentaire et ne se chargera pas sans
  il).
- La même version Minecraft et le même chargeur de mod que votre installation JourneyMap.
  La carte Web est conçue pour Fabric, NeoForge et Forge.

## **Downloading**

Téléchargez la carte Web JourneyMap à partir de :

- [CurseForge](https://www.curseforge.com/minecraft/mc-mods/journeymap-web-map)
- [Modrinth](https://modrinth.com/project/YaZ1fUTg)

Choisissez le fichier qui correspond à votre version de Minecraft et à votre chargeur de mod.

## **Steps**

1. Installez JourneyMap comme d'habitude (voir [Client Docs > Installing](../client/installing.md)).
2. Téléchargez le module complémentaire JourneyMap Webmap pour la même version de Minecraft
   et chargeur.
3. Placez le pot Webmap dans le même dossier `mods` que JourneyMap.
4. Lancez le jeu. La carte Web est maintenant disponible ; voir
   [Utilisation de base](basic-usage.md) pour savoir comment l'activer et l'ouvrir.

## **Code source**

La carte Web JourneyMap est open source :

- [TeamJM/journeymap-webmap](https://github.com/TeamJM/journeymap-webmap) -
  le module lui-même.
- [TeamJM/webmap-client](https://github.com/TeamJM/webmap-client) - le
  Frontend JavaScript servi dans le navigateur.
