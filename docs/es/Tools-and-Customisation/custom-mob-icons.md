## **Conjuntos de Iconos de Mob Personalizados**

JourneyMap solo viene con íconos de mobs para Minecraft Vanilla. (No existe una forma mágica de derivar íconos de mobs agregados por mods). Sin embargo, a partir de JourneyMap 5.3, los autores de mods y paquetes de recursos pueden proporcionar sus propios íconos de mobs para que los use JourneyMap. Consulte las [Instrucciones para autores de mods](#instrucciones-para-autores-de-mods) e [Instrucciones para autores de paquetes de recursos](#instrucciones-para-autores-de-paquetes-de-recursos) a continuación.

## **Fuentes de Iconos de los Mobs**

JourneyMap 5.3+ ya no utiliza carpetas de iconos. En cambio, utiliza íconos de mobs a través de la ubicación de recursos estándar, como cualquier otra textura en Minecraft. Esto es para que **los mods puedan proporcionar sus propios íconos de los mobs; los paquetes de recursos pueden proporcionar o anular los íconos de los mobs** como todo lo demás en el juego.

JourneyMap 5.3+ utiliza la ubicación del recurso de textura de entidad de los mobs y sustituye "/entity/" por "/entity_icon/" para buscar el ícono de los mobs. De este modo:

- Textura de entidad Mob: `minecraft:textures/entity/pig/pig.png`
- Textura del icono de los mobs: `minecraft:textures/entity_icon/pig/pig.png`

    o

- Textura de entidad Mob: `enderzoo:textures/entity/wither_cat.png`
- Textura del icono de los mobs: `enderzoo:textures/entity_icon/wither_cat.png`

!!! nota "Nota"

 Si eres un jugador y quieres proporcionar tus propios íconos similares a las versiones anteriores de JourneyMap, necesitarás crear un [paquete de recursos simple](http://minecraft.gamepedia.com/Tutorials/Creating_a_resource_pack) en un archivo zip. Consulte las instrucciones para los autores del paquete de recursos a continuación.

## **Instrucciones para Autores de Mods**

Ahora puedes proporcionar íconos a JourneyMap para los mobs de tu mod. He aquí cómo:

- JourneyMap 5.3+ buscará en su archivo mod íconos en `/assets/modname/textures/entity_icon`.
- Los iconos deben ser archivos PNG transparentes. Generalmente se admiten otros tamaños, pero se recomiendan 16x16 píxeles.
- La estructura de carpetas y los nombres de archivos de tus íconos deben reflejar la estructura de carpetas y el nombre de archivo de tus texturas de mob en `/assets/modname/textures/entity`.

Por ejemplo:

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

¿Por qué es necesario lo anterior? JourneyMap utiliza ResourceLocation devuelto por `net.minecraft.client.renderer.entity.Render.getEntityTexture()` como forma única de identificar un mob para cualquier mod. Proporcionar íconos con una misma ruta y nombre similar mantiene las cosas lo más simples posible.

## **Instrucciones para Autores de Paquetes de Recursos**

Puedes usar un paquete de recursos para proporcionar íconos a JourneyMap 5.3+ para cualquier mobs de Minecraft o mobs mod. He aquí cómo:

- JourneyMap buscará en el zip de su paquete de recursos íconos en `/assets/<modname>/textures/entity_icon`.
- Los iconos deben ser archivos PNG transparentes. Generalmente se admiten otros tamaños, pero se recomiendan 16x16 píxeles.
- La estructura de carpetas y los nombres de archivos de tus íconos deben reflejar la estructura de carpetas y el nombre de archivo de las texturas de mob en Minecraft u otras modificaciones en `/assets/<modname>/textures/entity`.

Por ejemplo, si desea proporcionar íconos personalizados tanto para los mobs de Minecraft como para un mod llamado "coolmod", las texturas de los mobs para ambos serían las siguientes:

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

Por lo tanto, en su paquete de recursos, debería reflejar los árboles de archivos anteriores, reemplazando "entidad" con "entity_icon" para almacenar sus archivos de iconos de mob personalizados:

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
