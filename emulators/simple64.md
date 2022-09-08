# simple64 Guide

❗ Follow the [Getting Started section](../README.md#getting-started) of `README.md` first.

This section of the guide explains how to setup [simple64](https://simple64.github.io/), a Nintendo 64 emulator. The emulator is based on [simple64-gui](https://github.com/simple64/simple64-gui), which itself is a frontend for [mupen64plus](https://mupen64plus.orgsimple64-gui
![A screenshot of simple64 running The Legend of Zelda: Ocarina of Time](https://user-images.githubusercontent.com/58091943/189030050-dc3aeb03-9d46-45f4-a7ee-b3413b962964.png)

## Installing simple64

Open Discover, SteamOS' app store, then search for **simple64**, then click on it.
![](https://user-images.githubusercontent.com/58091943/189030159-ed013e4e-c9eb-44a6-9318-d07521c5acd6.png)

In the top right, select **Sources**, then **Flatpak**, then press **Install**.

Alternatively, open up a terminal and run

```bash
flatpak install --user -y io.github.simple64.simple64
```

## Configuring simple64

Open up the emulator and navigate to **Settings > Core and Video Settings**, then switch to the ParaLLel Video tab. Enable Fullscreen, then set Upscaling to `4`, then exit out of this menu.

Go to **Settings > Controller Configuration**. Under Controller 1, set Gamepad to Auto. Switch to the Manage Profiles tab, then press "New Profile (Gamepad). From here, you can map the controls as you wish.

![](https://user-images.githubusercontent.com/58091943/157165447-b4b2bf7d-e2ee-42b2-b2e7-17eefbc9defc.png)

## Steam ROM Manager

Open Steam ROM Manager, press Parsers, then enter the following settings:

-   Select `Nintendo 64 - Mupen64Plus` under Community Presets.
-   You can add additional categories to Steam category using the format `${category name}`, this is case-sensitive.
-   Set executable to `/usr/bin/flatpak`.
-   Set command line arguments to `run io.github.simple64.simple64 "${filePath}"`
-   Set ROMs directory to wherever your N64 ROMs are - if you're using the recommended path, this should be `~/roms/n64`.
-   Press save.

Go to the Preview tab, then press Generate App List. You should see your games populated. You can change the cover art used by hovering over the game and pressing the arrows.

If it looks fine, press Save app list. Load up Steam or switch out of desktop mode, then check your library - you should see your N64 games!
