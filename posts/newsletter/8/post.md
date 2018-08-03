Here is the eighth issue of This Week in Lubuntu Development. You can read the last issue [here](https://lubuntu.me/this-week-in-lubuntu-development-7/).

NOTICE

# Changes

## General

This week was focused on polishing the installer experience and the desktop in general. Here are the changes made, with links to the full details.

#### Desktop Experience

 - [LXPanel-Qt: Don't auto-unmute the volume when it's changed.](https://phab.lubuntu.me/rLXQTPANELPACKAGING9635deb67b79e0483f89baa61b855428b688913b)
    - [Upstream commit.](https://github.com/lxqt/lxqt-panel/commit/41259bb4a9c58876e68337a287d968b4ed9fb7e4)
    - [Upstream bug report.](https://github.com/lxqt/lxqt/issues/1520)
    - If something is playing way too loud on your computer, now you can mute the volume, change it, and unmute, without the volume unmuting while you're changing it.

## Infrastructure and Project Changes

### Lubuntu Blog

The official Lubuntu blog is now [being kept](https://phab.lubuntu.me/source/blog/) under Git in our Phabricator instance. All blog posts from here on out will be written in Markdown and then published using the scripts there.

### Phabricator

### Miscellaneous

As always, feedback is appreciated.

# Bugs

## Incoming / Fix needed

 - [Lubuntu 18.10 lxqt-panel - 2 Notifications on log-in: 2 shortcuts "cannot be registered"](https://pad.lv/1781511)
 - [xdg user-dirs not being read/stored correctly for desktop icon in left panel](https://pad.lv/1768961)
    - Filed upstream: [Error when using a non-start disk for location of personal files.](https://github.com/lxqt/lxqt/issues/1389)
 - ["Format" partition edit option appears to keep reverting to "Keep"](https://pad.lv/1773610)
 - [Custom partition mount point not kept with "OK"; kept with <Enter>](https://bugs.launchpad.net/ubuntu/+source/calamares/+bug/1773608)
 - [sddm will not start lxqt desktop correctly](https://pad.lv/1781392)
 - [Calamares fails in UEFI mode after external command in Lubuntu Cosmic](https://pad.lv/1781015)

## Solved / Marked as invalid/duplicate

 - [Two usual install options may have been absent](https://pad.lv/1773613)
    - We're taking a new direction with the installer that doesn't necessarily involve these options directly.
 - [lubuntu fails to install on real hardware uefi](https://pad.lv/1781539)
    - Marked as a duplicate of: [Calamares fails in UEFI mode after external command in Lubuntu Cosmic](https://pad.lv/1781015)

## Solved
 - [Lubuntu Cosmic can't determine my location](https://pad.lv/1781310)
 - [Lubuntu Cosmic Has a "Install Lubuntu 18.10" on the desktop](https://pad.lv/1781309)
 - [Calamares fails after external command (cannot remove non-existing file) in Lubuntu Cosmic](https://pad.lv/1780977)
 - [Calamares fails after external command checking for UEFI mode in Lubuntu Cosmic](https://pad.lv/1780875)

## Want to help?

One of the easiest ways to get involved with Lubuntu and help us make this release the best one yet is to test Lubuntu and report bugs.

You can learn how to write an excellent bug report that helps us solve your issue quicker by reading [this guide](https://www.chiark.greenend.org.uk/~sgtatham/bugs.html).

More information about testing on Lubuntu can be found [here](https://phab.lubuntu.me/w/testing/).

# Translations

We have [a Weblate instance](https://translate.lubuntu.me/projects/) available for translations. Right now there are not many strings to translate, but as time goes on, we will add more.

Do you speak a language that isn't available to translate there? Let us know in the comments or [elsewhere](https://lubuntu.me/links/) and we will add that language.

Here are the translators who have contributed so far:
 - Henrik Christiansen (Danish)
 - Hans P. Möller (German, Spanish)
 - Daniel Absmeier (German)
 - Luís Rafael Gomes (Portuguese)
 - Lucas A. V. Dantas (Portuguese (Brazil))
 - Marcin Mikołajczak (Polish)
 - Tony Cuesta Escobar (Catalan)

Thank you for your valuable contributions!

# Roadmap

You can find the Cosmic Cuttlefish release cycle [here](https://wiki.ubuntu.com/CosmicCuttlefish/ReleaseSchedule).

You can stop expecting features on August 23, 2018 when Feature Freeze is put into effect. The beta is slotted for September 27, 2018 and the final release date for October 18, 2018.

Here are some major, Lubuntu-specific features you can expect before the release:

 - The beginnings of a welcome center (more details to come).
 - Calamares polish, including an additional module for more packages to be installed.
 - A plan for replacing Openbox, the current window manager used in Lubuntu.

Our artwork team is still working on Lenny, and we'll let you know when we have Lenny Cuttlefish. :)

# In the Press

This section is for highlighting exceptional Lubuntu coverage since the last issue.

 - [Lubuntu 18.10 May Support 32-Bit PCs If There's Demand, Here's How You Can Help](https://news.softpedia.com/news/lubuntu-18-10-may-support-32-bit-pcs-if-there-s-demand-here-s-how-you-can-help-521998.shtml)

Did you find any other exceptional stories about Lubuntu? [Let us know](https://lubuntu.me/links/) and we'll be happy to include them here.

# Contact us

Feel free to get in touch with us [here](https://lubuntu.me/links/) for support, and for press/marketing purposes or if you have a private inquiry, you can get in touch with Release Manager Simon Quigley [here](mailto:tsimonq2@lubuntu.me).
