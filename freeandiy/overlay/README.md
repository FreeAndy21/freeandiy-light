<!-- Modified-by: FreeANDIY (Free Andy Agency), 2026. Replaces upstream LightCraft's README. -->
<p align="center">
  <img src="assets/app-icon/freeandiy-light-1024.png" width="128" alt="FreeANDIY Light icon">
</p>

<h1 align="center">FreeANDIY Light</h1>

<p align="center">
  <b>A free, open-source photo library and non-destructive raw developer. Native Rust, runs on macOS, Windows, Linux and in the browser.</b><br>
  Part of <a href="https://freeandiy.freeandy.agency">FreeANDIY</a>, free creative and office apps by Free Andy Agency.
</p>

---

## About

FreeANDIY Light is a photo library and non-destructive raw developer: import, rate and keyword
your photos, develop raw files with local adjustments and masks, merge HDR and panoramas, and
export. It is a native egui/wgpu app (no webview), and the web version is the same Rust code
compiled to WebAssembly. Photo ▸ Edit In opens a photo in FreeANDIY Photo.

Every action is a command, so the app can be driven from a CLI (`freeandiy-light-cli`), a JSON
control channel or an MCP server.

**FreeANDIY Light is based on the open-source project
[LightCraft](https://github.com/storytold/lightcraft) (© ArtCraft Team and contributors,
MIT/Apache-2.0). FreeANDIY is not affiliated with the ArtCraft team.** The editor itself is their
work; FreeANDIY adds its own branding, packaging and translations, and follows upstream closely.

## Download

Builds for macOS, Windows and Linux are published on the
[Releases](https://github.com/FreeAndy21/freeandiy-light/releases) page as
`freeandiy-light-<version>-<os>-<arch>.*`.

## Build from source

Requires Rust (see `rust-version` in `Cargo.toml`).

```sh
cargo run --release -p lightcraft                         # desktop app (binary: freeandiy-light)
cargo run --release -p lightcraft-cli -- --help           # CLI (binary: freeandiy-light-cli)
cd apps/lightcraft-web && trunk build --release           # web build (WebAssembly)
```

The crate names keep upstream's `lightcraft-*`, so upstream changes merge cleanly. The developer documentation in `docs/` is
upstream's and still says LightCraft.

## How this fork is made

Everything FreeANDIY changes lives in [`freeandiy/`](freeandiy/): the brand definition
(`branding.toml`, `app.toml`), assets, a handful of small patches and text rules. All other files
are regenerated from upstream LightCraft by `freeandiy/scripts/regenerate.sh`, so updates from
upstream never conflict. See [`freeandiy/docs/upstream-sync.md`](freeandiy/docs/upstream-sync.md).

Issues with FreeANDIY builds go to
[our tracker](https://github.com/FreeAndy21/freeandiy-light/issues), not to upstream.

## License

The code is licensed, like upstream, under either of [MIT](LICENSE-MIT) or
[Apache-2.0](LICENSE-APACHE) at your option. See [`NOTICE`](NOTICE) and [`assets/ATTRIBUTION.md`](assets/ATTRIBUTION.md)
for third-party material.

The FreeANDIY and Free Andy Agency names, the angel Andy, logos and app icons are © Free Andy
Agency and **not** covered by the code license; see
[`freeandiy/assets/brand/LICENSE-brand.txt`](freeandiy/assets/brand/LICENSE-brand.txt).

<sub>Adobe and Lightroom are trademarks or registered trademarks of Adobe Inc. in the United
States and/or other countries. FreeANDIY Light is an independent, open-source project and is not
affiliated with, sponsored by or endorsed by Adobe Inc.; these names are used only to describe the
workflows it is compatible with.</sub>
