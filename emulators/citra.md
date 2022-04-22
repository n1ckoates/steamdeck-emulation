# Citra Guide

❗ Follow the [Getting Started section](../README.md#getting-started) of `README.md` first.

This section of the guide explains how to setup [Citra](https://citra-emu.org/), a Nintendo 3DS emulator.

## Installing Citra

Open Discover, SteamOS' app store, then search for **Citra**, then click on it.

![](https://user-images.githubusercontent.com/58091943/164586807-af85d4be-73f0-48be-bb37-a20783c4708f.png)

In the top right, select **Sources**, then **Flatpak**, then press **Install**.

Alternatively, open up a terminal and run

```bash
flatpak install --user -y org.citra_emu.citra
```

## Configuring Citra

Open up the emulator and navigate to **Emulation > Configure**, then switch to the **Graphics** tab on the sidebar. In the Enhancements tab, set **Internal Resolution** to **3x native**.

Switch to the **Controls** tab on the sidebar, and configure controls as you wish.

To load encrypted games, you'll need to dump some keys from your 3ds, then add them to Citra. You can find [instructions on Citra's website](https://citra-emu.org/wiki/aes-keys/).

## Steam ROM Manager

Open Steam ROM Manager, press Parsers, then enter the following settings:

-   Select `Nintendo 3DS - Citra(Flatpak)` under Community Presets.
-   You can add additional categories to Steam category using the format `${category name}`, this is case-sensitive.
-   Set ROMs directory to wherever your 3DS ROMs are - if you're using the recommended path, this should be `~/roms/3ds`.
-   Press save.

Go to the Preview tab, then press Generate App List. You should see your games populated. You can change the cover art used by hovering over the game and pressing the arrows.

If it looks fine, press Save app list. Load up Steam or switch out of desktop mode, then check your library - you should see your Switch games!
