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

