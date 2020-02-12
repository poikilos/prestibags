# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a
Changelog](https://keepachangelog.com/en/1.0.0/).

## [git] - 2020-02-12
### Changed
- The UVs for the entire fabric part and inside are now, where
  applicable, square and aligned with pixels (as if the bag is made of a
  single piece of fabric).
  - The left side is aligned with the right side so that making or using
    an existing rectangular seamless texture is now possible (see
    "Re-texturing" in README.md)

## [git] - 2020-02-10
### Added
- Low-poly version: "prestibags_bag.blend"
  - for high-poly version for rendering images, see below.

### Changed
- The original license said I could do whatever I want, and I wanted to
  change the license (See README.md and LICENSE).
- Append all objects from old blend file into a new Blender 2.8 (2.81)
  file (Move objects into new collections based on old layout (layers)).
  - Layer 4 and 11 were visible (if using Blender 2.79).
  - Overwrite "prestibags-hipoly.blend" with the new file (same design).
- Simplify the model (there was an exact copy of the bag with inverted
  normals inside the bag, but only polygons near the top are necessary).
  - Decimate to about 2%, then manually edit to make the rope and bag
    manifold (individually).
- Delete all vertices of inside that weren't showing.
- Redo UVs and texture (based on old texture).


## [1.0] - 2013-03-07
### Added
- First working version.
