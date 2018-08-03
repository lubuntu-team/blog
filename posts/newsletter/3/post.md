Here is the third issue of This Week in Lubuntu Development. You can read last week's issue [here](https://lubuntu.me/this-week-in-lubuntu-development-2/).

# Changes

## General

Some work was done on [the Lubuntu Manual](https://manual.lubuntu.me/) by Lubuntu contributor Lyn Perrine. Here's what she has been working on:

 * [Start page for Evince](https://github.com/lubuntu-team/lubuntu-manual/commit/320b11b3aa7c55f5c0b96259c5bd78184b3b423a).
 * [Start docs for the Document Viewer](https://github.com/lubuntu-team/lubuntu-manual/pull/26).
 * [Start work on the GNOME MPV documentation](https://github.com/lubuntu-team/lubuntu-manual/commit/2401e8423d2c96e715119bd787000b0d77509afd).
 * [Index fixes](https://github.com/lubuntu-team/lubuntu-manual/pull/28).

We need your help with the Lubuntu Manual! Take a look at PROGRESS.md on our [GitHub](https://github.com/lubuntu-team/lubuntu-manual) or [Launchpad](https://code.launchpad.net/~lubuntu-wiki-docs/lubuntu-manual/+git/lubuntu-manual) repositories, or [contact us](https://lubuntu.me/links/) for ways to help there. Pull requests on GitHub or Merge Requests on Launchpad are always welcome!

Here are some general fixes which have landed for the Bionic Beaver this week:

 * An upstream bugfix release for mpv (0.27.2) has been [merged from Debian](https://launchpad.net/ubuntu/+source/mpv/0.27.2-1ubuntu1). Thanks to [James Cowgill](https://launchpad.net/ubuntu/+source/mpv/0.27.2-1ubuntu1)!
 * A metapackage update for lubuntu-meta [has been done](https://launchpad.net/ubuntu/+source/lubuntu-meta/0.94). Here are the commits which correspond to this metapackage update:
    * [Seed gdebi.](https://github.com/lubuntu-team/lubuntu-seeds/commit/8dcdac62b55b5b325b3290a27961c1862a75e65e)
    * [Recommend ubuntu-report.](https://github.com/lubuntu-team/lubuntu-seeds/commit/cb0b37d32adbd117f046cdf59eb2e91b0ea0a0dc)
       * This allows us to utilize the opt-out metrics collection that will help us make Lubuntu better. If you don't want to use this on your system, you have the ability to opt out during the installation process. **If you opt out during the installation process, NOTHING will be collected. We value users' privacy, and although this data is absolutely anonymous, if they do not wish to report it, they don't have to.**
       * This change comes from Ubuntu, and is not a Lubuntu-specific addition.
 * Here are some other seed updates which aren't reflected in the metapackages:
    * [Add some additional language support.](https://github.com/lubuntu-team/lubuntu-seeds/commit/e052f7e028c5f3a1f053a6b12bb5e08dc0ab8d69)
    * [Seed samba-common-bin explicitly to live-share, as a missed recommends of cifs-utils.](https://github.com/lubuntu-team/lubuntu-seeds/commit/4bc6b3ab5947e17bc0d81c9ef51782041d89002f) Thanks to [Adam Conrad](https://launchpad.net/~adconrad)!
    * [Make sure the slideshow is installed...](https://github.com/lubuntu-team/lubuntu-seeds/commit/2516455666ad13c1fd8c99292d6de17eeb1686b1)

## Lubuntu Next

We have been busy landing the Qt 5.9.5 stack in the Bionic Beaver, which, as we're publishing this, has landed in the proposed pocket of 18.04.

We also worked on security updates for Calibre, which have been released to all users of [Trusty](https://launchpad.net/ubuntu/+source/calibre/1.25.0+dfsg-1ubuntu1.2), [Xenial](https://launchpad.net/ubuntu/+source/calibre/2.55.0+dfsg-1ubuntu0.2), and [Artful](https://launchpad.net/ubuntu/+source/calibre/3.7.0+dfsg-2ubuntu0.1). Huge thanks to the Ubuntu Security Team, specifically [Leonidas S. Barbosa](https://launchpad.net/~leosilvab) and [Marc Deslauriers](https://launchpad.net/~mdeslaur), for assisting in landing these updates!

Lastly, we helped to fix a race condition between sddm and logind in Bionic. This has been [released](https://launchpad.net/ubuntu/+source/sddm/0.17.0-1ubuntu4) to users. Please also note that sddm now starts on tty1 rather than tty7 (as it always has) in Bionic.

## Infrastructure and Project Changes

We continued [to have discussions](https://lists.ubuntu.com/archives/ubuntu-release/2018-April/004387.html) around reforming the milestone process in Ubuntu. We will let you know when something final has been decided.

# Roadmap

You can find the Bionic Beaver release schedule [here](https://wiki.ubuntu.com/BionicBeaver/ReleaseSchedule). This week is Bionic's [Final Freeze](https://wiki.ubuntu.com/FinalFreeze) and [Release Candidate](https://wiki.ubuntu.com/ReleaseCandidate) period. Additionally, Tuesday (typically) is the last day translations can get into the archive, as it's [Language Pack Translation Deadline](https://wiki.ubuntu.com/LanguagePackTranslationDeadline).

This means that any upload into the Ubuntu Archive past Thursday needs thorough vetting to ensure that it breaks nothing within the release. This means a higher degree of stability for Bionic going forward, with any non-release-critical bugs being postponed to go in as [a Stable Release Update](https://wiki.ubuntu.com/StableReleaseUpdates).

This means that next week is release week for Lubuntu 18.04! :D

We need your help testing so we can release in a week from Thursday! Keep your eyes peeled for updates to [the ISO QA Tracker](http://iso.qa.ubuntu.com/) with a milestone called "Bionic Final" and [let us know](https://lubuntu.me/links/) how things go. We are still aware of two bugs that need to be fixed ([non-Latin characters are improperly displayed on the alternate images](https://bugs.launchpad.net/bugs/1754646), [Install Lubuntu fails with Permission Denied](https://bugs.launchpad.net/bugs/1754174) (which needs help from people very familiar with that stack)) so please do not re-report these, but rather, if you have any additional notes that would help, please do comment on the bug reports, or just mark yourself as affected.

# Miscellaneous

Lubuntu will be at LinuxFest NorthWest 2018, come say hello! You can find Release Manager Simon Quigley running the Ubuntu booth, and QA Team Lead Walter Lapchynski at the conference as well.

You can find more details about the conference [here](https://linuxfestnorthwest.org/conferences/lfnw18).

We have a new Lenny!

![Lenny holding a Raspberry Pi](https://lubuntu.me/wp-content/uploads/2018/08/lennypi.png)

Thanks to the Artwork Team for designing this. :)

# Contact us

Feel free to get in touch with us [here](https://lubuntu.me/links/) for support, and for press/marketing purposes or if you have a private inquiry, you can get in touch with Release Manager Simon Quigley [here](mailto:tsimonq2@lubuntu.me).
