Thanks to all the hard work from our contributors, Lubuntu 19.04 has been released! With the codename Disco Dingo, Lubuntu 19.04 is the 16th release of Lubuntu and the second release of Lubuntu with LXQt as the default desktop environment.

# Support lifespan

Lubuntu 19.04 will be supported for 9 months, until January 2020. If you need Long Term Support, it is recommended you [use Lubuntu 18.04 LTS instead](https://lubuntu.me/downloads/) (with LXDE), which will be supported for 3 years, until April 2021.

Older Lubuntu versions have reached their end of life and are not supported anymore, with the exception of 18.04, which is supported until April 2021, and 18.10, which is supported until August 2019.

# What is Lubuntu?

Lubuntu is an official Ubuntu flavor which uses the Lightweight Qt Desktop Environment (LXQt). The project’s goal is to provide a lightweight yet functional Linux distribution based on a rock-solid Ubuntu base. Lubuntu provides a simple but modern and powerful graphical user interface, and comes with a wide variety of applications so you can browse, email, chat, play, and be productive.

This is the second Lubuntu release with LXQt as the main desktop environment. The Lubuntu project, in 18.10 and successive releases, will no longer support the LXDE desktop environment or tools in the Ubuntu archive, and will instead focus on the LXQt desktop environment. You can find the following major applications and toolkits installed by default in this release:

 - LXQt 0.14.1.
 - Qt 5.12.2.
 - Mozilla Firefox 66, which will receive updates from the Ubuntu Security Team throughout the support cycle of the release.
 - The LibreOffice 6.2.2 suite, with the Qt 5 frontend.
 - VLC 3.0.6, for viewing media and listening to music.
 - Featherpad 0.9.3, for notes and code editing.
 - Discover Software Center 5.15.4, for an easy, graphical way to install and update software.
 - The powerful and fast email client Trojitá 0.7 to get you to inbox zero in no time.

You can find a variety of other applications installed which aim to enhance your experience while staying out of the way of your normal workflow.

## Installer

Lubuntu uses the [Calamares](https://calamares.io/) system installer in place of the Ubiquity installer that other flavors use. 19.04 ships with Calamares 3.2.4, but the important fixes have been cherry-picked from 3.2.5 for stability.

One notable feature in this release is working full-disk encryption. HUGE thanks to [Jonathan Carter](https://jonathancarter.org/) and [Dmitry Shachnev](https://mitya57.me) for helping this land.

**Note:** In case of full-disk encryption, unlike the other flavors, Calamares does not create a separate, unencrypted */boot* partition. Therefore, LUKS 1 is the default, so that GRUB 2 can decrypt the partition. This is because GRUB 2 [does not have support for LUKS 2](https://savannah.gnu.org/bugs/?55093) and Ubuntu switched to it by default in this release.

Some notable upstream features and fixes include:

  - Easier customization of Calamares configurations using XDG configuration variables.
  - The default fullscreen mode can now be set.
  - RAID devices are now supported in the partitioner.
  - The Austrian keymap is now properly handled.

For a full description of the new features and fixes, see the upstream announcements for [3.2.3](https://calamares.io/calamares-3.2.3-is-out/) and [3.2.4](https://calamares.io/calamares-3.2.4-is-out/).

Lastly, due to popular demand, the minimum RAM requirement has been lowered to 0.5 GB of RAM. (The RAM consumption is around 300-400 MB after startup).

## Desktop Environment

Lubuntu 19.04 ships with the latest release of the LXQt desktop environment, [0.14.1](https://lxqt.org/release/2019/02/26/lxqt-0141/). Some notable features and fixes in this release include:

  - File manager/desktop icons:
    - Trash, Home, Computer, and Network icons have been added to the desktop for easy accessibility.
    - Hidden icons are now shadowed.
    - Split view has been implemented.
    - Allow full names to be shown instead of only display names.
    - Fixed view icons with HiDPI scaling.
    - Theme icons are preferred for view actions.
  - Image viewer:
    - An image's EXIF data can now be rendered.
    - A confirmation dialog is now present when using "Save as" without a file extension.
    - Added ImgBB as an upload provider.
    - Added the ability to annotate images.
    - Added a copy button to the upload dialog.
  - Terminal:
    - Margins have been added.
    - History-based tab switching has been implemented.
  - GTK Appearance settings have now been upstreamed.
  - Touchpad settings have been vastly improved.
  - Notification history has been implemented for persistent notifications.
  - Various security improvements for the LXQt sudo authenticator module.
  - MANY translation updates and other bugfixes.

## Lubuntu Manual

The Lubuntu Team has been hard at work in polishing a Lubuntu Manual book to make it easy for new and experienced users alike to use their system more productively. The book can be found at [manual.lubuntu.me](https://manual.lubuntu.me/).

We want to thank Lyn Perrine for all the hard work she has put into the Lubuntu Manual recently, because the majority of the text in the manual right now is what she has written. Thank you!

# Where can I download it?

You can download Lubuntu 19.04 on [our downloads page](https://lubuntu.me/downloads).

# Contributing to Lubuntu

## How can I help?

We can always use more help! **No matter your skill level or your technical experience, there's something you can help with that can make a huge difference in Lubuntu.** [Join](https://lubuntu.me/links/) us on our chat which is bridged three ways to Matrix, Telegram, and IRC and talk to us there. Whether you know another language, have some spare time to help us test Lubuntu, are good at writing documentation, or just want to stay "in the know," that is the place to be.

Another great method to get involved is bug reporting. If you notice an issue, please file a bug using [the instructions on the Lubuntu Wiki](https://phab.lubuntu.me/w/bugs/).

Don't want to file a bug? [Let us know](https://lubuntu.me/links/) what the problem is (in detail, enough that we can reproduce it) and we can assist you in filing one or do it ourselves.

## Contributors

We would like to thank the following contributors for dedicating some of their time to Lubuntu this cycle. Thank you!

 - [Simon Quigley](https://twitter.com/tsimonquigley2)
 - [Walter Lapchynski](https://polka.bike)
 - [Lyn Perrine](https://phab.lubuntu.me/p/lynorian/)
 - [Wendy Hill](https://www.wendyhillphoto.com/)
 - [Samuel Banya](http://www.musimatic.net/)
 - [Hans Möller](https://twitter.com/hpmoller)
 - [Tony Cuesta Escobar (Wolfenprey)](https://twitter.com/Wolfen48K)
 - [Dan Simmons](https://mastodon.technology/@kc2bez)
 - [Chris Guiver](https://launchpad.net/~guiverc)
 - [Raman Sarda](https://theloudspeaker.home.blog/)
 - [Thomas Ward](https://launchpad.net/~teward)
 - Many more contributors!


Known Bugs
==========

Please also check the [known bugs reported in the Ubuntu Release Notes](https://wiki.ubuntu.com/DiscoDingo/ReleaseNotes#Known_issues) for more common bugs affecting all Ubuntu flavors.

Installer
---------

 * Apparently unexpected order in language selection on welcome module ([1801498](https://bugs.launchpad.net/calamares/+bug/1801498))
 * Lubuntu doesn't have a "minimal install" option in the installer ([1769473](https://bugs.launchpad.net/ubuntu/+source/calamares-settings-ubuntu/+bug/1769473)); //workaround available//
 * No clear indication that format has been selected ([1773610](https://bugs.launchpad.net/calamares/+bug/1773610))
 * Summary window expands, cutting off buttons with 800x600 screen ([1824758](https://bugs.launchpad.net/calamares/+bug/1824758))

Desktop Environment
-------------------

 * lxqt-session allocates memory for process output never read ([1823416](https://bugs.launchpad.net/ubuntu/+source/lxqt-session/+bug/1823416))
 * Using $BROWSER environment variable to set default browser creates several problems ([182654](https://bugs.launchpad.net/ubuntu/+source/lxqt-session/+bug/1824654)); //workaround available//
 * LXQt Arc theme + Breeze widgets hides menu scroll bar when searching ([1787734](https://bugs.launchpad.net/ubuntu/+source/lubuntu-artwork/+bug/1787734))
 * Multiple monitors wallpaper handled as only one big monitor ([1730411](https://bugs.launchpad.net/lxqt/+bug/1730411))
 * Openbox shortcuts involving the Windows/Meta/Super key conflict with the use of that key to open the menu in lxqt-globalkeys ([1802501](https://bugs.launchpad.net/ubuntu/+source/lubuntu-default-settings/+bug/1802501)); //workaround available//
 * Sensors Widget forgets custom colors when re-opening the Configure Panel window ([1812826](https://bugs.launchpad.net/lxqt/+bug/1812826))

Applications
------------

 * usb-creator-kde shows the install popup after a few seconds of launching without any input ([1629715](https://bugs.launchpad.net/ubuntu/+source/usb-creator/+bug/1629715)); //workaround available//
 * Trojita segfaults when repeatedly sorting ([1797665](https://bugs.launchpad.net/ubuntu/+source/trojita/+bug/1797665))
 * QTerminal dropdown shortcut key does not consistently toggle visibility ([1795998](https://bugs.launchpad.net/ubuntu/+source/qterminal/+bug/1795998))
 * nm-tray is missing a native Qt UI for editing connections ([1782579](https://bugs.launchpad.net/nm-tray/+bug/1782579))
 * Lubuntu lacks an input method for Korean and other languages ([1810634](https://bugs.launchpad.net/ubuntu/+source/lubuntu-meta/+bug/1810634)); //workaround available//
