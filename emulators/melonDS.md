# melonDS Guide

❗ Follow the [Getting Started section](../README.md#getting-started) of `README.md` first.

This section of the guide explains how to setup [melonDS](https://melonds.kuribo64.net/), a Nintendo DS emulator.

![A screenshot of melonDS running Mario Kart DS](https://user-images.githubusercontent.com/58091943/160287489-6271bf56-2426-4ecb-bb4f-c80b197c1c2c.png)

## Installing melonDS

Open Discover, SteamOS' app store, then search for **melonDS**, then click on it.
![](https://user-images.githubusercontent.com/58091943/160287403-8f61cfe0-a3eb-4677-bfec-6a2ec99681d4.png)

In the top right, select **Sources**, then **Flatpak**, then press **Install**.

Alternatively, open up a terminal and run

```bash
flatpak install --user -y net.kuribo64.melonDS
```

## Configuring melonDS

Open up the emulator, then navigate to **Config > Input and hotkeys**. From here, you can map the controls as you wish. Press OK when you're done.

Navigate to **Config > Video settings**. Set 3D renderer to OpenGL (if it's not already), then under OpenGL renderer, set Internal resolution to 6x native. This will upscale the game to the Steam Deck's resolution.

## Steam ROM Manager

Open Steam ROM Manager, press Parsers, then enter the following settings:

-   Select `Nintendo DS - Retroarch - melonDS` under Community Presets.
    -   Steam ROM Manager doesn't have a preset for non-RetroArch melonDS, so we're going to modify the RetroArch one.
-   You can add additional categories to Steam category using the format `${category name}`, this is case-sensitive.
-   Change configuration title to `Nintendo DS - melonDS` to make it less confusing.
-   Set executable to `/usr/bin/flatpak`.
-   Set command line arguments to `run net.kuribo64.melonDS "${filePath}" -f`
-   Set ROMs directory to wherever your DS ROMs are - if you're using the recommended path, this should be `~/roms/ds`.
-   Press save.

Go to the Preview tab, then press Generate App List. You should see your games populated. You can change the cover art used by hovering over the game and pressing the arrows.

If it looks fine, press Save app list. Load up Steam or switch out of desktop mode, then check your library - you should see your DS games!
