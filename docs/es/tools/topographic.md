## **Terminología**

!!! warning "Translation needed for 6.0"

    This page was updated for JourneyMap 6.0. Some sections shown are
    the English source pending translation. See Contributing to help
    translate the docs.

- **Mapa Topográfico**: Representación gráfica de la posición, escala, forma, relieve y distribución de características naturales y culturales seleccionadas de un área de la superficie de la Tierra.
- **Línea de Contorno**: Línea dibujada en un mapa topográfico que conecta dos puntos de igual elevación sobre el nivel del mar.
- **Intervalo de Contorno**: La distancia vertical entre dos líneas de contorno adyacentes.

[Fuente](https://quizlet.com/16183184/topographic-maps-terms-flash-cards)

## **Descripción General de los Mapas Topográficos en JourneyMap**

JourneyMap's Topographic Maps let you see the elevation contours of your world.  You can customize the topographic map properties and colors in (`.minecraft/journeymap/config/6.0/journeymap.topo.config`) according to what looks best to you, or what you want to emphasize.

Here's how it works:

**{World height} / {Number of colors} = {Contour interval}**

So, given a **world height of 384** blocks, a palette of **32 colors** will create 32 elevation contours, each with a **contour interval of 12** blocks high.

- 1st color: the lowest 12 blocks
- 2nd color: the next 12 blocks
- etc.

!!! note "Custom Max Topo Height"

    By default the topographic map uses the world's full build height
    for the contour math. The [Cartography settings](../client/settings/cartography.md)
    have a **Custom Max Topo Height** option that lets you cap the
    height used, which is useful for emphasizing contours in a height
    range you care about. Any blocks above the cap are drawn in the
    top color.

## **Personalización**

The topographic maps config file `.minecraft/journeymap/config/6.0/journeymap.topo.config` can be edited with a simple text editor.  You can make changes to it, save it, and see the results immediately in JourneyMap without a need to restart.

El archivo tiene las siguientes propiedades:

- **showContour**: si se muestra una línea de contorno entre intervalos de contorno. El valor predeterminado es verdadero.
- **landContour**: Color hexadecimal (#rrggbb) de las curvas de nivel en tierra. Se ignora si showContour es falso.
- **waterContour**: Color hexadecimal (#rrggbb) de las líneas de contorno en el agua. Se ignora si showContour es falso.
- **land**: lista de colores hexadecimales delimitados por comas (#rrggbb) para terreno terrestre. El número de colores determina los intervalos del contorno (ver descripción general arriba).
- **water**: lista entrecomillada y delimitada por comas de colores hexadecimales (#rrggbb) para el agua. El número de colores determina los intervalos del contorno (ver descripción general arriba).
- **configVersion**: utilizado por JourneyMap para realizar un seguimiento de los cambios de configuración. Puede ignorar esto y no es necesario cambiarlo.

Si el archivo se rompe irremediablemente, no entre en pánico. Simplemente elimínelo y reinicie Minecraft, y se creará uno nuevo para usted.

## **Elegir Buenos Colores**

En verdad, no es probable encontrar un conjunto de colores "único para todos" para mapas topográficos. La mayoría de los mapas de la vida real tienen gradientes no lineales personalizados para funcionar mejor con las características únicas del terreno de un área específica. Por ejemplo, los colores que ayudan a ver claramente los cambios de elevación en un lugar como Kansas, EE. UU. (muy plano) no funcionarían bien en el estado vecino de Colorado y sus Montañas Rocosas.

Para ver algunos ejemplos de gradientes topográficos utilizados en el mundo real, consulte [este sitio](http://soliton.vm.bytemark.co.uk/pub/cpt-city/index.html), especialmente [esta página](https://soliton.vm.bytemark.co.uk/pub/cpt-city/views/topo.html).

Para su comodidad, [la herramienta Editor de color](https://jsfiddle.net/techbrew/4vm9as0o/embedded/result/) y la [herramienta Generador de degradado](https://jsfiddle.net/techbrew/umh423j0/embedded/resultado/) puede resultar útil a la hora de elegir colores para sus mapas topográficos.