
## **Installing**

L'installation de JourneyMap sur le serveur est facultative. Il ajoute une utilité pour
administrateurs de serveur : cela leur permet de restreindre certaines fonctionnalités client par dimension,
gérer les waypoints et prendre en charge les configurations multi-mondes. Clients JourneyMap sur
n'importe quel chargeur peut se connecter à un serveur exécutant JourneyMap, quel que soit le
quel chargeur le serveur utilise.

## **Serveurs Fabric, NeoForge et Forge**

1. Placez le pot JourneyMap dans le dossier `mods` de votre serveur :
   `(server folder)/mods`
2. La première fois que vous démarrez le serveur après avoir installé JourneyMap, un
   le fichier de configuration est généré sous
   `(server folder)/journeymap/server/<version>/`.
3. Les clients connectés sont automatiquement associés au serveur
   identifiant du monde. Chaque client crée un dossier pour stocker ses waypoints et
   Images de la carte : `.minecraft/journeymap/data/mp/(server_worldid)`

## **Paper servers**

!!! info "Minecraft 26.1 et 26.2 uniquement"

    La version papier de JourneyMap est disponible pour Minecraft 26.1 et
    26.2 versions de JourneyMap 6.0. Il n'est pas disponible pour la version 1.21.1 ou
    Versions 1.21.11.

Sur les serveurs Paper, JourneyMap est livré sous forme de plugin plutôt que de mod. Lieu
le pot JourneyMap Paper dans le dossier `plugins` de votre serveur au lieu de
`mods`. La configuration et le comportement par monde sont par ailleurs les mêmes que ceux de
versions du chargeur de mod.

## **Commandes du serveur**

Les commandes du serveur JourneyMap vivent sous le préfixe `/jm`. Le principal
est la commande waypoint, `/jm waypoint` (alias `/jm wp`), documentée sur
la page [Waypoint Command](commands/waypoint_command.md).
