## **Mobs Personalizados en el Mapa (radar de mobs)**

- Asegúrese de que sus EntityCreatures implementen al menos una de estas interfaces principales de Minecraft: IAnimal, IMob, INpc o IWaterMob.
- Si desea proporcionar sus propios iconos de Mob, consulte [Conjuntos de iconos de Mob personalizados](custom-mob-icons.md).
- Las EntityCreatures con un objetivo hostil se mostrarán como hostiles.
- Las EntityCreatures configuradas como invisibles (furtivas) se ocultarán en el radar.

## **Crear Sugerencias de Puntos de Ruta en el chat**

Los jugadores pueden agregar puntos de ruta haciendo clic en el texto con formato especial en el chat. (Útil para realizar misiones, mensajes de bienvenida, etc.)

Por ejemplo:

`NPC dice: "Aquí es donde enterré mi botín:" [nombre:"tesoro", x:1212, y:70, z:456, dim:0]`

El texto del chat en sí no cambia, sino que se convierte en un enlace para los jugadores con JourneyMap. El texto al pasar el mouse muestra que se puede hacer clic en él para crear un punto de ruta o hacer clic en Mayús y hacer clic para mostrarlo en el mapa en pantalla completa.

!!! note "Nota"

 ''nombre'' y ''dim'' son opcionales. Si se omite "dim", se asume la dimensión del jugador.

## **Mostrar Formas, Texto o Puntos de Ruta Personalizados en el Mapa**

Hay una [API de JourneyMap](https://github.com/TeamJM/journeymap-api) (para Minecraft 1.9.4 y versiones posteriores) que le brinda la posibilidad de administrar puntos de referencia personalizados y agregar superposiciones en el minimapa y el mapa en pantalla completa. o mapa web.

## **¡En caso de duda, habla con nosotros!**

Póngase en contacto con el equipo de JourneyMap @Developers en el [servidor de Discord de JourneyMap](https://discord.gg/eP8gE69) público.