Waypoints
=========

Waypoints allow you to mark specific locations on your map, in order
to keep track of those locations or easily find your way back to them
later.

Additionally, death waypoints are created when, for example, you're 
blown off the edge of a cliff by `a trumpet-wielding skeleton`_.

By default, they're shown using a coloured beacon beam, and the name and
icon for the waypoint will be displayed when you look towards it - but
this behaviour can be changed in the :ref:`settings manager <settings>`.
Death waypoints may also be disabled there, if preferred.

.. warning:: 
    If you're using OptiFine, it's likely that you won't be able
    to see waypoints in the world. We're not sure what causes this.
    For more information, please see our :ref:`our troubleshooting page`.

.. figure:: /_static/images/waypoint.png
    :alt: Waypoint example

You can create waypoints using one of the following methods:

* By pressing :kbd:`B` ingame to create one where you're standing
* By double-clicking or pressing :kbd:`B` in 
  :ref:`the full-screen map <full-screen>` to create a waypoint at the cursor
* By opening the waypoint manager and manually creating a waypoint

Waypoint Management
-------------------

The waypoint manager provides a single place for - as you may expect - managing
your waypoints. You can open it in the following ways:

* By pressing :kbd:`Ctrl` :kbd:`B` ingame
* By opening :ref:`the full-screen map <full-screen>` and clicking on the waypoint
  manager button at the bottom

.. figure:: /_static/images/waypoint-manager.png
    :alt: Waypoint manager

The waypoint manager gives you a list of all of your waypoints, and provides some
options to manage them. At the bottom are the following buttons:

* **Options**: Open the :ref:`settings manager <settings>`
* **New**: Create a new waypoint
* **Dimension**: Filter shown waypoints based on dimension
* **Close**: Close the waypoint manager

Each waypoint has the following options available:

* **Teleport**: If allowed by the server, teleport directly to the waypoint
* **Find**: Find the waypoint on :ref:`the full-screen map <full-screen>`
* **On**/**Off**: Toggle the waypoint's visibilty ingame
* **Remove**: Delete the waypoint
* **Edit**: Open the waypoint editor
* **Chat**: Copy the waypoint's information to the chat box, as shown:

  .. figure:: /_static/images/waypoint-chat.png
      :alt: Waypoint in the chat box

Editing waypoints
~~~~~~~~~~~~~~~~~

When creating or editing a waypoint, the following screen is shown:

.. figure:: /_static/images/waypoint-edit.png
    :alt: Waypoint editor

The waypoint editor provides the following settings for each waypoint:

* **Name**: This display name for the waypoint
* **Location**: The position for this waypoint
* **Dimensions**: Toggles for the dimensions the waypoint should be enabled within
* **Enabled**: Whether this waypoint is enabled and should be visible
* **Colour**: The waypoint's color, given as red, green and blue values

  You can also click on the colour wheel to pick a colour, or click on the
  **Random Colour** button to get a new colour

Here's what each of the other buttons do:

* **Remove**: Delete the waypoint entirely
* **Reset**: Undo your edits to the current waypoint
* **Save**: Save the changes you've made to the waypoint
* **Close**: Close the editor and discard your changes

.. Shameless plug. :>

.. _a trumpet-wielding skeleton: https://www.curseforge.com/minecraft/mc-mods/trumpet-skeleton-redooted
