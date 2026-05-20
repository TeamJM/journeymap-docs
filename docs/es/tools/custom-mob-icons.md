
!!! warning "Translation needed for 6.0"

    This page was updated for JourneyMap 6.0 in English. Translation
    is pending; the content shown is the English source. See
    Contributing to help translate the docs.

## **Custom Mob Icons**

JourneyMap shows an icon for each mob on the map and the entity radar.

As of JourneyMap 6.0, JourneyMap **automatically generates an icon** for
every mob, including modded mobs, from the mob's model. You no longer
need to provide icons just to get something to show up. You can still
provide your own icons to replace the generated ones, and you are no
longer restricted to a mod-specific texture path to do it.

## **Icon path**

Custom mob icons live under the `journeymap` namespace at this path:

```text
assets/journeymap/icon/entity/{mod_id}/{mob_name}.png
```

- `{mod_id}` is the id of the mod the mob belongs to, or `minecraft`
  for a vanilla mob.
- `{mob_name}` is the name of the mob.

For example, a custom creeper icon goes at:

```text
assets/journeymap/icon/entity/minecraft/creeper.png
```

This path is the same whether you are a mod author bundling icons in
your mod jar or a resource pack author shipping them in a resource pack.

## **Image size**

The recommended icon size is 16x16. Icons can be any size, but they
have to fit inside the marker's circle to display correctly. If you use
a larger image, put transparent pixels in the corners so they do not
stick out past the circle.

## **Outlined icons**

JourneyMap has an icon "outlined" display option. Resource packs can
provide an outlined variant of an icon by adding a second file with an
`_outline.png` suffix, for example:

```text
assets/journeymap/icon/entity/minecraft/creeper.png
assets/journeymap/icon/entity/minecraft/creeper_outline.png
```

The outlined variant is optional. If the outlined display option is
enabled and no `_outline.png` variant exists, JourneyMap uses the
regular icon instead. So if a resource pack replaces `creeper.png` but
not `creeper_outline.png`, the outlined option will use the replaced
`creeper.png`.

## **Adding icons without a resource pack**

You can also drop icons straight into JourneyMap's icon folder, without
making a resource pack:

```text
{minecraft}/journeymap/icon/entity/{mod_id}/{mob_name}.png
```

Icons added this way require a client restart to be picked up.

The icons JourneyMap generates automatically are stored under
`{minecraft}/journeymap/icon/entity/`. You can browse that folder to see
the mob names JourneyMap uses and to use the generated icons as a
starting point for your own.
