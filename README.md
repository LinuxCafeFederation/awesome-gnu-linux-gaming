# Awesome GNU/Linux gaming [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of awesome GNU/Linux tips & tricks, games, tools, and resources. Inspired by [awesome-vulkan](https://github.com/vinjn/awesome-vulkan) and other awesome-related projects.

**Disclaimer**: It is recommended for the Linux user who finds their knowledge regarding the construction of a Linux based distribution limited to use a rather stable Linux distribiution approved by the Linux community instead of using a Linux distributions solely because of what has been advertised in its regard. Many Linux distributions claim to maintain stability and harmony while in actual reality failing to comply with their claims and thus resulting in system failure, confusion and hatred towards what is thought to be the operating system aiming to provide its users with the wonders of Linux for the newcomer.

## Table of contents

- [Utilities](#utilities)
- [CPU](#cpu)
	- [AMD](#amd)
	- [Intel](#intel)
- [GPU](#gpu)
	- [AMD](#amd-1)
		- [ACO compiler](#aco-compiler)
		- [Custom Xorg configuration](#custom-xorg-configuration)
	- [Intel](#intel-1)
	- [Nvidia](#nvidia)
- [Steam](#steam)
- [Lutris](#lutris)
- [WINE](#wine)
- [Emulators](#emulators)
	- [Dolphin]
- [F.A.Q.](#faq)
- [Future plans](#future-plans)

# Utilities

[**FeralInteractive / gamemode**](https://github.com/FeralInteractive/gamemode) — A **systemd** daemon/lib to optimise Linux system performance on demand.

[**flightlessmango / MangoHud**](https://github.com/flightlessmango/MangoHud) — A Vulkan and OpenGL overlay for monitoring FPS, temperatures, CPU/GPU load and more.

[**DadSchoorse / vkBasalt**](https://github.com/DadSchoorse/vkBasalt) — A Vulkan post processing layer to enhance the visual graphics of games while barely impacting performance.

[**benjamimgois / GOverlay**](https://github.com/benjamimgois/goverlay) — A Graphical UI to manage Linux overlays, such as MangoHud and vkBasalt.


# CPU

## AMD

## Intel

# GPU

## AMD

### ACO compiler

The [ACO compiler](https://steamcommunity.com/games/221410/announcements/detail/1602634609636894200) is an open source shader compiler created and developed by [Valve Corporation](https://en.wikipedia.org/wiki/Valve_Corporation) to directly compete with the LLVM compiler, the AMDVLK drivers, as well as Windows 10. It offers lesser compilation time and also performs better while gaming than LLVM and AMDVLK.

(Sources from [It's FOSS](https://itsfoss.com/linux-games-performance-boost-amd-gpu/), [Laboratoryo Neil](https://youtu.be/p7usPG4Ay34), Phoronix[[1](https://www.phoronix.com/scan.php?page=article&item=radv-aco-llvm&num=1)][[2](https://www.phoronix.com/scan.php?page=article&item=radv-aco-gcn10&num=1)][[3](https://www.phoronix.com/scan.php?page=article&item=mesa20radv-aco-amdvlk&num=1)])


You can enable the ACO compiler by [exporting `RADV_PERFTEST=aco`](https://wiki.archlinux.org/index.php/Environment_variables).

### Custom Xorg configuration

Xorg has had a lot of problems with the [xf86-video-amdgpu](https://gitlab.freedesktop.org/xorg/driver/xf86-video-amdgpu) drivers, one of the being screen tearing. It is advisable to create xorg.conf file in order to remove some issues.

Instructions will be found in:

- [Arch wiki](https://wiki.archlinux.org/index.php/AMDGPU#Xorg_configuration)

For those that want to look more into Xorg configurations, you can look into:

- [AMDGPU[4]](https://manpages.debian.org/testing/xserver-xorg-video-amdgpu/amdgpu.4.en.html)
- [xorg.conf[5]](https://manpages.debian.org/testing/xserver-xorg-core/xorg.conf.5.en.html)

### Overclocking

Overclocking your graphics card often yields to superior performance, at the cost of lifespan.

**Warning: you are on your own if you create a nuclear bomb.**

You can find instructions to overclock in the [Arch wiki](https://wiki.archlinux.org/index.php/AMDGPU#Overclocking).

## Intel

## Nvidia


# Steam
Steam is a video game digital distribution service by Valve.

# Lutris
Lutris is a FOSS game manager for Linux-based operating systems developed and maintained by Mathieu Comandon and the community, listed under the GNU General Public License.

# WINE
Wine is a free and open-source compatibility layer that aims to allow computer programs developed for Microsoft Windows to run on Unix-like operating systems.

# Emulators

### Dolphin
Dolphin is an emulator for two recent Nintendo video game consoles: the GameCube and the Wii. It allows PC gamers to enjoy games for these two consoles in full HD (1080p) with several enhancements: compatibility with all PC controllers, turbo speed, networked multiplayer, and even more! 

# F.A.Q.

**Q.1** Why create this repository?

**A.1** The reason behind this action could be explained by the lack of repositories which has managed to unite tips & tricks and resources regarding GNU/Linux gaming in one repository with the aim of reducing the amount of search queries required by the user to look up certain information regarding the situation of a game on Linux, how to emulate specific games and so on. There are a lot of interesting projects, such as ACO, which we deem worthy of fame and have thus included those in this repo.

**Q.2** Why GitLab over GitHub?

**A.2** Because we do not !

# Future plans

Everything we plan to add in the future in this page will be in [TODO.md](/TODO.md).
