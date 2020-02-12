# Prestibags Minetest Mod
by prestidigitator and Poikilos <https://github.com/poikilos/prestibags>
(original Git Repo:
<https://github.com/prestidigitator/minetest-mod-prestibags>)

Prestibags are simple bags that act like chests you can pick up.  They
do not modify the player's normal inventory formspec, so they will not
interfere with any mods that do.

## Differences in Poikilos' Fork
- The model is much lighter, without sacrificing significant details.
- The license is viable (see "License" below).

### Re-texturing
The following assume a 256x256 texture resolution (the locations under
"UV Map details" do not). Also, to avoid texture edge artifacts, the UV
map is actually 2px shy of the outline of the texture (4px total on each
dimension), so expect up to 2px of the textures below to be cropped if
they touch the edge. There will also be warping due to the bag shape,
but due to the improved UV map, large text or decals will still be
legible.
- To add a decal, the following location will place it on the "front"
  (The side seen upon placing the bag; The height can be anything, but y
  may have to be adjusted for different heights):
  - `[combine:112x112:40,112=texture.png]`
- To replace the entire "fabric" of the bag (including visible inner
  part of top):
  - `[combine:224x224:0,32=texture.png]`
- To replace the entire "outside" of the bag (not visible inner part of
  top) like in a "full-bleed" wrap-around print on an IRL bag:
  - `[combine:224x192:0,64=texture.png]`
- None of the above replace the "contents" of the bag. To replace that
  part:
  - `[combine:248x64:0,0=texture.png]`
- To replace the entire rectangle that makes up the texture, including
  the contents and only excluding the rope, you can use
  any 224x256 image and place it at 0,0.
  - `[combine:224x256:0,0=texture.png]`

#### UV Map details
- If you want a decal on the same side of the bag as the rope's ends,
  place it on the first 7/16ths of the image. However, since the rope
  is on the left when placed, a decal should probably be about 1/2 of
  the image width and centered at 7/16ths.
- The left 7/8ths of the image is the bag.
   - The top 1/8th of the image is the contents of the bag.
   - The next 1/8th is the inside of the top part of the bag.
   - The other 6/8ths are the outside of the bag.
     - Including a bottom margin of 1/64.
- The left edge of the region and right edge (at 7/8ths of width) are
  "sewn" together to make the "seam" of the bag.
- Halfway between 0 and 7/8ths (which is 7/16ths) is the "fold"
  of the bag (At this division, the left part of the bottom is "sewn"
  to the right part of the bottom).
- Rope:
   - The right 1/8th of the image is the rope, including a margin of 1/64.
     However, since the rope is a separate manifold object in the mesh
     file, the rope can be anywhere on the 3D model and be posed without
     negative effects.
     - The rope is currently over the left part of the bag relative to
       the halves described above, but this can be changed in future
       revisions.
- The specifications above should remain the same for any future
  revisions of the UV map in the 3d model files.

## Main Features
- Retain their inventory when picked up or unloaded/reloaded by the
  server.
- Can be stored in other bags, nested as deeply as you like.
- Are NOT owned, so any player can open them and pick them up.
- Are flammable, so don't put them near lava or fire!
- Fit in spaces with non-solid nodes (e.g. water, torches), but don't
  build solid stuff on top of them!

Note that bags are "active entities", although they are non-physical
and act in many ways like nodes.  This means that the "/clearobjects"
command will destroy them, and they can potentially take damage from
sources other than fire.  They will show wear like a tool when taken
into inventory if they have taken any damage.

Required Minetest Version: >=0.4.5

Dependencies: (none)

Optional Dependencies: default, wool (for crafting), fire

Craft Recipies (W = "group:wool"):
```
   — W —
   W — W
   W W W
```



## Future Plans
> In the future I may enhance bags so they can be opened directly from
> inventory by wielding and "using" them, but I'm struggling with this
> because I kind of like the drawback that you have to risk placing them
> to interact with their inventories.
-prestidigitator

## License
- Authors: prestidigitator, poikilos (edited by)
  - prestidigitator created the original versions of all media from
    scratch.
- Code License: MIT (see LICENSE)
- Media License: CC0
- The original license said I could do whatever I want, and I wanted to
  change the license.

