Thanks to all the hard work from our contributors, Lubuntu 18.10 has been released! With the codename Cosmic Cuttlefish, Lubuntu 18.10 is the 15th release of Lubuntu and the first release of Lubuntu with LXQt as the default desktop environment, with support until July of 2019.

NOTICE

# Welcome to LXQt

<img style="float: center; width: 33%;" src="https://phab.lubuntu.me/file/data/zwng7o6qanhvvucgajdc/PHID-FILE-djx4vzahriz23c5622vu/Screenshot_20181007_Desktop.png" />

This is the first Lubuntu release with LXQt as the main desktop environment. The Lubuntu project, in 18.10 and successive releases, will no longer support the LXDE desktop environment or tools in the Ubuntu archive, and will instead focus on the LXQt desktop environment. You can find the following major applications and toolkits installed by default in this release:

 - LXQt 0.13.0, with many bugfixes and improvements backported from upstream.
 - Qt 5.11.1, which is the first point release in the Qt 5.11 series.
 - Mozilla Firefox 62, which will receive updates from the Ubuntu Security Team throughout the support cycle of the release.
 - The LibreOffice 6.1.2 suite, with the Qt 5 frontend.
 - VLC 3.0.4, for viewing media and listening to music.
 - Featherpad 0.9.0, for notes and code editing.
 - Discover Software Center 5.13.5, for an easy, graphical way to install and update software.

You can find a variety of other applications installed which aim to enhance your experience while staying out of the way of your normal workflow.

# What is Lubuntu?

Lubuntu is an official Ubuntu flavor which uses the Lightweight Qt Desktop Environment (LXQt). The project’s goal is to provide a lightweight yet functional Linux distribution based on a rock-solid Ubuntu base. Lubuntu provides a simple but modern and powerful graphical user interface, and comes with a wide variety of applications so you can browse, email, chat, play, and be productive.

# Where can I download it?

You can download Lubuntu 18.10 on [our downloads page](https://lubuntu.me/downloads/).

# Known Issues and Workarounds

## Issues with workarounds

LXQt treats all monitors as one when painting the desktop background. We plan on solving this in a more native way by the 19.04 release, but in the meantime, Lubuntu contributor Hans P. Möller has written [a script](https://git.launchpad.net/~hmollercl/stitchwp/tree/stitchWP.sh) which can be used as a workaround for treating all of the backgrounds differently.

We have not ported over the "Additional drivers" tab from software-properties-gtk to software-properties-qt, which can be used for installing additional CPU and graphics drivers. As a workaround, you can install the `kubuntu-driver-manager` package which will provide this functionality.

## Issues with fixes

The default LibreOffice theme that ships on the ISOs is the default Adwaita theme, which is not consistent with the system theme. However, if you update the LibreOffice package immediately after installing Lubuntu, this issue will be fixed.

# Would you like to help?

We can always use more help! No matter your skill level, there's likely something you can help with that can make a huge difference in Lubuntu. Feel free to [join](https://lubuntu.me/links/) us on Telegram (which is bridged three ways to Matrix, Telegram, and IRC) and talk to us there. Whether you know another language, have some spare time to help us [test](https://phab.lubuntu.me/w/testing/) Lubuntu, are good at writing documentation, or just want to stay "in the know," that is the place to be.

Another great method to get involved is bug reporting. If you notice an issue please [file a bug](https://bugs.launchpad.net/lubuntu/+filebug) and tag it with "lubuntu".

Don't want to file a bug? [Let us know](https://lubuntu.me/links/) what the problem is (in detail, enough that we can reproduce it) and we can assist you in filing one.

# Stay Connected!

We [publish a newsletter](https://lubuntu.me/category/newsletter/) usually every week which details the work that is currently happening in Lubuntu, including fixed bugs and additional ways you can help.

For the latest Lubuntu information and announcements follow us on [Twitter](https://twitter.com/LubuntuOfficial), [Mastodon](https://mastodon.technology/@lubuntu), or [Telegram](https://t.me/LubuntuOfficial). We have other social media pages and ways to stay connected which you can find [here](https://lubuntu.me/links/).
