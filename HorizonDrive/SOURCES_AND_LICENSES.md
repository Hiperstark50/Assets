# Asset sources and licensing

Source and license facts below were checked against the publishers' official pages on 2026-10-26. Original downloads and local derivatives are preserved under `assets/`; the Webdev registration facts are in `assets.lock.json`. Game-world models are actual GLB files, and environment/road materials are ordinary maps—not AI images standing in for 3D models.

## Poly Haven — CC0

Poly Haven's [asset license](https://polyhaven.com/license) states that its HDRIs, textures, and 3D models are CC0 and may be used commercially and redistributed. Attribution is not required but is appreciated.

- **Asphalt 02** by Rob Tuytel: [official asset page](https://polyhaven.com/a/asphalt_02), [official file map](https://api.polyhaven.com/files/asphalt_02). Downloaded 1K maps are retained at `assets/textures/road/asphalt_02_diff_1k.jpg`, `asphalt_02_nor_gl_1k.jpg`, `asphalt_02_rough_1k.jpg`, and `asphalt_02_rough_ao_1k.jpg`. The color, normal and roughness maps are used for the road; the AO source is retained for provenance/completeness. The game uses separately generated 512px filtered mobile copies in `assets/textures/mobile/road/`. The exact filenames and registered storage keys remain in `assets.lock.json`.
- **Autumn Field (Pure Sky)**: [official asset page](https://polyhaven.com/a/autumn_field_puresky), official `1K` Radiance environment source at `assets/hdri/autumn_field_puresky_1k.hdr`. `assets/textures/sky/autumn_field_puresky_1k_tonemapped.jpg` is a deterministic equirectangular JPEG derivative for lightweight browser loading; the original Radiance HDR file is preserved unchanged. The environment image supplies natural sky/light colour.

## ambientCG — CC0 1.0 Universal

ambientCG's [official license documentation](https://docs.ambientcg.com/license/) states that downloaded assets use CC0 1.0 Universal, can be copied, modified, distributed and commercially used, and may be included as raw files in a game. Attribution is optional but suggested.

- **Grass 001**: [official asset page](https://ambientcg.com/view?id=Grass001). Source color, OpenGL normal and roughness maps in `assets/textures/grass/`; filtered 512px runtime copies in `assets/textures/mobile/grass/` supply the roadside grass.
- **Ground 014**: [official asset page](https://ambientcg.com/view?id=Ground014). Source color, OpenGL normal and roughness maps in `assets/textures/ground/`; filtered 512px copies in `assets/textures/mobile/ground/` supply non-road ground/gravel.
- **Rock 064**: [official asset page](https://ambientcg.com/view?id=Rock064). Source color, OpenGL normal and roughness maps in `assets/textures/rock/`; filtered 512px copies in `assets/textures/mobile/rock/` supply rock/cliff surface detail.

The mobile derivatives were produced by `scripts/prepare-mobile-textures.py` with deterministic filtered downscaling from the 1K maps. Originals remain unchanged. No attribution is required under these source CC0 terms; the project retains publisher links and credits to preserve provenance.

## Models and branding

- `assets/models/horizon-sports-coupe.glb` and `assets/models/tropical-tree.glb` were generated specifically for the approved project by Manus's built-in text-to-3D generator. The generation tool did not expose a separate third-party asset license. They are **not** represented as Poly Haven, ambientCG, or CC0 models. The tree model is a repeated foliage prop; other forest, traffic, road and terrain elements are shared/procedural runtime geometry.
- `assets/share/favicon.png` is an original simple brand mark created for the first Three.js game checkpoint.
- `assets/share/og.png` is separately generated Open Graph promotional artwork (1200×675). It is brand/social preview artwork only; it is **not** an in-game model, material or playable scene substitute.

The target asset-repository copy includes a file-by-file `ASSET_MANIFEST.json` with exact repository paths, file hashes and verified raw GitHub URLs; see the project README for the repository link.
