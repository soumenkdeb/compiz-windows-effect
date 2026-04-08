# Compiz windows effect for GNOME Shell

Compiz wobbly windows effect with compiz plugin engine.

[<img src="assets/screenshot.png" width="100%">](https://extensions.gnome.org/extension/3210/compiz-windows-effect)

## Supported GNOME Shell Versions

GNOME Shell 45, 46, 47, 48, 49, and 50.

## Prerequisite

Does NOT require any external library.

## Installation

### From GNOME Extensions Website

You can install this extension by visiting [the GNOME Shell Extensions page](https://extensions.gnome.org/extension/3210/compiz-windows-effect) for this extension.

[<img src="assets/get-it-on-ego.png" height="100">](https://extensions.gnome.org/extension/3210/compiz-windows-effect)

### Manual Installation (from source)

1. Clone this repository:
   ```bash
   git clone https://github.com/hermes83/compiz-windows-effect.git
   ```

2. Copy the extension to the GNOME Shell extensions directory:
   ```bash
   cp -r compiz-windows-effect ~/.local/share/gnome-shell/extensions/compiz-windows-effect@hermes83.github.com
   ```

3. Compile the GSettings schema:
   ```bash
   glib-compile-schemas ~/.local/share/gnome-shell/extensions/compiz-windows-effect@hermes83.github.com/schemas/
   ```

4. Restart GNOME Shell:
   - On X11: press `Alt+F2`, type `r`, and press `Enter`
   - On Wayland: log out and log back in

5. Enable the extension using GNOME Extensions app or run:
   ```bash
   gnome-extensions enable compiz-windows-effect@hermes83.github.com
   ```

## Changes

### Version 30 — GNOME 5.0 (Shell 50) support

- Added GNOME Shell 50 to the supported versions list.
- Fixed a version comparison bug: `Config.PACKAGE_VERSION` is a string, so it now uses `parseFloat()` before comparing against the numeric threshold (49) that determines which `get_maximize_flags()` API to call. Without this fix the string comparison would produce incorrect results on two-digit version numbers.

## Video

You can see extension in action in this [video](https://youtu.be/G8bAVIB9A7A)