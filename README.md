# Awesome GNU/Linux gaming [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of awesome GNU/Linux tips & tricks, games, tools, and resources. Inspired by [awesome-vulkan](https://github.com/vinjn/awesome-vulkan) and other awesome-related projects.


## Overview

This is a hobby project to improve the quality of gaming in Linux because it is possible to improve performance by tweaking your Linux machine. Most Linux distributions have a lot of issues when it comes to gaming performance, as they do not utilise the modern and superior counterparts.

### **Disclaimer**

This list does provide proprietary software, but they will be exclusively marked as "**WARNING: Proprietary Software!**".


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

~~[**Manjaro Linux**](https://manjaro.org/) — Based on [Arch Linux](https://www.archlinux.org/). Attempt from the Manjaro team to provide a GUI installer, as well as test packages before they are released.~~ **WARNING: see *[Why not add Manjaro?](#why-not-add-manjaro).***

[**Pop!_OS**](https://system76.com/pop) — Based on [Ubuntu](https://ubuntu.com/). Attempt from System76 to "de-Canonical-ise" Ubuntu, as well as some minor tweaks for gaming.

[**Linux Mint**](https://www.linuxmint.com/) — Based on [Ubuntu](https://ubuntu.com/). Comes with the [Cinnamon desktop](https://en.wikipedia.org/wiki/Cinnamon_(desktop_environment)). Built for Windows users in mind, to facilitate switching from Windows to GNU/Linux thanks to its familiarity.

[**Fedora**](https://getfedora.org/) — Based on [RHEL](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux). Comes with some performance tools pre-installed such as [gamemode](https://github.com/FeralInteractive/gamemode).

[**Alpine Linux**](https://www.alpinelinux.org/) — Minimal, simple and secure binary based distribution aimed for performance.

[**Arch Linux**](https://www.archlinux.org/) — Lightweight and independent distribution to provide as much performance with as less time spent.

[**Gentoo**](https://www.gentoo.org/) — Minimal and secure source based distribution to maximise performance.

[**Frogging-Family / community-patches**](https://github.com/Frogging-Family/community-patches) — A list of patches maintained by the community.


## Utilities

[**GameMode**](https://github.com/FeralInteractive/gamemode) — A **systemd** daemon/lib to optimise Linux system performance on demand. — **WARNING: this utility will not work in the distributions listed in the following website: [Wikipedia: Linux distributions without systemd](https://en.wikipedia.org/wiki/Category:Linux_distributions_without_systemd).** — [Video](https://www.youtube.com/watch?v=zN8by3wchVw&t=35s)

[**MangoHud**](https://github.com/flightlessmango/MangoHud) — A Vulkan and OpenGL overlay for monitoring FPS, temperatures, CPU/GPU load and more. — [Video](https://www.youtube.com/watch?v=RbOY0TmArH0)

[**vkBasalt**](https://github.com/DadSchoorse/vkBasalt) — A Vulkan post processing layer to enhance the visual graphics of games while barely impacting performance. — [Video](https://www.youtube.com/watch?v=hSlaGkbTRi8&t=55s)

[**GOverlay**](https://github.com/benjamimgois/goverlay) — A Graphical UI to manage Linux overlays, such as [MangoHud](https://github.com/flightlessmango/MangoHud) and [vkBasalt](https://github.com/DadSchoorse/vkBasalt). — [Video](https://www.youtube.com/watch?v=-2OmhsGnsIk)

[**CoreCtrl**](https://gitlab.com/corectrl/corectrl) — Overclocking software with the aesthetics based on AMD's Radeon Software Adrenalin from 2018.

[**QMK**](https://qmk.fm/) — Keyboard firmware to customize key switches. Based on the [tmk_keyboard firmware](https://github.com/tmk/tmk_keyboard).

[**AppDB**](https://appdb.winehq.org/) — Website maintained by [WINE HQ](https://www.winehq.org/) to track reports and ratings of video games.
- [**ProtonDB**](https://www.protondb.com/) — Website maintained by a community to track reports and ratings of video games written by other users for [Steam](https://store.steampowered.com/) and [Proton](https://github.com/ValveSoftware/Proton).
	- [**ProtonDB-Tags**](https://github.com/CorruptComputer/ProtonDB-Tags) — A small Python script to pull ratings from ProtonDB and import them into your Steam library as tags.

[**Chiaki**](https://github.com/thestr4ng3r/chiaki) — Cross-platform client for PlayStation 4 Remote Play. — [Video](https://www.youtube.com/watch?v=w_9eyUgdaYg)

[**ZeroTierOne**](https://github.com/zerotier/ZeroTierOne) — Programmable Ethernet switch that allows all networked devices, VMs, containers, and applications to communicate as if they all reside in the same physical data center or cloud region, similar to [LogMeIn Hamachi](https://en.wikipedia.org/wiki/LogMeIn_Hamachi).


## Processors

### AMD

[**RyzenAdj**](https://github.com/FlyGoat/RyzenAdj) — CLI tool to adjust core clock and voltage of Ryzen processors.
- [**Ryzen Controller**](https://gitlab.com/ryzen-controller-team/ryzen-controller) — Fork [RyzenAdj](https://github.com/FlyGoat/RyzenAdj) with a front-end (GUI).

### Intel

[**intel-power-control**](https://github.com/jmechnich/intel-power-control) — A [GUI](https://en.wikipedia.org/wiki/Graphical_user_interface) tool to adjust the core clock and voltage of Intel [iGPU](https://en.wikipedia.org/wiki/Graphics_processing_unit#INTEGRATED)s.

## Graphics cards

### AMD

**NOTE: this is only for the [AMDGPU](https://en.wikipedia.org/wiki/AMDGPU) drivers. We might add AMDGPU-PRO or AMDVLK specific categories later.**

[**ACO compiler**](https://wiki.archlinux.org/index.php/AMDGPU#ACO_compiler) — Open source shader compiler by [Valve Corporation](https://en.wikipedia.org/wiki/Valve_Corporation) to compete with the [LLVM compiler](http://llvm.org/), [AMDVLK drivers](https://github.com/GPUOpen-Drivers/AMDVLK) drivers and [Windows 10](https://en.wikipedia.org/wiki/Windows_10).

[**Overclocking**](https://wiki.archlinux.org/index.php/AMDGPU#Overclocking) — Guide to overclock an AMD GPU using the AMDGPU drivers.

[**AMDGPU Clocks**](https://github.com/sibradzic/amdgpu-clocks) — CLI tool to adjust the core clock, memory and voltage of AMD graphics cards.

[**vibrantLinux-AMD**](https://github.com/Scrumplex/vibrantLinux-AMD) — Fork of [vibrantLinux](https://github.com/zee-mzha/vibrantLinux); utility that automates NVIDIA's Digitial Vibrance Control and AMD's Saturation for games. — **WARNING: only works on AMD GPUs.**

#### Xorg

**Note: Xorg has had a lot of problems with the [xf86-video-amdgpu](https://gitlab.freedesktop.org/xorg/driver/xf86-video-amdgpu) drivers, one of them being screen tearing. It is advisable to create a custom `xorg.conf` file in order to remove some issues.**

[**TearFree**](/XORG.md#tearfree) — Enable tearing prevention using the hardware page flipping mechanism.

[**FreeSync**](/XORG.md#freesync) — An  open source [Variable refresh rate](https://en.wikipedia.org/wiki/Variable_refresh_rate) technology developed by [AMD](https://en.wikipedia.org/wiki/Advanced_Micro_Devices) to eliminate screen tearing and reduce stuttering.

**Others** — If you want to explore into the Xorg configuration options, you can look into:
- [AMDGPU[4]](https://manpages.debian.org/testing/xserver-xorg-video-amdgpu/amdgpu.4.en.html)
- [xorg.conf[5]](https://manpages.debian.org/testing/xserver-xorg-core/xorg.conf.5.en.html)
- [Arch wiki](https://wiki.archlinux.org/index.php/Xorg#Configuration)

### Nvidia

#### [**Drivers**](https://www.nvidia.com/en-us/drivers/unix/) — **WARNING: Proprietary Software!**

**NOTE: It is not advised to install the driver through the package provided from the NVIDIA website. It is better to install it through the distribution's package manager.**

- **Debian** — https://wiki.debian.org/NvidiaGraphicsDrivers#Installation
- **Arch Linux** — https://wiki.archlinux.org/index.php/NVIDIA#Installation
- **Gentoo** — https://wiki.gentoo.org/wiki/NVIDIA/nvidia-drivers#Installation
- **Clear Linux** — https://docs.01.org/clearlinux/latest/tutorials/nvidia.html#installation

[**vibrantLinux**](https://github.com/zee-mzha/vibrantLinux) — Inspired by [vibranceGUI](https://github.com/juv/vibranceGUI) to port in Linux; utility that automates NVIDIA's Digitial Vibrance Control and AMD's Saturation for games. — **WARNING: only works on Nvidia GPUs.**


## Platforms

[**Steam**](https://store.steampowered.com/) — Video game [digital distribution](https://en.wikipedia.org/wiki/Digital_distribution) developed by [Valve Corporation](https://en.wikipedia.org/wiki/Valve_Corporation) to provide games from third-party publishers. It also offers [Proton](https://github.com/ValveSoftware/Proton) (a fork of [WINE](https://wiki.winehq.org)) to facilitate gaming on Linux. — **WARNING: Proprietary Software!**

[**Lutris**](https://lutris.net/) — Client with install scripts provided by the community to utilise applications and games without the hassle of manually setting them up.

[**GameHub**](https://github.com/tkashkin/GameHub) — Unified library for all your games. It supports all games from [GOG](https://www.gog.com/), [Steam](https://store.steampowered.com/), [HumbleBundle](https://www.humblebundle.com/) and [Humble Trove](https://www.humblebundle.com/subscription/trove).

[**GOG**](https://www.gog.com/) — Video game [digital distribution](https://en.wikipedia.org/wiki/Digital_distribution) developed by [CD Projekt](https://en.wikipedia.org/wiki/CD_Projekt) to provide third-party [DRM](https://en.wikipedia.org/wiki/Digital_rights_management)-free games. — **WARNING: Proprietary Software!**
- [**Minigalaxy**](https://github.com/sharkwouter/minigalaxy) — A simple GTK GOG client for Linux.

[**itch.io**](https://itch.io/games/platform-linux) — Website for users to host, sell and download [indie](https://en.wikipedia.org/wiki/Indie_game) video games.

[**GameJolt**](https://gamejolt.com/) — Hosting service for free and commercial video games (in browser and a downloadable client) with social functions.

[**BeamDog**](https://www.beamdog.com/) — Online-based game software program which allows players to keep their games up to date with the latest fixes and enhancements.

[**Legendary**](https://github.com/derrod/legendary) — CLI client to launch games from the Epic Games Store.


## Kernels

[**ZEN/Liquorix**](https://liquorix.net/) — Distro kernel replacement built using the best configuration and kernel sources for desktop, multimedia, and gaming workloads.

[**XanMod**](https://xanmod.org/) — A general-purpose Linux kernel aimed for performance and to provide more features. 

[**sirlucjan / kernel-patches**](https://github.com/sirlucjan/kernel-patches) — Repository with various kernel [patchsets](https://en.wikipedia.org/wiki/Patch_(Unix)).

[**gloriouseggroll / kernel**](https://copr.fedorainfracloud.org/coprs/gloriouseggroll/kernel/) — Latest upstream Linux kernel in addition of the [TKG](https://github.com/Frogging-Family/linux-tkg/tree/9b8bb89cd3775f0090ee3bff8545ac73603e42cc) patchsets. — **WARNING: only available in Fedora.**


## WINE

[**WINE**](https://wiki.winehq.org) — A compatibility layer capable of running Windows applications on several [POSIX](http://www.robelle.com/smugbook/posix.html)-compliant operating systems such as Linux, macOS, & BSD.
- [**WINE Staging**](https://wiki.winehq.org/Wine-Staging) — Development branch of [WINE](https://wiki.winehq.org).

[**Winetricks**](https://wiki.winehq.org/Winetricks) — Helper script to download and install various redistributable runtime libraries needed to run some programs in Wine.

### WINE implementations

[**VKD3D**](https://github.com/d3d12/vkd3d) — A Vulkan-based translation layer for Direct3D 12 which allows running 3D applications on Linux using Wine.

[**DXVK**](https://github.com/doitsujin/dxvk) — A Vulkan-based translation layer for Direct3D 9/10/11 which allows running 3D applications on Linux using Wine.
- [**D9VK**](https://github.com/Joshua-Ashton/d9vk) — A Vulkan-based translation layer for Direct3D 9 which allows running 3D applications on Linux using Wine. It has now been merged with [DXVK](https://github.com/doitsujin/dxvk).

[**wine-wayland**](https://github.com/varmd/wine-wayland) — A Vulkan-based translation layer for [DirectX 9](https://en.wikipedia.org/wiki/DirectX#DirectX_9) & [DirectX 11](https://en.wikipedia.org/wiki/DirectX#DirectX_11) to play in Wayland without the need of [X11](https://en.wikipedia.org/wiki/X_Window_System) or [XWayland](https://wayland.freedesktop.org/xserver.html). **(Arch derivatives only!)**

[**Proton**](https://github.com/ValveSoftware/Proton) — A WINE implementation from [Valve Corporation](https://en.wikipedia.org/wiki/Valve_Corporation) to play Windows games directly from Steam Linux.
- [**Protontricks**](https://github.com/Matoking/protontricks) — Extension to [Winetricks](https://wiki.winehq.org/Winetricks) for Proton enabled games.
- [**proton-ge-custom**](https://github.com/GloriousEggroll/proton-ge-custom) — Fork of [Proton](https://github.com/ValveSoftware/Proton) by RedHat developer GloriousEggroll to port the latest versions of WINE in Proton.


## Emulators

[**taminaru / awesome-emulators-simulators**](https://github.com/taminaru/awesome-emulators-simulators#consoles) — A curated list of software emulators and simulators of PCs, home computers, mainframes, consoles, robots and much more...


## Development

[**μProf**](https://developer.amd.com/amd-uprof/) — Performance analysis tool for AMD for applications running on Windows and Linux operating systems. — **WARNING: Proprietary Software!**

[**Ogre**](https://www.ogre3d.org/) — Cross-platform and cross-language open source engine written in C++.

[**Godot**](https://godotengine.org/) — 2D and 3D cross-platform game engine written in C, C++.

[**Blender**](https://www.blender.org/) — 3D computer graphics software toolset used for creating animated films, visual effects, art, 3D printed models, motion graphics, interactive 3D applications, and computer games.

[**vinjn / awesome-vulkan**](https://github.com/vinjn/awesome-vulkan) — A curated list of awesome Vulkan libraries, debuggers and resources.


## YouTube channels

[**FlightlessMango**](https://www.youtube.com/channel/UCDmXLiZTBaFuCOXjy6mdw5w) — Benchmark comparisons between different operating systems, different hardware and different software, as well as graphics comparisons.

[**Chris Titus Tech**](https://www.youtube.com/playlist?list=PLc7fktTRMBoxAo8k95vnIaPynvk0wXomc) — Focused on technical aspects of GNU/Linux, as well as gaming.

[**Egee**](https://www.youtube.com/user/EtherealGaming1) — Reviews, benchmark comparisons of different GNU/Linux distributions and installation guides of games. 


## Q&As

### Why create this repository?

The reason behind this action could be explained by the lack of repositories which has managed to unite tips & tricks and resources regarding GNU/Linux gaming in one repository with the aim of reducing the amount of search queries required by the user to look up certain information regarding the situation of a game on Linux, how to emulate specific games and so on. There are a lot of interesting projects, such as ACO, which we deem worthy of fame and have thus included those in this repo.

### Why GitLab over GitHub?

Due to the recent change of ownership to GitHub, the open source project hosting service, to Microsoft, we have decided not to maintain the following repository on their server. The reasoning behind the following action could be explained by Microsoft's behaviour towards the open source community for the past decade and thus we concluded to refrain from using GitHub as the host of the this repository.

### Why not just contribute to the Arch wiki?

I am aware of the [Arch wiki / Gaming](https://wiki.archlinux.org/index.php/Gaming) page, but despite the Arch wiki having constant attention, it is not a place where people take the time and effort to look at it. I did contribute in the Arch wiki several times, but I then realised that not many people will look into it despite having this much attention, so I stopped contributing. [Here is an example in Reddit](https://www.reddit.com/r/linux_gaming/comments/fyuqc7/a_fantastic_amd_gpu_gui_software_for_linux/fn2723y?utm_source=share&utm_medium=web2x) of a person recently discovering CoreCtrl, when it was mentioned in the [Arch wiki](https://wiki.archlinux.org/index.php/AMDGPU#GUI_tools) a couple of months prior to the date of the release of the thread.

#### Why not just promote it then?

Because the Arch wiki has been promoted by many youtubers already, and it is also a meme for the epicc arch linux users btw xddd!1!11

### Why not add Manjaro?

Because we do not agree with Manjaro's practices and outcome. Those are the following:

- **Developers**
	- The Manjaro developers have done a lot of controversies. There is a brief summary that explains the lack of proper maintenance to the distribution:
		- https://github.com/vizs/manjarno

- **Security and Privacy**
	- Manjaro **does not** have a security policy (like [SELinux](https://www.redhat.com/en/topics/linux/what-is-selinux)) enabled by default. The lack of a security policy brings to an [increased amount of kernel-level security vulnerabilities](https://www.cvedetails.com/product/47/Linux-Linux-Kernel.html?vendor_id=33). On top of that, the lack of a security policy can also decrease the privacy of the user, because packages will have the permissions to view the whole filesystem, resources and more.
		- https://forum.manjaro.org/t/manjaro-why-you-have-no-selinux/128757
	- Manjaro holds back packages for several weeks, **including security updates**, which makes security updates arrive a couple of weeks later. This can potentially decrease the security of a user's device.
		- http://allanmcrae.com/2013/01/manjaro-linux-ignoring-security-for-stability/

- **Instability and bugs that are non-existant in Arch**
	- Manjaro has had a lot of issues with bugs and instability that were non-existant in Arch. One example to this is users had issues with Pipewire hogging all the RAM of their device:
		- https://forum.manjaro.org/t/after-upgrade-no-sound-pipewire-100-cpu-load-system-freeze/131580
		- https://forum.manjaro.org/t/troubleshooting-random-system-freeze/106554
		- https://www.reddit.com/r/ManjaroLinux/comments/fpydtg/pipewire_process_consuming_almost_all_of_my_ram/

- **Extras**
	- In the Manjaro wiki, it is written clearly that you "Use the AUR at your own risk!". The issue with this is when using Pamac or Octopi, the users are a couple of clicks away to enabling the AUR, and none tell you about the disadvantages of the AUR.
		- https://wiki.manjaro.org/index.php/Arch_User_Repository#Overview
	- Manjaro's PKGBUILD repository **does not** show the latest versions. For example, the latest version of GNOME Shell released in Manjaro is `gnome-shell-3.36.*`, but the version provided in the repository is `gnome-shell-3.34.3`, which was three months ago of the day of this text (April 28, 2020).
		- https://gitlab.manjaro.org/arch-packages/extra/gnome-shell/-/commits/packages/gnome-shell/repos/extra-x86_64/PKGBUILD

**We** do not recommend Manjaro to the users, but we will not restrict you from using it. You are free to use anything you want.


## Future plans

Everything we plan to add in the future in this page will be in [TODO.md](/TODO.md).


## Contributing

See [CONTRIBUTING.md](/CONTRIBUTING.md).


## Special thanks

Special thanks go to:

- the [contributors](https://gitlab.com/TheMainGroup/awesome-gnu-linux-gaming/-/graphs/master) that have contributed in this project;
- everyone that has suggested something to add, remove or fix;
- the developers and writers that have created and contributed to the awesome projects that we have mentioned;
- to everyone that has shared this project to others.

This project would never have happened and continued without you :)
