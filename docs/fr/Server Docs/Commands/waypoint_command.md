# **Commandes de Point de Repère**

Les commandes permettent de créer et de supprimer des points de repère à partir du chat.

Remarque : <u>Cette fonctionnalité ne sera pas portée sur les anciennes versions</u>

- Commande : waypoint
- Alias : wp

## **Créer un Point de Repère**

```text
Les champs entre [] sont optionnels -> 
[player] est le joueur ciblé, si aucun joueur n'est spécifié, une erreur sera affichée.
[announce] indique si le joueur a une notification qu'un point de repère est en cours de création, si ce n'est pas spécifié, la valeur par défaut est false, il est créé silencieusement.
- /waypoint create "nom" dimension x y z couleur [joueur] [annoncer]
- /waypoint delete "nom" [joueur] [annoncer]
```

### **Exemples**

```text
-   /waypoint create "Spawn" minecraft:overworld 1 50 12 aqua
-   /waypoint create "Maison" minecraft:overworld 1 50 12 aqua mysticdrew
-   /waypoint create "Maison" minecraft:overworld 1 50 12 aqua true~~  actuellement bugué dans v5.8.x
-   /waypoint create "Maison" minecraft:overworld 1 50 12 aqua mysticdrew true
```

## **Supprimer un Point de Repère**

Remarque : <u>Supprime uniquement les points de repère créés par commande</u>

```text
/waypoint delete "NomDuPoint"
/waypoint delete "NomDuPoint" true
/waypoint delete "NomDuPoint" mysticdrew
/waypoint delete "NomDuPoint" mysticdrew true
```

## **À partir de JourneyMap 5.9.0**

Toutes les commandes de point de repère nécessitent l'utilisation du champ joueur. Il prend un joueur, une liste de joueurs ou `@a` pour les deux lors de la création et de la suppression.