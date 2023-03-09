## **Custom Mob Icon Sets**

JourneyMap only comes with mob icons for Vanilla Minecraft mobs. (There's no magic way to derive icons from mobs added by mods.)   However, as of JourneyMap 5.3, mod authors and resource pack authors can provide their own mob icons for JourneyMap to use.  See [Instructions for Mod Authors](https://teamjm.github.io/journeymap-docs/Tools%20and%20Customisation/custom-mob-icons/#instructions-for-mod-authors) and [Instructions for Resource Pack Authors](https://teamjm.github.io/journeymap-docs/Tools%20and%20Customisation/custom-mob-icons/#instructions-for-resource-pack-authors) below.

## **Mob Icon Sources (Legacy)**

!!! note "Note"
    This section is for JourneyMap 5.2 and older.  It is no longer relevant for JourneyMap 5.3+.

Whenever JourneyMap encounters a mob without a known icon, it creates a blank placeholder file that you can replace with your own icon.  Look for them here <code>.minecraft/journeymap/icon/entity/(set name)/ ...</code>

If you view the folder tree with thumbnails displayed, it should be easy to spot the blank placeholder files. Simply find and replace them with your own mob icon. It must be a PNG file and should have the same dimensions as the one you are replacing (usually 32x32 pixels).

Or, you can create your own custom mob icon set in it's own folder:

- Look in <code>.minecraft/journeymap/icon/entity/</code> for existing icon set folders, like "2D", "3D", or "Default" (JourneyMap 5.3+)
- Copy that folder and give it a new name, placing it in the same directory as above.
- Within the copied folder, you can optionally edit the <code>[[#sources.json|sources.json]]</code> file to define how new icon sources (mods and resource packs) will be handled.
- Within the copied folder, replace existing PNG images with a newer version your own. Do not change the filename. It is highly recommended that you keep the image sizes the same (32x32 pixels).
- Restart Minecraft and go into (J > Options Manager > Fullscreen Map) or (J > Options Manager > MiniMap Preset). You will now be able to select your new mob icon set for these displays.

## **Mob Icon Sources**

JourneyMap 5.3+ no longer uses folders of icons.  Instead, it uses mob icons via standard resource location, just like any other texture in Minecraft.  This is so **mods can provide their own mob icons</b> and <b>resource packs can provide or override mob icons** like everything else in the game.

JourneyMap 5.3+ uses the mob's entity texture resource location and substitutes "/entity/" with "/entity_icon/" to look up the mob icon.  Thus:

* Mob entity texture: <code>minecraft:textures/entity/pig/pig.png</code>
* Mob icon texture: <code>minecraft:textures/entity_icon/pig/pig.png</code>

(or)

* Mob entity texture: <code>enderzoo:textures/entity/wither_cat.png</code>
* Mob icon texture: <code>enderzoo:textures/entity_icon/wither_cat.png</code>

*Note: If you are a player and you want to provide your own icons similiar to older versions of JourneyMap, you'll need to put together a [http://minecraft.gamepedia.com/Tutorials/Creating_a_resource_pack simple resource pack] in a zip file. See the Instructions for Resource Pack Authors below.*

## **Instructions for Mod Authors**

You can now provide icons to JourneyMap for your mod's mobs. Here's how:

- JourneyMap 5.3+ will look in your mod jar for icons in <code>/assets/modname/textures/entity_icons</code> .  
- Icons should be transparent PNG files. Other sizes are usually supported, but 16x16 pixels is recommended.
- The folder structure and filenames for your icons must mirror the folder structure and filename for your mob textures in <code>/assets/modname/textures/entity</code>.

For example:
```
  coolmod-1.0.jar
   └───assets
       └───coolmod
           └───textures
               └───entity
               │   │   owlbear.png
               │   └───kobold
               │       │   kobold_green.png
               │       │   kobold_blue.png
               └───entity_icons
                   │   owlbear.png
                   └───kobold
                       │   kobold_green.png
                       │   kobold_blue.png
```

Why is the above necessary?  JourneyMap uses the ResourceLocation returned by <code>net.minecraft.client.renderer.entity.Render.getEntityTexture()</code> as the unique way to identify a mob for any mod.  Providing icons with a similar same path and name keeps things as simple as possible.

## **Instructions for Resource Pack Authors**

You can use a resource pack to provide icons to JourneyMap 5.3+ for any Minecraft mobs or mod mobs. Here's how:

- JourneyMap will look in your resource pack zip for icons in <code>/assets/<modname>/textures/entity_icon</code> .  
- Icons should be transparent PNG files. Other sizes are usually supported, but 16x16 pixels is recommended.
- The folder structure and filenames for your icons must mirror the folder structure and filename for mob textures in minecraft or other mods in <code>/assets/<modname>/textures/entity</code>.

For example, if you want to provide custom icons for both Minecraft mobs and a mod called "coolmod", the mob textures for both would along these lines:
```
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
```
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
