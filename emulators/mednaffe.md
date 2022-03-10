# Mednaffe guide

 ❗ Follow the [Getting Started section](../README.md#getting-started) of `README.md` first.

This section of the guide explains how to setup [Mednaffe](https://github.com/AmatCoder/mednaffe), a front-end for [Mednafen](https://mednafen.github.io/), a multi-system emulator.

![A screenshot of Mednaffe running Ginga Fukei Densetsu Sapphire](https://user-images.githubusercontent.com/9209426/157373278-adeecff8-726d-414d-a599-5ac4fa143afb.png)

## Installing Mednaffe

Open Discover, SteamOS' app store, then search for **Mednaffe**, then click on it.

![Discover](https://user-images.githubusercontent.com/9209426/157377104-dfa105bb-d82c-401a-bb7d-d5590585c2cc.png)

In the top right, select **Sources**, then **Flatpak**, then press **Install**.

Alternatively, open up a terminal and run

```
flatpak install --user -y com.github.AmatCoder.mednaffe
```

## Configuring Mednaffe

### Issues with sound

Open up the emulator, then navigate to **Global Settings > Sound**. Make sure `Enable sound output` is ticked, and that `Driver` is set to `sdl`, otherwise you won't get any sound. 

### Input mapping

Switch to the **Systems** tab. For each system, you can map various controllers under the **Input** sub-tab. In Desktop mode, you'll need to launch Steam before mapping Steam Deck inputs properly, otherwise it won't be recognized as a controller.

![](https://user-images.githubusercontent.com/9209426/157373743-a198fc69-7eeb-43e4-b091-484ad9dfb1ec.png)

<u>NB</u>: `Input device` refers to the emulated system's controller, not the real one you're using.

### Graphics (optional)

From the same **Systems** tab, you can access a **Graphics** sub-tab for each system, in which I'd recommend making the following changes:

* In **Fullscreen**, set `Stretch to fill screen` to `aspect`, otherwise by default the output will be integer-scaled (to the nearest multiple of 2), so it won't fill your Steam Deck's screen.

* This one is quite personal, but making changes to either the **Scaler/Filter** or **Shader** tabs might suit you, if you're looking for a specific feel. My recommended setting would be `autoipsharper` for `OpenGL shader` in **Shader**, but you might want to tweak and read [Mednafen's documentation](https://mednafen.github.io/documentation/).

### CD BIOS (optional)

You will need to get `syscard3.pce` (BIOS) for PC Engine CD / TurboGrafx-CD emulation and set the correct path in the **Systems > Emulation** tab (`CD BIOS`).

## Steam ROM Manager

Open Steam ROM Manager, press Parsers, then enter the following settings:

* Select `NEC PC Engine/TurboGrafx 16 - Retroarch - Beetle PCE` under Community Presets.
  - Steam ROM Manager doesn't have a preset for non-RetroArch PCE (Mednafen), so we're going to modify the RetroArch one.
- You can add additional categories to Steam category using the format `${category name}`, this is case-sensitive.
- Change configuration title to `NEC PC Engine/TurboGrafx 16 - Mednafen` to make it less confusing.
- Tick `Show advanced options` and untick `Append arguments to executable`.
- Set executable to `/usr/bin/flatpak`.
- Set command line arguments to `run --branch=stable --arch=x86_64 --command=mednafen com.github.AmatCoder.mednaffe "${filepath}"`.
  - <u>NB</u>: `--command=mednafen` is important here, as we're effectively launching the `Mednafen` CLI from within the `Mednaffe` flatpak.
- Set ROMs directory to wherever your PC Engine/TurboGrafx-16 ROMs are - if you're using the recommended path, this should be `~/roms/pce`.
  - If you have `.pce` ROMs, you will need to change User's glob to take those into account, eg: `${title}@(.7z|.7Z|.ccd|.CCD|.chd|.CHD|.cue|.CUE|.iso|.ISO|.pce|.PCE|.zip|.ZIP)`.
  - If you have sub-directories for your ROMs (eg: PC Engine CD ROMs in the `.cue/bin` format), then an appropriate User's glob would be: `${title}/*.@(cue|CUE)`.
- Press save.

![Mednafen parser example](https://user-images.githubusercontent.com/9209426/157376859-9af92e02-ca56-4849-b4b3-8e2610162ff4.png)

Go to the Preview tab, then press Generate App List. You should see your games populated. You can change the cover art used by hovering over the game and pressing the arrows.

If it looks fine, press Save app list. Load up Steam or switch out of desktop mode, then check your library - you should see your PC Engine/TurboGrafx-16 games!

<u>NB</u>: If you have separate ROMs directories for PC Engine CD/TurboGrafx-CD/SuperGrafx games, then repeat the same process with a different parser.
