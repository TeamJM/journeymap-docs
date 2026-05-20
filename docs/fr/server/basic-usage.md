## **Aperçu**

!!! warning "Translation needed for 6.0"

    This page was updated for JourneyMap 6.0. Some sections shown are
    the English source pending translation. See Contributing to help
    translate the docs.

You don't have to have JourneyMap installed on the server to use the JourneyMap client. Installing it on the server gives admins a way to restrict some client features, manage waypoints, and support multi-world and proxy (BungeeCord / Velocity) setups. JourneyMap server runs on Fabric, NeoForge, and Forge servers, and on Paper servers (Minecraft 26.1 line). See [Installing](installing.md) for details.

## **Configuration de l'Administrateur de Serveur**

Pour accéder à l'écran d'administration du serveur, ouvrez l'écran des options de JourneyMap. En tant qu'utilisateur Opped, un bouton `Server Admin` apparaîtra en bas de l'écran.

Toutes les options de l'écran d'administration du serveur ont des info-bulles qui les expliquent en détail.

Si le bouton n'apparaît pas, vous devrez peut-être vous déconnecter et vous reconnecter à votre serveur si vous avez récemment été Opped, ou l'administrateur l'a désactivé dans le fichier de configuration.

Par défaut, tous les utilisateurs Opped ont accès à l'écran d'administration du serveur. Cela peut être modifié via un fichier de configuration sur le serveur.

Emplacement du fichier de configuration pour les serveurs Fabric : `(server_folder)/configs/journeymap_server.cfg`.

The config file location for NeoForge and Forge servers: `(server_folder)/world/serverconfig/journeymap_server.cfg`.

```text
    server {
    # Les joueurs dans cette liste ont accès au panneau d'administration du serveur de JourneyMap
    # Ajoutez des utilisateurs par nom ou UUID, privilégiez l'UUID car c'est plus sécurisé !
    # Chaque valeur sur une nouvelle ligne avec le format d'exemple fourni. (veuillez supprimer les valeurs par défaut)
    S:"Administrateurs du Serveur Journeymap" <
    mysticdrew
    12341234132
    >
    
        # Par défaut, tous les Ops ont accès à l'interface d'administration du serveur dans l'écran des Options.
        # Si défini sur false, seuls les utilisateurs de la liste des administrateurs auront accès.
        # Si défini sur true, tous les ops et les utilisateurs de la liste des administrateurs auront accès.
        B:"Accès Admin Ops"=true
    }
```

## **Ce que ce n'est pas**

* Ce n'est pas un mod de cartographie côté serveur. Aucun carte n'est créée, générée, hébergée, partagée ou même envisagée sur le serveur.
* Ce n'est pas un moyen d'administrer quoi que ce soit d'autre que les fonctionnalités du client JourneyMap.
* Ce n'est ni un jacuzzi ni une machine à remonter le temps.

## **Utilisation de Modpack**

Le mod client JourneyMap est régi par une [politique de modpack différente](../about/licensing.md) de celle du serveur.

Les éléments suivants s'appliquent uniquement au mod du serveur :

Vous pouvez inclure JourneyMapServer dans la configuration côté serveur d'un modpack, à condition d'accepter les conditions suivantes :

1. Votre lanceur doit établir un lien direct vers un téléchargement ici sur le Curse CDN s'il est capable de le faire (ATLauncher, MCUpdater, etc.). Si le lanceur ne peut pas établir de lien directement vers le fichier, le fichier jar du serveur JourneyMap peut être hébergé/emballé uniquement aux fins de votre modpack, mais ne doit pas être distribué d'une autre manière.
2. Vous devez fournir un lien vers cette page pour les administrateurs de serveur qui utilisent votre modpack. La documentation est une bonne chose.

## **Crédits et Plaintes**

JourneyMapServer a été créé par Mysticdrew au nom d'un Techbrew surchargé. Tous les crédits vont à Mysticdrew. Les plaintes doivent être rédigées à l'aide de lettres découpées dans des magazines et des journaux, puis envoyées par courrier postal à votre fonctionnaire gouvernemental local dans une enveloppe contenant de la farine de cuisson. Assurez-vous d'inclure une adresse de retour et une photo récente.