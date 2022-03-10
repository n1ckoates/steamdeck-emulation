# Snes9x Guide

❗ Follow the [Getting Started section](../README.md#getting-started) of `README.md` first.

This section of the guide explains how to setup [Snes9x](https://snes9x.com), a Super NES/Super Famicom emulator.

![A screenshot of Snes9x running Super Mario World](https://user-images.githubusercontent.com/58091943/157359764-4c9ff6e3-0d3d-4e55-9e8a-448b239383ec.png)

## Installing Snes9x

Open Discover, SteamOS' app store, then search for **Snes9x**, then click on it.

![](https://user-images.githubusercontent.com/58091943/157359926-70aaffd0-37da-4c9a-9913-56c5a615f000.png)

In the top right, select **Sources**, then **Flatpak**, then press **Install**.

Alternatively, open up a terminal and run

```bash
flatpak install --user -y com.snes9x.Snes9x
```

## Configuring Snes9x

Open up the emulator, then navigate to **Options > Preferences**. Switch to the Joypads tab and map the controller as you wish. You can also map hotkeys in the Shortcuts tab. You can configure any other options as you wish. If you want Full Screen set that in the **Options > Display**

## Steam ROM Manager

Open Steam ROM Manager, press Parsers, then enter the following settings:

-   Select `Nintendo SNES - Retroarch - Snes9x` under Community Presets.
    -   Steam ROM Manager doesn't have a preset for non-RetroArch Snes9x, so we're going to modify the RetroArch one.
-   You can add additional categories to Steam category using the format `${category name}`, this is case-sensitive.
-   Change configuration title to `Nintendo SNES - Snes9x` to make it less confusing.
-   Set executable to `/usr/bin/flatpak`.
-   Set command line arguments to `run com.snes9x.Snes9x "${filePath}"`
-   Set ROMs directory to wherever your SNES ROMs are - if you're using the recommended path, this should be `~/roms/snes`.
-   Press save.

Go to the Preview tab, then press Generate App List. You should see your games populated. You can change the cover art used by hovering over the game and pressing the arrows.

If it looks fine, press Save app list. Load up Steam or switch out of desktop mode, then check your library - you should see your SNES games!
