## Configuring PCSX2
Open Config -> General Settings, then make sure to enable MTVU under the microVU Hacks section in the Speedhacks menu.
Open GS Window in General Settings, then change the aspect ratio to "Fit to Window/Screen"
Apply and close General Settings

OpenConfig -> Graphics Settings, Set the following:
  Internal Resolution: 2x Native
  CRC Hack Level: Aggressive
  
Open the Hacks tab, and set the following:
  Manual HW Hacks: toggle ON
  Fast Texture Invalidation: toggle ON
  
Open Advanced settings, and set the following:
  Precache Textures: toggle ON

## Steam ROM Manager

Open Steam ROM Manager, press Parsers, then enter the following settings:

-   Select `Sony Playstation 2 - PCSX2` under Community Presets.
-   You can add additional categories to Steam category using the format `${category name}`, this is case-sensitive. Example: ${Playstation 2}
-   Set executable to `/usr/bin/flatpak`.
-   Set command line arguments to `run net.pcsx2.PCSX2 "${filepath}" --nogui --fullscreen`
-   Set ROMs directory to wherever your PS2 ROMs are. This is the same location from before.
-   Press save.

Go to the Preview tab, then press Generate App List. You should see your games populated. You can change the cover art used by hovering over the game and pressing the arrows.

If it looks fine, press Save app list. Load up Steam or switch out of desktop mode, then check your library - you should see your PS2 games!
