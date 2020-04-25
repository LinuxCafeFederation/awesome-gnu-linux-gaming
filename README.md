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
- [Gaming platforms](#gaming-platforms)
- [Custom kernels](#custom-kernels)
- [WINE](#wine)
- [Emulators](#emulators)
- [Developers](#developers)
- [YouTube channels](#youtube-channels)
- [Q&As](#qas)
- [Future plans](#future-plans)
- [Contributing](#contributing)
- [Special thanks](#special-thanks)


## Distributions

*From simplest to complex.*

~~[**Manjaro Linux**](https://manjaro.org/) — Based on [Arch Linux](https://www.archlinux.org/). Attempt from the Manjaro team to provide a GUI installer, as well as test packages before they are released.~~ **WARNING: see *[Why not add Manjaro?](#why-not-add-manjaro).***

[**Pop!_OS**](https://system76.com/pop) — Based on [Ubuntu](https://ubuntu.com/). Attempt from System76 to "de-Canonical-ise" Ubuntu, as well as some minor tweaks for gaming.

[**Kubuntu**](https://kubuntu.org/) — [Flavour of Ubuntu](https://ubuntu.com/download/flavours) with a [Plasma](https://kde.org/plasma-desktop) desktop to facilitate Windows users to switch to Linux.

[**Fedora**](https://getfedora.org/) — Based on [RHEL](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux). Comes with some performance tools pre-installed such as [gamemode](https://github.com/FeralInteractive/gamemode).

[**Alpine Linux**](https://www.alpinelinux.org/) — Minimal, simple and secure binary based distribution aimed for performance.

[**Arch Linux**](https://www.archlinux.org/) — Lightweight and independent distribution to provide as much performance with as less time spent.

[**Gentoo**](https://www.gentoo.org/) — Minimal and secure source based distribution to maximise performance.


## Utilities

[**GameMode**](https://github.com/FeralInteractive/gamemode) — A **systemd** daemon/lib to optimise Linux system performance on demand.

[**MangoHud**](https://github.com/flightlessmango/MangoHud) — A Vulkan and OpenGL overlay for monitoring FPS, temperatures, CPU/GPU load and more.

[**vkBasalt**](https://github.com/DadSchoorse/vkBasalt) — A Vulkan post processing layer to enhance the visual graphics of games while barely impacting performance.

[**GOverlay**](https://github.com/benjamimgois/goverlay) — A Graphical UI to manage Linux overlays, such as [MangoHud](https://github.com/flightlessmango/MangoHud) and [vkBasalt](https://github.com/DadSchoorse/vkBasalt).

[**CoreCtrl**](https://gitlab.com/corectrl/corectrl) — Overclocking software with the aesthetics based on AMD's Radeon Software Adrenalin from 2018.

[**QMK**](https://qmk.fm/) — Keyboard firmware based on the [tmk_keyboard firmware](https://github.com/tmk/tmk_keyboard).

## Processors

### AMD

[**RyzenAdj**](https://github.com/FlyGoat/RyzenAdj) — CLI tool to adjust core clock and voltage of Ryzen processors.
- [**Ryzen Controller**](https://gitlab.com/ryzen-controller-team/ryzen-controller) — Fork [RyzenAdj](https://github.com/FlyGoat/RyzenAdj) with a front-end (GUI).

## Intel

[**intel-power-control**](https://github.com/jmechnich/intel-power-control) — A GUI GPU power management tool for Intel hardware.

## Graphics cards

### AMD

**NOTE: this is only for the [AMDGPU](https://en.wikipedia.org/wiki/AMDGPU) drivers. We might add AMDGPU-PRO or AMDVLK specific categories later.**

[**ACO compiler**](https://wiki.archlinux.org/index.php/AMDGPU#ACO_compiler) — Open source shader compiler by [Valve Corporation](https://en.wikipedia.org/wiki/Valve_Corporation) to compete with the [LLVM compiler](http://llvm.org/), [AMDVLK drivers](https://github.com/GPUOpen-Drivers/AMDVLK) drivers and [Windows 10](https://en.wikipedia.org/wiki/Windows_10).

[**Overclocking**](https://wiki.archlinux.org/index.php/AMDGPU#Overclocking) — Guide to overclock an AMD GPU using the AMDGPU drivers.

[**AMDGPU Clocks**](https://github.com/sibradzic/amdgpu-clocks) — CLI tool to adjust the core clock, memory and voltage of AMD graphics cards.

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


## Gaming platforms

[**Steam**](https://store.steampowered.com/) — Video game [digital distribution](https://en.wikipedia.org/wiki/Digital_distribution) developed by [Valve Corporation](https://en.wikipedia.org/wiki/Valve_Corporation) to provide games from third-party publishers. It also offers [Proton](https://github.com/ValveSoftware/Proton) (a fork of [WINE](https://wiki.winehq.org)) to facilitate gaming on Linux. — **WARNING: Proprietary Software!**

[**Lutris**](https://lutris.net/) — [FOSS](https://en.wikipedia.org/wiki/Free_and_open-source_software) game manager for Linux-based operating systems developed and maintained by Mathieu Comandon and the community, listed under the GNU General Public License.

[**GOG**](https://www.gog.com/) — Video game [digital distribution](https://en.wikipedia.org/wiki/Digital_distribution) developed by [CD Projekt](https://en.wikipedia.org/wiki/CD_Projekt) to provide third-party [DRM](https://en.wikipedia.org/wiki/Digital_rights_management)-free games. — **WARNING: Proprietary Software!**
- [**Minigalaxy**](https://github.com/sharkwouter/minigalaxy) — A simple GTK GOG client for Linux.

[**itch.io**](https://itch.io/games/platform-linux) — Website for users to host, sell and download [indie](https://en.wikipedia.org/wiki/Indie_game) video games.

[**GameJolt**](https://gamejolt.com/) — Hosting service for free and commercial video games (in browser and a downloadable client) with social functions.

[**BeamDog**](https://www.beamdog.com/) — Online-based game software program which allows players to keep their games up to date with the latest fixes and enhancements.

## Custom kernels

[**ZEN/Liquorix**](https://liquorix.net/) — Distro kernel replacement built using the best configuration and kernel sources for desktop, multimedia, and gaming workloads.

[**XanMod**](https://xanmod.org/) — A general-purpose Linux kernel aimed for performance and to provide more features. 


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


## Developers

[**μProf**](https://developer.amd.com/amd-uprof/) — Performance analysis tool for AMD for applications running on Windows and Linux operating systems. — **WARNING: Proprietary Software!**


## YouTube channels

[**FlightlessMango**](https://www.youtube.com/channel/UCDmXLiZTBaFuCOXjy6mdw5w) — Benchmark comparisons between different operating systems, different hardware and different software, as well as graphics comparisons.

[**Chris Titus Tech**](https://www.youtube.com/playlist?list=PLc7fktTRMBoxAo8k95vnIaPynvk0wXomc) — Focused on technical aspects and also gaming on Linux.

## Q&As

### Why create this repository?

The reason behind this action could be explained by the lack of repositories which has managed to unite tips & tricks and resources regarding GNU/Linux gaming in one repository with the aim of reducing the amount of search queries required by the user to look up certain information regarding the situation of a game on Linux, how to emulate specific games and so on. There are a lot of interesting projects, such as ACO, which we deem worthy of fame and have thus included those in this repo.

### Why GitLab over GitHub?

Due to the recent change of ownership to GitHub, the open source project hosting service, to Microsoft, we have decided not to maintain the following repository on their server. The reasoning behind the following action could be explained by Microsoft's behaviour towards the open source community for the past decade and thus we concluded to refrain from using GitHub as the host of the this repository.

### Why not just contribute to the Arch wiki?

I am aware of the [Arch wiki / Gaming](https://wiki.archlinux.org/index.php/Gaming) page, but despite the Arch wiki having constant attention, it is not a place where people take the time to look in. I did contribute in the Arch wiki, but I realised that not many people look into it, so I did not bother. [Here is an example in Reddit](https://www.reddit.com/r/linux_gaming/comments/fyuqc7/a_fantastic_amd_gpu_gui_software_for_linux/fn2723y?utm_source=share&utm_medium=web2x) of a person recently discovering [CoreCtrl](), when it was mentioned in the [Arch wiki](https://wiki.archlinux.org/index.php/AMDGPU#GUI_tools) a couple of months ago.

#### Why not just promote it then?

Because the Arch wiki has been promoted by many youtubers, and it is also a meme for the epicc arch linux users btw xddd!1!11

### Why not add Manjaro?

Because we do not agree with Manjaro's practices and outcome. Those are the following:

- **Developers**
	- The Manjaro developers have done a lot of controversies. There are some articles that summarise Manjaro team's lack of proper maintenance to the distribution:
		- https://rentry.co/manjaro-controversies
		- https://github.com/vizs/manjarno

- **Security and Privacy**
	- Manjaro **does not** have a security policy (like [SELinux](https://www.redhat.com/en/topics/linux/what-is-selinux)) enabled by default. The lack of a security policy brings to an increased amount of kernel-level security vulnerabilities. On top of that, the lack of a security policy can also decrease the privacy of the user, because packages will have the permissions to view the whole filesystem, resources and more.
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
