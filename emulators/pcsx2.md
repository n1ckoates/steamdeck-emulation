# PCSX2 Guide

❗ Follow the [Getting Started section](../README.md#getting-started) of `README.md` first.

This section of the guide explains how to setup [PCSX2](https://pcsx2.net/), a PlayStation 2 emulator.

## Installing PCSX2

Open Discover, SteamOS' app store, then search for **PCSX2**, then click on it.

![](https://user-images.githubusercontent.com/58091943/159169454-555ab88e-5bce-4e29-b27d-f18192931e56.png)

In the top right, select **Sources**, then **Flatpak**, then press **Install**.

Alternatively, open up a terminal and run

```bash
flatpak install --user -y net.pcsx2.PCSX2
```

## Configuring PCSX2

Open up the emulator, then navigate through the initial setup. You'll have to provide your own PS2 BIOS file.

Navigate to **Config > General Settings**, then in the Speedhacks menu, enable MTVU under the microVU Hacks section.

Open GS Window in General Settings, then change the aspect ratio to "Fit to Window/Screen", then apply & close general settings.

Navigate to **Config > Graphics Settings**, then set the following:

-   Internal Resolution: 2x Native
-   CRC Hack Level: Aggressive

Open the Hacks tab, then set the following:

-   Manual HW Hacks: toggle ON
-   Fast Texture Invalidation: toggle ON

Open Advanced settings, then set the following:

-   Precache Textures: toggle ON

## Steam ROM Manager

Open Steam ROM Manager, press Parsers, then enter the following settings:

-   Select `Sony Playstation 2 - PCSX2` under Community Presets.
-   You can add additional categories to Steam category using the format `${category name}`, this is case-sensitive.
-   Set executable to `/usr/bin/flatpak`.
-   Set command line arguments to `run net.pcsx2.PCSX2 "${filepath}" --nogui --fullscreen`
-   Set ROMs directory to wherever your PS2 ROMs are - if you're using the recommended path, this should be `~/roms/ps2`.
-   Press save.

Go to the Preview tab, then press Generate App List. You should see your games populated. You can change the cover art used by hovering over the game and pressing the arrows.

If it looks fine, press Save app list. Load up Steam or switch out of desktop mode, then check your library - you should see your PS2 games!
