# Totem ZMK Config

Personal ZMK firmware configuration for the [Totem](https://github.com/GEIGEIGEIST/TOTEM) keyboard.

Based on [GEIGEIGEIST/zmk-config-totem](https://github.com/GEIGEIGEIST/zmk-config-totem).

Inspired by [Selenium](https://onedeadkey.github.io/selenium/), [Seniply](https://stevep99.github.io/seniply/), and [Callum](https://github.com/callum-oakley/qmk_firmware/tree/master/users/callum#readme).

## Layout Notes

- Base layer uses Graphite.
- The left isolated outer key holds `Esc/Shift`; the right isolated outer key opens the Omarchy menu (`Super+Space`) on `BASE`.
- The left isolated outer key is `ESC` on `MOD`; it switches to the previous window (`Alt+Shift+Tab`) on `EXT`.
- The layer diagrams document the isolated outer keys separately from the five-column halves.
- `Mod/Ext` is the main layer key:
  - tap = sticky `MOD`
  - hold = `EXT`
- The remaining thumb keys are organized by role:
  - tap the far-left `Esc/Shift` for Escape; hold it for Shift
  - tap `Sym` or `Num` for one sticky layer key; hold for a sequence
  - `Backspace`, `Enter`, and `Space` are dedicated, normally repeatable keys
  - hold `Esc/Shift` and tap `Backspace` for Delete
  - hold `Esc/Shift` and tap `Enter` for Shift+Enter
  - tap or hold `Mod/Ext`, then tap `Enter` for an alternate resting-thumb Shift+Enter chord
- `Backspace` and `Space` keep their base behavior on `MOD` and `EXT`.
- `Delete` is available on the `EXT` comma position.
- `EXT` left half is a one-handed mouse companion: window switching, tab cycling, browser back/forward, close, select all, undo/cut/copy/paste while the right hand stays on the mouse.
- `MF` is a momentary thumb-chord layer:
  - hold both outer layer thumbs (`Sym` + `Num`) = `MF`
- `BT` is a momentary thumb-chord layer:
  - hold `Mod/Ext` + `Num` = `BT`
- `MOD`, `SYM`, and `NUM` home-row modifiers are hybrid modifiers:
  - tap = sticky mod
  - hold = normal held mod
- Sticky `SYM` and `NUM` remain active while modifiers are entered, then release on the shortcut key. For example, tap `NUM`, tap `CTRL*` and `SHIFT*`, then tap `1` for Ctrl+Shift+1.
- `TMX` on `MOD` sends the tmux prefix (`Ctrl+Space`)

### Thumb Placement Philosophy

`Mod/Ext` and `Space` occupy the middle resting positions. `Backspace` and `Enter` mirror each other on the inner thumbs nearest the split, while `Sym` and `Num` mirror each other on the outer thumbs. Backspace, Enter, and Space stay dedicated and repeatable.

## Layer Access

| Layer | Access                                      |
| ----- | ------------------------------------------- |
| MOD   | tap `Mod/Ext`                               |
| EXT   | hold `Mod/Ext`                              |
| SYM   | tap `Sym` for sticky; hold for momentary    |
| NUM   | tap `Num` for sticky; hold for momentary    |
| MF    | hold both outer thumbs (`Sym` + `Num`)       |
| BT    | hold `Mod/Ext` + `Num`                      |

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
| `SYM†`      | `MOD/EXT`  | `BSP/DEL`  | `RET`       | `SPC`        | `NUM†`      |

Isolated outer keys: left `Esc/Shift`, right `Omarchy menu` (`Super+Space`).

## MOD (tap `Mod/Ext`)

Isolated outer keys: left `ESC`, right blank.

Left half

| Row    | Col 1      | Col 2      | Col 3   | Col 4    | Col 5   |
| ------ | ---------- | ---------- | ------- | -------- | ------- |
| Top    | `ALT+LEFT` | `CTRL+TAB` | `QSWAP` | `SUPER+W` | `CTRL+Z` |
| Home   | `SHIFT*`   | `ALT*`     | `CTRL*` | `SUPER*` | `CTRL+R` |
| Bottom | `ALT+RIGHT` | `SUPER+X` | `CTRL+A` | `SUPER+C` | `SUPER+V` |

Right half

| Row    | Col 1 | Col 2  | Col 3 | Col 4 | Col 5 |
| ------ | ----- | ------ | ----- | ----- | ----- |
| Top    |       |        |       |       |       |
| Home   |       |        |       |       | `TMX` |
| Bottom |       |        |       |       |       |

Thumbs

| Left outer | Left middle | Left inner | Right inner | Right middle | Right outer |
| ---------- | ----------- | ---------- | ----------- | ------------ | ----------- |
|            | `MOD`       | `BSP/DEL`  | `SHIFT+RET` | `SPC`        |             |

## EXT (hold `Mod/Ext`)

Isolated outer keys: left `ALT+SHIFT+TAB`, right blank.

Left half

| Row    | Col 1       | Col 2  | Col 3 | Col 4     | Col 5    |
| ------ | ----------- | ------ | ----- | --------- | -------- |
| Top    | `ALT+LEFT`  | `TSWAP` | `SWAP` | `SUPER+W` | `CTRL+Z` |
| Home   | `SHIFT†`    | `ALT†` | `CTRL†` | `SUPER†` | `CTRL+R` |
| Bottom | `ALT+RIGHT` | `SUPER+X` | `CTRL+A` | `SUPER+C` | `SUPER+V` |

Right half

| Row    | Col 1  | Col 2  | Col 3 | Col 4   | Col 5  |
| ------ | ------ | ------ | ----- | ------- | ------ |
| Top    | `F9 PTT` | `HOME` | `END` |         | `PGUP` |
| Home   | `LEFT` | `DOWN` ① | `UP` ①② | `RIGHT` ② | `TMX`  |
| Bottom |        | `TAB`  | `DEL` |         | `PGDN` |

Word-navigation chords (press the marked keys together):

| Chord | Base positions | Output |
| ----- | -------------- | ------ |
| ① `DOWN` + `UP` | `H` + `A` | Ctrl+Left |
| ② `UP` + `RIGHT` | `A` + `E` | Ctrl+Right |

Thumbs

| Left outer | Left middle | Left inner | Right inner | Right middle | Right outer |
| ---------- | ----------- | ---------- | ----------- | ------------ | ----------- |
|            | `EXT`       | `BSP/DEL`  | `SHIFT+RET` | `SPC`        |             |

## SYM (tap `Sym` for sticky; hold for momentary)

Left half

| Row    | Col 1   | Col 2 | Col 3  | Col 4 | Col 5 |
| ------ | ------- | ----- | ------ | ----- | ----- |
| Top    |         | `^`   | `&`    | `\|`  |       |
| Home   | `SHIFT*` | `ALT*` | `CTRL*` | `SUPER*` |       |
| Bottom |         |       |        |       |       |

Right half

| Row    | Col 1  | Col 2 | Col 3 | Col 4 | Col 5 |
| ------ | ------ | ----- | ----- | ----- | ----- |
| Top    | `~`    | `@`   | `` ` `` | `#`   | `$`   |
| Home   | `-`    | `(` ① | `<` ① | `[`   | `:`   |
| Bottom | `_`    | `)` ② | `>` ② | `]`   | `;`   |

Brace chords (press the marked keys together):

| Chord | Output |
| ----- | ------ |
| ① `(` + `<` | `{` |
| ② `)` + `>` | `}` |

Thumbs

| Left outer | Left middle | Left inner | Right inner | Right middle | Right outer |
| ---------- | ----------- | ---------- | ----------- | ------------ | ----------- |
| `SYM`      |             | `BSP/DEL`  | `RET`       | `SPC`        | `NUM†`      |

## NUM (tap `Num` for sticky; hold for momentary)

Left half

| Row    | Col 1 | Col 2 | Col 3 | Col 4 | Col 5 |
| ------ | ----- | ----- | ----- | ----- | ----- |
| Top    | `/`   | `7`   | `8`   | `9`   | `%`   |
| Home   | `-`   | `1`   | `2`   | `3`   | `+`   |
| Bottom | `:`   | `4`   | `5`   | `6`   | `*`   |

Right half

| Row    | Col 1 | Col 2 | Col 3  | Col 4 | Col 5   |
| ------ | ----- | ----- | ------ | ----- | ------- |
| Top    |       |       |        |       |         |
| Home   |        | `SUPER*` | `CTRL*` | `ALT*` | `SHIFT*` |
| Bottom |       |       |        |       |         |

Thumbs (left hand)

| Left outer | Left middle | Left inner |
| ---------- | ----------- | ---------- |
| `.`        | `0`         | `=`        |

The right outer thumb holds the `NUM` trigger, so right-hand thumb positions are omitted.

## MF (hold both outer layer thumbs: `Sym` + `Num`)

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

## BT (hold `Mod/Ext` + `Num`)

Left half

| Row    | Col 1    | Col 2      | Col 3      | Col 4   | Col 5    |
| ------ | -------- | ---------- | ---------- | ------- | -------- |
| Top    | `BT CLR ALL` | `OUT USB`  | `OUT BLE`  |         |          |
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
- `SYM†`, `NUM†` = tap for a sticky one-key layer, hold for a momentary layer
- `BSP/DEL` sends Backspace normally and Delete while either Shift is active.
- `SHIFT+RET` on `MOD` and `EXT` provides the alternate resting-thumb Shift+Enter chord.
- `DEL` is on the `EXT` comma position.
- `SHIFT*`, `ALT*`, `CTRL*`, and `SUPER*` on `MOD`:
  - tap = sticky modifier
  - hold = normal held modifier
- `SHIFT*`, `ALT*`, `CTRL*`, and `SUPER*` on `SYM` and `NUM` use the same tap/hold behavior as `MOD`. On the right-hand `NUM` layer they are mirrored as `SUPER`, `CTRL`, `ALT`, `SHIFT` from the inner usable column outward.
- `SHIFT†`, `ALT†`, `CTRL†`, `SUPER†` on `EXT`:
  - sticky modifiers (tap to activate, auto-release after next keypress)
  - stackable: tap multiple to combine (e.g., `SUPER†` then `SHIFT†` then `F` = Super+Shift+F)
- `SWAP` = Alt+Tab window switcher (tri-state): tap to advance, Alt stays held across taps, tap `SHIFT†` to cycle backward, release `Mod/Ext` (or press any other key) to commit
- `QSWAP` = instant switch to the previous window (Alt+Tab with immediate release), same key as `SWAP`
- `TSWAP` = Ctrl+Tab tab switcher (tri-state): holds Ctrl across taps so the browser tab switcher stays up, tap `SHIFT†` to reverse (Ctrl+Shift+Tab), release `Mod/Ext` to commit. Sits beside `SWAP` (tab switching next to window switching)
- `CTRL+TAB` on `MOD` = plain one-shot Ctrl+Tab, same key position as `TSWAP`
- `ALT+LEFT` / `ALT+RIGHT` = browser/file-manager back and forward
- `CTRL+Z/A/R` use standard Linux application shortcuts for undo, select all, and reload
- `SUPER+X/C/V` use Omarchy's universal clipboard shortcuts, including terminal-safe behavior
- `SUPER+W` closes the active Hyprland window
- Left-hand editing shortcuts exist on both layers: tap `Mod/Ext` for a one-shot (`MOD`), or hold it for repeats and `SWAP` cycling (`EXT`)
- `TMX` = tmux prefix (`Ctrl+Space`), available on both `MOD` and `EXT`
- `F9 PTT` = hold-to-talk Voxtype dictation through the Omarchy F9 press/release bindings
- `BT 0`-`BT 4` = directly select Bluetooth profile slots 0-4
- `BT CLR ALL` = clear Bluetooth bonds from all five profiles
- `BT NXT` / `BT PRV` = switch Bluetooth profile
- `OUT USB` / `OUT BLE` = explicitly select USB or Bluetooth output
- The isolated outer keys hold `Esc/Shift` on the left and the Omarchy menu on the right on `BASE`; the left becomes `ESC` on `MOD` and previous-window on `EXT`.

## Bluetooth Recovery

If Bluetooth stops working after a firmware change:

1. Remove the keyboard from Omarchy's Bluetooth settings.
2. Hold `Mod/Ext` + `Num` to reach `BT`.
3. Press `BT CLR ALL`.
4. Use `BT 0`-`BT 4` to jump directly to the host profile you want, or `BT NXT` / `BT PRV` to cycle.
5. If the board is on the wrong output, press `OUT BLE` or `OUT USB`.
6. If that still does not recover it, flash the `settings_reset` UF2 to both halves, then re-flash the normal left/right firmware.

## Combos

| Layer | Keys      | Output                 |
| ----- | --------- | ---------------------- |
| EXT   | `H` + `A` | Ctrl+Left (word left)   |
| EXT   | `A` + `E` | Ctrl+Right (word right) |
| SYM   | `(` + `<` | `{`                    |
| SYM   | `)` + `>` | `}`                    |
