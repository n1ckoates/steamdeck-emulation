# Yuzu Guide

❗ Follow the [Getting Started section](../README.md#getting-started) of `README.md` first.

This section of the guide explains how to setup [Yuzu](https://yuzu-emu.org/), a Nintendo Switch emulator.

![A screenshot of Yuzu's main user interface](https://user-images.githubusercontent.com/58091943/157156779-02f24ec9-1f14-4dfb-97b1-c7939c806f0b.png)

## Installing Yuzu

Open Discover, SteamOS' app store, then search for **Yuzu**, then click on it.

![](https://user-images.githubusercontent.com/58091943/157156930-854f93d8-6eb6-4f2f-a408-4ccea50f67cd.png)

In the top right, select **Sources**, then **Flatpak**, then press **Install**.

Alternatively, open up a terminal and run

```bash
flatpak install --user -y org.yuzu_emu.yuzu
```

## Configuring Yuzu

You'll need to dump your keys from your Switch before proceeding. This is out of scope for this guide, but Yuzu has [a guide for it](https://yuzu-emu.org/help/quickstart/#yuzu-quickstart-guide). Once you have `prod.keys` and `title.keys`, go to **File > Open Yuzu folder**. In the directory opened, create a folder named `keys`, then place the two files there.

Back in Yuzu, press **Add New Game Directory**. Navigate to wherever your Switch ROMs are - if you used the recommended path, this should be `~/roms/switch`. Your games should appear in Yuzu now.

Go to **Emulation > Configure**, then **Controls**. You can map your Deck's controller to a Switch controller as you wish.

## Steam ROM Manager

Open Steam ROM Manager, press Parsers, then enter the following settings:

-   Select `Nintendo Switch - Yuzu` under Community Presets.
-   Set Steam category to `${Switch}`. You can add additional categories by using the format `${category name}`, this is case-sensitive.
-   Set executable to `/usr/bin/flatpak`.
-   Set command line arguments to `run org.yuzu_emu.yuzu -f -g "${filePath}"`
-   Set ROMs directory to wherever your Switch ROMs are. This is the same location from before.
-   Press save.

Go to the Preview tab, then press Generate App List. You should see your games populated. You can change the cover art used by hovering over the game and pressing the arrows.

If it looks fine, press Save app list. Load up Steam or switch out of desktop mode, then check your library - you should see your Switch games!
