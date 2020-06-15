# Q&As

## Why create this repository?

The reason behind this action could be explained by the lack of repositories which has managed to unite tips & tricks and resources regarding GNU/Linux gaming in one repository with the aim of reducing the amount of search queries required by the user to look up certain information regarding the situation of a game on Linux, how to emulate specific games and so on. There are a lot of interesting projects, such as ACO, which we deem worthy of fame and have thus included those in this repo.

### Why GitLab over GitHub?

Due to the recent change of ownership to GitHub, the open source project hosting service, to Microsoft, we have decided not to maintain the following repository on their server. The reasoning behind the following action could be explained by Microsoft's behaviour towards the open source community for the past decade and thus we concluded to refrain from using GitHub as the host of the this repository.

### Why not just contribute to the Arch wiki?

I am aware of the [Arch wiki / Gaming](https://wiki.archlinux.org/index.php/Gaming) page, but despite the Arch wiki having constant attention, it is not a place where people take the time and effort to look at it. I did contribute in the Arch wiki several times, but I then realised that not many people will look into it despite having this much attention, so I stopped contributing. [Here is an example in Reddit](https://www.reddit.com/r/linux_gaming/comments/fyuqc7/a_fantastic_amd_gpu_gui_software_for_linux/fn2723y?utm_source=share&utm_medium=web2x) of a person recently discovering CoreCtrl, when it was mentioned in the [Arch wiki](https://wiki.archlinux.org/index.php/AMDGPU#GUI_tools) a couple of months prior to the date of the release of the thread.

#### Why not just promote it then?

Because the Arch wiki has been promoted by many youtubers already, and it is also a meme for the epicc arch linux users btw xddd!1!11

### Why not add Manjaro?

Because we do not agree with Manjaro's practices and outcome. While this repository is about gaming, we still consider that security is important for the end user. The issues we have observed from Manjaro are the following:

- **Developers**
	- The Manjaro developers have done a lot of controversies. There is a brief summary that explains the lack of proper maintenance to the distribution:
		- https://github.com/vizs/manjarno

- **Security and Privacy**
	- ~~[Manjaro **does not** have a security policy (like SELinux) enabled by default](https://forum.manjaro.org/t/manjaro-why-you-have-no-selinux/128757). The lack of a security policy brings to an [increased amount of kernel-level security vulnerabilities](https://www.cvedetails.com/product/47/Linux-Linux-Kernel.html?vendor_id=33). On top of that, the lack of a security policy can also decrease the privacy of the user, because packages will have the permissions to view the whole filesystem, resources and more.~~ CORRECTION: Manjaro does use AppArmor instead, but it is [hardly used](https://www.reddit.com/r/linux/comments/g7f1y1/awesome_gnulinux_gaming_a_curated_list_of_awesome/fop4hsr?utm_source=share&utm_medium=web2x). The poor use of a security policy can decrease the privacy and security of the user because any package will have all the permissions to view the whole filesystem, resources and more.
	- ~~Manjaro holds back packages for several weeks, **including security updates**, which makes security updates arrive a couple of weeks later.~~ CORRECTION: While Manjaro does keep some packages, for example Firefox, up to date, the only packages that *are* being updated are [very few (7)](https://gitlab.manjaro.org/security-overlay), while the other packages are still outdated. This can potentially decrease the security of a user's device nonetheless as the packages get released in Manjaro a couple of days (or even weeks) later.

- **Instability and bugs that are non-existant in Arch**
	- Manjaro has had a lot of issues with bugs and instability that were non-existant in Arch. One example to this is users having issues with Pipewire hogging all the RAM of their device:
		- https://forum.manjaro.org/t/after-upgrade-no-sound-pipewire-100-cpu-load-system-freeze/131580
		- https://forum.manjaro.org/t/troubleshooting-random-system-freeze/106554
		- https://www.reddit.com/r/ManjaroLinux/comments/fpydtg/pipewire_process_consuming_almost_all_of_my_ram/

- **Extras**
	- In the [Manjaro wiki, it is written clearly that you "Use the AUR at your own risk!"](https://wiki.manjaro.org/index.php/Arch_User_Repository#Overview). The issue with this is when using Pamac or Octopi, the users are a couple of clicks away to enabling the AUR, and both Pamac and Octopi **do not** mention you the disadvantages of the AUR whatsoever. Further, Manjaro will not support you if you have issues related to the AUR, which this is not mentioned in Pamac and Octopi either.

**We** do not recommend Manjaro to the users because of their poor and distrustful practices, but we will not restrict you from using it. You are free to use anything you want.
