Here is the second issue of This Week in Lubuntu Development. You can read last week's issue [here](https://lubuntu.me/this-week-in-lubuntu-development-1/).

NOTICE

# Changes

## General

 * We released 18.04 Final Beta this week. You can find the announcement [here](https://lubuntu.me/lubuntu-bionic-beaver-final-beta-has-been-released/).
    * The [encrypted LVM bug](https://bugs.launchpad.net/ubuntu/+source/partman-auto-crypto/+bug/1759732) we described last week has been fixed (thanks to [Steve Langasek](https://launchpad.net/~vorlon)!).
    * We are still working hard to try to find what is causing [the other bug](https://bugs.launchpad.net/ubuntu/+source/ubiquity/+bug/1754174) that is causing Lubuntu to be uninstallable when selecting "Install Lubuntu" on the boot screen. For now, you can select "Try Lubuntu" and go to the installer from there, and it will work. **Please avoid filing duplicate bugs, but you can mark that bug as affecting you as well.**
 * Since Lubuntu's seeds are different, we needed adjustments to the tooling to be able to support the minimal install option. Those changes have landed, and this option is now being utilized.
    * [https://code.launchpad.net/~tsimonq2/livecd-rootfs/lubuntu-seed-mangling/+merge/342064](https://code.launchpad.net/~tsimonq2/livecd-rootfs/lubuntu-seed-mangling/+merge/342064)
    * [https://launchpad.net/ubuntu/+source/livecd-rootfs/2.517](https://launchpad.net/ubuntu/+source/livecd-rootfs/2.517)
    * Thanks to [Iain Lane](https://launchpad.net/~laney)!
    * This adds it to the seed: [https://github.com/lubuntu-team/lubuntu-seeds/commit/806639acd4f2c1720da06b9cde9a6af11013c07c](https://github.com/lubuntu-team/lubuntu-seeds/commit/806639acd4f2c1720da06b9cde9a6af11013c07c)
 * A Stable Release Update was issued to users of Lubuntu 16.04 fixing some LXPanel issues after switching to a Right-to-Left language.
    * [https://bugs.launchpad.net/ubuntu/xenial/+source/lxpanel/+bug/1537334](https://bugs.launchpad.net/ubuntu/xenial/+source/lxpanel/+bug/1537334)
    * [https://launchpad.net/ubuntu/+source/lxpanel/0.8.2-1ubuntu2.1](https://launchpad.net/ubuntu/+source/lxpanel/0.8.2-1ubuntu2.1)

## Lubuntu Next

 * Per the advice of the Ubuntu Technical Board, Lubuntu has adjusted the support length for Lubuntu Next to only be nine months, officially.
    * [https://code.launchpad.net/~tsimonq2/ubuntu-archive-publishing/lubuntu-next-support-cycle-adjustment/+merge/342475](https://code.launchpad.net/~tsimonq2/ubuntu-archive-publishing/lubuntu-next-support-cycle-adjustment/+merge/342475)
    * Thanks to [Steve Langasek](https://launchpad.net/~vorlon)!

## Infrastructure and Project Changes

I [proposed](https://lists.ubuntu.com/archives/ubuntu-release/2018-April/004387.html) to the Ubuntu Release Team and other flavors (as well as the Desktop and Server teams) last night that we should discontinue the Alpha and Beta 1 milestones in favor of monthly coordinated testing of all ISOs we typically ship in a release. Feel free to let us know your thoughts as a comment below or on the mailing list if you have anything for us to consider.

# Roadmap

You can find the Bionic Beaver release schedule [here](https://wiki.ubuntu.com/BionicBeaver/ReleaseSchedule). This week is Bionic's Kernel Freeze and Non-Language-Pack Translation Deadline.

In layman's terms, this means that as of Thursday at 21 UTC, 18.04's usage of Linux 4.15 is final, and if you want to help with translating any of the programs [listed on the wiki page](https://wiki.ubuntu.com/NonLanguagePackTranslationDeadline), there are no guarantees that your translations will be included in the release (although they will certainly be included in the 18.10 release and on, so we encourage help in translating those applications regardless of the release status :) ).

In technical terms, this means that while the Linux kernel will still bump ABI (as is usual with kernel updates, unfortunately), it will not bump the patch version string. As for translations, a manual export might not be done from Rosetta past that date into the source packages (which would likely have to happen before Final Freeze).

Next week, the RC comes out, and Final Freeze is put into place. This means that only critical updates will go into the Lubuntu release, and whatever updates don't get spun into the ISOs will arrive via an update. From there, Lubuntu 18.04 will receive point releases like a normal LTS.

In terms of the LTS releases, there's nothing unusual in the roadmap. The tentative date for 16.04.5 is August 5th, 2018, and our support for 16.04 ends in April of 2019.

One point of clarification that should be made from last week is that Lubuntu Next will **not** ship as a release ISO for 18.04, but will stay as a daily ISO. The packages in the archive (so, the LXQt stack) will only be supported for nine months. See last week's newsletter for why that is.

# In the Press

This section is for highlighting exceptional Lubuntu coverage throughout the past week.

## English

 * [Ubuntu Podcast Season 11 Episode 05 -- "High Five"](http://ubuntupodcast.org/2018/04/05/s11e05-high-five/).
 * [Softpedia Linux - "Lubuntu Next Adopts the Calamares Installer, Continues to Be in Development" by Marius Nestor](http://news.softpedia.com/news/lubuntu-next-is-adopting-the-calamares-installer-continues-to-be-in-development-520533.shtml).

## Español

 * [MuyLinux - "Lubuntu Next cambiará el instalador por defecto a Calamares" por Eduardo Medina](https://www.muylinux.com/2018/04/04/lubuntu-next-instalador-calamares/).

# Miscellaneous

Lubuntu will be at LinuxFest NorthWest 2018, come say hello! You can find Release Manager Simon Quigley running the Ubuntu booth, and potentially QA Team Lead Walter Lapchynski at the conference as well.

You can find more details about the conference [here](https://linuxfestnorthwest.org/conferences/lfnw18).

# Contact us

Feel free to get in touch with us [here](https://lubuntu.me/links/) for support, and for press/marketing purposes or if you have a private inquiry, you can get in touch with Release Manager Simon Quigley [here](mailto:tsimonq2@lubuntu.me).
