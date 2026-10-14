<!-- Modified-by: FreeANDIY (Free Andy Agency), 2026. New file, not part of upstream LightCraft. -->
# FreeANDIY Light: changes from upstream LightCraft

This file lists what the FreeANDIY fork changes in LightCraft (Apache-2.0 section 4(b)). The
exact changes are generated from `freeandiy/` (see `NOTICE`); `git diff upstream-main main`
shows every changed file.

## Unreleased

### Branding
- Product name **FreeANDIY Light** everywhere users see it: window title, menus, About, messages,
  all bundled translations, installers, desktop entries, the web page.
- Application id `agency.freeandy.light` (was `ai.storyteller.lightcraft`), so FreeANDIY builds
  install next to LightCraft. Settings folder `FreeANDIY Light` (macOS, Windows) /
  `freeandiy-light` (Linux); portable mode uses `FreeANDIY Light Data`.
- Executables `freeandiy-light` and `freeandiy-light-cli`; the cargo packages keep their names.
- New app icon set (the angel Andy, Free Andy Agency) and DMG background.
- Every theme gets FreeANDIY's stamp-rose accent and flat print shape; Paper is paper and ink,
  Midnight ink and paper. Charcoal and Silver keep their neutral greys for judging photos.
- UI font IBM Plex Sans (OFL 1.1) on the desktop.

### Changed
- Photo ▸ Edit In opens FreeANDIY Photo (found by its app id and executable) instead of PhotoCraft.
- Help links point to the FreeANDIY website and this repository (help, feedback, source).

### Removed
- The ArtCraft name, wordmark and logos (`docs/brand/`), as their terms require of forks.
- The ArtCraft Discord button and links (top bar, Help menu, About).
- Upstream's release and platform workflows.

### Added
- About: attribution to upstream LightCraft and the Free Andy Agency seal.
- Slovak user interface (menus; the rest falls back to English for now).
- `NOTICE` section and `assets/ATTRIBUTION.md` rows for FreeANDIY's assets and fonts; packages
  now ship `ATTRIBUTION.md`, the font licences and the brand terms.
