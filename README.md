<h1 align="center">Steam Deck Emulation Guide</h1>

This guide covers how to install emulators on a Steam Deck, setting up controls, playing games with optimal settings, and integrating them into Steam itself. It uses [Steam ROM Manager](https://steamgriddb.github.io/steam-rom-manager/), which automatically downloads cover art for each game and adds a shortcut to Steam. The end result will look like this, with Steam collections for each system:

![](https://cdn.discordapp.com/attachments/809297772850839552/950265581087637554/unknown.png)

**This is an unofficial guide, not affiliated with Valve**. To the best of my knowledge, it's not possible to mess up your Deck from this guide, but I'm not responsible if you do.

This guide **does not** cover getting ROMs or other copyrighted material.

### Current Systems Supported

-   [x] Nintendo Switch (Yuzu)
-   [ ] Wii U (CEMU)
-   [x] Wii (Dolphin)
-   [x] GameCube (Dolphin)
-   [x] Nintendo 64 (simple64)
-   [x] SNES (Snes9x)
-   [ ] NES (FCEUX)
-   [ ] PlayStation 3 (RPCS3)
-   [x] PlayStation 2 (PCSX2)
-   [ ] PlayStation (DuckStation)
-   [ ] Xbox (Xemu)
-   [x] 3DS (Citra)
-   [ ] DS (melonDS)
-   [ ] GBA (mGBA)
-   [x] PSP (PPSSPP)
-   [x] PC Engine (CD) / TurboGrafx-16 (-CD) / SuperGrafx (Mednaffe)

[Open a GitHub issue](https://github.com/nchristopher/steamdeck-emulation/issues/new) if you want support for a different system.

### Storage

This guide assumes your ROMs are under `~/roms` (a folder in your home directory), with a file structure like this:

```
roms
├── switch
├── wii
├── gamecube
├── n64
├── snes
├── pce
├── ps2
├── 3ds
└── psp
```

---

If you store your roms on an SD card, substitute `~/roms` with `/run/media/mmcblk0p1/roms` in the guide. You'll have to give Flatpaks access to your SD card - open up a terminal and run

```bash
flatpak override <name> --filesystem=/run/media/
```

Substitute `<name>` with the flatpak's name, this should be apparent in the guide. For example, Snes9x's flatpak name is `com.snes9x.Snes9x`, so you'd run

```bash
flatpak override com.snes9x.Snes9x --filesystem=/run/media/
```

## Getting Started

To start off, switch to Desktop mode by pressing the **Steam** button, navigating to **Power**, then **Switch to Desktop**.

Go to Steam ROM Manager's [latest release](https://github.com/SteamGridDB/steam-rom-manager/releases/latest), then download the file ending in `.AppImage` that **DOES NOT** contain `i386`. It should be named something like `Steam-ROM-Manager-2.3.29.AppImage`. If prompted for Steam's directory, enter `/home/deck/.local/share/Steam`.

Open SteamOS' file manager Dolphin (it's different from the emulator Dolphin), then navigate to wherever you saved the file, probably in **Downloads**. You can run it by just double-tapping the file.

From here, the guide branches off for each system you want to emulate:

-   [Nintendo Switch](./emulators/yuzu.md)
-   [GameCube and/or Wii](./emulators/dolphin.md)
-   [Nintendo 64](./emulators/simple64.md)
-   [SNES](./emulators/snes9x.md)
-   [PC Engine (CD) / TurboGrafx-16 (-CD) / SuperGrafx](./emulators/mednaffe.md)
-   [PlayStation 2](./emulators/pcsx2.md)
-   [Nintendo 3DS](./emulators/citra.md)
-   [PlayStation Portable (PSP)](./emulators/ppsspp.md)

## ❓ Support

If you have any trouble with the guide, feel free to [open a GitHub discussion](https://github.com/nchristopher/steamdeck-emulation/discussions/new) or visit the `#emulation` channel on the [Steam Deck Discord](https://discord.gg/myS7JkUtvA).

## 📜 License

Copyright &copy; 2022 Nicholas Christopher

Unless otherwise stated, this guide is licensed under [Creative Commons BY 4.0](https://creativecommons.org/licenses/by/4.0/).
