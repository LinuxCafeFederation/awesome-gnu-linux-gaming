# Awesome GNU/Linux gaming [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of awesome GNU/Linux tips & tricks, games, tools, and resources. Inspired by [awesome-vulkan](https://github.com/vinjn/awesome-vulkan) and other awesome-related projects.

**Disclaimer**: It is recommended for the Linux user who finds their knowledge regarding the construction of a Linux based distribution limited to use a rather stable Linux distribiution approved by the Linux community instead of using a Linux distributions solely because of what has been advertised in its regard. Many Linux distributions claim to maintain stability and harmony while in actual reality failing to comply with their claims and thus resulting in system failure, confusion and hatred towards what is thought to be the operating system aiming to provide its users with the wonders of Linux for the newcomer.

## Table of contents

- [Awesome GNU/Linux gaming ![Awesome](https://github.com/sindresorhus/awesome)](#awesome-gnulinux-gaming-img-src%22httpsgithubcomsindresorhusawesome%22-alt%22awesome%22)
	- [Table of contents](#table-of-contents)
- [Utilities](#utilities)
- [CPU](#cpu)
	- [AMD](#amd)
	- [Intel](#intel)
- [GPU](#gpu)
	- [AMD](#amd-1)
		- [ACO compiler](#aco-compiler)
		- [Xorg](#xorg)
			- [Eliminate screen tearing](#eliminate-screen-tearing)
			- [FreeSync](#freesync)
			- [Others](#others)
		- [Overclocking](#overclocking)
	- [Intel](#intel-1)
	- [Nvidia](#nvidia)
- [Gaming platforms](#gaming-platforms)
	- [Steam](#steam)
		- [Arch Linux](#arch-linux)
	- [Lutris](#lutris)
		- [Arch Linux](#arch-linux-1)
	- [WINE](#wine)
		- [Arch Linux](#arch-linux-2)
- [Emulators](#emulators)
		- [Dolphin](#dolphin)
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

### [ACO compiler](https://wiki.archlinux.org/index.php/Gaming#ACO_compiler)

### Xorg

Xorg has had a lot of problems with the [xf86-video-amdgpu](https://gitlab.freedesktop.org/xorg/driver/xf86-video-amdgpu) drivers, one of them being screen tearing. It is advisable to create a custom `xorg.conf` file in order to remove some issues.

#### Eliminate screen tearing

You will have to create a file in `/etc/X11/xorg.conf.d/` and enable the `TearFree` option. To do so, follow the example:

```
/etc/X11/xorg.conf.d/99-amdgpu.conf
――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――
Section "Device"
     Identifier "AMD"
     Driver "amdgpu"
     Option "TearFree" "true"
  EndSection
```

Then, log back in, and enjoy the tear free rendering!

#### FreeSync

[FreeSync](https://en.wikipedia.org/wiki/FreeSync) is a technology developed by [AMD](https://en.wikipedia.org/wiki/Advanced_Micro_Devices) to eliminate screen tearing and reduce stuttering.

This feature, however, is only available if your [**monitor is compatible with FreeSync**](https://www.amd.com/en/products/freesync-monitors), as well as if your [**GPU is compatible with FreeSync**](https://www.amd.com/en/technologies/free-sync-faq#faq-Which-products-support-AMD-FreeSync%E2%84%A2-technology?).

If you are using a laptop, you can check if your [**laptop is compatible with FreeSync**](https://www.amd.com/en/products/freesync-laptops).

If you have the requirements, you can simply enable the `VariableRefresh` option. To do so, follow the example:

```
/etc/X11/xorg.conf.d/99-amdgpu.conf
――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――
Section "Device"
     Identifier "AMD"
     Driver "amdgpu"
     Option "VariableRefresh" "true"
  EndSection
```

Then, log back in, and enjoy your FreeSync enabled gaming!

#### Others

If you want to explore into the Xorg configuration options, you can look into:

- [AMDGPU[4]](https://manpages.debian.org/testing/xserver-xorg-video-amdgpu/amdgpu.4.en.html)
- [xorg.conf[5]](https://manpages.debian.org/testing/xserver-xorg-core/xorg.conf.5.en.html)
- [Arch wiki](https://wiki.archlinux.org/index.php/Xorg#Configuration)

### [Overclocking](https://wiki.archlinux.org/index.php/AMDGPU#Overclocking)

## Intel

## Nvidia

# Gaming platforms

## Steam
Steam is a video game digital distribution service by Valve. On August 21, 2018 Valve released a newly developed project with the name `Proton`; a project based on a fork of WINE aiming to improve the current gaming situation on Linux. Proton is a mostly free and open-source compatibility layer that allows software designed for Microsoft Windows to run on Linux-based operating systems.

### Arch Linux
To install steam on `Arch Linux` one has to install the required packages and later optimize steam for running Windows architectured games on Linux.

The process for an AMD based device could be achieved as follow:
1. Enable multilib repositories by excluding the `#` affront of `[multilib]` and `#include` found in `/etc/pacman.conf`.

The process mentioned above should look as follows: 
   1. `nano/vim /etc/pacman.conf` (choose your desired editor).
   2.  
	```
   	[multilib]
	Include = /etc/pacman.d/mirrorlist
	```
	3. Make sure to run `sudo pacman -Syu` after enabling the `multilib` repositories found in `pacman.conf`.

1. Install the missing packages from your Arch Linux installation. **It should be understood that the packages listed below are not indented to be installed on one functional Linux system**, but rather for the user to select the suitable packages required by his/her system to later install.
   1. `steam ttf-liberation wqy-zenhei lib32-mesa mesa xf86-video-amdgpu/xf86-video-ati/xf86-video-intel/xf86-video-nouveau`.
   2. In the following example it is shown how an installation of steam would look like on a laptop running on AMDGPU: `sudo pacman -Sy steam ttf-liberation wqy-zenhei lib32-mesa mesa xf86-video-amdgpu`

2. Run `Steam (Runtime)`, open up the settings window and later enable `Steam Play` through the Steam Play category.

## Lutris
Lutris is a FOSS game manager for Linux-based operating systems developed and maintained by Mathieu Comandon and the community, listed under the GNU General Public License.

### Arch Linux
The installation of Lutris is rather simple compared to Steam and thus the users has to attempt the installation of the package alone and wait for it to finish the installation. This could be achieved with the help of running the following command: `sudo pacman -Sy lutris`.

It's worth mentioning that the installation of Lutris is not the complex part of running the software, but the installation of games through Lutris could be thought of as more complex as one would hope for. The installation of League of Legends on Linux through Lutris is a good example of such task. 

## WINE
Wine (originally an acronym for "Wine Is Not an Emulator") is a compatibility layer capable of running Windows applications on several POSIX-compliant operating systems such as Linux, macOS, & BSD.

### Arch Linux
The installation of WINE varries between a stable/testing package and could thus be installed, if one desires a stable WINE installation, through the following command: `sudo pacman -S wine wine-gecko wine-mono`, where the `wine-gecko wine-mono` are packages required by applications dependent on `IE` and `.NET`.

To install a more up-to-date version of wine, one has to replace wine with `wine-staging` and thus the command becomes as follows: `sudo pacman -S wine-staging wine-gecko wine-mono`

# Emulators

### Dolphin
Dolphin is an emulator for two recent Nintendo video game consoles: the GameCube and the Wii. It allows PC gamers to enjoy games for these two consoles in full HD (1080p) with several enhancements: compatibility with all PC controllers, turbo speed, networked multiplayer, and even more! 

# F.A.Q.

**Q.1** Why create this repository?

**A.1** The reason behind this action could be explained by the lack of repositories which has managed to unite tips & tricks and resources regarding GNU/Linux gaming in one repository with the aim of reducing the amount of search queries required by the user to look up certain information regarding the situation of a game on Linux, how to emulate specific games and so on. There are a lot of interesting projects, such as ACO, which we deem worthy of fame and have thus included those in this repo.

**Q.2** Why GitLab over GitHub?

**A.2** Due to the recent change of ownership to GitHub, the open source project hosting service, to Microsoft, we have decided not to maintain the following repository on their server. The reasoning behind the following action could be explained by Microsoft's behaviour towards the open source community for the past decade and thus we concluded to refrain from using GitHub as the host of the this repository.

# Future plans

Everything we plan to add in the future in this page will be in [TODO.md](/TODO.md).
