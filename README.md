# Awesome Nintendo Switch Homebrew

A curated collection of awesome things related to Nintendo Switch hacking and homebrew.

> **Note:** All retail products will link to the manufacturer's site when possible. The products may not be available for purchase at that site.
Please perform due diligence when purchasing console modding products online.

**Last Updated**: February 3, 2021

## Contents

- [Documentation](#documentation)
  - [Guides](#guides)
  - [Forums](#forums)
- [Hardware](#hardware)
  - [Payload Injectors](#payload-injectors)
  - [Modchips](#modchips)
- [System Software](#system-software)
  - [Bootloaders](#bootloaders)
  - [Payloads](#payloads)
  - [Custom Firmware](#custom-firmware)
  - [Signature Patches](#signature-patches)
  - [Operating Systems](#operating-systems)
- [Homebrew](#homebrew)
  - [Utilities](#utilities)
  - [System Modules](#system-modules)
  - [Tesla Overlays](#tesla-overlays)
  - [Games](#games)
  - [Emulation](#emulation)
  - [Media and Streaming](#media-and-streaming)

## Documentation

### Guides

- [Nintendo Homebrew Switch Guide](https://nh-server.github.io/switch-guide/) - Excellent getting started guide to Nintendo Switch hacking, maintained by Nintendo Homebrew Discord Server
- [Sending a Payload](https://nh-server.github.io/switch-guide/user_guide/sysnand/sending_payload/) - Overview of various methods of sending payloads to the Switch
- [SAMD21 Modchip Install Guide](https://gbatemp.net/threads/internal-modchip-samd21-trinket-m0-gemma-m0-itsybitsy-m0-express-guide-files-support.508068/) - Install guide for Trinket M0, Rebug SwitchME M0, etc.

### Forums

GBAtemp will contain the most information regarding the current state of Nintendo Switch homebrew and hacking, and will usually be the place to find help setting up or troubleshooting homebrew. The subreddits are a nice place for people who just want to keep up with the latest homebrew releases and information in an easily digestible format.

- [GBAtemp - Nintendo Switch Discussions](https://gbatemp.net/categories/nintendo-switch-discussions.282/)
- [r/SwitchHacks](https://www.reddit.com/r/SwitchHacks/)
- [r/SwitchHaxing](https://www.reddit.com/r/SwitchHaxing/)

## Hardware

### Payload Injectors

Payload injectors allow you to run custom software on unpatched Switches when they are in RCM mode.

- [NS-Atmosphere](http://www.ns-atmosphere.com/en/)
- [RCMloader](https://www.xkit.xyz/rcmloader/), [RCMloader zero](https://www.xkit.xyz/rcmloader-zero/)
- [SX Pro](https://sx.xecuter.com/#prod-sxpro) - Comes with SX OS license

### Modchips

The SAMD21-based microcontroller boards can be purposed as modchips for unpatched Switches only. The SX modchips use a
different method of launching a custom payload and are compatible with all current Nintendo Switch consoles.

- [Trinket M0](https://www.adafruit.com/product/3500), [Gemma M0](https://www.adafruit.com/product/3501), [ItsyBitsy M0 Express](https://www.adafruit.com/product/3727), [Feather M0 Express](https://www.adafruit.com/product/3403) - SAMD21-based microcontroller boards from Adafruit that can be used as modchips in unpatched Switches
- [Rebug SwitchME M0](https://github.com/Aboshi/SwitchME) - An open source SAMD21-based modchip designed for use in unpatched Switches
- [SX Core](https://sx.xecuter.com/#prod-sxcore), [SX Lite](https://sx.xecuter.com/#prod-sxlite) - Modchips by Team Xecuter, comes with SX Pro license

## System Software

### Bootloaders

Bootloaders allow pushing payloads to unpatched Switches when in RCM mode.

- [TegraRcmGUI](https://github.com/eliboa/TegraRcmGUI) - Windows utility to inject payloads in RCM mode
- [NS-USBloader](https://github.com/developersu/ns-usbloader) - Title installer with payload injection functionality
- [Fusee_Suite](https://gbatemp.net/threads/trinket-rebug-others-modchip-software-new-fusee_suite-uf2-packages.553998/) - Firmware for SAMD21-based modchips

### Payloads

Payloads are injected during and override the Switch boot sequence, allowing for custom firmware and other utilities to run.

- [Hekate](https://github.com/CTCaer/hekate) - A GUI based Nintendo Switch Bootloader
- [ArgonNX-SE](https://github.com/Storm21CH/argon-nx) - GUI payload chainloader for Nintendo Swtich
- [fusee-primary](https://github.com/Atmosphere-NX/Atmosphere/releases) - Payload for running Atmosphère
- [Incognito_RCM](https://github.com/jimzrt/Incognito_RCM) - Utility to remove console serial number from sysnand or emunand
- [Lockpick_RCM](https://github.com/shchmue/Lockpick_RCM) - Utility for dumping console encryption keys
- [SX Loader](https://sx.xecuter.rocks/) - Payload for running SX OS custom firmware

### Custom Firmware

Custom firmware modifies and enhances the stock Switch software to allow running homebrew, applying custom themes, etc., with Atmosphère being the most popular and widely supported.

- [Atmosphère](https://github.com/Atmosphere-NX/Atmosphere) - Open source custom firmware for Nintendo Switch
- [DeepSea](https://github.com/Team-Neptune/DeepSea) - Custom firmware package containing Atmosphère and common homebrew modules and utilities
- [SX OS](https://sx.xecuter.rocks/) - Commercial custom firmware for Nintendo Switch

### Signature Patches

> **Note:** It is not recommended to run homebrew from unsigned NSPs, as this can easily lead to a ban from Nintendo. The recommended method of running homebrew in Atmosphere is via title replacement - hold R while launching a legit application, which will launch HBMenu.

Signature patches, a.k.a. sigpatches, allow unsigned code to run on a Switch running custom firmware. While this can allow running pirated software, sigpatches also have a legitimate use for running homebrew NSP packages and using NSP forwarders for convenience. They can be updated using the homebrew apps [AIO Switch Updater](https://github.com/HamletDuFromage/aio-switch-updater) or [Awoo Installer](https://github.com/Huntereb/Awoo-Installer), or manually from the following locations:

- [Sigpatches for Atmosphere (fusee-primary only)](https://github.com/eXhumer/patches/releases)
- [Sigpatches for Atmosphere (Hekate/fss0/fusee-secondary only!)](https://gbatemp.net/threads/sigpatches-for-atmosphere-hekate-fss0-fusee-secondary-only.571543/)

### Operating Systems

These packages allow usage of alternate operating systems on the Switch.

- [L4T Ubuntu](https://gbatemp.net/threads/l4t-ubuntu-a-fully-featured-linux-on-your-switch.537301/) - Ubuntu Linux based on NVIDIA's Linux for Tegra project
- [Lakka](https://lakka-switch.github.io/documentation/) - L4T Ubuntu build focused on emulation using RetroArch as the frontend
- [LineageOS](https://forum.xda-developers.com/nintendo-switch/nintendo-switch-news-guides-discussion--development/rom-switchroot-lineageos-15-1-t3951389) - LineageOS (Android) for Nintendo Switch

## Homebrew

All homebrew listed below is compatible with Atmosphère. Note that a lot of the apps listed below can be installed via the Homebrew App Store.

### Utilities

- [nx-hbmenu](https://github.com/switchbrew/nx-hbmenu) - Nintendo Switch Homebrew Menu, comes bundled with Atmosphère
- [Homebrew App Store](https://github.com/vgmoose/hb-appstore) - GUI for downloading/managing homebrew apps
- [AIO Switch Updater](https://github.com/HamletDuFromage/aio-switch-updater) - A Nintendo Switch homebrew app to download and update custom firmware, sigpatches, official firmware and cheat codes
- [Awoo Installer](https://github.com/Huntereb/Awoo-Installer) - Title installer for Nintendo Switch
- [Checkpoint](https://github.com/FlagBrew/Checkpoint) - Fast and simple homebrew save manager
- [ChoiDujourNX](https://switchtools.sshnuke.net/) - Firmware update utility
- [EdiZon](https://github.com/WerWolv/EdiZon) - A homebrew save management, editing tool and memory trainer
- [Goldleaf](https://github.com/XorTroll/Goldleaf) - Multipurpose homebrew tool (file browser, title installer)
- [nxdumptool](https://github.com/DarkMatterCore/nxdumptool) - Cartridge and eShop title dumping utility
- [NX-Shell](https://github.com/joel16/NX-Shell) - File manager
- [NXThemes Installer](https://github.com/exelix11/SwitchThemeInjector) - Switch theme manager
- [Payload Launcher](https://github.com/suchmememanyskill/Payload_Launcher) - Reboot to payload utility with a nice user interface
- [uLaunch](https://github.com/XorTroll/uLaunch) - Custom, open-source qlaunch (Nintendo Switch HOME menu) replacement/reimplementation

### System Modules

System modules are software that enhance the Switch operating system when using custom firmware.

- [nx-ovlloader](https://github.com/WerWolv/nx-ovlloader) - Host process for loading Tesla overlays
- [sys-clk](https://github.com/retronx-team/sys-clk) - CPU and GPU overclocking system module
- [sys-con](https://github.com/cathery/sys-con) - Nintendo Switch sysmodule that allows support for third-party controllers
- [sys-ftpd-light](https://github.com/cathery/sys-ftpd-light) - FTP server system module
- [sys-tune](https://github.com/HookedBehemoth/sys-tune) - Background audio player for the Nintendo switch
- [MissionControl](https://github.com/ndeadly/MissionControl) - Use controllers from other consoles natively on your Nintendo Switch via Bluetooth

### Tesla Overlays

Tesla is a homebrew which allows custom menus to be displayed over a game, similar to the Quick Settings menu when holding Home.

- [Tesla Menu](https://github.com/WerWolv/Tesla-Menu) - Base overlay required to load child overlays
- [Status Monitor Overlay](https://github.com/masagrator/Status-Monitor-Overlay) - Monitor many stats of Nintendo Switch hardware
- [sys-clk-Overlay](https://github.com/Sun-Research-University/sys-clk-Overlay) - Overlay for managing sys-clk system module settings

### Games

Most homebrew games are ports of open source games or game engines. Game engines will typically require files from the original game, or game packs, for full functionality.

- [DevilutionX](https://github.com/lantus/devilution-nx) - Diablo port for Switch
- [Doom64EX](https://github.com/fgsfdsfgs/Doom64EX) - Doom64EX port for Switch
- [EDuke32](https://github.com/fgsfdsfgs/eduke32) - EDuke32 port for Switch
- [GZDoom](https://github.com/fgsfdsfgs/gzdoom/tree/switch) - 3D-accelerated Doom source port
- [OpenBOR](https://github.com/Cpasjuste/openbor) - OpenBOR engine port for Switch
- [OpenLara](https://github.com/XProger/OpenLara/releases/tag/latest) - Classic Tomb Raider open-source engine (check last update date in release notes)
- [Postal-NX](https://github.com/Sch-LikA/postal-nx) - Postal port for Switch
- [re3-nx](https://github.com/AGraber/re3-nx) - GTA 3 decompilation ported to the Nintendo Switch
- [Sonic 1 & 2 (2013)](https://github.com/heyjoeway/Sonic-1-2-2013-Decompilation) - Port of Sonic 1 & 2 (2013)
- [Sonic CD (2011)](https://github.com/heyjoeway/Sonic-CD-11-Decompilation) - Port of Sonic CD (2011)
- [Sonic 3 A.I.R.](https://s3airswitch.jojudge.com/) - Port of Sonic 3 & Knuckles remaster
- [Taisei Project](https://taisei-project.org/) - Awesome bullet hell shoot'em up

These games only work on firmware up to version 8.1.0 due to a change in the way inputs are handled in firmware 9.0.0 and up.

- [NXQuake2](https://github.com/fgsfdsfgs/nxquake2) - Nintendo Switch port of the Yamagi Quake II client
- [QuakespasmNX](https://github.com/fgsfdsfgs/QuakespasmNX) - Nintendo Switch port of Quakespasm
- [Wolf4SDL-Switch](https://github.com/keeganatorr/Wolf4SDL-Switch) - Enhanced port of Wolfenstein 3D

### Emulation

The emulation performance of the Switch is excellent. RetroArch is a great "one-stop-shop" for most emulation needs. For more
demanding systems like Sony PSP and Nintendo DS, standalone emulators like PPSSPP can have better performance.

- [melonDS](https://github.com/RSDuck/melonDS) - Standalone Nintendo DS emulator
- [RetroArch](https://www.retroarch.com/?page=platforms) - Multi-platform emulation framework
- [PPSSPP](https://www.ppsspp.org/downloads.html) - Standalone PSP emulator
- [pemu (pFBN, pNES, pSNES)](https://github.com/Cpasjuste/pemu) - Suite of standalone emulators by Cpasjuste

### Media and Streaming

- [Chiaki](https://git.sr.ht/~thestr4ng3r/chiaki) - PS4/PS5 remote play client
- [Moonlight-NX](https://github.com/rock88/moonlight-nx) - Game streaming for PCs with NVIDIA graphics cards
- [SKyNX](https://github.com/DevL0rd/SkyNX) - PC game streaming
