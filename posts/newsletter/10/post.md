This is the tenth issue of The Lubuntu Development Newsletter. You can read the last issue [here](https://lubuntu.me/lubuntu-development-newsletter-9/).

NOTICE

# Changes

## General

As always, more polish!

A lot of the polish changes we had made, including a new version of SDDM, migrated with Qt 5.11.1 a few days ago. Thanks to everyone involved in driving the transition!

### Desktop Experience

 - All packages which are non-essential have [now been demoted](https://phab.lubuntu.me/rSEEDfc9c1389cf0e9928a7bd2cf1b460d18a3264b605) to recommends in our metapackage.
 - In LXQt Sudo, [text is no longer cut off](https://phab.lubuntu.me/rLXQTSUDOPACKAGING196967406935b3d8e0aafb32968bb73b96778dcb).
 - You can now (optionally) [override](https://phab.lubuntu.me/rLXQTPANELPACKAGINGcac77df97847bc4008fae01446f121e68275e248) the icon theme for the panel. This has laid the groundwork so we can choose an icon theme which looks better visually for the panel.
 - Network Manager Tray, the pure Qt implementation of a NM indicator icon we use in Lubuntu, has [been blacklisted](https://phab.lubuntu.me/rDEFAULTSETTINGS9e192e55224221d4d01b0ceeb9575699d54c0d5a) from the menu. This avoids users getting confused and starting several duplicate nm-tray sessions.
 - We [fixed](https://phab.lubuntu.me/rDEFAULTSETTINGS51d5e2fa96937089ee8e39b56bf1224f48f5e8f4) running commands as root with the built-in PCManFM-Qt option.

### Calamares

 - XFS support has now been [enabled](https://phab.lubuntu.me/rSEED8a2e4b0be76619f93dc78b27bfb56970dd5e171a) with Calamares.
 - We fixed the autologin feature for the Lubuntu installer. If you installed a daily with autologin enabled before August 21st, we recommend that you reinstall.
    - [The fix our settings needed.](https://phab.lubuntu.me/rCALASETTINGS4f328dc3d72a509463c368ef1514ac5080e87977)
    - [The fix needed in upstream Calamares.](https://phab.lubuntu.me/rCALAPACKAGING4ef8ded762c93b8b797802cb3abf02c8b7d92b0b)
 - Before the last newsletter, we enabled password checking. After some vocal feedback, we [asked the community](https://lists.ubuntu.com/archives/lubuntu-devel/2018-August/001221.html) on [our development mailing list](https://lists.ubuntu.com/mailman/listinfo/lubuntu-devel) what they thought about it, and an overwhelming majority had the same opinion; it should warn, but you should still be able to set a weak password. While the Lubuntu Team **very strongly recommends choosing a strong password when installing Lubuntu**, we have [disabled](https://phab.lubuntu.me/rCALASETTINGSfcc2036633b31b2ebb4dca6d41421aacfbef7265) password checking.

## Infrastructure and Project Changes

### New Documentation

We have started several pieces of documentation on our Phabricator instance which go into more detail about how to contribute to Lubuntu. Here are the ones we are currently working on:

 - [Packaging Tutorial](https://phab.lubuntu.me/w/packaging-tutorial/)
 - [Packaging Policy Document](https://phab.lubuntu.me/w/packaging/)

We also have a general [Contributors Guide](https://phab.lubuntu.me/w/contributor-guide/) that has been started. All of these documents are a work in progress, and will be updated as we have the manpower.

### Social Media Changes

Lubuntu has recently held [our Twitter account](https://twitter.com/LubuntuOfficial) (which is now bidirectionally mirrored to [our Mastodon account](https://mastodon.technology/@lubuntu)) as the main source for informing users of changes and promoting positive information. Although different members have accounts in different places, we also maintain presences on [Reddit](https://www.reddit.com/r/Lubuntu), [Google+](https://plus.google.com/communities/102737741860934586009), and [Instagram](https://www.instagram.com/lubuntu_os/) among others.

Namely, we have several Facebook groups: [Lubuntu Official](https://www.facebook.com/groups/lubuntu.official/), [Lubuntu QA](https://www.facebook.com/groups/LubuntuQA/), and [Lubuntu Offtopic](https://www.facebook.com/groups/lubuntu.offtopic/) as well as [our only official page](https://www.facebook.com/Lubuntu.Official.Page/) (there is an unofficial one that we do not control by the same people who control Lubuntu DOT net, and we don't recommend following them).

We are looking for people with a particular interest in maintaining and inspiring discussion on our Reddit, Facebook, and Google+ groups. At the moment, these either have support requests or are just links to these blog posts from the team. If you are interested, please [send an email to Simon Quigley](mailto:tsimonq2@lubuntu.me) with the subject "I want to help maintain Lubuntu's SITE presence" (where "SITE" is either Reddit, Facebook, or Google+).

If nobody steps up to help administer these groups, we are likely to shut them down within the next month or so. We will be happy to train whoever is interested.

Also, we are opening our support and offtopic Telegram groups to the public. **Please note that the following links are temporary and may change at any time; feel free to ask us in the main development channel for the updated ones if these links change.** [Support](https://t.me/joinchat/DH6s1ELAZusx_9mFamoScg), [offtopic](https://t.me/joinchat/DH6s1EKjxEYc6M3YGRGt-Q). These links will become available on [our main links page](https://lubuntu.me/links/) within the coming days.

### Answering Questions About Wayland

In the last newsletter we announced that we are going to switch to Wayland via Mir for 20.10. Here are a few common questions we have received, and some answers for them.

**Q:** Why did you choose 20.10? Why not sooner?
**A:** Some people speculated that this was because the work to actually port Openbox would take this long. It will likely take much less time than that, but the real reason for waiting this long is because 20.04 is the first LTS we will ship with LXQt. By shipping an LTS with an already tried-and-true X stack, it is less we have to worry about supporting before we know it is ready. Therefore, we will likely have an alternative session with Wayland once it is ready and ship that in the LTS, but not truly support that as the **default** until the 20.10 dailies.

**Q:** Why choose Mir instead of wlroots?
**A:** Mir has support for NVIDIA graphics cards figured out, while wlroots does not. A core principle of Lubuntu is to not break the operating system if we can help it. That also goes for support for a very popular graphics card brand. Here is a comment that Chris Halse Rogers from the Mir team left on the last blog post that is worth highlighting:

> About NVIDIA support: [this PR](https://github.com/MirServer/mir/pull/415) has just been merged, fixing the eglstream-kms platform (which supports NVIDIA, when you turn on the modesetting support in the NVIDIA driver).
>
> It does not yet support GL clients, but the extensions are in place and that's one of the next things on my list.

Additionally, Alan Griffiths from the Mir team responded to a comment asking about remote desktops, saying:

> This is something every Wayland compositor has to deal with, it has to happen and consensus will come.
>
> From the Mir perspective the core team hasn't got to this yet. However, I am aware of a couple of community efforts in this space:
> https://github.com/MirServer/mir/issues/467
> https://forums.ubports.com/topic/1389/reverse-convergence-view-control-your-phone-from-computer-like-vnc-rdp
>
> We will get there.

While we have been in conversations with Drew DeVault since the previous newsletter, and we do plan on using some of the standards which he and others have worked on such as layer shells, we still believe that for the forseeable future, Mir is the best option.

**Q:** What about the already-existing Waybox project?
**A:** We were not aware this existed before stating we were going to port Openbox to Mir, and we are currently in discussions with the author of that code to utilize that instead of duplicating work, if possible.

### Miscellaneous

As always, feedback is appreciated.

# Want to help?

One of the easiest ways to get involved with Lubuntu and help us make this release the best one yet is to test Lubuntu and report bugs.

You can learn how to write an excellent bug report that helps us solve your issue quicker by reading [this guide](https://www.chiark.greenend.org.uk/~sgtatham/bugs.html).

More information about testing on Lubuntu can be found [here](https://phab.lubuntu.me/w/testing/).

# Translations

We have [a Weblate instance](https://translate.lubuntu.me/projects/) available for translations. Right now there are not many strings to translate, but as time goes on, we will add more.

Do you speak a language that isn't available to translate there? Let us know in the comments or [elsewhere](https://lubuntu.me/links/) and we will add that language.

This week, Wolfenprey translated several Lubuntu blog posts into Spanish. Thank you!

We have also added support for Korean after a comment on our last post.

Here are the translators who have contributed so far:

 - Henrik Christiansen (Danish)
 - Hans P. Möller (German, Spanish)
 - Daniel Absmeier (German)
 - Luís Rafael Gomes (Portuguese)
 - Lucas A. V. Dantas (Portuguese (Brazil))
 - Marcin Mikołajczak (Polish)
 - Tony Cuesta Escobar (Catalan)
 - Einar Mostad (Norwegian Bokmål)
 - Emanuele Antonio Faraone (Italian)
 - Carl Schwan (French)

Thank you for your valuable contributions!

# Roadmap

You can find the Cosmic Cuttlefish release cycle [here](https://wiki.ubuntu.com/CosmicCuttlefish/ReleaseSchedule). The beta is slotted for September 27, 2018 and the final release date for October 18, 2018.

Instead of continuing to list our goals here, we have created [a task on our Phabricator instance](https://phab.lubuntu.me/T53) with all of the Lubuntu release blockers and expected features. Additionally, we now have [a wiki page](https://phab.lubuntu.me/w/lubuntu_2/) detailing the work we are going to do by the end of the next development cycle.

Our artwork team is still working on Lenny, and we'll let you know when we have Lenny Cuttlefish. :)

# In the Press

This section is for highlighting exceptional Lubuntu coverage since the last issue.

## English

 - [After Adopting LXQt, Lubuntu Is Switching to Wayland by Default for Ubuntu 20.10](https://news.softpedia.com/news/after-adopting-lxqt-lubuntu-is-switching-to-wayland-by-default-for-ubuntu-20-10-522370.shtml)
 - [Lubuntu Planning Switch To Wayland, Porting Openbox To Mir](https://www.phoronix.com/scan.php?page=news_item&px=Lubuntu-Openbox-Mir-Wayland)

Release Manager Simon Quigley was on an episode of a weekly, very informal podcast-like live Linux hangout called [BigDaddyLinux](https://www.youtube.com/channel/UCtZRKfyvx7GUEi-Lr7f4Nxg) (Rocco) Live. They talked about our call for testing on [their episode a week ago](https://www.youtube.com/watch?v=e-OmgNAiif4) and made it their weekly distro challenge. Simon joined [the latest episode](https://www.youtube.com/watch?v=AoCy98PIM1o) which gave the Lubuntu team some valuable feedback about the future direction.

Feel free to [join the Destination Linux Telegram group](https://t.me/joinchat/DH6s1EJ4bp9iKemtBhgf5A) (the main chat spot for BDLL) and tell them we sent you.

## Spanish

 - [Lubuntu utilizará Wayland pero no será hasta el 2020](https://ubunlog.com/lubuntu-utilizara-wayland-pero-no-sera-hasta-el-2020/)
 - [Lubuntu optara por el servidor grafico Wayland para sus próximas versiones](https://www.linuxadictos.com/lubuntu-optara-por-el-servidor-grafico-wayland-para-sus-proximas-versiones.html)

Did you find any other exceptional stories about Lubuntu? [Let us know](https://lubuntu.me/links/) and we’ll be happy to include them here.

# Contact us

Follow us on [Twitter](https://twitter.com/LubuntuOfficial) for the latest Lubuntu updates! Don't use Twitter because it's not free software? No worries! Follow us on [Mastodon](https://mastodon.technology/@lubuntu) where the same content is published.

Feel free to get in touch with us [here](https://lubuntu.me/links/) for support, and for press/marketing purposes or if you have a private inquiry, you can get in touch with Release Manager Simon Quigley [here](mailto:tsimonq2@lubuntu.me).
