# Low-Y witch huts

Swamp witch huts whose lowest spawning height is **-55 or deeper**, each one re-read by Minecraft 1.21.4's own world-generation code
(the oracle in [Low Witch Finder](https://github.com/kyoubitt/Low-Witch-Finder)). Listed at the depth the game gave, not the depth anyone claimed.

<!-- huts:start -->
![huts](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fkyoubitt%2Flow-y-witch-huts%2Fmain%2Fdata%2Fsummary.json&query=%24.total&label=huts&color=2ea44f&style=flat-square) ![y -59](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fkyoubitt%2Flow-y-witch-huts%2Fmain%2Fdata%2Fsummary.json&query=%24.y59&label=y%20-59&color=e0457b&style=flat-square) ![y -58](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fkyoubitt%2Flow-y-witch-huts%2Fmain%2Fdata%2Fsummary.json&query=%24.y58&label=y%20-58&color=f0883e&style=flat-square) ![updated](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fkyoubitt%2Flow-y-witch-huts%2Fmain%2Fdata%2Fsummary.json&query=%24.updated&label=updated&color=6e7781&style=flat-square)

| Depth | Huts | | Closest to 0,0 |
|---:|---:|:---|---|
| **-59** | 29 | `██` | `/tp 10775571 -57 -1979225` |
| **-58** | 208 | `███████████` | `/tp 5811 -56 4423` |
| **-57** | 221 | `████████████` | `/tp 11451648 -55 2183904` |
| **-56** | 95 | `█████` | `/tp 9740096 -54 1107104` |
| **-55** | 90 | `█████` | `/tp 14663264 -53 -462528` |

### Top 10
Deepest first, then closest to 0,0. [The full ranking](RANKING.md) lists all 643.

| # | Depth | Teleport | From 0,0 | Seed |
|---:|---:|---|---:|---|
| 1 | **-59** | `/tp 10775571 -57 -1979225` | 11.0M | `2331238980023747641` |
| 2 | **-59** | `/tp 9943776 -57 -18517296` | 21.0M | `392626046297007803` |
| 3 | **-59** | `/tp 10605152 -57 21621056` | 24.1M | `5031827728419125698` |
| 4 | **-59** | `/tp -19446992 -57 -14874912` | 24.5M | `5593787904694793058` |
| 5 | **-59** | `/tp 22848096 -57 11549184` | 25.6M | `3472990385799769684` |
| 6 | **-59** | `/tp 20073536 -57 -16419744` | 25.9M | `-6365651520887280832` |
| 7 | **-59** | `/tp -12967696 -57 22667872` | 26.1M | `2596740206080755241` |
| 8 | **-59** | `/tp -8824160 -57 -24605888` | 26.1M | `-4885706337220503668` |
| 9 | **-59** | `/tp -17366528 -57 -21854368` | 27.9M | `149223218598936182` |
| 10 | **-59** | `/tp -27136480 -57 -9937872` | 28.9M | `-7942261308732107398` |
<!-- huts:end -->

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
