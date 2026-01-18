# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

ZMK firmware configuration for the [Totem](https://github.com/GEIGEIGEIST/TOTEM) split keyboard using Seeeduino XIAO BLE controllers. Fork of GEIGEIGEIST/zmk-config-totem.

## Build System

Firmware builds via GitHub Actions on push/PR/manual trigger. No local build needed.

**To build**: Push to GitHub → Actions tab → download firmware artifacts

**Build targets** (defined in `build.yaml`):
- `seeeduino_xiao_ble` + `totem_left`
- `seeeduino_xiao_ble` + `totem_right`

## Key Files

| File | Purpose |
|------|---------|
| `config/totem.keymap` | Keymap: layers, combos, macros, behaviors |
| `config/totem.conf` | Firmware settings |
| `build.yaml` | Build targets |
| `config/boards/shields/totem/totem.dtsi` | Matrix transform, GPIO config |
| `config/boards/shields/totem/*.overlay` | Per-half pin mappings |

## ZMK References

- [ZMK Keycodes](https://zmk.dev/docs/keymaps/list-of-keycodes)
- [Behaviors](https://zmk.dev/docs/keymaps/behaviors)
- [Combos](https://zmk.dev/docs/keymaps/combos)
