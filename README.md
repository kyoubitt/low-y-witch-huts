# Low-Y witch huts

Swamp witch huts whose lowest spawning height is **-55 or deeper**, each one re-read by Minecraft 1.21.4's own world-generation code
(the oracle in [Low Witch Finder](https://github.com/kyoubitt/Low-Witch-Finder)). **643 huts**, listed at the depth the game gave, not the depth anyone claimed.

| Depth | Huts | From team109's list | Other |
|---:|---:|---:|---:|
| -59 | 29 | 28 | 1 |
| -58 | 208 | 162 | 46 |
| -57 | 221 | 218 | 3 |
| -56 | 95 | 95 | 0 |
| -55 | 90 | 89 | 1 |

## Files
- `data/y-59.jsonl` ... `data/y-55.jsonl`: one hut per line, closest to 0,0 first:
  `{"seed":"2331238980023747641","x":10775571,"z":-1979225,"y":-59,"source":"known list","verified":"1.21.4"}`
- `data/all.tsv`: the same in the layout Low Witch Finder's own list uses (`depth seed x y z note`, `y` is the `/tp` height).

`seed` is the full world seed. `x`, `z` are the hut's block position. Java Edition, default overworld. A few huts depend on
chunk-loading order, so approach from a few directions if one doesn't show up.

## How it is made
`tools/export_catalog.py` in Low Witch Finder reads each candidate (seed + position), runs the game's code on it, and writes only the ones that
come out at -55 or deeper. Candidates that don't reproduce are dropped, not listed. New finds from the finder are added the same way.

## Credit
- [xvyz1](https://github.com/xvyz1), who helped make the witch hut finder this list comes from.
- [team109/ultra_low_swamp_hut](https://github.com/team109/ultra_low_swamp_hut) (MIT): most of the huts here were first listed in its catalog. Each one was
  re-checked before being added; 11 of its 1.21.4 entries did not reproduce and are left out. See `SOURCES.md`.
