## **Terminología**

- **Mapa Topográfico**: Representación gráfica de la posición, escala, forma, relieve y distribución de características naturales y culturales seleccionadas de un área de la superficie de la Tierra.
- **Línea de Contorno**: Línea dibujada en un mapa topográfico que conecta dos puntos de igual elevación sobre el nivel del mar.
- **Intervalo de Contorno**: La distancia vertical entre dos líneas de contorno adyacentes.

[Fuente](https://quizlet.com/16183184/topographic-maps-terms-flash-cards)

## **Descripción General de los Mapas Topográficos en JourneyMap**

Los mapas topográficos de JourneyMap le permiten ver los contornos de elevación de su mundo. Puedes personalizar las propiedades y los colores del mapa topográfico en (`.minecraft/journeymap/config/5.2/journeymap.topo.config`) según lo que te parezca mejor o lo que quieras enfatizar.

Así Es Como Funciona:

**{Altura mundial} ÷ {Número de colores} = {Intervalo de contorno}**

Entonces, dada una **altura mundial de 256** bloques, una paleta de **32 colores** creará 32 contornos de elevación, cada uno con un **intervalo de contorno de 8** bloques de altura.

- 1er color: y 0-7
- 2do color: y 8-15
- etc.

## **Personalización**

El archivo de configuración de mapas topográficos `.minecraft/journeymap/config/5.2/journeymap.topo.config` se puede editar con un simple editor de texto. Puede realizar cambios, guardarlo y ver los resultados inmediatamente en JourneyMap sin necesidad de reiniciar.

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