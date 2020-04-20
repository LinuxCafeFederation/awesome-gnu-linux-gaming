# Awesome GNU/Linux gaming [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of awesome GNU/Linux tips & tricks, games, tools, and resources. Inspired by [awesome-vulkan](https://github.com/vinjn/awesome-vulkan) and other awesome-related projects.

# Overview

This is a hobby project to improve the quality of gaming in Linux because it is possible to improve performance by tweaking your Linux machine. Most Linux distributions have a lot of issues when it comes to gaming performance, as they do not utilise the modern and superior counterparts.

## **Disclaimer**

It is recommended for the Linux user who finds their knowledge regarding the construction of a Linux based distribution limited to use a rather stable Linux distribiution approved by the Linux community instead of using a Linux distributions solely because of what has been advertised in its regard. Many Linux distributions claim to maintain stability and harmony while in actual reality failing to comply with their claims and thus resulting in system failure, confusion and hatred towards what is thought to be the operating system aiming to provide its users with the wonders of Linux for the newcomer.

# Table of contents

- [Utilities](#utilities)
- [Processors](#processors)
	- [AMD](#amd)
	- [Intel](#intel)
- [Graphics cards](#graphics-cards)
	- [AMD](#amd-1)
		- [Xorg](#xorg)
			- [Eliminate screen tearing](#eliminate-screen-tearing)
			- [FreeSync](#freesync)
			- [Others](#others)
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
- [Developers](#developers)
- [YouTube channels](#youtube-channels)
- [Q&As](#qas)
- [Future plans](#future-plans)

# Distributions

*From simplest to complex.*

~~[**Manjaro Linux**](https://manjaro.org/) — Based on [Arch Linux](https://www.archlinux.org/). Attempt from the Manjaro team to provide a GUI installer, as well as test packages before they are released.~~ **WARNING: see *[Why not add Manjaro?](#why-not-add-manjaro).***

[**Pop!_OS**](https://system76.com/pop) — Based on [Ubuntu](https://ubuntu.com/). Attempt from System76 to "de-Canonical-ise" Ubuntu, as well as some minor tweaks for gaming.

[**Fedora**](https://getfedora.org/) — Based on [RHEL](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux). Comes with some performance tools pre-installed such as [**FeralInteractive / gamemode**](https://github.com/FeralInteractive/gamemode).

[**Alpine Linux**](https://www.alpinelinux.org/) — Minimal, simple and secure binary based distribution aimed for performance.

[**Arch Linux**](https://www.archlinux.org/) — Lightweight and independent distribution to provide as much performance with as less time spent.

[**Clear Linux**](https://clearlinux.org/) — Independent distribution by [Intel](https://en.wikipedia.org/wiki/Intel) with various [patches](https://github.com/clearlinux-pkgs/linux) aimed for performance.

[**Gentoo**](https://www.gentoo.org/) — Minimal and secure source based distribution to maximise performance.

# Utilities

[**FeralInteractive / gamemode**](https://github.com/FeralInteractive/gamemode) — A **systemd** daemon/lib to optimise Linux system performance on demand.

[**flightlessmango / MangoHud**](https://github.com/flightlessmango/MangoHud) — A Vulkan and OpenGL overlay for monitoring FPS, temperatures, CPU/GPU load and more.

[**DadSchoorse / vkBasalt**](https://github.com/DadSchoorse/vkBasalt) — A Vulkan post processing layer to enhance the visual graphics of games while barely impacting performance.

[**benjamimgois / GOverlay**](https://github.com/benjamimgois/goverlay) — A Graphical UI to manage Linux overlays, such as MangoHud and vkBasalt.

[**varmd / wine-wayland**](https://github.com/varmd/wine-wayland) — A WINE implementation to play [DirectX 9](https://en.wikipedia.org/wiki/DirectX#DirectX_9) & [DirectX 11](https://en.wikipedia.org/wiki/DirectX#DirectX_11) games in Wayland without the need of X11 or XWayland. **(Arch derivatives only!)**

# Processors

## AMD

[**FlyGoat / RyzenAdj**](https://github.com/FlyGoat/RyzenAdj) — CLI tool to adjust core clock and voltage of Ryzen processors.

[**ryzen-controller-team / ryzen-controller**](https://gitlab.com/ryzen-controller-team/ryzen-controller) — Adjust core clock and voltage of Ryzen processors; front-end for [**FlyGoat / RyzenAdj**](https://github.com/FlyGoat/RyzenAdj).

## Intel

# Graphics cards

## AMD

### **NOTE: this is only for the AMDGPU drivers. We might add AMDGPU-PRO or AMDVLK specific categories later.**

[**ACO compiler**](https://wiki.archlinux.org/index.php/AMDGPU#ACO_compiler) — Open source shader compiler by [Valve Corporations](https://en.wikipedia.org/wiki/Valve_Corporation) to compete with the [LLVM compiler](http://llvm.org/), [AMDVLK drivers](https://github.com/GPUOpen-Drivers/AMDVLK) drivers and [Windows 10](https://en.wikipedia.org/wiki/Windows_10).

[**Overclocking**](https://wiki.archlinux.org/index.php/AMDGPU#Overclocking) — Guide to overclock an AMD GPU using the AMDGPU drivers.

[**sibradzic / amdgpu-clocks**](https://github.com/sibradzic/amdgpu-clocks) — CLI tool to adjust the core clock, memory and voltage of AMD graphics cards.

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

[**mcicolella / awesome-emulators-simulators**](https://github.com/mcicolella/awesome-emulators-simulators#consoles) — A curated list of software emulators and simulators of PCs, home computers, mainframes, consoles, robots and much more.

# Custom Kernels

There are various alternative Linux kernels available for Linux distributions, each one has it's own patchset, but most custom kernels' goal is to increase performance and stability.
Kernel packages are installed onto the file system under /boot/. To be able to boot into kernels, the boot loader has to be configured appropriately. 

## ZEN/Liquorix Kernel
ZEN/Liquorix kernels is a distro kernel replacement built using the best configuration and kernel sources for desktop, multimedia, and gaming workloads.
Although Liquorix is based on ZEN and specially optimized for Debian and Debian based distibutions.
Some of their major features are "Hard Kernel Preemption", "TCP BBR Congestion Control" and "Zen Interactive Tuning".

### Installation
### Pop!_OS
To install Liquorix Kernel on Pop!_OS all you have to do is run:
```
sudo add-apt-repository ppa:damentz/liquorix && sudo apt update
```
and
```
sudo apt install linux-image-liquorix-amd64 linux-headers-liquorix-amd64
```

# Developers

[**μProf**](https://developer.amd.com/amd-uprof/) — Performance analysis tool for AMD for applications running on Windows and Linux operating systems.


# YouTube channels

**FlightlessMango** — https://www.youtube.com/channel/UCDmXLiZTBaFuCOXjy6mdw5w

# Q&As

### Why create this repository?

The reason behind this action could be explained by the lack of repositories which has managed to unite tips & tricks and resources regarding GNU/Linux gaming in one repository with the aim of reducing the amount of search queries required by the user to look up certain information regarding the situation of a game on Linux, how to emulate specific games and so on. There are a lot of interesting projects, such as ACO, which we deem worthy of fame and have thus included those in this repo.

### Why GitLab over GitHub?

Due to the recent change of ownership to GitHub, the open source project hosting service, to Microsoft, we have decided not to maintain the following repository on their server. The reasoning behind the following action could be explained by Microsoft's behaviour towards the open source community for the past decade and thus we concluded to refrain from using GitHub as the host of the this repository.

In short: f*ck Microshit. I want my freedom.

### Why put "*username / gitPage*" instead of only "*gitPage*" for project repositories?

Because I highly dislike to not credit the maintainers.

### Why not just contribute to the Arch wiki?

Because the Arch wiki does not get enough attention. I did contribute in the Arch wiki, but I realised that not many people look into it. Here is an example of a [Reddit thread I have replied before](https://www.reddit.com/r/linux_gaming/comments/fyuqc7/a_fantastic_amd_gpu_gui_software_for_linux/fn2723y?utm_source=share&utm_medium=web2x).

#### Why not just promote it then?

Because the Arch wiki has been promoted by many youtubers, and it is also a meme for the epicc arch linux users btw xddd!1!11

### Why not add Manjaro?

Because Manjaro sucks.

- **Incompetent developers**
	- The Manjaro developers are filled with incompetent developers. Here are summaries to prove Manjaro developers' incompetency:
		- https://rentry.co/manjaro-controversies
		- https://github.com/vizs/manjarno
- **Bad security**
	- Manjaro does not have a security policy enabled by default, which this itself already makes Manjaro several times more unsecured than most other distributions: https://forum.manjaro.org/t/manjaro-why-you-have-no-selinux/128757. They then [reply](https://forum.manjaro.org/t/manjaro-why-you-have-no-selinux/128757/4) and have the audacity to say that it does not matter.
	- Manjaro holds back packages for several weeks, including security patches, which makes security updates come a couple of weeks later, which makes it even more insecure: http://allanmcrae.com/2013/01/manjaro-linux-ignoring-security-for-stability/
- **Instability and bugs that are non-existant in Arch**
	- Arch is already unstable, but Manjaro takes the instability two steps further and produces more bugs that are/were never present in Arch. Here are some examples of people having issues with Pipewire in Manjaro, which was non-existent in Arch:
		- https://forum.manjaro.org/t/after-upgrade-no-sound-pipewire-100-cpu-load-system-freeze/131580
		- https://forum.manjaro.org/t/troubleshooting-random-system-freeze/106554
		- https://www.reddit.com/r/ManjaroLinux/comments/fpydtg/pipewire_process_consuming_almost_all_of_my_ram/
- **Dishonesty**
	- They claim to have their own repository, but it is just the Arch repository delayed for a couple of weeks.
	- In their [website](https://manjaro.org/): ```Manjaro is not a consumer-oriented operating system. You have full control and you will not be prevented from breaking your own installation [...]``` They tell you that you have full control of the system, which is not true because you cannot use other init systems for example, since they have been deprecated:
		- https://forum.manjaro.org/t/manjaro-openrc-will-be-discontinued/28387
# Future plans

Everything we plan to add in the future in this page will be in [TODO.md](/TODO.md).
