# **Commande de point de cheminement**

Lorsque JourneyMap est installé sur le serveur, les administrateurs du serveur peuvent créer et
supprimez les waypoints sur les clients des joueurs du chat.

Toutes les commandes du serveur JourneyMap vivent sous le préfixe `/jm`. Le point de cheminement
La commande est `/jm waypoint`, avec `/jm wp` comme alias plus court.

## **Permissions**

La commande peut être utilisée par :

- Joueurs au niveau d'autorisation 2 (GAMEMASTERS) ou supérieur.
- Joueurs dans la liste des administrateurs du serveur JourneyMap.
- N'importe qui en mode solo.

## **Créer un waypoint**

```text
/jm waypoint create "name" <dimension> <x> <y> <z> <color> <players> [announce]
```

- `"name"` - le nom du waypoint, entre guillemets.
- `<dimension>` - l'identifiant de dimension, par exemple `minecraft:overworld`.
- `<x> <y> <z>` - les coordonnées du waypoint.
- `<color>` - un nom de couleur Minecraft, par exemple `aqua`.
- `<players>` - le ou les joueurs cibles. Accepte un nom de joueur, un
  liste des joueurs, ou `@a` pour tout le monde. Cet argument est nécessaire.
- `[announce]` - en option. `true` informe le joueur qu'un waypoint
  a été créé; la valeur par défaut est `false` (créé silencieusement).

### Examples

```text
/jm waypoint create "Spawn" minecraft:overworld 1 50 12 aqua @a
/jm waypoint create "Home" minecraft:overworld 1 50 12 aqua mysticdrew
/jm waypoint create "Home" minecraft:overworld 1 50 12 aqua mysticdrew true
```

## **Créer un waypoint temporaire**

Ajoutez `temp` avant `create` pour créer un waypoint temporaire, qui n'est pas
enregistré sur le disque :

```text
/jm waypoint temp create "name" <dimension> <x> <y> <z> <color> <players> [announce]
```

## **Supprimer un waypoint**

```text
/jm waypoint delete "name" <players> [announce]
```

- `"name"` - le nom du waypoint à supprimer.
- `<players>` - le ou les joueurs cibles. Requis.
- `[announce]` - en option. `true` informe le joueur ; par défaut
  `false`.

Seuls les waypoints créés par la commande peuvent être supprimés par la commande.

### Examples

```text
/jm waypoint delete "Home" @a
/jm waypoint delete "Home" mysticdrew
/jm waypoint delete "Home" mysticdrew true
```
