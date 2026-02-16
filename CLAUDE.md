# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

ZMK firmware configuration for the [Totem](https://github.com/GEIGEIGEIST/TOTEM) split keyboard using Seeeduino XIAO BLE controllers. Fork of GEIGEIGEIST/zmk-config-totem.

## Build System

Firmware builds via GitHub Actions on push/PR/manual trigger. No local build needed.

**To build**: Push to GitHub → Actions tab → download firmware artifacts

**Build targets** (defined in `build.yaml`):
- `xiao_ble//zmk` + `totem_left`
- `xiao_ble//zmk` + `totem_right`

**Important**: The `//zmk` board variant suffix is required (ZMK HWMv2 board extensions). Without it, the build produces a stock Zephyr image (~87KB) missing the BLE stack instead of a proper ZMK firmware (~335KB).

Both `config/west.yml` and `.github/workflows/build.yml` track ZMK `main` (unpinned). Upstream ZMK changes can silently break builds. If firmware size drops significantly or BLE stops working, compare artifact sizes across recent builds with `gh api repos/kewah/totem-zmk-config/actions/runs/{id}/artifacts`.

## Troubleshooting BLE

If the keyboard won't connect after a firmware update:
1. Forget device in macOS Bluetooth settings
2. Hit BT_CLR on the keyboard (FUN layer)
3. If still broken: flash `settings_reset` UF2 to both halves, then re-flash normal firmware. Add `settings_reset` shield to `build.yaml` to generate it.

## Key Files

| File | Purpose |
|------|---------|
| `config/totem.keymap` | Keymap: layers, combos, macros, behaviors |
| `config/totem.conf` | Firmware settings |
| `build.yaml` | Build targets |
| `config/boards/shields/totem/totem.dtsi` | Matrix transform, GPIO config |
| `config/boards/shields/totem/*.overlay` | Per-half pin mappings |

## Dev Notes

Working directory is the repo root. No need for `git -C` or `cd` prefixes.

## ZMK References

- [ZMK Keycodes](https://zmk.dev/docs/keymaps/list-of-keycodes)
- [Behaviors](https://zmk.dev/docs/keymaps/behaviors)
- [Combos](https://zmk.dev/docs/keymaps/combos)
