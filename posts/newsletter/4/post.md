Here is the fourth issue of This Week in Lubuntu Development. You can read last week's issue [here](https://lubuntu.me/this-week-in-lubuntu-development-3/).

# Changes

## General

Some work was done on [the Lubuntu Manual](https://manual.lubuntu.me/) by Lubuntu contributor Lyn Perrine. You can see the commits she has made [here](https://github.com/lubuntu-team/lubuntu-manual/compare/682d4f639f96c50f9f07a6c13a02b487fd87f8ea...72389683f21cb4d812fcf0b451d0e1fbc077ea82).

We need your help with the Lubuntu Manual! Take a look at PROGRESS.md on our [GitHub](https://github.com/lubuntu-team/lubuntu-manual) or [Launchpad](https://code.launchpad.net/~lubuntu-wiki-docs/lubuntu-manual/+git/lubuntu-manual) repositories, or [contact us](https://lubuntu.me/links/) for ways to help there. Pull requests on GitHub or Merge Requests on Launchpad are always welcome!

The two bugs we listed last week as release blockers for Lubuntu have been fixed:

 * [Install Lubuntu fails with Permission Denied](https://bugs.launchpad.net/bugs/1754174) has been fixed in a way which we can't describe other than it "disappeared." Please yell loudly if this reappears.
 * [Non-Latin characters are improperly displayed on the alternate images](https://bugs.launchpad.net/bugs/1754646) has also been fixed. Many thanks to [Colin Watson](https://launchpad.net/~cjwatson) and [Łukasz Zemczak](https://launchpad.net/~sil2100)!

## Lubuntu Next

Qt 5.9.5 landed in Bionic last week, with [automated tests](https://wiki.ubuntu.com/ProposedMigration) passing very quickly!

Many thanks to [Dmitry Shachnev](https://launchpad.net/~mitya57) for helping a great deal with this update.

Some further updates to SDDM landed, which fix some more race conditions:

 * [Now we start on VT1 we need to avoid collision with plymouth. So take the startup ordering recommended in the sddm.service comments, and currently in use by KDE Neon.](https://launchpad.net/ubuntu/+source/sddm/0.17.0-1ubuntu5)
 * [Apply the fix for the race between sddm and logind to our service template as this is what we install. Drop previous fix-logind-race.patch.](https://launchpad.net/ubuntu/+source/sddm/0.17.0-1ubuntu6)
 * [Always wait for plymouth quit to run before trying to start.](https://launchpad.net/ubuntu/+source/sddm/0.17.0-1ubuntu7)

Many thanks to [Rik Mills](https://launchpad.net/~rikmills) for working on these updates!

## Infrastructure and Project Changes

The proposal regarding getting rid of the Alphas and Beta 1 has been [finalized and adopted](https://lists.ubuntu.com/archives/ubuntu-release/2018-April/004434.html). Thanks to everyone for the discussion!

# Roadmap

You can find the Bionic Beaver release schedule [here](https://wiki.ubuntu.com/BionicBeaver/ReleaseSchedule).

This is release week! Please help test the Bionic Beaver so we can release on Thursday. As Adam Conrad [said](https://lists.ubuntu.com/archives/ubuntu-release/2018-April/004438.html) in his email, the ISOs will be regenerated one last time, with a fresh kernel and `lsb_release` (among other things) being changed to reflect the final release. But, to quote Adam:

## DO NOT DELAY, TEST NOW, FIX BUGS, FILE BUGS, ESCALATE FOR HELP.

Please do [let us know](https://lubuntu.me/links/) if you come across any issues.

# Miscellaneous

Lubuntu will be at LinuxFest NorthWest 2018 this weekend in Bellingham, Washington, USA. Come say hello! You can find Release Manager Simon Quigley running the Ubuntu booth, and QA Team Lead Walter Lapchynski at the conference as well.

You can find more details about the conference [here](https://linuxfestnorthwest.org/conferences/lfnw18).

# Contact us

Feel free to get in touch with us [here](https://lubuntu.me/links/) for support, and for press/marketing purposes or if you have a private inquiry, you can get in touch with Release Manager Simon Quigley [here](mailto:tsimonq2@lubuntu.me).
