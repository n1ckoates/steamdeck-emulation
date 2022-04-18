# PPSSPP Guide

❗ Follow the [Getting Started section](../README.md#getting-started) of `README.md` first.

This section of the guide explains how to setup [PPSSPP](https://www.ppsspp.org), a PSP emulator.

![A screenshot of PPSSPP's main menu](https://user-images.githubusercontent.com/59558433/163827712-fe70ad3e-b625-4439-96ea-40038c128a00.png)

## Installing PPSSPP

Open Discover, SteamOS' app store, then search for **PPSSPP**. Click on the one labeled "A PlayStation Portable emulator"

In the top right, press **Install**.

Alternatively, open up a terminal and run

```bash
flatpak install --user -y org.ppsspp.PPSSPP
```

## Configuring PPSSPP

Open up the emulator and press **Settings**.

In **Graphics**:
 * select **Vulkan** as a Backend and say *Yes* to restart now, then launch PPSSPP again.
 * Go back in Settings, Graphics, then set **AMD RADV VANGOGH** as a Device.
 * Turn ON **Fullscreen**, **VSync** and set the **Rendering resolution** to **Auto (1:1)**
 * Set **Upscale level** to **2x** and **Upscale type** to **Hybrid + Bicubic**, then check **Deposterize**

Go back and select *Exit*. Launch the emulator one last time and in the **Games** tabs on the main menu, navigate to wherever your PSP ROMs are - if you used the recommended path, this should be `~/roms/psp`.

## Steam ROM Manager

Open Steam ROM Manager, press Parsers, then enter the following settings:

-   Select `Sony PlayStation Portable - PPSSPP (Flatpak)` under Community Presets.
-   You can add additional categories to Steam category using the format `${category name}`, this is case-sensitive.
-   Set executable to `/usr/bin/flatpak`.
-   Set command line arguments to `run org.ppsspp.PPSSPP "${filePath}"`
-   Set ROMs directory to wherever your PSP ROMs are. This is the same location from before.
-   Press save.

Go to the Preview tab, then press Generate App List. You should see your games populated. You can change the cover art used by hovering over the game and pressing the arrows.

If it looks fine, press Save app list. Load up Steam or switch out of desktop mode, then check your library - you should see your PSP games!
