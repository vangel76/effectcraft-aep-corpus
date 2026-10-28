# EffectCraft After Effects test corpus

Test projects for the `.aep` / `.aepx` reader, importer and exporter of
[EffectCraft](https://github.com/storytold/effectcraft) (`crates/aep`). They are fetched by
`cargo xtask aep-corpus` in the EffectCraft repository, pinned to a commit of this repository
and checked file by file against a SHA-256 manifest there (`xtask/aep-corpus.sha256`). They are
not committed to EffectCraft itself (AGENTS.md: large binary fixtures are fetched pinned).

## What is here

`aep/` holds 17 small After Effects 2026 projects, about 27 MB in total:

- 15 combined projects, one per feature family (effects, masks, shapes, layer styles, text,
  layers and compositions, keyframes, 3D, footage and precompositions, markers, project
  settings in three files, the `.aep` / `.aepx` pair). Each case is one composition named like
  the case. EffectCraft's `crates/aep/tests/fixtures/CASES.md` lists every case with its file,
  composition and change.
- `empty.aep`, an empty project.
- `fx-switch.aep`, the fx switch of an effect instance.

Every file has an `.attribution` sidecar (author, source, licence, how it was made), as
EffectCraft's AGENTS.md §1 asks.

## How they were made

All files are original work: generated from scratch in Adobe After Effects 2026 by the
contributor, driven through scripting with one change per case (the generator is in EffectCraft's
`crates/aep/tests/fixtures/tools/`). They contain only synthetic project structure: no
third-party footage, presets, templates, Adobe sample projects or personal data. Footage paths
and the host name were replaced by neutral ones of the same length, and the XMP packet by the
base project's.

## Licence

MIT OR Apache-2.0, like EffectCraft ([LICENSE-MIT](LICENSE-MIT), [LICENSE-APACHE](LICENSE-APACHE)).
The repository can be transferred to the `storytold` organisation at the maintainers' request.
