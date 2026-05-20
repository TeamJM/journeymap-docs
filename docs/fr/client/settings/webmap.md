# **Webmap Settings**

!!! warning "Translation needed for 6.0"

    This page was updated for JourneyMap 6.0 in English. Translation
    is pending; the content shown is the English source. See
    Contributing to help translate the docs.

The webmap is a different way to view your map: in a web browser instead
of in-game. This lets you keep a map view on a second monitor or another
device on your network.

![Webmap-Settings](../../img/settings/client/webmap.png){: .center}

!!! info "Requires the Webmap addon"

    As of JourneyMap 6.0 the webmap is a separate addon mod. This
    settings category is always shown, but the settings only take effect
    when the JourneyMap Webmap addon is installed. If the addon is not
    installed, the settings are disabled.

    See the [Webmap](../../webmap/installing.md) section for how to
    install and use it.

## **Toggles**

This toggle is **off** by default.

| Toggle         | Description                                          |
|----------------|------------------------------------------------------|
| Enable Web Map | Whether the webmap server is enabled and accessible. |

## **Other Settings**

| Setting | Options                               | Description                                  |
|---------|---------------------------------------|----------------------------------------------|
| Port    | Range: 80 - 65535 (Default: **8080**) | The port the webmap server tries to bind to. |

!!! note "Port selection"

    If the configured port is already in use, the webmap falls back to a
    free port chosen by the operating system instead of failing to
    start, so the port actually used can differ from what you set. If
    the Announce Mod advanced option is enabled (the default), JourneyMap
    posts the webmap address in chat once when you join a world. The
    resolved port is also written to the game log.
