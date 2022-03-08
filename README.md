<h1 align="center">Steam Deck Emulation Guide</h1>

This guide covers how to install emulators on a Steam Deck, setting up controls, playing games with optimal settings, and integrating them into Steam itself.

**This is an unofficial guide, not affiliated with Valve**. To the best of my knowledge, it's not possible to mess up your Deck from this guide, but I'm not responsible if you do.

### Current Systems Supported

-   [ ] Nintendo Switch (Yuzu)
-   [ ] Wii U (CEMU)
-   [x] Wii (Dolphin)
-   [ ] GameCube (Dolphin)
-   [ ] Nintendo 64 (m64p)
-   [ ] SNES (Snes9x)
-   [ ] NES (FCEUX)
-   [ ] PlayStation 3
-   [ ] PlayStation 2
-   [ ] PlayStation
-   [ ] Xbox

[Open a GitHub issue](https://github.com/nchristopher/steamdeck-emulation/issues/new) if you want support for a different system.

## Getting Started

This guide assumes your ROMs are under `~/roms` (a folder in your home directory), with a file structure like this:

```
roms
├── switch
├── wiiu
├── wii
├── gamecube
├── n64
├── snes
└── nes
```

This guide **does not** cover getting the games themselves.

We're going to use [Steam ROM Manager](https://steamgriddb.github.io/steam-rom-manager/) for this guide. It will automatically download cover art for each ROM, then add a shortcut to Steam for the game. The end result will look like this, with Steam collections for each system:

![](https://cdn.discordapp.com/attachments/809297772850839552/950265581087637554/unknown.png)

Switch to Desktop mode by pressing the **Steam** button, navigating to **Power**, then **Switch to Desktop**.

Go to Steam ROM Manager's [latest release](https://github.com/SteamGridDB/steam-rom-manager/releases/latest), then download the file ending in `.AppImage` that **DOES NOT** contain `i386`. It should be named something like `Steam-ROM-Manager-2.3.29.AppImage`.

Open SteamOS' file manager Dolphin (it's different from the emulator Dolphin), then navigate to wherever you saved the file, probably in **Downloads**. You can run it by just double-tapping the file.

From here, the guide branches off for each system you want to emulate:

-   [GameCube and/or Wii](./emulators/dolphin.md)

## 📜 License

Copyright &copy; 2022 Nicholas Christopher

Unless otherwise stated, this guide is licensed under [Creative Commons BY 4.0](https://creativecommons.org/licenses/by/4.0/).
