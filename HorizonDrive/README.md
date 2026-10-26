# Horizon Drive assets

Initial asset library for the Horizon Drive Three.js driving game. This folder contains **actual binary files** for the runtime and original source maps used to make their mobile variants. `ASSET_MANIFEST.json` records exact paths, byte sizes, per-file SHA-256 digests, provenance/license and commit-pinned raw links.
The pushed binary-content commit on `main` is `caf7c1caf13918b5647932e788918e19bd5b8830`; the manifest's raw URLs use that immutable SHA.

## Inventory

- `assets/models/horizon-sports-coupe.glb` — generated red sports-coupe vehicle GLB.
- `assets/models/tropical-tree.glb` — generated broadleaf vegetation GLB.
- `assets/hdri/autumn_field_puresky_1k.hdr` and `assets/textures/sky/autumn_field_puresky_1k_tonemapped.jpg` — retained outdoor source HDRI and lightweight equirectangular browser derivative.
- `assets/textures/road/`, `grass/`, `ground/`, and `rock/` — retained 1K source PBR maps. Road maps are from Poly Haven Asphalt 02; ground/vegetation/rock maps are ambientCG CC0 assets.
- `assets/textures/mobile/` — filtered 512px runtime derivatives grouped by material, preserving the larger source maps separately.
- `assets/share/favicon.png` and `assets/share/og.png` — original game mark and generated promotional image. The cover is social artwork, **not** an in-game model, material or scene substitute.
- `SOURCES_AND_LICENSES.md` — authoritative publisher links, rights and file-to-use notes.
- `ASSET_MANIFEST.json` — per-file verifiable metadata; raw URLs are pinned to the immutable asset commit recorded there.

## Usage notes

Generated GLBs are self-contained binary glTF files. Texture maps are ordinary JPG images. Reuse each source map with the matching material: `color`/`diff` as base color, `normalgl`/`nor_gl` as the OpenGL normal map, `roughness`/`rough` as roughness, and the Asphalt 02 `rough_ao` file as its combined surface source when desired. Keep color-space handling for base-color images separate from linear normal/roughness inputs.

The original downloadable PBR/HDRI sources retain their listed CC0 terms. Generated models and promotional artwork are **not** claimed to be CC0 because the generation tool did not supply a separate third-party license; consult source notes before re-licensing them outside the project. The repository root `LICENSE` is preserved.

Repository landing page: [README](../README.md). Project source and implementation: https://github.com/Hiperstark50/Assets/tree/main/HorizonDrive
