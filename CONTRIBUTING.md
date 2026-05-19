# Contributing to JourneyMap Docs

See the [README](README.md) for setup and local-preview instructions.

## Admonition conventions (6.0 docs)

Use Material for MkDocs admonitions for branch-specific or version-specific
notes. The site has `admonition` enabled in `config/mkdocs.yml`, so the
following blocks are rendered with the standard Material styling.

- `!!! info "26.1 only"` - feature exists only on JourneyMap for Minecraft
  26.1 (locator bar, Paper server, etc.). When the feature has a known
  Minecraft-version floor, mention it inline, e.g. "Minecraft 1.21.6+".
- `!!! info "1.21.1 only"` - feature exists only on the 1.21.1 line.
- `!!! note "Available since 6.0.0"` - useful when readers may be comparing
  against the 5.x docs and need a clear marker that something is new.
- `!!! warning "Translation needed for 6.0"` - placed at the top of any
  `fr` or `es` page whose content has been replaced by an English 6.0
  update awaiting translation. Remove the admonition once the page has
  been translated in that locale.

### Example

```markdown
!!! info "26.1 only"
    Show On Locator Bar is available on JourneyMap for Minecraft 1.21.6
    and newer. It is not present on the 1.21.1 line.
```

## File layout reminders

- English source lives under `docs/en/`. French and Spanish mirrors live
  under `docs/fr/` and `docs/es/` with the same paths.
- Images are kept in `docs/{lang}/img/` and the same filenames are used in
  every locale.
- Navigation and per-locale labels live in `config/mkdocs.yml` under the
  `i18n` plugin's `nav_translations` blocks.
