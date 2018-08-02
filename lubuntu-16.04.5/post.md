Thanks to all the hard work from our contributors, we are pleased to announce that Lubuntu 16.04.5 LTS has been released!

<!--more-->
# What is Lubuntu?
Lubuntu is an official Ubuntu flavor which uses the Lightweight X11 Desktop Environment (LXDE). The project’s goal is to provide a lightweight yet functional Linux distribution based on a rock solid Ubuntu base. Lubuntu specifically targets older machines with lower resources, but also runs great on newer hardware. Along with a simple but usable graphical user interface, Lubuntu comes with a wide variety of applications chosen for their small footprint so you can browse, email, chat, play, and be productive.

# Where can I download it?
You can download Lubuntu 16.04.5 LTS on [our downloads page](https://lubuntu.me/downloads/).

This announcement on our official website ([Lubuntu.me](https://lubuntu.me/), NOT Lubuntu dot net, which is not run by Lubuntu contributors) replaces the traditional release notes we have provided in the past on the wiki. We have left out some notes that are common to all flavors, so we recommend that you read [the Ubuntu release notes](https://wiki.ubuntu.com/XenialXerus/ReleaseNotes).

## What's The Difference Between Lubuntu 16.04.4 LTS And This Release?
Lubuntu 16.04.5 is a set of images produced for convenience so that a fresh install of the latest Lubuntu LTS does not require as many updates after install (as Lubuntu continues to release Stable Release Updates and security fixes to make your experience as smooth as possible and to fix any bugs, if you want to help us out with this, see below, we always need more help), but is not a new major release of Lubuntu in and of itself. If you do system updates regularly, you are already running Lubuntu 16.04.5 LTS, and if you install Lubuntu on a system using a Lubuntu 16.04.5 LTS image or a previous point release and do system updates, that system will also then be running Lubuntu 16.04.5 LTS.

# How do I get support?
You can get support for Lubuntu [here](https://lubuntu.me/links/).

**Please note that this is the final point release in the 16.04 series, and is only supported until April 2019.**

If you would like commercial support, or more support than is provided on that page (for a low price), [contact Simon Quigley](mailto:tsimonq2@lubuntu.me) and we can discuss options. Please note that this is not provided by Canonical.

# How do I help?
We always need more help! Feel free to [join](https://lubuntu.me/links/) our development channel (which is bridged three ways to Matrix, Telegram, and IRC) and talk to us there. Whether you know another language, have some spare time to help us test Lubuntu, are good at writing documentation, or just want to stay "in the know," that is the place to be.

Otherwise, we [publish a newsletter](https://lubuntu.me/category/newsletter/) usually every week which details the work that is currently happening in Lubuntu, including fixed bugs and ways you can help.

# Known Issues
At the moment, encrypted LVM installs do not work with Lubuntu due to Ubiquity not correctly identifying zram partitions. This is only an issue with 16.04-based images; 18.04-based images work correctly.

[Here](https://bugs.launchpad.net/ubuntu/+source/partman-crypto/+bug/1759732) is the bug report if you would like the full technical details.

As a workaround, you can edit line 158 of `/lib/partman/lib/crypto-base.sh` in a live Lubuntu system as follows:

```
 	for swap in $(cat /proc/swaps); do
 		case $swap in
-		    Filename*)
+		    Filename*|/dev/zram*)
 			continue
 			;;
 		    /dev/mapper/*)
```

Or, you can run `sudo swapoff -a` before installing.

We apologize for the inconvenience; we're exploring different solutions to solve this.

Did we miss something? Please [file a bug](https://bugs.launchpad.net/lubuntu/+filebug) and tag it with "lubuntu".

Don't want to file a bug? [Let us know](https://lubuntu.me/links/) what the problem is (in detail, enough that we can reproduce it) and we can assist you in filing one.
