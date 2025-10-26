## InputDrivers

`InputDrivers` is a parameter in [preferences.ini](/user-guide/config/preferences). It determines the input drivers the game will use. If nothing is specified, the following defaults will be used:

Windows: ``Para,legacy,minisdl``

macOS: ``portmidi,SDL`` (LTS 4), ``SDL2`` (Alpha V)

Linux: ``SDL`` (LTS 4), ``SDL2`` (Alpha V)

Default value: nothing

## List of input drivers

### Cross-platform

Name | Description
--- | ---
``lxio`` | Dance/ITG and 5 Panel Pump (for LXIO cabinets)[^alphaV]
``minisdl`` | Window handler for cabinets (no keyboard driver!)[^alphaV]
``mk6piuio`` | (mk6) PIUIO for cabinets[^alphaV]
``para`` | For ParaParaParadise PS2/Dreamcast controllers, threaded, supports 2(3) players[^alphaV]
``portmidi`` | Single MIDI threaded device driver for MIDI devices, covers base eDrums, some older DJ controllers, and single instance MIDI devices
``ps3ddr`` | 2p supported threaded Konami PS3/Xbox 360 DDR pad[^alphaV]
``pspad`` | Custom threaded HIDRAW driver for TWINUSB adapters and PS2 pads (needs more testing, but works)[^alphaV]
``Python23IO`` | For P2IO/P3IO cabinets 32bit only on Windows until we find someone to help us make a new 64bit driver
``Reflex`` | Threaded For Reflex pad project
``rtmidi`` | Multi MIDI device driver for all MIDI devices, covers eDrums, DJ controllers, DAW/MIDI fighters with multiple MIDI devices
``SextetStreamFromFile`` | For sextetstream driver from Peter May[^alphaV]
``sdeck`` | Custom threaded HIDAPI Steam Deck input driver[^alphaV]
``SDL`` | SDL input system
``SDL2`` | Legacy pulling input system

### Windows-only

Name | Description
--- | ---
``ddrio`` | DDRIO cabinet threaded driver, thanks to Din[^alphaV]
``DirectInput`` | Rewritten threaded _SM4_ driver for Pre-2006 direct input devices[^alphaV]
``legacy`` | Bugfixed threaded DirectInput driver (old default on SM5.x) 
``mk5piuio`` | Legacy SM3.x driver for (mk5) PIUIO[^alphaV]
``Rtio`` | SM5 backported - DDR Raw Thrills Cabinet Driver, thanks to x0rbl

### Linux-only

Name | Description
--- | ---
``Linux_PIUIO`` | Threaded PIUIO driver which supports kernel/userspace patches - reworked from DJPohly's 2012 contribution[^alphaV]

[^alphaV]: Available since Alpha V
