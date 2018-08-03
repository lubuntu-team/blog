Here is the fifth issue of This Week in Lubuntu Development. You can read the previous issue [here](https://lubuntu.me/this-week-in-lubuntu-development-4/).

NOTICE

# Changes

## General

[Lubuntu 18.04 was released!](https://lubuntu.me/bionic-released/)

Some work was done on [the Lubuntu Manual](https://manual.lubuntu.me/) by Lubuntu contributor Lyn Perrine and Lubuntu Translations Team Lead Marcin Mikołajczak. You can see the commits they have made [here](https://github.com/lubuntu-team/lubuntu-manual/compare/d977ae6493c9312ca7c89abfafce5b16c598dac6...9c251f8c01b5dc2fa41ad1f35300d766908ac3da).

We need your help with the Lubuntu Manual! Take a look at PROGRESS.md on our [GitHub](https://github.com/lubuntu-team/lubuntu-manual) or [Launchpad](https://code.launchpad.net/~lubuntu-wiki-docs/lubuntu-manual/+git/lubuntu-manual) repositories, or [contact us](https://lubuntu.me/links/) for ways to help there. Otherwise, if you know another language, you can also help with translations! Pull requests on GitHub or Merge Requests on Launchpad are always welcome.

The **Cosmic Cuttlefish** is now [open for development](https://lists.ubuntu.com/archives/lubuntu-devel/2018-May/001173.html) so the Lubuntu team has been hard at work syncing and merging things from Debian, and starting work on bugfixes. Here's what we have done in the Cosmic cycle this far:

 * [Synced](https://launchpad.net/ubuntu/+source/lxqt-l10n/0.12.0-5) a new version of lxqt-l10n from Debian which includes some packaging updates.
 * [Synced](https://launchpad.net/ubuntu/+source/transmission/2.94-1) a new upstream version of Transmission, 2.94, from Debian. Thanks to [Julian Andres Klode](https://launchpad.net/~juliank) for sponsoring the upload!

A lot of core changes have happened for the Cosmic Cuttlefish this far which may affect Lubuntu; far too many to list here. Thanks to everyone who has helped open up the archive this cycle!

## Infrastructure and Project Changes

### Lubuntu is switching to LXQt for 18.10

This is a huge change we have been planning for years, and we're finally doing it.

Simon Quigley, Lubuntu's Release Manager, broke the news on [the Ask Noah Show](http://podcast.asknoahshow.com/63) and Softpedia Linux [wrote an article](https://news.softpedia.com/news/lubuntu-is-finally-moving-to-lxqt-by-default-with-the-lubuntu-18-10-release-520951.shtml) the next day. We've received mixed feedback so far from the people we've talked to, so here's a quick FAQ:

**Q:** Why are you switching? **A:** This is for quite a few reasons, but here are the main ones:

 * Upstream LXDE development has drastically slowed, and most if not all of the desktop is GTK 2, which is losing support and will eventually be phased out.
 * LXQt development upstream is fairly active, and LXQt is based off of the Qt 5 framework, which has a tendency to be more stable than GTK (no dependency on GNOME).

**Q:** LXQt is not yet on 1.0; do you have concerns about stability? **A:** Upstream LXQt only hits 1.0 when it's Wayland-complete, and is not necessarily an accurate mark of stability. LXQt was marked as "stable" for the 0.11 release (arguably for the 0.10 release), and with steady progress on 0.13, we could reach 1.0 sooner than later.

**Q:** Lubuntu has been promising to switch for ages. Why has it taken this long? **A:** This was for two main reasons which have been resolved: lack of team resources, and the technology hasn't been in place quite yet. We don't want to switch close to an LTS release, because **we take users' stability very seriously**. LXDE has been rock solid and stable, and while it is potentially subject to bitrot, tends to work very well. So the ideal time to switch is right **after** the LTS so we have close to two years to iron things out before rolling it out to LTS users. We didn't decide to make the switch after the 16.04 LTS release because we were having some glaring issues, and team resources were scarce. Between that time and now, Lubuntu has also [changed Release Managers](https://lists.ubuntu.com/archives/lubuntu-devel/2017-February/000968.html) and gained new members of the team. So, after evaluation both in person at LinuxFest NorthWest among part of the Lubuntu team, and online with the whole Lubuntu team shortly after the release, we decided this was the right time to jump.

**Q:** Will Lubuntu still be as light as it once was? **A:** Yes and no. Lubuntu, with this transition, is no longer what it originally was. As we use more modern technologies, Lubuntu will use more resources (which is inevitable). **However**, while we won't have the amount of granular minimalism that we once had, the statistics we have seen internally strongly suggest that users won't see much of an increase. Some people may have noticed that in the release announcement for 18.04, we bumped the system requirements to 1 GB of RAM at minimum (among other things); this wasn't because Lubuntu had actually gotten larger, it was because we hadn't updated those particular values in ten years. Yes, Lubuntu can probably run with less, but as we move forward, applications like web browsers can and will use more resources.

**Q:** I have Lubuntu running in production environments which need support of an LXDE Lubuntu (18.04 or 16.04) for longer than the length of the support cycle. Can I still get support? **A:** [Contact Simon Quigley](mailto:tsimonq2@lubuntu.me). We are absolutely open to working with you, and, in fact, we are in the process of setting up a more formal framework for this. More details to come.

**Q:** Lxqt? lxqt? LxQt? LXQT? What is it? **A:** It's LXQt. It used to be named LxQt, but it has since been renamed LXQt.

So far, to work towards this, we have [reworked the seeds](https://github.com/lubuntu-team/lubuntu-seeds/compare/99390b0315d02f368ba75275f107b83336fe1033...a91c70bc6fdf76aef5da04bc8bf9605267824955), [updated the metapackage](https://launchpad.net/ubuntu/+source/lubuntu-meta/1.0), and made [a fix to our Calamares settings](https://launchpad.net/ubuntu/+source/calamares-settings-ubuntu/2) to fix the installer. Expect steady progress, and furthermore, [the daily ISOs](http://cdimage.ubuntu.com/lubuntu/daily-live/current/) use LXQt now.

# Roadmap

We don't have a Cosmic Cuttlefish release schedule yet at the time of writing, but when we do, you can find it [here](https://wiki.ubuntu.com/CosmicCuttlefish/ReleaseSchedule). The **tentative** 18.10 release date is October 18, 2018.

Have an idea for what the next Lenny should look like? Let the Artwork Team know in the comments. :)

# Miscellaneous

Simon Quigley and Walter Lapchynski from Lubuntu were at LinuxFest NorthWest 2018! Here are some pictures from the event:

<img src="https://pictor.ialis.me/media_attachments/files/001/113/047/original/c7a6fdd90eede72e.jpg" alt="ePaper watch" width="200px"/>

Here's an ePaper watch that William Wold (who works on the Mir team) made.

![Day 1 booth aftermath](https://pictor.ialis.me/media_attachments/files/001/113/082/original/12a1b5414fd20476.jpg)

Lots of the stickers we had laid out were taken, so Walter brought some additional ones.

![Python programming session](https://pictor.ialis.me/media_attachments/files/001/113/096/original/e68247b54a24f48b.jpg)

Valorie Zimmerman from Kubuntu (top right) helps with the booth while Dustin Krysak from Ubuntu Budgie (bottom right) writes Python with his daughter, while Walter and Simon were at a talk.

![Day 2 of the booth](https://pictor.ialis.me/media_attachments/files/001/118/419/original/b0de66a8e2d770b7.jpeg)

Simon helps a conferencegoer (right) put Linux on their 2009 MacBook Pro (center) while Dustin (left back) talks with another conferencegoer.

Lubuntu would like to thank Ubuntu for helping fund this trip for Walter and Simon. You can donate to the same funds which made this possible [here](https://www.ubuntu.com/download/desktop/contribute) (while increasing the "Community" slider).

# Contact us

Feel free to get in touch with us [here](https://lubuntu.me/links/) for support, and for press/marketing purposes or if you have a private inquiry, you can get in touch with Release Manager Simon Quigley [here](mailto:tsimonq2@lubuntu.me).
