
## **Custom Mob Icons**

JourneyMap affiche une icône pour chaque foule sur la carte et sur le radar de l'entité.

Depuis JourneyMap 6.0, JourneyMap **génère automatiquement une icône** pour
chaque foule, y compris les foules modifiées, à partir du modèle de la foule. Tu n'es plus
besoin de fournir des icônes juste pour que quelque chose apparaisse. Vous pouvez toujours
fournissez vos propres icônes pour remplacer celles générées, et vous n'êtes pas
plus limité à un chemin de texture spécifique au mod pour le faire.

## **Icon path**

Les icônes de foule personnalisées se trouvent sous l'espace de noms `journeymap` à ce chemin :

```text
assets/journeymap/icon/entity/{mod_id}/{mob_name}.png
```

- `{mod_id}` est l'identifiant du mod auquel appartient le mob, ou `minecraft`
  pour une foule vanille.
- `{mob_name}` est le nom de la foule.

Par exemple, une icône de creeper personnalisée va à :

```text
assets/journeymap/icon/entity/minecraft/creeper.png
```

Ce chemin est le même que vous soyez un auteur de mod regroupant des icônes dans
votre pot de mod ou un auteur de pack de ressources les expédiant dans un pack de ressources.

## **Image size**

La taille d'icône recommandée est de 16 x 16. Les icônes peuvent être de n'importe quelle taille, mais elles
doivent s'insérer à l'intérieur du cercle du marqueur pour s'afficher correctement. Si vous utilisez
une image plus grande, mettez des pixels transparents dans les coins pour qu'ils ne
dépassez le cercle.

## **Outlined icons**

JourneyMap a une option d'affichage d'icône « décrite ». Les packs de ressources peuvent
fournir une variante décrite d'une icône en ajoutant un deuxième fichier avec un
Suffixe `_outline.png`, par exemple :

```text
assets/journeymap/icon/entity/minecraft/creeper.png
assets/journeymap/icon/entity/minecraft/creeper_outline.png
```

La variante décrite est facultative. Si l'option d'affichage décrite est
activé et qu'aucune variante `_outline.png` n'existe, JourneyMap utilise le
icône régulière à la place. Ainsi, si un pack de ressources remplace `creeper.png` mais
pas `creeper_outline.png`, l'option décrite utilisera le remplacement
`creeper.png`.

## **Ajout d'icônes sans pack de ressources**

Vous pouvez également déposer des icônes directement dans le dossier d'icônes de JourneyMap, sans
créer un pack de ressources :

```text
{minecraft}/journeymap/icon/entity/{mod_id}/{mob_name}.png
```

Les icônes ajoutées de cette manière nécessitent un redémarrage du client pour être récupérées.

Les icônes générées automatiquement par JourneyMap sont stockées sous
`{minecraft}/journeymap/icon/entity/`. Vous pouvez parcourir ce dossier pour voir
les noms de foule utilisés par JourneyMap et pour utiliser les icônes générées comme
point de départ pour le vôtre.
