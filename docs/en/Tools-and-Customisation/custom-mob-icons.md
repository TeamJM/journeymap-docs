## **Custom Mob Icon Sets**

JourneyMap only comes with mob icons for Vanilla Minecraft mobs. (There's no magic way to derive icons from mobs added by mods.)   However, as of JourneyMap 5.3, mod authors and resource pack authors can provide their own mob icons for JourneyMap to use.  See [Instructions for Mod Authors](#instructions-for-mod-authors) and [Instructions for Resource Pack Authors](#instructions-for-resource-pack-authors) below.

## **Mob Icon Sources**

JourneyMap 5.3+ no longer uses folders of icons.  Instead, it uses mob icons via standard resource location, just like any other texture in Minecraft.  This is so **mods can provide their own mob icons resource packs can provide or override mob icons** like everything else in the game.

JourneyMap 5.3+ uses the mob's entity texture resource location and substitutes "/entity/" with "/entity_icon/" to look up the mob icon.  Thus:

- Mob entity texture: `minecraft:textures/entity/pig/pig.png`
- Mob icon texture: `minecraft:textures/entity_icon/pig/pig.png`

(or)

- Mob entity texture: `enderzoo:textures/entity/wither_cat.png`
- Mob icon texture: `enderzoo:textures/entity_icon/wither_cat.png`

!!! note "Note"

    If you are a player and you want to provide your own icons similar to older versions of JourneyMap, you'll need to put together a [simple resource pack](http://minecraft.gamepedia.com/Tutorials/Creating_a_resource_pack) in a zip file. See the Instructions for Resource Pack Authors below.

## **Instructions for Mod Authors**

You can now provide icons to JourneyMap for your mod's mobs. Here's how:

- JourneyMap 5.3+ will look in your mod jar for icons in `/assets/modname/textures/entity_icon`.  
- Icons should be transparent PNG files. Other sizes are usually supported, but 16x16 pixels is recommended.
- The folder structure and filenames for your icons must mirror the folder structure and filename for your mob textures in `/assets/modname/textures/entity`.

For example:

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

Why is the above necessary?  JourneyMap uses the ResourceLocation returned by `net.minecraft.client.renderer.entity.Render.getEntityTexture()` as the unique way to identify a mob for any mod.  Providing icons with a similar same path and name keeps things as simple as possible.

## **Instructions for Resource Pack Authors**

You can use a resource pack to provide icons to JourneyMap 5.3+ for any Minecraft mobs or mod mobs. Here's how:

- JourneyMap will look in your resource pack zip for icons in `/assets/<modname>/textures/entity_icon`.  
- Icons should be transparent PNG files. Other sizes are usually supported, but 16x16 pixels is recommended.
- The folder structure and filenames for your icons must mirror the folder structure and filename for mob textures in minecraft or other mods in `/assets/<modname>/textures/entity`.

For example, if you want to provide custom icons for both Minecraft mobs and a mod called "coolmod", the mob textures for both would along these lines:

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

In your resource pack, therefore, you would mirror the above file trees, replacing "entity" with "entity_icon" to store your custom mob icon files:

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
