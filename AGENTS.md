# ASUS C302 Chromebook Configuration Project

This project manages the configuration of an ASUS Chromebook Flip C302 running Omarchy Linux (Arch-based) with Hyprland.

## Rules

1. **Document everything.** Every change must be logged in `notes.md` with a numbered heading, date, file(s) modified, and a description of what was done and why.
2. **Back up before editing.** Before modifying any config file, create a timestamped backup (e.g. `cp file file.bak.$(date +%s)`).
3. **Read `notes.md` first.** Before making changes, read the notes file to understand what has already been configured and avoid conflicts or regressions.
4. **Use the omarchy skill.** This system runs Omarchy Linux. Load and follow the omarchy skill for any desktop/WM/system configuration tasks. Never edit files in `~/.local/share/omarchy/` — only `~/.config/`.
5. **Respect the hardware.** This is a low-power machine (m3-6Y30, 3.7 GB RAM, 58 GB eMMC). Prefer lightweight solutions. Avoid heavy animations, blur, or resource-intensive settings.
6. **Test changes.** After editing Hyprland configs, verify with `hyprctl reload`. For Waybar, run `omarchy-restart-waybar`. Check the notes for component-specific reload commands.
7. **Chromebook keyboard.** The top row keys are F1-F10 but have been remapped to their printed Chromebook functions (back, forward, refresh, fullscreen, overview, brightness, volume). SUPER+F-key sends the actual F-key. See notes entry #1 for details.

## Key Files

| File | Purpose |
|------|---------|
| `notes.md` | Change log — **all modifications documented here** |
| `~/.config/hypr/bindings.conf` | Custom keybindings (Chromebook fn keys + app launchers) |
| `~/.config/hypr/input.conf` | Keyboard/touchpad settings |
| `~/.config/hypr/looknfeel.conf` | Appearance (gaps, borders, animations) |
| `~/.config/hypr/monitors.conf` | Display configuration |
| `~/.config/hypr/autostart.conf` | Startup applications |
| `~/.config/hypr/hyprland.conf` | Main config (sources defaults + user overrides) |
| `~/.config/waybar/` | Status bar config and styling |

## System Quick Reference

- **OS:** Omarchy Linux v3.4.1 (Arch-based)
- **WM:** Hyprland 0.54.0
- **Display:** 1920x1080 @ 60Hz, 12.5" (eDP-1)
- **CPU:** Intel m3-6Y30 (dual-core, low power)
- **RAM:** 3.7 GB
- **Storage:** 58 GB eMMC (encrypted)
- **Theme:** Tokyo Night
- **Font:** JetBrainsMono Nerd Font
