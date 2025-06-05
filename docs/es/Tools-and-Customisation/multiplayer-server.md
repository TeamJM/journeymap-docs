## **Descripción General**

A partir de JourneyMap 5.1.3, no existe ningún mecanismo del lado del servidor para generar un mapa de un servidor multijugador. Sin embargo, si es propietario de un servidor (o puede obtener acceso a una copia de la carpeta de datos mundiales del servidor), existe una solución alternativa:

## **Solución Alternativa**

- Copie la carpeta de datos del mundo del servidor a su PC local y cárguela como un mundo para un jugador de Minecraft.
- En JourneyMap, vaya a **J > Opciones > Avanzado** y establezca "Frecuencia de sondeo de Auto-Mapeo" en el valor más bajo permitido (500 ms). (Esta es la cantidad de tiempo que JourneyMap le permite a Minecraft tomar un descanso entre los archivos de región. La ejecución de Auto-Mapeo puede causar un retraso si intentas seguir jugando mientras se está ejecutando. Reducir la tasa de sondeo aumenta el retraso, pero reduce el tiempo total que lleva Automap el mundo.)
- En JourneyMap, ejecute **J > Acciones > Mapa automatico** para todas las regiones. Tenga en cuenta que Automap hará solo la dimensión en la que se encuentra y solo la superficie si se encuentra en la superficie. O si estás bajo tierra, solo el segmento vertical (fragmento) en el que estabas cuando iniciaste Automap. Si desea automatizar múltiples sectores o dimensiones, vaya al área correspondiente y ejecute Automap nuevamente.
- Si tienes la intención de compartir los resultados con otros jugadores, ten en cuenta que cualquier punto de ruta que crees irá a la misma carpeta que los mosaicos de imágenes del mapa.

Cuando termine, los mosaicos de imágenes del mapa generados y los puntos de referencia estarán en `.minecraft/journeymap/data/sp/{worldname}`. Para usar los resultados al conectarse nuevamente al servidor, deberá copiar el contenido de esa carpeta a la que JourneyMap usa para su conexión al servidor: `.minecraft/journeymap/data/mp/{servername}`. Si quieres compartir los resultados con otros jugadores, simplemente comprime la carpeta y dales estas instrucciones.