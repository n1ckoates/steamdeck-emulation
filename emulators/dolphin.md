# Dolphin Guide

❗ Follow the [Getting Started section](../README.md#getting-started) of `README.md` first.

This section of the guide explains how to setup [Dolphin](https://dolphin-emu.org), a Wii and GameCube emulator.

![A screenshot of Dolphin's main user interface](https://user-images.githubusercontent.com/58091943/157139724-46e11a1b-b47b-4b38-9e17-ae2ebb3b79b8.png)

## Installing Dolphin

Open Discover, SteamOS' app store, then search for **Dolphin**. Click on the one labeled "A Wii/Gamecube Emulator."

![](https://user-images.githubusercontent.com/58091943/157140225-6284c97e-eab2-4c5d-bf0a-7000465b56e2.png)

In the top right, select **Sources**, then **Flatpak**, then press **Install**.

Alternatively, open up a terminal and run

```bash
flatpak install --user -y org.DolphinEmu.dolphin-emu
```

## Configuring Dolphin

Open up the emulator and press **Config**, then the **Paths** tab. Press Add, then navigate to wherever your Wii ROMs are - if you used the recommended path, this should be `~/roms/wii`.

Press Add again, this time navigating to your GameCube roms - this should be `~/roms/gamecube`.

Press Close; your games should appear in Dolphin now.

Press **Graphics**, then change Backend to Vulkan. Switch to the Enhancements tab, then change Internal Resolution to 3x Native. This will upscale titles to 1080p from the base 480p. Press Close.

Press **Controllers**. You can configure this as you wish, but most people will want to:

-   Select Standard Controller for Port 1 under GameCube Controllers.
    -   Press Configure, then bind the buttons to your preference. Save your setup as a profile.
-   Select Emulate the Wii's Bluetooth adapter under Wii Controllers.
    -   Press Configure, then bind the buttons to your preference. Some games require extensions, and some games map better to the Deck's controller with an extension (eg. Mario Kart Wii works best mapped to a Classic Controller.)

Press Close, then Close again. At this point, you can load a game to test it.

Most games should work fine out-of-the-box, but for some, you might want to configure them more. Refer to the [Dolphin wiki](https://wiki.dolphin-emu.org/index.php?title=Main_Page) for more information.

## Steam ROM Manager

Open Steam ROM Manager, press Parsers, then enter the following settings:

-   Select `Nintendo Wii - Dolphin` under Community Presets.
-   You can add additional categories to Steam category using the format `${category name}`, this is case-sensitive.
-   Set executable to `/usr/bin/flatpak`.
-   Set command line arguments to `run org.DolphinEmu.dolphin-emu -b -e "${filePath}"`
-   Set ROMs directory to wherever your Wii ROMs are. This is the same location from before.
-   Press save.

Do the same thing again, but select `Nintendo GameCube - Dolphin` instead for Community Presets, and change your ROMs directory to your GameCube one.

Go to the Preview tab, then press Generate App List. You should see your games populated. You can change the cover art used by hovering over the game and pressing the arrows.

If it looks fine, press Save app list. Load up Steam or switch out of desktop mode, then check your library - you should see your Wii and GameCube games!
