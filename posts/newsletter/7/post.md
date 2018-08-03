Here is the seventh issue of This Week in Lubuntu Development. You can read the last issue [here](https://lubuntu.me/this-week-in-lubuntu-development-6/).

NOTICE

# Changes

## General

This week was focused on polishing the installer experience and the desktop in general. Here are the changes made, with links to the full details.

### Lubuntu Artwork

 * [Rename sddm-theme-lubuntu-chooser to sddm-theme-lubuntu.](https://phab.lubuntu.me/rART0477ab4875887327fa545e094c4af687226a95ec)
 * [Since Ubuntu's sddm is hardcoded to use the Breeze theme, add postinst and prerm scripts which install the Lubuntu SDDM theme as the Breeze theme. Conflict against sddm-theme-breeze accordingly.](https://phab.lubuntu.me/rART8a631ad0bc7ba379170cf8cafe24ac11bc9624d4)
 * [Change the SDDM theme wallpaper to the default 18.04 one.](https://phab.lubuntu.me/rART5cdb2f8c602dbddaa83ce34515c82e731d920d56)
 * [Fix the description for sddm-theme-lubuntu.](https://phab.lubuntu.me/rARTa00aad5f02402ee2bd08487762ee8dcf962d8d87)

### Lubuntu Seed

 * [Don't pull in update-notifier, which is GTK-based and pulls in other unnecessary dependencies.](https://phab.lubuntu.me/rSEED83446ec4ebcf5048d843e3c0b1e778f60344d19e)
 * [Instead of using a blanket dependency on lxqt which pulls in some extra recommends that we don't need, be more granular in the dependencies.](https://phab.lubuntu.me/rSEEDf895921ffc2a57fd4be6a6f5644db652932bdc47)
 * [Rename sddm-theme-lubuntu-chooser to sddm-theme-lubuntu.](https://phab.lubuntu.me/rSEED9a2177b06c1eb3fe8f7fc397be8ccd0ce9f8e9fb)
 * [Remove the minimal install file, which doesn't work with Calamares. We have something else in mind.](https://phab.lubuntu.me/rSEEDb535573700457f145cf98926c1b3d7a7d774a2dd)
 * Replace [dmz-cursor-theme](https://phab.lubuntu.me/rSEEDd8a8b733998c3b880602f73bca9510431e8b3bcf) with [breeze-cursor-theme](https://phab.lubuntu.me/rSEEDbca3f39b4f1dc9609dc2d1367e2e717bec4c9afa).
 * [Unseed Calibre because normal users don't usually need it.](https://phab.lubuntu.me/rSEEDee53b3ab2d0d16a5e10a9593188dd7d4f7ee3746)
 * [Install Vim by default.](https://phab.lubuntu.me/rSEEDc4a41c8b4709a005609874fe184e4f6ee12c856e)
 * [Don't pull in some GTK-based Openbox recommends.](https://phab.lubuntu.me/rSEED870ab0223d0fb9a955e98c8c6faba2e71a066c1a)

### Calamares settings

 * [Enable GeoIP support for the timezone detection by default](https://phab.lubuntu.me/rCALASETTINGSe7f71611133ac3c780f828b9fb561c2ed276f595) and later [fix it](https://phab.lubuntu.me/rCALASETTINGS4091552f748eb26c32d2d8e6241058bc4a88a494).
 * [Fix the slideshow so it is visible.](https://phab.lubuntu.me/rCALASETTINGS7fabcbcae72336824dc11448edb34a375087a4c6)

#### Desktop Experience

 * [QTermWidget: Add patch reworking memory management of filter-related objects.](https://phab.lubuntu.me/rQTERMWIDGETPACKAGINGedd363472bdc8f581faecd756c4ea4e8b89f810f)
    * [Upstream bug report.](https://github.com/lxqt/qterminal/issues/358)
    * [Upstream commit.](https://github.com/lxqt/qtermwidget/commit/0154e036c702b82ebe4b12bed30085247451362c)
    * In certain contexts, this disallowed a user from right-clicking on a link and selecting "Open Link" (in the browser) or "Copy Link Address" because that part of the context menu would immediately disappear. This commit fixes that.
 * [QTerminal: Add patch adjusting for the API changes in QTermWidget](https://phab.lubuntu.me/rQTERMINALPACKAGINGc84b3f3e666e75721afd2f82b3b6307626625900).
    * [Upstream commit.](https://github.com/lxqt/qterminal/commit/cbdb9e2b107768a4e44b1890007eb44f73a2a1ba)
    * This makes an adjustment in QTerminal for the above API changes.
 * [LibFM-Qt: Add LXQt Archiver integration.](https://phab.lubuntu.me/rLIBFMQTPACKAGING48279cbc1423a04666dfc31b118ed437e3b8a9a5)
    * [Upstream commit.](https://github.com/lxqt/libfm-qt/commit/9a3bf23581543aada5095604a0fea4a13d15a61a)
 * [LibFM-Qt: Fix failure to open smb:// caused by incorrect file info handling.](https://phab.lubuntu.me/rLIBFMQTPACKAGINGb0dea37e48336ac38c500f7f6d3f407b853f4b15)
    * [Upstream commit.](https://github.com/lxqt/libfm-qt/commit/1a6fa2632388ffcc57ce723501a588c90b940f93)
    * [Upstream pull request explaining this a bit better; some functionality may need to be fixed still.](https://github.com/lxqt/libfm-qt/pull/210)
 * [LibFM-Qt: Use the window text color for the places pane.](https://phab.lubuntu.me/rLIBFMQTPACKAGING07036c23c2e8ae1989e2d057f072a24e29b0b2c4)
    * [Upstream commit.](https://github.com/lxqt/libfm-qt/commit/87df010ed548856fad8fc822cfb8390ea1118ccc)
    * [Upstream bug report.](https://github.com/lxqt/pcmanfm-qt/issues/696)
 * [LibQtXDG: Fix inability to drag a menu item to the desktop.](https://phab.lubuntu.me/rLIBQTXDGPACKAGING8ff1b3cedbf9477af466de94003bd43cc52fffb7)
    * [Upstream commit.](https://github.com/lxqt/libqtxdg/commit/a26e700818af2b3afe93d70a645b69b102741592)
    * [Upstream bug report.](https://github.com/lxqt/lxqt/issues/1512)
 * [LXQt Notification Daemon: Keep notification height when others are added and/or removed.](https://phab.lubuntu.me/rLXQTNOTIFICATIONDPACKAGING6f67315566d534594dbb07234eea60f2ada85eff)
    * [Upstream bug report.](https://github.com/lxqt/lxqt-notificationd/commit/db5707d739870cee6ffe140171b6d80ff7cbd218)
    * This fixes many notifications from exponentially stacking up and overlapping each other.
 * [Openbox: Add a backup recommends on obconf-qt, so obconf isn't always pulled in.](https://launchpad.net/ubuntu/+source/openbox/3.6.1-7ubuntu2)
 * [Software Properties: Port the KDE frontend to pure Qt (not reviewed yet)](https://code.launchpad.net/~tsimonq2/software-properties/port-away-from-kde/+merge/349592)

### Miscellaneous

Our Lubuntu metapackage is now [in Git](https://phab.lubuntu.me/source/lubuntu-meta/).

When starting the ISO, [it now says](https://code.launchpad.net/~tsimonq2/debian-cd/lubuntu-cosmic-changes/+merge/345792) "Start Lubuntu" instead of "Try Lubuntu without installing" / "Install Lubuntu".

As always, feedback is appreciated.

## Stable Releases (Lubuntu Classic)

 * [GtkTreeView separators garbled display with Lubuntu default theme](https://pad.lv/1781689) was fixed and uploaded to the queue. [Here](https://phab.lubuntu.me/rART53dcb9c9a1c7) are the packaging changes. Please help test!
 * Help us test LTS to LTS upgrades! We are looking for help in testing and filing bugs to fix before the 18.04.1 release on July 26th.

## Bugs

### Incoming / Fix needed

 * [Lubuntu 18.10 lxqt-panel - 2 Notifications on log-in: 2 shortcuts "cannot be registered"](https://pad.lv/1781511)
 * [xdg user-dirs not being read/stored correctly for desktop icon in left panel](https://pad.lv/1768961)
    * Filed upstream: [Error when using a non-start disk for location of personal files.](https://github.com/lxqt/lxqt/issues/1389)
 * ["Format" partition edit option appears to keep reverting to "Keep"](https://pad.lv/1773610)
 * [Custom partition mount point not kept with "OK"; kept with](https://bugs.launchpad.net/ubuntu/+source/calamares/+bug/1773608)
 * [sddm will not start lxqt desktop correctly](https://pad.lv/1781392)
 * [Calamares fails in UEFI mode after external command in Lubuntu Cosmic](https://pad.lv/1781015)

### Marked as invalid/duplicate

 * [Two usual install options may have been absent](https://pad.lv/1773613)
    * We're taking a new direction with the installer that doesn't necessarily involve these options directly.
 * [lubuntu fails to install on real hardware uefi](https://pad.lv/1781539)
    * Marked as a duplicate of: [Calamares fails in UEFI mode after external command in Lubuntu Cosmic](https://pad.lv/1781015)

### Solved

 * [Lubuntu Cosmic can't determine my location](https://pad.lv/1781310)
 * [Lubuntu Cosmic Has a "Install Lubuntu 18.10" on the desktop](https://pad.lv/1781309)
 * [Calamares fails after external command (cannot remove non-existing file) in Lubuntu Cosmic](https://pad.lv/1780977)
 * [Calamares fails after external command checking for UEFI mode in Lubuntu Cosmic](https://pad.lv/1780875)

### Want to help?

One of the easiest ways to get involved with Lubuntu and help us make this release the best one yet is to test Lubuntu and report bugs.

You can learn how to write an excellent bug report that helps us solve your issue quicker by reading [this guide](https://www.chiark.greenend.org.uk/~sgtatham/bugs.html).

More information about testing on Lubuntu can be found [here](https://phab.lubuntu.me/w/testing/).

## Infrastructure and Project Changes

### Phabricator

We now take advantage of [the calendar](https://phab.lubuntu.me/calendar/) on our Phabricator instance.

### Translations

We now have [a Weblate instance](https://translate.lubuntu.me/projects/)!

Right now there are not many strings to translate, but as time goes on, we will add more.

Do you speak a language that isn't available to translate there? Let us know in the comments or [elsewhere](https://lubuntu.me/links/) and we will add that language.

Please note: if you are a registered user, you will be able to contribute translations with only one stop gap, but if you are contributing anonymously, there's quite a bit more work involved for us. So please do try and get an account there, so we can give you credit for your hard work. :)

Here are the translators who have contributed so far:

 * Henrik Christiansen (Danish)
 * Hans P. Möller (German, Spanish)
 * Daniel Absmeier (German)
 * Luís Rafael Gomes (Portuguese)
 * Lucas A. V. Dantas (Portuguese (Brazil))
 * Marcin Mikołajczak (Polish)
 * Tony Cuesta Escobar (Catalan)

Thank you for your valuable contributions!

### State of i386 Images Going Forward

Lubuntu has, for the entirety of its lifetime, supported the i386 architecture (commonly referred to as 32-bit). But, as hardware is becoming newer, we are starting to have a hard time maintaining i386 going forward, as the machines are becoming rare. We understand that there is still interest for keeping the i386 images for Lubuntu, and thus, have not dropped it like the majority of other Ubuntu flavors have.

However, **when we stop receiving adequate testing on the ISO QA tracker for i386, especially before a milestone or release, we believe this indicates the end of user interest for supporting it**. As such, we will only continue to support these images if there is adequate testing for them, and they will no longer be a release blocker if the images are not tested (they will not be released in that case, and will not receive further releases).

So, if you have i386 machines that you are still using Lubuntu on, **please help us test, or the images will no longer be released**.

Furthermore, we will need help fixing i386-specific bugs should they arise. **If more than a few i386-specific bugs go unfixed as well, including any release-blocking bugs, the images will no longer be released.**

# Roadmap

You can find the Cosmic Cuttlefish release cycle [here](https://wiki.ubuntu.com/CosmicCuttlefish/ReleaseSchedule).

You can stop expecting features on August 23, 2018 when Feature Freeze is put into effect. The beta is slotted for September 27, 2018 and the final release date for October 18, 2018.

Here are some major, Lubuntu-specific features you can expect before the release:

 * The beginnings of a welcome center (more details to come).
 * Calamares polish, including an additional module for more packages to be installed.
 * A plan for replacing Openbox, the current window manager used in Lubuntu.

Our artwork team is still working on Lenny, and we'll let you know when we have Lenny Cuttlefish. :)

# In the Press

This section is for highlighting exceptional Lubuntu coverage since the last issue.

 * [Lubuntu 18.04 Review: Stable and Dependable As Always](https://itsfoss.com/lubuntu-review/amp/)

Did you find any other exceptional stories about Lubuntu? [Let us know](https://lubuntu.me/links/) and we'll be happy to include them here.

# Contact us

Feel free to get in touch with us [here](https://lubuntu.me/links/) for support, and for press/marketing purposes or if you have a private inquiry, you can get in touch with Release Manager Simon Quigley [here](mailto:tsimonq2@lubuntu.me).
