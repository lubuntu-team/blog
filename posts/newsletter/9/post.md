This is the ninth issue of The Lubuntu Development Newsletter. You can read the last issue [here](https://lubuntu.me/this-week-in-lubuntu-development-8/).

NOTICE

# Changes

## General

We've been polishing the desktop more, but work has been blocked by the still ongoing Qt transition.

The 16.04 to 18.04 upgrade has now been enabled! Please do let us know if there's any issues. [Here's](https://www.youtube.com/watch?v=QhdQIzyscGw) a video we made when 17.04 went End of Life; the instructions are still current.

Our main developer, Simon Quigley, [became an Ubuntu Core Developer](https://lists.ubuntu.com/archives/ubuntu-devel/2018-August/040436.html) this past Monday! He now has access to the entire Ubuntu archive.

### Desktop Experience

 - We have split the Qt style plugins into separate binary packages. This will eventually result in us not shipping the broken Blackberry style, for example, by default.
 - For WiFi connection editing using nm-tray, we now use QTerminal. Long term, this will be a native Qt dialog, but it's getting close for this cycle.
 - The LXQt Panel spacer plugin now has an autoexpansion option, like in LXDE.

### Calamares

 - We wrote a Calamares module called `automirror` which will automatically select an Ubuntu mirror based on your geographic location. We are working on upstreaming this for other distributions to use.
 - A minimum password strength is now enforced. This is to help promote secure passwords and prevent easy brute force attacks. We're going to be strengthening this as time goes on.
 - Calamares [adds](https://phab.lubuntu.me/rCALASETTINGSa2e6868a2a61c4e15770cc965c0b4b001c332e81) the user to less groups by default. This fixes various issues and makes Lubuntu more consistent with other flavors.

## Infrastructure and Project Changes

### Lubuntu is switching to Wayland

Lubuntu will be switching to Wayland by default for 20.10.

We are going to do this by porting Openbox to use the Mir [display server](https://mir-server.io/), Drew DeVault's [QtLayerShell](https://github.com/SirCmpwn/qtlayershell), and other associated bits.

**Q:** Why are you switching to Wayland?
**A:** The X implementation is old and won't be updated to address the way desktop Linux is used today. Window managers are an afterthought, and many things aren't implemented correctly. Wayland is a modern take on the Linux display system.

**Q:** What about people with NVIDIA graphics cards?
**A:** More details to solve, but the plan is to get this working with those graphics cards by that time.

**Q:** I thought Mir was abandoned when the Ubuntu Touch platform was dropped?
**A:** Mir survived, and still has a team of Canonical employees working on it.

More details to come; feel free to leave comments below.

### Miscellaneous

As always, feedback is appreciated.

# Want to help?

One of the easiest ways to get involved with Lubuntu and help us make this release the best one yet is to test Lubuntu and report bugs.

You can learn how to write an excellent bug report that helps us solve your issue quicker by reading [this guide](https://www.chiark.greenend.org.uk/~sgtatham/bugs.html).

More information about testing on Lubuntu can be found [here](https://phab.lubuntu.me/w/testing/).

# Translations

We have [a Weblate instance](https://translate.lubuntu.me/projects/) available for translations. Right now there are not many strings to translate, but as time goes on, we will add more.

This week, Henrik Christiansen helped us translate Calamares into Danish. Thank you!

Do you speak a language that isn't available to translate there? Let us know in the comments or [elsewhere](https://lubuntu.me/links/) and we will add that language.

Here are the translators who have contributed so far:

 - Henrik Christiansen (Danish)
 - Hans P. Möller (German, Spanish)
 - Daniel Absmeier (German)
 - Luís Rafael Gomes (Portuguese)
 - Lucas A. V. Dantas (Portuguese (Brazil))
 - Marcin Mikołajczak (Polish)
 - Tony Cuesta Escobar (Catalan)
 - Einar Mostad (Norwegian Bokmål)

Thank you for your valuable contributions!

# Roadmap

You can find the Cosmic Cuttlefish release cycle [here](https://wiki.ubuntu.com/CosmicCuttlefish/ReleaseSchedule).

You can stop expecting features on August 23, 2018 when Feature Freeze is put into effect. The beta is slotted for September 27, 2018 and the final release date for October 18, 2018.

Here are some major, Lubuntu-specific features you can expect before the release:

 - The beginnings of a welcome center (more details to come).
 - Calamares polish, including an additional module for more packages to be installed.

Our artwork team is still working on Lenny, and we'll let you know when we have Lenny Cuttlefish. :)

# In the Press

Did you find any exceptional stories about Lubuntu? [Let us know](https://lubuntu.me/links/) and we'll be happy to include them here.

# Contact us

Follow us on [Twitter](https://twitter.com/LubuntuOfficial) for the latest Lubuntu updates! Don't use Twitter because it's not free software? No worries! Follow us on [Mastodon](https://mastodon.technology/@lubuntu) where the same content is published.

Feel free to get in touch with us [here](https://lubuntu.me/links/) for support, and for press/marketing purposes or if you have a private inquiry, you can get in touch with Release Manager Simon Quigley [here](mailto:tsimonq2@lubuntu.me).
