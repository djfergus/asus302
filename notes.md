# ASUS C302 Chromebook - Omarchy Linux Configuration Notes

## System Info

| Component | Details |
|-----------|---------|
| **Device** | ASUS Chromebook Flip C302 |
| **CPU** | Intel Core m3-6Y30 @ 0.90GHz |
| **RAM** | 3.7 GB |
| **Storage** | 58.2 GB eMMC (encrypted root) |
| **Display** | 1920x1080 @ 60Hz (eDP-1, 280x160mm) |
| **OS** | Omarchy Linux (Arch-based) v3.4.1 |
| **WM** | Hyprland |
| **Theme** | Tokyo Night |
| **Font** | JetBrainsMono Nerd Font |
| **Swap** | 4 GB zram |

## Changes Log

### 1. Chromebook Function Key Remapping (2026-04-04)

**File:** `~/.config/hypr/bindings.conf` (backup created with timestamp)

Remapped the top row F1-F10 keys to match the icons printed on the Chromebook keyboard:

| Key | Function | Implementation |
|-----|----------|---------------|
| F1 | ← Back | Sends ALT+Left to active window |
| F2 | → Forward | Sends ALT+Right to active window |
| F3 | ↻ Refresh | Sends CTRL+R to active window |
| F4 | ⛶ Fullscreen | Hyprland fullscreen toggle |
| F5 | ▦ Overview | Walker window switcher |
| F6 | 🔅 Brightness- | `omarchy-brightness-display 5%-` |
| F7 | 🔆 Brightness+ | `omarchy-brightness-display +5%` |
| F8 | 🔇 Mute | Volume mute toggle (SwayOSD) |
| F9 | 🔉 Vol- | Volume down (SwayOSD) |
| F10 | 🔊 Vol+ | Volume up (SwayOSD) |

**SUPER + F1-F10** sends the original F-key to the active window via `sendshortcut`.

Volume keys (F8-F10) use `bindeld`/`bindeld` for key-repeat support on hold.
