## **Descripción General**

!!! warning "Translation needed for 6.0"

    This page was updated for JourneyMap 6.0. Some sections shown are
    the English source pending translation. See Contributing to help
    translate the docs.

You don't have to have JourneyMap installed on the server to use the JourneyMap client. Installing it on the server gives admins a way to restrict some client features, manage waypoints, and support multi-world and proxy (BungeeCord / Velocity) setups. JourneyMap server runs on Fabric, NeoForge, and Forge servers, and on Paper servers (Minecraft 26.1 line). See [Installing](installing.md) for details.

## **Configuración de Administrador del Servidor**

Para acceder a la pantalla de administración del servidor, abra la pantalla de opciones de JourneyMap. Como usuario Op, habrá un botón "Administrador del servidor" en la parte inferior de la pantalla.

Todas las opciones en la pantalla de administración del servidor tienen información sobre herramientas que las explican en detalle.

Si el botón no aparece, es posible que deba cerrar sesión y volver a ingresar a su servidor si recientemente fue Op, o si el administrador lo deshabilitó en el archivo de configuración.

De forma predeterminada, todos los usuarios Op tienen acceso a la pantalla de administración del servidor. Esto se puede cambiar mediante un archivo de configuración en el servidor.

The config file location for Fabric servers: `(server_folder)/configs/journeymap_server.cfg`.

The config file location for NeoForge and Forge servers: `(server_folder)/world/serverconfig/journeymap_server.cfg`.

```text
    server {
    # Los jugadores de esta lista tienen acceso al panel de administración del servidor de Journeymap.
    # Agregue usuarios por nombre o UUID. ¡Prefiera UUID ya que es más seguro!
    # Cada valor en una nueva línea con el formato de ejemplo proporcionado. (elimine los valores predeterminados)
    S:"Journeymap Server Admins" <
    mysticdrew
    12341234132
    >
    
        # Por defecto, Todos los ops tienen acceso a la interfaz de usuario de Administración del Servidor en la pantalla Opciones.
        # Si se establece en falso, solo los usuarios de la lista de administradores tendrán acceso.
        # Si se establece en verdadero, todos los operadores y usuarios en la Lista de administradores tendrán acceso.
        B:"Ops Admin Access"=true
    }
```

## **Qué No Es**

* Este no es un mod de mapeo del lado del servidor. No se crean, elaboran, alojan, comparten ni siquiera contemplan mapas en el servidor.
* Esta no es una forma de administrar nada más que las funciones del cliente JourneyMap.
* Esto no es un jacuzzi ni una máquina del tiempo.

## **Uso del Paquete de Modificaciones**

El mod JourneyMap Client se rige por una [política de modpack diferente](../about/licensing.md) que el servidor.

Lo siguiente se aplica únicamente al mod del servidor:

Puede incluir JourneyMapServer en la configuración del lado del servidor de un modpack, siempre que acepte las siguientes condiciones:

1. Su iniciador debe vincularse directamente a una descarga aquí en Curse CDN si es capaz de hacerlo (ATLauncher, MCUpdater, etc.). Si el iniciador no puede vincular el archivo directamente, el archivo jar de JourneyMap Server puede realojarse/empaquetarse solo para los fines de su modpack, pero no distribuirse de ninguna otra manera.
2. Debes proporcionar un enlace a esta página para los administradores del servidor que usan tu modpack. La documentación es algo bueno.

## **Créditos y Quejas**

JourneyMapServer fue creado por Mysticdrew en nombre de un Techbrew con exceso de trabajo. Todo el crédito es para Mysticdrew. Las quejas deben redactarse utilizando cartas recortadas de revistas y periódicos y luego enviarse por correo postal a su funcionario del gobierno local dentro de un sobre que contenga harina para hornear. Asegúrese de incluir una dirección de remitente y una foto reciente.
