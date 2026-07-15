# **Paramètres de la carte Web**

La carte Web est une manière différente d'afficher votre carte : dans un navigateur Web.
du jeu. Cela vous permet de conserver une vue cartographique sur un deuxième moniteur ou un autre
appareil sur votre réseau.

![Webmap-Paramètres](../../img/settings/client/webmap.png){: .center}

!!! info "Nécessite le module complémentaire Webmap"

    Depuis JourneyMap 6.0, la carte Web est un module complémentaire distinct. Ceci
    La catégorie des paramètres est toujours affichée, mais les paramètres ne prennent effet que
    lorsque le module complémentaire JourneyMap Webmap est installé. Si l'addon n'est pas
    installé, les paramètres sont désactivés.

Voir la section [Webmap](../../webmap/installing.md) pour savoir comment
installez-le et utilisez-le.

## **Toggles**

Cette bascule est **désactivée** par défaut.

| Basculer | Descriptif |
|----------------|------------------------------------------------------|
| Activer la carte Web | Si le serveur de cartes Web est activé et accessible. |

## **Autres paramètres**

| Paramètre | Options | Descriptif |
|--------------|-----------------------------|------------------------------------------------------------|
| Port | Plage : 80 - 65 535 (par défaut : **8080**) | Le port auquel le serveur de cartes Web tente de se lier. |

!!! note "Port selection"

    Si le port configuré est déjà utilisé, la carte Web revient à un
    port libre choisi par le système d'exploitation au lieu de échouer
    démarrer, donc le port réellement utilisé peut différer de celui que vous avez défini. Si
    l'option avancée Announce Mod est activée (par défaut), JourneyMap
    publie l'adresse de la carte Web dans le chat une fois lorsque vous rejoignez un monde. Le
    le port résolu est également écrit dans le journal du jeu.
