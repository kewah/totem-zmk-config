# Totem ZMK Config

Personal ZMK firmware configuration for the [Totem](https://github.com/GEIGEIGEIST/TOTEM) keyboard.

Based on [GEIGEIGEIST/zmk-config-totem](https://github.com/GEIGEIGEIST/zmk-config-totem).

Inspired by [Seniply](https://stevep99.github.io/seniply/) and [Callum](https://github.com/callum-oakley/qmk_firmware/tree/master/users/callum#readme).

## Layout Notes

- Base layer uses Graphite.
- The right isolated outer key is intentionally unused. The left isolated outer key holds `Mouseless` (`Hyper+Enter`) on `BASE` and `` CMD+` `` (cycle app windows) on `EXT`/`MOD`.
- The layer diagrams omit isolated outer keys unless one is used on that layer.
- `Mod/Ext` is the main layer key:
  - tap = sticky `MOD`
  - hold = `EXT`
- `EXT` left half is a one-handed mouse companion: app switching, tab cycling, window cycling, back/forward, close, select all, undo/cut/copy/paste while the right hand stays on the mouse.
- `MF` is a momentary thumb-chord layer:
  - hold both middle thumbs = `MF`
- `BT` is a momentary thumb-chord layer:
  - hold left middle thumb + right outer thumb = `BT`
- `MOD` keys are hybrid modifiers:
  - tap = sticky mod
  - hold = normal held mod
- `TMX` on `MOD` sends the tmux prefix (`Ctrl+Space`)

## Layer Access

| Layer | Access                  |
| ----- | ----------------------- |
| MOD   | tap `Mod/Ext`           |
| EXT   | hold `Mod/Ext`          |
| SYM   | hold `Bspc/Sym`         |
| NUM   | hold `Space/Num`        |
| MF    | hold both middle thumbs |
| BT    | hold left middle thumb + right outer thumb |

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
| Bottom | `K`   | `P`   | `,/?` | `./!` | `/\`  |

Thumbs

| Left outer | Left middle | Left inner | Right inner | Right middle | Right outer |
| ---------- | ----------- | ---------- | ----------- | ------------ | ----------- |
| `ESC`      | `MOD/EXT`   | `RET`      | `BSP/SYM`   | `SPC/NUM`    | `SHIFT`     |

## MOD (tap `Mod/Ext`)

Left half

| Row    | Col 1    | Col 2     | Col 3   | Col 4   | Col 5   |
| ------ | -------- | --------- | ------- | ------- | ------- |
| Top    | `CMD+[`  | `CTRL+TAB` | `QSWAP` | `CMD+W` | `CMD+Z` |
| Home   | `SHIFT*` | `ALT*`    | `CTRL*` | `CMD*`  | `CMD+R` |
| Bottom | `CMD+]`  | `CMD+X`   | `CMD+A` | `CMD+C` | `CMD+V` |

Right half

| Row    | Col 1 | Col 2  | Col 3 | Col 4 | Col 5 |
| ------ | ----- | ------ | ----- | ----- | ----- |
| Top    |       |        |       |       |       |
| Home   |       | `HYP*` |       |       | `TMX` |
| Bottom |       |        |       |       |       |

## EXT (hold `Mod/Ext`)

Left half

| Row    | Col 1    | Col 2     | Col 3   | Col 4   | Col 5   |
| ------ | -------- | --------- | ------- | ------- | ------- |
| Top    | `CMD+[`  | `TSWAP`    | `SWAP`  | `CMD+W` | `CMD+Z` |
| Home   | `SHIFT†` | `ALT†`    | `CTRL†` | `CMD†`  | `CMD+R` |
| Bottom | `CMD+]`  | `CMD+X`   | `CMD+A` | `CMD+C` | `CMD+V` |

Right half

| Row    | Col 1  | Col 2  | Col 3 | Col 4   | Col 5  |
| ------ | ------ | ------ | ----- | ------- | ------ |
| Top    | `RALT` | `HOME` | `END` |         | `PGUP` |
| Home   | `LEFT` | `DOWN` | `UP`  | `RIGHT` |        |
| Bottom |        | `TAB`  | `DEL` |         | `PGDN` |
                                                
Thumbs

| Left outer | Left middle | Left inner | Right inner | Right middle | Right outer |
| ---------- | ----------- | ---------- | ----------- | ------------ | ----------- |
|            | `EXT`       |            | `DEL`       | `SPC`        |             |

## SYM (hold `Bspc/Sym`)

Left half

| Row    | Col 1   | Col 2 | Col 3  | Col 4 | Col 5 |
| ------ | ------- | ----- | ------ | ----- | ----- |
| Top    |         | `~`   | `@`    | `#`   | `$`   |
| Home   | `SHIFT` | `ALT` | `CTRL` | `CMD` | `HYP` |
| Bottom | `^`     | `&`   | `*`    | `+`   | `\|`  |

Right half

| Row    | Col 1 | Col 2   | Col 3 | Col 4 | Col 5 |
| ------ | ----- | ------- | ----- | ----- | ----- |
| Top    | `=`   | `` ` `` | `:`   | `;`   | `%`   |
| Home   | `-`   | `(`     | `{`   | `[`   | `<`   |
| Bottom | `_`   | `)`     | `}`   | `]`   | `>`   |

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

## BT (hold left middle thumb + right outer thumb)

Left half

| Row    | Col 1    | Col 2      | Col 3      | Col 4   | Col 5    |
| ------ | -------- | ---------- | ---------- | ------- | -------- |
| Top    | `BT CLR` | `OUT USB`  | `OUT BLE`  |         |          |
| Home   | `BT PRV` | `BT 0`     | `BT 1`     | `BT 2`  | `BT NXT` |
| Bottom |          | `BT 3`     | `BT 4`     |         |          |

Right half

| Row    | Col 1 | Col 2 | Col 3 | Col 4 | Col 5 |
| ------ | ----- | ----- | ----- | ----- | ----- |
| Top    |       |       |       |       |       |
| Home   |       |       |       |       |       |
| Bottom |       |       |       |       |       |

## Legend

- `X/Y` = tap `X`, hold `Y`
- `SHIFT*`, `ALT*`, `CTRL*`, `CMD*`, `HYP*` on `MOD`:
  - tap = sticky modifier
  - hold = normal held modifier
- `SHIFT†`, `ALT†`, `CTRL†`, `CMD†` on `EXT`:
  - sticky modifiers (tap to activate, auto-release after next keypress)
  - stackable: tap multiple to combine (e.g., `CMD†` then `SHIFT†` then `F` = Cmd+Shift+F)
- `SWAP` = Cmd+Tab app switcher (tri-state): tap to open the macOS switcher and advance, Cmd stays held across taps, tap `SHIFT†` to cycle backward, release `Mod/Ext` (or press any other key) to commit
- `QSWAP` = instant switch to previous app (Cmd+Tab with immediate release, no switcher UI), same key as `SWAP`
- `TSWAP` = Ctrl+Tab tab switcher (tri-state): holds Ctrl across taps so the browser tab switcher stays up, tap `SHIFT†` to reverse (Ctrl+Shift+Tab), release `Mod/Ext` to commit. Sits beside `SWAP` (tab switching next to app switching)
- `CTRL+TAB` on `MOD` = plain one-shot Ctrl+Tab, same key position as `TSWAP`
- `CMD+[` / `CMD+]` = back / forward, same-column open/close pattern as `SYM` brackets
- `CMD+Z/X/C/V/W` sit on their Graphite letter positions as mnemonics
- `CMD+A` (select all) sits left of `CMD+C` to cluster select/copy/paste for one-handed use, not on its letter position
- `CMD+R` (reload) sits on the home row inner column (R's letter position holds `ALT†`/`ALT*`)
- Left-hand `CMD` shortcuts exist on both layers: tap `Mod/Ext` for a one-shot (`MOD`), hold for repeats and `SWAP` cycling (`EXT`)
- `HYP` = Hyper (`Ctrl+Alt+Cmd+Shift`)
- `TMX` = tmux prefix (`Ctrl+Space`)
- `RALT` = Right Alt (used for VoiceInk speech-to-text)
- `BT 0`-`BT 4` = directly select Bluetooth profile slots 0-4
- `BT CLR` = clear Bluetooth bonds
- `BT NXT` / `BT PRV` = switch Bluetooth profile
- `OUT USB` / `OUT BLE` = explicitly select USB or Bluetooth output
- The right isolated outer key is unused; the left holds `Mouseless` (`BASE`) and `` CMD+` `` (`EXT`/`MOD`)

## Bluetooth Recovery

If Bluetooth stops working after a firmware change:

1. Forget the keyboard in macOS Bluetooth settings.
2. Hold left middle thumb + right outer thumb to reach `BT`.
3. Press `BT CLR`.
4. Use `BT 0`-`BT 4` to jump directly to the host profile you want, or `BT NXT` / `BT PRV` to cycle.
5. If the board is on the wrong output, press `OUT BLE` or `OUT USB`.
6. If that still does not recover it, flash the `settings_reset` UF2 to both halves, then re-flash the normal left/right firmware.

## Combos (EXT layer)

| Keys | Output                 |
| ---- | ---------------------- |
| H+A  | Opt+Left (word left)   |
| A+E  | Opt+Right (word right) |
