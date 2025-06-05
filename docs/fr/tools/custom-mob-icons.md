## **Ensembles d'icônes de mobs personnalisés**

JourneyMap ne fournit des icônes de mobs que pour les mobs de Vanilla Minecraft. (Il n'y a pas de moyen magique pour dériver des icônes des mobs ajoutés par des mods.) Cependant, à partir de JourneyMap 5.3, les auteurs de mods et de packs de ressources peuvent fournir leurs propres icônes de mobs pour que JourneyMap les utilise. Consultez les [Instructions pour les auteurs de mods](#instructions-for-mod-authors) et les [Instructions pour les auteurs de packs de ressources](#instructions-for-resource-pack-authors) ci-dessous.

## **Sources des icônes de mobs**

JourneyMap 5.3+ n'utilise plus de dossiers d'icônes. Désormais, il utilise les icônes de mobs via un emplacement de ressource standard, comme toute autre texture dans Minecraft. Ainsi, **les mods peuvent fournir leurs propres icônes de mobs et les packs de ressources peuvent fournir ou remplacer les icônes de mobs** comme tout autre élément du jeu.

JourneyMap 5.3+ utilise l'emplacement de la texture de l'entité du mob et remplace "/entity/" par "/entity_icon/" pour rechercher l'icône du mob. Ainsi :

- Texture de l'entité du mob : `minecraft:textures/entity/pig/pig.png`
- Texture de l'icône du mob : `minecraft:textures/entity_icon/pig/pig.png`

(ou)

- Texture de l'entité du mob : `enderzoo:textures/entity/wither_cat.png`
- Texture de l'icône du mob : `enderzoo:textures/entity_icon/wither_cat.png`

!!! note "Remarque"

    Si vous êtes un joueur et que vous souhaitez fournir vos propres icônes comme dans les anciennes versions de JourneyMap, vous devrez créer un [pack de ressources simple](http://minecraft.gamepedia.com/Tutorials/Creating_a_resource_pack) dans un fichier zip. Consultez les Instructions pour les auteurs de packs de ressources ci-dessous.

## **Instructions pour les auteurs de mods**

Vous pouvez désormais fournir des icônes à JourneyMap pour les mobs de votre mod. Voici comment :

- JourneyMap 5.3+ cherchera les icônes dans le fichier jar de votre mod dans `/assets/modname/textures/entity_icon`.  
- Les icônes doivent être des fichiers PNG transparents. D'autres tailles sont généralement prises en charge, mais 16x16 pixels est recommandé.
- La structure des dossiers et les noms de fichiers de vos icônes doivent refléter la structure des dossiers et les noms de fichiers de vos textures de mobs dans `/assets/modname/textures/entity`.

Par exemple :

```text
  coolmod-1.0.jar
   └───assets
       └───coolmod
           └───textures
               └───entity
               │   │   owlbear.png
               │   └───kobold
               │       │   kobold_green.png
               │       │   kobold_blue.png
               └───entity_icon
                   │   owlbear.png
                   └───kobold
                       │   kobold_green.png
                       │   kobold_blue.png
```

Pourquoi est-ce nécessaire ? JourneyMap utilise la ResourceLocation renvoyée par `net.minecraft.client.renderer.entity.Render.getEntityTexture()` comme moyen unique d'identifier un mob pour tout mod. Fournir des icônes avec une structure de chemin et de nom similaire simplifie au maximum le processus.

## **Instructions pour les auteurs de packs de ressources**

Vous pouvez utiliser un pack de ressources pour fournir des icônes à JourneyMap 5.3+ pour n'importe quel mob de Minecraft ou de mod. Voici comment :

- JourneyMap cherchera les icônes dans votre fichier zip de pack de ressources dans `/assets/<modname>/textures/entity_icon`.  
- Les icônes doivent être des fichiers PNG transparents. D'autres tailles sont généralement prises en charge, mais 16x16 pixels est recommandé.
- La structure des dossiers et les noms de fichiers de vos icônes doivent refléter la structure des dossiers et les noms de fichiers des textures de mobs dans Minecraft ou d'autres mods dans `/assets/<modname>/textures/entity`.

Par exemple, si vous souhaitez fournir des icônes personnalisées pour les mobs de Minecraft et un mod appelé "coolmod", les textures des mobs pour les deux ressembleraient à ceci :

```text
 minecraft.jar                         coolmod-1.0.jar
   └───assets                               └───assets
       └───minecraft                            └───coolmod
           └───textures                             └───textures
               └───entity                               └───entity
                   │   bat.png                              │   owlbear.png
                   │   chicken.png                          └───kobold
                   └───zombie                                   |   kobold_green.png
                       |   zombie.png                           |   kobold_blue.png
```

Dans votre pack de ressources, vous devrez donc refléter les arbres de fichiers ci-dessus, en remplaçant "entity" par "entity_icon" pour stocker vos fichiers d'icônes de mobs personnalisés :

```text
 awesomepack.zip                    
   └───assets                              
       ├───minecraft                       
       │   └───textures                    
       │       └───entity_icon      
       │           │   bat.png             
       │           │   chicken.png         
       │           └───zombie              
       │               |   zombie.png      
       └───coolmod                         
           └───textures                    
               └───entity_icon      
                   │   owlbear.png         
                   └───kobold              
                       |   kobold_green.png
                       |   kobold_blue.png
```