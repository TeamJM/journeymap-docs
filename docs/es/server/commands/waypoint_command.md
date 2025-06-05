# **Comandos de Punto de Ruta**

Comandos te permite crear y eliminar waypoints del chat.

Nota: <u>No se trasladará a versiones anteriores</u>

- Comando: punto de ruta
- Alias: wp

**Crear Punto de Ruta**

```text
Los campos en [] son ​​opcionales ->
[player] es el jugador objetivo, si no se especifica ningún jugador, mostrará un error.
[announce] es si el jugador tiene una notificación de que se está creando un punto de ruta; si no se especifica, el valor predeterminado es falso y se crea de forma silenciosa.
- /waypoint create "nombre" dimension x y z color [player] [announce]
- /waypoint delete "nombre" [player] [announce]
```

**Ejemplos**

```text
-   /waypoint create "Spawn" minecraft:overworld 1 50 12 aqua
-   /waypoint create "Home" minecraft:overworld 1 50 12 aqua mysticdrew
-   /waypoint create "Home" minecraft:overworld 1 50 12 aqua true~~  actualmente con errores en v5.8.x
-   /waypoint create "Home" minecraft:overworld 1 50 12 aqua mysticdrew true
```

**Eliminar Punto de Ruta**

Nota: <u>Solo elimina punto de ruta creados por comando</u>

```text
/waypoint delete "NombrePuntoDeRuta"
/waypoint delete "NombrePuntoDeRuta" true
/waypoint delete "NombrePuntoDeRuta" mysticdrew
/waypoint delete "NombrePuntoDeRuta" mysticdrew true
```

**A Partir de JourneyMap 5.9.0**

Todos los comandos de waypoint requieren el uso del campo del jugador. Se necesita un jugador o una lista de jugadores o `@a` tanto para crear como para eliminar.
