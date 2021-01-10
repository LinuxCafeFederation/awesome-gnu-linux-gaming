# Awesome GNU/Linux gaming [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of awesome GNU/Linux tips & tricks, games, tools, and resources. Inspired by [awesome-vulkan](https://github.com/vinjn/awesome-vulkan) and other awesome-related projects.


## Overview

This is a hobby project to improve the quality of gaming in Linux because it is possible to improve performance by tweaking your Linux machine. Most Linux distributions have a lot of issues when it comes to gaming performance, as they do not utilise the modern and superior counterparts.


## Table of contents

- [Distributions](#distributions)
- [Utilities](#utilities)
- [Processors](#processors)
	- [AMD](#amd)
	- [Intel](#intel)
- [Graphics cards](#graphics-cards)
	- [AMD](#amd-1)
	- [Nvidia](#nvidia)
- [Platforms](#platforms)
- [Kernels](#kernels)
- [WINE](#wine)
- [Emulators](#emulators)
- [Development](#development)
- [YouTube channels](#youtube-channels)
- [Q&As](#qas)
- [Future plans](#future-plans)
- [Contributing](#contributing)
- [Special thanks](#special-thanks)


## Distributions

### Beginner

#### [**Pop!_OS**](https://system76.com/pop) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Based on [Ubuntu](https://ubuntu.com/). Attempt from System76 to "de-Canonical-ise" Ubuntu, as well as some minor tweaks for gaming.
- Full ootb support for Nvidia and AMD GPUs.
- Better power management built-in.
- All common gaming related applications are in Pop Shop, making it trivial to install everything needed to start gaming.
- 64 bit Vulkan drivers are pre-installed, but Steam installation is modified to include them too just in case.
- No snaps pre-installed and Pop!_Shop gives an option between .deb and flatpak for many applications.

#### [**Fedora**](https://getfedora.org/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Community maintained distribution to provide the [upstream](https://en.wikipedia.org/wiki/Upstream_(software_development)) kernel in correlation with stable packages. Comes with performance tools pre-installed such as [gamemode](https://github.com/FeralInteractive/gamemode).
- Built on bleeding edge/stable model, provides a very stable experience while staying fairly up-to-date on software.
- In other words, when installing drivers and libraries, you get more recent versions compared to some other distros.
- When installing [Steam](#steam), [GameMode](#gamemode) will be installed as well, to improve performance.

#### [**openSUSE Leap**](https://www.opensuse.org/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
- A step above SuSe Enterprise Linux which means it is stable.


### Moderate

#### [**Arch Linux**](https://www.archlinux.org/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Lightweight and independent distribution to provide as much performance with as less time spent.
- Higher maintainance than Beginner distros, but comes with less pre-installed.
- This provides a cleaner base, letting the user focus on installing only what they need. 
- This can aid lower-end systems. 

#### [**openSUSE Tumbleweed**](https://www.opensuse.org/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)

- Rolling distro with [openQA](http://open.qa/)
- Less likely to break than Arch due to testing
- Great Nvidia support

### Advanced

#### [**Gentoo**](https://www.gentoo.org/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Minimal and secure source based distribution to maximise performance.
- High potential for increased stability and reduced latency of the system thanks to building everything from source and in turn adapting to user's hardware and needs per program basis.
- Users with lower-end hardware may experience higher FPS in games as a result of said optimisations of the system, however this is not guaranteed and will depend highly on the hardware used. 


## Utilities

#### [**GameMode**](https://github.com/FeralInteractive/gamemode) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
A **systemd** daemon/lib to optimise Linux system performance on demand. — **WARNING: this utility will not work in the distributions listed in the following website: [Wikipedia: Linux distributions without systemd](https://en.wikipedia.org/wiki/Category:Linux_distributions_without_systemd).** — [Video](https://www.youtube.com/watch?v=zN8by3wchVw&t=35s)

#### [**CoreCtrl**](https://gitlab.com/corectrl/corectrl) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Overclocking software with the aesthetics based on AMD's Radeon Software Adrenalin from 2018.

#### [**QMK**](https://qmk.fm/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Keyboard firmware to customize key switches. Based on the [tmk_keyboard firmware](https://github.com/tmk/tmk_keyboard). — [Video](https://www.youtube.com/watch?v=-imgglzDMdY) - **WARNING: Flashing firmware is not a risk-free process and can result in a brick if anything goes wrong. Recovery ranges from time consuming to impossible and may even require buying extra tools.**

#### [**Chiaki**](https://github.com/thestr4ng3r/chiaki) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Cross-platform client for PlayStation 4 Remote Play. — [Video](https://www.youtube.com/watch?v=w_9eyUgdaYg)

#### [**ZeroTierOne**](https://github.com/zerotier/ZeroTierOne) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Programmable Ethernet switch that allows all networked devices, VMs, containers, and applications to communicate as if they all reside in the same physical data center or cloud region, similar to [LogMeIn Hamachi](https://en.wikipedia.org/wiki/LogMeIn_Hamachi).

#### [**Frogging-Family / community-patches**](https://github.com/Frogging-Family/community-patches)
A list of patches maintained by the community.

#### [**Luxtorpeda**](https://github.com/dreamer/luxtorpeda) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Steam Play compatibility tool to run games using native Linux engines.

#### [**libratbag**](https://github.com/libratbag/libratbag) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
DBus daemon to configure input devices for gaming mice. — **WARNING: this utility will not work in the distributions listed in the following website: [Wikipedia: Linux distributions without systemd](https://en.wikipedia.org/wiki/Category:Linux_distributions_without_systemd).**
- #### [**Piper**](https://github.com/libratbag/piper) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
	GTK+ front-end for [libratbag](https://github.com/libratbag/libratbag). — **WARNING: this utility will not work in the distributions listed in the following website: [Wikipedia: Linux distributions without systemd](https://en.wikipedia.org/wiki/Category:Linux_distributions_without_systemd).**

#### [**logiops**](https://github.com/PixlOne/logiops) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Unofficial drivers for Logitech mice and keyboard.

### Overlays

#### [**MangoHud**](https://github.com/flightlessmango/MangoHud) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
A Vulkan and OpenGL overlay for monitoring FPS, temperatures, CPU/GPU load and more. — [Video](https://www.youtube.com/watch?v=RbOY0TmArH0)

#### [**vkBasalt**](https://github.com/DadSchoorse/vkBasalt) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
A Vulkan post processing layer to enhance the visual graphics of games while barely impacting performance. — [Video](https://www.youtube.com/watch?v=hSlaGkbTRi8&t=55s)

#### [**GOverlay**](https://github.com/benjamimgois/goverlay) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
A Graphical UI to manage Linux overlays, such as [MangoHud](https://github.com/flightlessmango/MangoHud) and [vkBasalt](https://github.com/DadSchoorse/vkBasalt). — [Video](https://www.youtube.com/watch?v=-2OmhsGnsIk)

#### [**DiscordOverlayLinux**](https://github.com/trigg/DiscordOverlayLinux) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Discord Overlay for Linux.

### Websites

#### [**AppDB**](https://appdb.winehq.org/)
Website maintained by [WINE HQ](https://www.winehq.org/) to track reports and ratings of video games.
- #### [**ProtonDB**](https://www.protondb.com/)
	Website maintained by a community to track reports and ratings of video games written by other users for [Steam](https://store.steampowered.com/) and [Proton](https://github.com/ValveSoftware/Proton).
	- #### [**ProtonDB-Tags**](https://github.com/CorruptComputer/ProtonDB-Tags)
		A small Python script to pull ratings from ProtonDB and import them into your Steam library as tags.

#### [**GamingOnLinux**](https://www.gamingonlinux.com/)
The home of Linux and SteamOS gaming. Covering Linux Gaming News, Linux Games, SteamOS, Indie Game Reviews and more.
- #### [**GamingOnLinux wiki**](https://www.gamingonlinux.com/wiki/)
	GamingOnLinux' official wiki focusing on various topics of gaming on Linux, such as games, engines, guides and more.

#### [**Open Source Game Clones**](https://osgameclones.com/)
A list of open source game alternatives to their proprietary counterparts.

#### [**The Linux Gamers' Game List**](https://www.icculus.org/lgfaq/gamelist.php)
A list of games that work natively in Linux.

#### [**Arch Wiki / Gaming**](https://wiki.archlinux.org/index.php/Gaming)
A list of information about running games and related system configuration tips. 

#### [**VR Software Status**](https://gitlab.com/vr-on-linux/VR-on-Linux)
Repository containing the status of Steam games working in Virtual Reality.

#### [LibreGameWiki](https://libregamewiki.org/)
A wiki of free games and related topics started by Han Dao. 

## Processors

### AMD

#### [**RyzenAdj**](https://github.com/FlyGoat/RyzenAdj) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
CLI tool to adjust core clock and voltage of Ryzen processors.
- #### [**Ryzen Controller**](https://gitlab.com/ryzen-controller-team/ryzen-controller) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
	Graphical UI for [RyzenAdj](https://github.com/FlyGoat/RyzenAdj).

### Intel

#### [**intel-power-control**](https://github.com/jmechnich/intel-power-control) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
A [GUI](https://en.wikipedia.org/wiki/Graphical_user_interface) tool to adjust the core clock and voltage of Intel [iGPU](https://en.wikipedia.org/wiki/Graphics_processing_unit#INTEGRATED)s.

## Graphics cards

#### [**Graphics drivers overview**](https://old.reddit.com/r/linux_gaming/comments/g8h5no/can_someone_clarify_the_situation_with_amd_drivers/foniza1/?context=3) [![Generic badge](https://img.shields.io/badge/Tip-blue.svg)](https://img.shields.io/badge/Tip-blue.svg)
An overview of the graphical Linux drivers.

#### [**Shaders overview**](https://old.reddit.com/r/linux_gaming/comments/gtdifa/what_does_compiling_shaders_mean/fsazz2x/) [![Generic badge](https://img.shields.io/badge/Tip-blue.svg)](https://img.shields.io/badge/Tip-blue.svg)
An overview of the shaders used in games in Linux.

### AMD

**Note: this is only for the [AMDGPU](https://en.wikipedia.org/wiki/AMDGPU) drivers. We might add [AMDGPU-PRO](https://www.amd.com/en/support/kb/release-notes/rn-radpro-lin-16-40) or [AMDVLK](https://github.com/GPUOpen-Drivers/AMDVLK) specific categories later.**

#### [**ACO compiler**](https://wiki.archlinux.org/index.php/AMDGPU#ACO_compiler) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg) [![Generic badge](https://img.shields.io/badge/Tip-blue.svg)](https://img.shields.io/badge/Tip-blue.svg)
Open source shader compiler by [Valve Corporation](https://en.wikipedia.org/wiki/Valve_Corporation) to compete with the [LLVM compiler](http://llvm.org/), [AMDVLK drivers](https://github.com/GPUOpen-Drivers/AMDVLK) drivers and [Windows 10](https://en.wikipedia.org/wiki/Windows_10).

#### [**Overclocking**](https://wiki.archlinux.org/index.php/AMDGPU#Overclocking) [![Generic badge](https://img.shields.io/badge/Tip-blue.svg)](https://img.shields.io/badge/Tip-blue.svg)
Guide to overclock an AMD GPU using the AMDGPU drivers.

#### [**AMDGPU Clocks**](https://github.com/sibradzic/amdgpu-clocks) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
CLI tool to adjust the core clock, memory and voltage of AMD graphics cards.

#### [**vibrantLinux-AMD**](https://github.com/Scrumplex/vibrantLinux-AMD) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Fork of [vibrantLinux](https://github.com/zee-mzha/vibrantLinux); utility that automates NVIDIA's Digitial Vibrance Control and AMD's Saturation for games. — **Only for AMD GPUs.**

#### [**amdvbflash**](https://github.com/patrickschur/amdvbflash) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg) [![Generic badge](https://img.shields.io/badge/Tip-blue.svg)](https://img.shields.io/badge/Tip-blue.svg)
Tool to flash AMD GPU's [vBIOS](https://en.wikipedia.org/wiki/Video_BIOS)es. — [Guide](https://andrealmeid.com/post/2020-05-01-vbios2/)

#### [**radeon-profile**](https://github.com/marazmista/radeon-profile) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Powerful app for tuning AMD GPUs.  Monitor and adjust fans, temperatures, usage, power, and core/memory clocks.  Configure overclocking profiles and set custom fan curves.  Watch for events (e.g. temp threshold reached, game launched) and change parameters automatically.  [Additional screenshots here.](https://imgur.com/a/DMRr9)

### Xorg

**Note: Xorg has had a lot of problems with the [xf86-video-amdgpu](https://gitlab.freedesktop.org/xorg/driver/xf86-video-amdgpu) drivers, one of them being screen tearing. It is advisable to create a custom `xorg.conf` file in order to remove some issues.**

#### [**TearFree**](XORG.md#tearfree) [![Generic badge](https://img.shields.io/badge/Tip-blue.svg)](https://img.shields.io/badge/Tip-blue.svg)
Enable tearing prevention using the hardware page flipping mechanism.

#### [**FreeSync**](XORG.md#freesync) [![Generic badge](https://img.shields.io/badge/Tip-blue.svg)](https://img.shields.io/badge/Tip-blue.svg)
An  open source [Variable refresh rate](https://en.wikipedia.org/wiki/Variable_refresh_rate) technology developed by [AMD](https://en.wikipedia.org/wiki/Advanced_Micro_Devices) to eliminate screen tearing and reduce stuttering.

#### **Others** [![Generic badge](https://img.shields.io/badge/Tip-blue.svg)](https://img.shields.io/badge/Tip-blue.svg)
If you want to explore into the Xorg configuration options, you can look into:
- [AMDGPU[4]](https://manpages.debian.org/testing/xserver-xorg-video-amdgpu/amdgpu.4.en.html)
- [xorg.conf[5]](https://manpages.debian.org/testing/xserver-xorg-core/xorg.conf.5.en.html)
- [Arch wiki](https://wiki.archlinux.org/index.php/Xorg#Configuration)

### Nvidia

#### [**Drivers**](https://www.nvidia.com/en-us/drivers/unix/) [![Generic badge](https://img.shields.io/badge/Proprietary-red.svg)](https://img.shields.io/badge/Proprietary-red.svg)

**Note: It is not advised to install the driver through the package provided from the NVIDIA website. It is better to install it through the distribution's package manager.**

- **Debian** — https://wiki.debian.org/NvidiaGraphicsDrivers#Installation
- **Arch Linux** — https://wiki.archlinux.org/index.php/NVIDIA#Installation
- **Gentoo** — https://wiki.gentoo.org/wiki/NVIDIA/nvidia-drivers#Installation
- **Clear Linux** — https://docs.01.org/clearlinux/latest/tutorials/nvidia.html#installation

#### [**GreenWithEnvy (GWE)**](https://github.com/leinardi/gwe) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
GWE is a GTK system utility designed to provide information, control the fans and overclock your NVIDIA video card and graphics processor. — **Only for Nvidia GPUs.**

#### [**vibrantLinux**](https://github.com/zee-mzha/vibrantLinux) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Inspired by [vibranceGUI](https://github.com/juv/vibranceGUI) to port in Linux; utility that automates NVIDIA's Digitial Vibrance Control and AMD's Saturation for games. — **Only for Nvidia GPUs.**


## Platforms

#### [**Steam**](https://store.steampowered.com/) [![Generic badge](https://img.shields.io/badge/Proprietary-red.svg)](https://img.shields.io/badge/Proprietary-red.svg)
Video game [digital distribution](https://en.wikipedia.org/wiki/Digital_distribution) developed by [Valve Corporation](https://en.wikipedia.org/wiki/Valve_Corporation) to provide games from third-party publishers. It also offers [Proton](https://github.com/ValveSoftware/Proton) (a fork of [WINE](https://wiki.winehq.org)) to facilitate gaming on Linux.

#### [**Lutris**](https://lutris.net/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Client with install scripts provided by the community to utilise applications and games without the hassle of manually setting them up.

#### [**GameHub**](https://github.com/tkashkin/GameHub) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Unified library for all your games. It supports all games from [GOG](https://www.gog.com/), [Steam](https://store.steampowered.com/), [HumbleBundle](https://www.humblebundle.com/) and [Humble Trove](https://www.humblebundle.com/subscription/trove).

#### [**GOG**](https://www.gog.com/) [![Generic badge](https://img.shields.io/badge/Proprietary-red.svg)](https://img.shields.io/badge/Proprietary-red.svg)
Video game [digital distribution](https://en.wikipedia.org/wiki/Digital_distribution) developed by [CD Projekt](https://en.wikipedia.org/wiki/CD_Projekt) to provide third-party [DRM](https://en.wikipedia.org/wiki/Digital_rights_management)-free games.
- #### [**Minigalaxy**](https://github.com/sharkwouter/minigalaxy) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
	A simple GTK GOG client for Linux.

#### [**itch.io**](https://itch.io/games/platform-linux) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Website for users to host, sell and download [indie](https://en.wikipedia.org/wiki/Indie_game) video games.

#### [**GameJolt**](https://gamejolt.com/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Hosting service for free and commercial video games (in browser and a downloadable client) with social functions.

#### [**BeamDog**](https://www.beamdog.com/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Online-based game software program which allows players to keep their games up to date with the latest fixes and enhancements.

#### [**Legendary**](https://github.com/derrod/legendary) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
CLI client to launch games from the Epic Games Store.


## Kernels

#### [**XanMod**](https://xanmod.org/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
A general-purpose Linux kernel aimed for performance and to provide more features. 

#### [**Tk-Glitch / PKGBUILDS / linux-tkg**](https://github.com/Tk-Glitch/PKGBUILDS/wiki/linux-tkg)
A custom Linux kernel with various [patchsets](https://en.wikipedia.org/wiki/Patch_(Unix)) to improve gaming performance. — **Only available in Arch-based distributions!**

#### [**gloriouseggroll / kernel**](https://copr.fedorainfracloud.org/coprs/gloriouseggroll/kernel/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Latest upstream Linux kernel in addition of the [TKG](https://github.com/Frogging-Family/linux-tkg/tree/9b8bb89cd3775f0090ee3bff8545ac73603e42cc) patchsets. — **Only available in Fedora!**

#### [**sirlucjan / kernel-patches**](https://github.com/sirlucjan/kernel-patches)
Repository with various kernel [patchsets](https://en.wikipedia.org/wiki/Patch_(Unix)).

#### [**Arch wiki / Kernel**](https://wiki.archlinux.org/index.php/Kernel)
Arch wiki page describing various Linux kernels.


## WINE

#### [**WINE**](https://wiki.winehq.org) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
A compatibility layer capable of running Windows applications on several [POSIX](http://www.robelle.com/smugbook/posix.html)-compliant operating systems such as Linux, macOS, & BSD.
- #### [**WINE Staging**](https://wiki.winehq.org/Wine-Staging) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
	Development branch of [WINE](https://wiki.winehq.org).

[**Winetricks**](https://wiki.winehq.org/Winetricks) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Helper script to download and install various redistributable runtime libraries needed to run some programs in Wine.

### WINE implementations

#### [**VKD3D**](https://github.com/d3d12/vkd3d) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
A Vulkan-based translation layer for Direct3D 12 which allows running 3D applications on Linux using Wine.

#### [**DXVK**](https://github.com/doitsujin/dxvk) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
A Vulkan-based translation layer for Direct3D 9/10/11 which allows running 3D applications on Linux using Wine.
- #### [**D9VK**](https://github.com/Joshua-Ashton/d9vk) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
	A Vulkan-based translation layer for Direct3D 9 which allows running 3D applications on Linux using Wine. It has now been merged with [DXVK](https://github.com/doitsujin/dxvk).

#### [**wine-wayland**](https://github.com/varmd/wine-wayland) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
A Vulkan-based translation layer for [DirectX 9](https://en.wikipedia.org/wiki/DirectX#DirectX_9) & [DirectX 11](https://en.wikipedia.org/wiki/DirectX#DirectX_11) to play in pure Wayland without the need of [X11](https://en.wikipedia.org/wiki/X_Window_System) or [XWayland](https://wayland.freedesktop.org/xserver.html). — **Only available in Arch-based distributions!**

#### [**Proton**](https://github.com/ValveSoftware/Proton) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
A WINE implementation from [Valve Corporation](https://en.wikipedia.org/wiki/Valve_Corporation) to play Windows games directly from Steam Linux.
- #### [**Protontricks**](https://github.com/Matoking/protontricks) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
	Extension to [Winetricks](https://wiki.winehq.org/Winetricks) for Proton enabled games.
- #### [**proton-ge-custom**](https://github.com/GloriousEggroll/proton-ge-custom) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
	Fork of [Proton](https://github.com/ValveSoftware/Proton) by RedHat developer GloriousEggroll to port the latest versions of WINE in Proton.


## Emulators

#### [**RetroArch**](https://www.retroarch.com/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
RetroArch is a frontend for emulators, game engines and media players.

#### [**taminaru / awesome-emulators-simulators**](https://github.com/taminaru/awesome-emulators-simulators) [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
A curated list of software emulators and simulators of PCs, home computers, mainframes, consoles, robots and much more...

#### [**`mesa_glthread=true` for OpenGL**](https://old.reddit.com/r/emulation/comments/gilg8b/mesa_drivers_use_mesa_glthreadtrue_when_using/) [![Generic badge](https://img.shields.io/badge/Tip-blue.svg)](https://img.shields.io/badge/Tip-blue.svg)
Mesa drivers flag to enable multi-threading on the Mesa drivers.


## Development

#### [**ROCm**](https://github.com/RadeonOpenCompute/ROCm) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
GPU-accelerated computing drivers for **AMD GPUs**.

#### [**μProf**](https://developer.amd.com/amd-uprof/) [![Generic badge](https://img.shields.io/badge/Proprietary-red.svg)](https://img.shields.io/badge/Proprietary-red.svg)
Performance analysis tool for AMD for applications running on Windows and Linux operating systems.

#### [**Ogre**](https://www.ogre3d.org/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
Cross-platform and cross-language open source engine written in C++.

#### [**Godot**](https://godotengine.org/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
2D and 3D cross-platform game engine written in C, C++.

#### [**Blender**](https://www.blender.org/) [![Generic badge](https://img.shields.io/badge/FOSS-brightgreen.svg)](https://img.shields.io/badge/FOSS-brightgreen.svg)
3D computer graphics software toolset used for creating animated films, visual effects, art, 3D printed models, motion graphics, interactive 3D applications, and computer games.

#### [**vinjn / awesome-vulkan**](https://github.com/vinjn/awesome-vulkan) [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
A curated list of awesome Vulkan libraries, debuggers and resources.

#### [**eug / awesome-opengl**](https://github.com/eug/awesome-opengl) [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
A curated list of awesome OpenGL libraries, debuggers and resources.


## YouTube channels

#### [**FlightlessMango**](https://www.youtube.com/channel/UCDmXLiZTBaFuCOXjy6mdw5w)
Benchmark comparisons between different operating systems, different hardware and different software, as well as graphics comparisons.

#### [**Chris Titus Tech**](https://www.youtube.com/playlist?list=PLc7fktTRMBoxAo8k95vnIaPynvk0wXomc)
Focused on technical aspects of GNU/Linux, as well as gaming.

#### [**Egee**](https://www.youtube.com/user/EtherealGaming1)
Reviews, benchmark comparisons of different GNU/Linux distributions and installation guides of games. 

#### [**Intelligent Gaming**](https://www.youtube.com/channel/UCH4d4o0Otxa7BNYs5Z5UEjg/videos)
Linux gaming tutorials and gameplay.


## Q&As

See [Q&AS.md](Q&AS.md).

## Future plans

Everything we plan to add in the future in this page will be in [TODO.md](TODO.md).


## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Linux to Linux Café

- [Linux Café Website](https://linuxcafefederation.github.io/LinuxCafe/)
- [Linux Café Discord](https://discord.gg/YY4zrNR)
- [Linux Café Matrix](https://matrix.to/#/+linuxcafegroup:linuxcafe.chat)
- [Linux Café Telegram](https://t.me/joinchat/Mn4RpxM6KrSLQMBL78yloQ)
- [Linux Café Reddit](https://reddit.com/r/linuxcafe)


## Special thanks

Special thanks go to:

- the [contributors](https://gitlab.com/TheMainGroup/awesome-gnu-linux-gaming/-/graphs/master) that have contributed in this project;
- everyone that has suggested something to add, remove or fix;
- the developers and writers that have created and contributed to the awesome projects that we have mentioned;
- to everyone that has shared this project to others.

This project would never have happened and continued without you :)
