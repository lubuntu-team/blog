Here is the eighth issue of This Week in Lubuntu Development. You can read the last issue [here](https://lubuntu.me/this-week-in-lubuntu-development-7/).

NOTICE

# Changes

## General

[Lubuntu 18.04.1 has been released!](https://lubuntu.me/bionic-1-released/)
[Lubuntu 16.04.5 has been released!](https://lubuntu.me/xenial-5-released/)
[We're taking a new direction.](https://lubuntu.me/taking-a-new-direction/)

The past couple of weeks have been focused on more desktop polish and some heavy infrastructure and project changes.

Unfortunately, a lot of the fixes we've been working on are blocked by the in-progress Qt 5.11.1 transition. It has been uploaded to the cosmic-proposed pocket, where it awaits automated testing before it becomes generally installable. More technical details about that process are available [here](https://wiki.ubuntu.com/ProposedMigration).

This transition is also being done in Debian Sid as well.

Huge thanks to [UBports](https://ubports.com/) for contributing financially to allow Lubuntu contributors to spend time on this! You can help sponsor their work (and therefore, some of our work) [here](https://ubports.com/donate).

### Desktop Experience

 - [LXPanel-Qt: Don't auto-unmute the volume when it's changed.](https://phab.lubuntu.me/rLXQTPANELPACKAGING9635deb67b79e0483f89baa61b855428b688913b)
    - [Upstream commit.](https://github.com/lxqt/lxqt-panel/commit/41259bb4a9c58876e68337a287d968b4ed9fb7e4)
    - [Upstream bug report.](https://github.com/lxqt/lxqt/issues/1520)
    - If something is playing way too loud on your computer, now you can mute the volume, change it, and unmute, without the volume unmuting while you're changing it.
 - Default settings:
    - [Remove /usr/share/applications; these files are native in LXQt.](https://phab.lubuntu.me/rDEFAULTSETTINGS758e4746525465c15c1cc7cfec2ba7c38b182d90)
    - [Don't launch a file manager on Ctrl + Alt + D, because that already shows the desktop in LXQt.](https://phab.lubuntu.me/rDEFAULTSETTINGS804d49dfc6350f0c16fd19ec2b44f5b9964191db)
    - [Remove the volume button shortcuts as these are built into LXQt.](https://phab.lubuntu.me/rDEFAULTSETTINGS5209b412656d71f5ecb6296c6a9dc941e9460665)
    - [Double the splitter position for the PCManFM-Qt Places panel.](https://phab.lubuntu.me/rDEFAULTSETTINGSc58864779695ded62d70e34e13c756133a45588b)
    - [gksu -> pkexec in PCManFM-Qt.](https://phab.lubuntu.me/rDEFAULTSETTINGSaaa50f079236906a8f8ac97d96b37c281fcd9d4e)
 - [QTerminal: Remember the maximization state of the window.](https://phab.lubuntu.me/rQTERMINALPACKAGING6a643cd600a187bf472232b0d41ecfa7c932d1f9)
    - [Launchpad bug report.](https://pad.lv/1754496)
    - [Upstream bug report (submitted by us).](https://github.com/lxqt/qterminal/issues/450)
    - [Upstream pull request (submitted by us).](https://github.com/lxqt/qterminal/pull/451)
    - [Upstream commit.](https://github.com/lxqt/qterminal/commit/14b1ee093b6712c4d3e1b6fe832ba353afa3d35a)
 - Move the file dialog from the LXQt Qt Plugin to LibFM-Qt for better platform integration.
    - LibFM-Qt:
        - [Upstream pull request.](https://github.com/lxqt/libfm-qt/pull/243)
        - [Upstream commit.](https://github.com/lxqt/libfm-qt/commit/da5966a5f36bd927cffdfc790da4a96cd5568083)
        - [Packaging commit.](https://phab.lubuntu.me/rLIBFMQTPACKAGING19fd5f3c8be72f799ddb966f68e84bb5521b416c)
    - LXQt Qt Plugin:
        - [Upstream pull request.](https://github.com/lxqt/lxqt-qtplugin/pull/39)
        - [Upstream commit.](https://github.com/lxqt/lxqt-qtplugin/commit/73d20ab01995ca869f8d967535d4969409b22ec3)
        - [Packaging commit.](https://phab.lubuntu.me/rLXQTQTPLUGINPACKAGING0144765ce2217c62aa69d170369c980e6d9e8e26)
 - Add the ability to set GTK themes from within the LXQt Appearance Configuration.
    - [Upstream pull request.](https://github.com/lxqt/lxqt-config/pull/244)
    - [Packaging commit.](https://phab.lubuntu.me/rLXQTCONFIGPACKAGINGae2282e219fa929077a3ebddf9aa79f8df023bff)

### Calamares

 - We [replaced](https://phab.lubuntu.me/rCALASETTINGS88e201e0c82eda4438f78ad949b25a43409556a2) some awfully complex one-liners with more robust lines, thanks to KDE Neon.
    - This also fixed Calamares so it can be installed on BIOS, non-secure boot UEFI, and secure boot UEFI computers, something that was not previously possible.
 - [By default](https://phab.lubuntu.me/rCALASETTINGSec8d1863c8ae49a73cff15547aa773e02d953dfa), GRUB is now installed to `/boot/efi/EFI/ubuntu` instead of `/boot/efi/EFI/lubuntu`.
 - [Make](https://phab.lubuntu.me/rCALASETTINGS912a94ead53188a2f222e3d72a2f8d5e553b7373) `/bin/bash` the default shell.

### Lubuntu Seed

 - [Remove ship; it's no longer used.](https://phab.lubuntu.me/rSEEDd8529092ee6708b0c2693eb338d508c45cf8cba8)
 - [Make vim a recommends, not a hard dependency.](https://phab.lubuntu.me/rSEED1b4ee934da65a22550f43e54725c7d68af75e713)
 - [Recommend zsync by default.](https://phab.lubuntu.me/rSEED2df3b53a1fccffb4bdafa86297189954cb455ccd)

### Miscellaneous

 - [SDDM 0.18.0](https://github.com/sddm/sddm/releases/tag/v0.18.0) has been uploaded to Debian Sid and Ubuntu Cosmic.
    - Packaging changes were made to make it easier for other Ubuntu flavors and derivatives. Instead of hardcoding the Breeze theme in, we now have a theming system in Ubuntu very similar to Debian's, where a package can install their SDDM theme into the ubuntu-theme directory in a postinst script.
    - This fixes CVE-2018-14345; we're looking into cherry-picking this patch into previous stable Ubuntu releases.
 - Thanks to [Nate Graham](https://pointieststick.wordpress.com/) for [the pointer](https://phabricator.kde.org/T9244), we backported fix for [a bug](https://bugreports.qt.io/browse/QTBUG-66036) which visually affected KDE-based programs under HiDPI screens.

## Infrastructure and Project Changes

### Lubuntu Blog

The official Lubuntu blog is now [being kept](https://phab.lubuntu.me/source/blog/) under Git in our Phabricator instance. All blog posts from here on out will be written in Markdown and then published using the scripts there.

We're (slowly) working on converting all of the posts over to Markdown and keeping them there.

Translations for each post are kept under the `l10n` directory of each post (with the file being named like `LANG_CODE.md`) and the localization code is put in a YAML list in the info.yaml (see the 16.04.5 announcement for an example). This is because Weblate does not support translations for Markdown at the moment.

### Lugito

 - In select repositories, Lugito will [automatically](https://phab.lubuntu.me/rLUGITOf91111a1807701daf1c3cdb4ee7bd2db7b57fc6a) comment on bug reports that are in commit messages with a message that the fix is in progress.

### Miscellaneous

As always, feedback is appreciated.

# Bugs

## Incoming / Fix needed

 - [xdg user-dirs not being read/stored correctly for desktop icon in left panel](https://pad.lv/1768961)
    - Filed upstream: [Error when using a non-start disk for location of personal files.](https://github.com/lxqt/lxqt/issues/1389)
 - ["Format" partition edit option appears to keep reverting to "Keep"](https://pad.lv/1773610)
 - [Custom partition mount point not kept with "OK"; kept with <Enter>](https://bugs.launchpad.net/ubuntu/+source/calamares/+bug/1773608)
 - [sddm will not start lxqt desktop correctly](https://pad.lv/1781392)

## Solved

 - [Lubuntu 18.10 lxqt-panel - 2 Notifications on log-in: 2 shortcuts "cannot be registered"](https://pad.lv/1781511)
 - [Calamares fails in UEFI mode after external command in Lubuntu Cosmic](https://pad.lv/1781015)

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

This week we have added Norwegian Bokmål! Thanks to Einar Mostad for translating.

Thank you for your valuable contributions!

## Spanish group

We have [a Lubuntu Spanish Telegram group](https://t.me/lubuntues) that has as many members as [our (English) Development group](https://t.me/lubuntudevel) at the time of writing!

This is a general-purpose Spanish-only Lubuntu group for enthusiasts and contributors alike. Feel free to join!

Thanks to [Wolfenprey](https://twitter.com/Wolfen48K), the newly-appointed head of the Lubuntu Spanish Team, for driving this!

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

## English

 - [Lubuntu 18.10 May Support 32-Bit PCs If There's Demand, Here's How You Can Help](https://news.softpedia.com/news/lubuntu-18-10-may-support-32-bit-pcs-if-there-s-demand-here-s-how-you-can-help-521998.shtml)
 - [Future Lubuntu Releases Won't Focus on Old PCs, Will Offer a Modular Linux OS](https://news.softpedia.com/news/future-lubuntu-releases-won-t-focus-on-old-pcs-will-offer-a-modular-linux-os-522141.shtml)
 - [Ubuntu Linux-based Lubuntu no longer focusing on old hardware after move to LXQt](https://betanews.com/2018/07/30/ubuntu-linux-lubuntu-old-lxqt/)
 - [Destination Linux EP81 - Canonical Fanboys (coverage starts at 26:24)](https://www.youtube.com/watch?v=7xlY0GQ-XvY)

## Spanish

 - [Lubuntu cambia de rumbo: los “equipos obsoletos” ya no son el objetivo](https://www.muylinux.com/2018/07/30/lubuntu-cambia-rumbo/)
 - [Lubuntu ya no será una distro para PCs antiguos](https://www.computekni.com/2018/08/lubuntu-ya-no-sera-una-distro-para-pcs.html)

Did you find any other exceptional stories about Lubuntu? [Let us know](https://lubuntu.me/links/) and we'll be happy to include them here.

# Contact us

Follow us on [Twitter](https://twitter.com/LubuntuOfficial) for the latest Lubuntu updates! We're working on having tweets automatically propogate to [our Mastodon account](https://mastodon.technology/@lubuntu) for people who prefer not to use Twitter.

Feel free to get in touch with us [here](https://lubuntu.me/links/) for support, and for press/marketing purposes or if you have a private inquiry, you can get in touch with Release Manager Simon Quigley [here](mailto:tsimonq2@lubuntu.me).
