# Totem ZMK Config

Personal ZMK firmware configuration for the [Totem](https://github.com/GEIGEIGEIST/TOTEM) keyboard.

Based on [GEIGEIGEIST/zmk-config-totem](https://github.com/GEIGEIGEIST/zmk-config-totem).

Inspired by [Seniply](https://stevep99.github.io/seniply/) and [Callum](https://github.com/callum-oakley/qmk_firmware/tree/master/users/callum#readme).

## Layout Notes

- Base layer uses Graphite.
- The two isolated outer keys are intentionally unused.
- The layer diagrams omit those two unused outer keys.
- `Mod/Ext` is the main layer key:
  - tap = sticky `MOD`
  - hold = `EXT`
- `MF` is a momentary thumb-chord layer:
  - hold both middle thumbs = `MF`
- `MOD` keys are hybrid modifiers:
  - tap = sticky mod
  - hold = normal held mod

## Layer Access

| Layer | Access                  |
| ----- | ----------------------- |
| MOD   | tap `Mod/Ext`           |
| EXT   | hold `Mod/Ext`          |
| SYM   | hold `Bspc/Sym`         |
| NUM   | hold `Space/Num`        |
| MF    | hold both middle thumbs |

## BASE (Graphite)

Left half

| Row    | Col 1 | Col 2 | Col 3 | Col 4 | Col 5 |
| ------ | ----- | ----- | ----- | ----- | ----- |
| Top    | `B`   | `L`   | `D`   | `W`   | `Z`   |
| Home   | `N`   | `R`   | `T`   | `S`   | `G`   |
| Bottom | `Q`   | `X`   | `M`   | `C`   | `V`   |

Right half

| Row    | Col 1 | Col 2 | Col 3 | Col 4 | Col 5 |
| ------ | ----- | ----- | ----- | ----- | ----- |
| Top    | `'/"` | `F`   | `O`   | `U`   | `J`   |
| Home   | `Y`   | `H`   | `A`   | `E`   | `I`   |
| Bottom | `K`   | `P`   | `,`   | `.`   | `/`   |

Thumbs

| Left outer | Left middle | Left inner | Right inner | Right middle | Right outer |
| ---------- | ----------- | ---------- | ----------- | ------------ | ----------- |
| `RET`      | `MOD/EXT`   | `CMD`      | `BSP/SYM`   | `SPC/NUM`    | `SHIFT`     |

## MOD (tap `Mod/Ext`)

Left half

| Row    | Col 1    | Col 2  | Col 3   | Col 4  | Col 5  |
| ------ | -------- | ------ | ------- | ------ | ------ |
| Top    |          |        |         |        |        |
| Home   | `SHIFT*` | `ALT*` | `CTRL*` | `CMD*` | `HYP*` |
| Bottom |          |        |         |        |        |

Right half

| Row    | Col 1 | Col 2 | Col 3 | Col 4 | Col 5 |
| ------ | ----- | ----- | ----- | ----- | ----- |
| Top    |       |       |       |       |       |
| Home   |       |       |       |       |       |
| Bottom |       |       |       |       |       |

## EXT (hold `Mod/Ext`)

Left half

| Row    | Col 1   | Col 2 | Col 3  | Col 4 | Col 5 |
| ------ | ------- | ----- | ------ | ----- | ----- |
| Top    | `ESC`   |       |        |       |       |
| Home   | `SHIFT` | `ALT` | `CTRL` | `CMD` |       |
| Bottom |         |       |        |       |       |

Right half

| Row    | Col 1  | Col 2  | Col 3 | Col 4   | Col 5  |
| ------ | ------ | ------ | ----- | ------- | ------ |
| Top    |        | `HOME` | `END` |         | `PGUP` |
| Home   | `LEFT` | `DOWN` | `UP`  | `RIGHT` |        |
| Bottom |        | `TAB`  |       |         | `PGDN` |

Thumbs

| Left outer | Left middle | Left inner | Right inner | Right middle | Right outer |
| ---------- | ----------- | ---------- | ----------- | ------------ | ----------- |
|            | `EXT`       |            | `DEL`       | `SPC`        |             |

## SYM (hold `Bspc/Sym`)

Left half

| Row    | Col 1   | Col 2 | Col 3  | Col 4 | Col 5 |
| ------ | ------- | ----- | ------ | ----- | ----- |
| Top    | `` ` `` | `~`   | `@`    | `#`   | `$`   |
| Home   | `SHIFT` | `ALT` | `CTRL` | `CMD` | `HYP` |
| Bottom | `^`     | `&`   | `!`    | `?`   | `\|`  |

Right half

| Row    | Col 1 | Col 2 | Col 3 | Col 4 | Col 5 |
| ------ | ----- | ----- | ----- | ----- | ----- |
| Top    |       | `/`   | `:`   | `;`   | `\`   |
| Home   | `<`   | `(`   | `{`   | `[`   | `-`   |
| Bottom | `>`   | `)`   | `}`   | `]`   | `_`   |

Thumbs

| Left outer | Left middle | Left inner | Right inner | Right middle | Right outer |
| ---------- | ----------- | ---------- | ----------- | ------------ | ----------- |
|            |             |            | `SYM`       |              |             |

## NUM (hold `Space/Num`)

Left half

| Row    | Col 1 | Col 2 | Col 3 | Col 4 | Col 5 |
| ------ | ----- | ----- | ----- | ----- | ----- |
| Top    | `/`   | `7`   | `8`   | `9`   | `%`   |
| Home   | `-`   | `1`   | `2`   | `3`   | `+`   |
| Bottom | `x`   | `4`   | `5`   | `6`   | `*`   |

Right half

| Row    | Col 1 | Col 2 | Col 3  | Col 4 | Col 5   |
| ------ | ----- | ----- | ------ | ----- | ------- |
| Top    |       |       |        |       |         |
| Home   | `HYP` | `CMD` | `CTRL` | `ALT` | `SHIFT` |
| Bottom |       |       |        |       |         |

Thumbs

| Left outer | Left middle | Left inner | Right inner | Right middle | Right outer |
| ---------- | ----------- | ---------- | ----------- | ------------ | ----------- |
| `:`        | `0`         | `=`        |             | `NUM`        |             |

## MF (hold both middle thumbs)

Left half

| Row    | Col 1  | Col 2        | Col 3  | Col 4  | Col 5 |
| ------ | ------ | ------------ | ------ | ------ | ----- |
| Top    |        | `MUTE`       | `VOL-` | `VOL+` |       |
| Home   | `STOP` | `PLAY/PAUSE` | `PREV` | `NEXT` |       |
| Bottom |        |              | `BRI-` | `BRI+` |       |

Right half

| Row    | Col 1 | Col 2 | Col 3 | Col 4 | Col 5 |
| ------ | ----- | ----- | ----- | ----- | ----- |
| Top    | `F12` | `F7`  | `F8`  | `F9`  |       |
| Home   | `F10` | `F1`  | `F2`  | `F3`  |       |
| Bottom | `F11` | `F4`  | `F5`  | `F6`  |       |

## Legend

- `X/Y` = tap `X`, hold `Y`
- `SHIFT*`, `ALT*`, `CTRL*`, `CMD*`, `HYP*` on `MOD`:
  - tap = sticky modifier
  - hold = normal held modifier
- `HYP` = Hyper (`Ctrl+Alt+Cmd+Shift`)
- Outer isolated keys are unused

## Special Base Key

This layout has one custom base-layer key behavior:

- the top-right first key sends `'` normally
- if you hold `SHIFT`, that same key sends `"`

In the tables above, that key is shown as `'/"`.

## Combos (EXT layer)

| Keys | Output                 |
| ---- | ---------------------- |
| H+A  | Opt+Left (word left)   |
| A+E  | Opt+Right (word right) |
