Thanks to all the hard work from our contributors, Lubuntu 18.10 has been released! With the codename Cosmic Cuttlefish, Lubuntu 18.10 is the 15th release of Lubuntu and the first release of Lubuntu with LXQt as the default desktop environment, with support until July of 2019.

NOTICE

# What is Lubuntu?

Lubuntu is an official Ubuntu flavor which uses the Lightweight Qt Desktop Environment (LXQt). The project’s goal is to provide a lightweight yet functional Linux distribution based on a rock-solid Ubuntu base. Lubuntu provides a simple but modern and powerful graphical user interface, and comes with a wide variety of applications so you can browse, email, chat, play, and be productive.

# Welcome to LXQt

<img style="float: center; width: 33%;" src="https://phab.lubuntu.me/file/data/zwng7o6qanhvvucgajdc/PHID-FILE-djx4vzahriz23c5622vu/Screenshot_20181007_Desktop.png" />

This is the first Lubuntu release with LXQt as the main desktop environment. The Lubuntu project, in 18.10 and successive releases, will no longer support the LXDE desktop environment or tools in the Ubuntu archive, and will instead focus on the LXQt desktop environment. You can find the following major applications and toolkits installed by default in this release:

 - LXQt 0.13.0, with many bugfixes and improvements backported from upstream.
 - Qt 5.11.1, which is the first point release in the Qt 5.11 series.
 - Mozilla Firefox 62, which will receive updates from the Ubuntu Security Team throughout the support cycle of the release.
 - Trojitá 0.7, a light and efficient Qt-based email client.
 - The LibreOffice 6.1.2 suite, with the Qt 5 frontend.
 - VLC 3.0.4, for viewing media and listening to music.
 - Featherpad 0.9.0, for notes and code editing.
 - Discover Software Center 5.13.5, for an easy, graphical way to install and update software.
 - The powerful and fast email client Trojitá 0.7 to get you to inbox zero in no time.

You can find a variety of other applications installed which aim to enhance your experience while staying out of the way of your normal workflow.

## Calamares

Lubuntu has switched to using the [Calamares](https://calamares.io/) system installer in place of the Ubiquity installer that other flavors use. There were several advantages to choosing Calamares as our installer:

 - Calamares features a modern, C++-based codebase with a Qt 5 frontend.
 - Customization of the installation experience is easier, as the installer is module-based, and code can be written in Python or C++ while cleanly and elegantly sharing elements like translations, global variables, etc.
 - It allows us to work with other projects to solve common problems in a way that is clean and works in many cases, leading to cleaner code.

In this cycle our main focus was working out any issues that arose from the switch in installer, especially around the Ubuntu tooling which is geared towards the use of Ubiquity, so it lacks features such as the minimal install, but in the next cycle we are going to put an emphasis on improving feature parity.

Unfortunately though, we had issues with EFI systems and encrypted LUKS systems setting up GRUB correctly. In the meantime, you are encouraged to utilize the enhanced and simple-to-use manual partitioning experience provided by Calamares. Otherwise, the Lubuntu QA Team has been hard at work testing many installation combinations to ensure everything else is working as expected. You can find a full chart of tested installations [here](https://phab.lubuntu.me/T107).

Thanks to Adriaan de Groot and many others on the Calamares team; without you, Calamares would not have worked as well as it does for us.

## Lubuntu Manual

The Lubuntu Team has been hard at work in polishing a Lubuntu Manual book to make it easy for new and experienced users alike to use their system more productively. The book can be found at [manual.lubuntu.me](https://manual.lubuntu.me/).

We will eventually ship this in the default install of Lubuntu, but for now our goal is to polish it and receive feedback from the community, so it will stay published as a website only for now.

The manual is built using [Sphinx](http://www.sphinx-doc.org/en/stable/), and the source can be found on our Phabricator instance [here](https://phab.lubuntu.me/source/lubuntu-manual/), or if you prefer to use GitHub to contribute, it is mirrored [there](https://github.com/lubuntu-team/manual) as well.

We want to thank Lyn Perrine for all the hard work she has put into the Lubuntu Manual recently, because the majority of the text in the manual right now is what she has written. Thank you!

## Lubuntu Spanish Community

Throughout this cycle, Lubuntu has started a Spanish community for Spanish speakers (either as a native language or a secondary language) to talk about and contribute to Lubuntu and Linux in general. The group has grown in size and is now larger than our development group.

If you speak Spanish and want to join a friendly community of Linux people with all levels of technical experience, the Lubuntu Spanish community is for you. You can join the Telegram group at [telegram.lubuntu.me/español](https://telegram.lubuntu.me/español) or the IRC channel at #lubuntu-es on freenode.

Thanks to [Wolfenprey](https://twitter.com/Wolfen48K), [GatoOscuro](https://gatooscuro7.wordpress.com/), [Hans Möller](https://twitter.com/hpmoller), and many, many other great community members which make this possible. 

# Where can I download it?

You can download Lubuntu 18.10 on [our downloads page](https://lubuntu.me/downloads/).

# Known Issues and Workarounds

## Issues with workarounds

LXQt treats all monitors as one when painting the desktop background. We plan on solving this in a more native way by the 19.04 release, but in the meantime, Lubuntu contributor Hans P. Möller has written [a script](https://git.launchpad.net/~hmollercl/stitchwp/tree/stitchWP.sh) which can be used as a workaround for treating all of the backgrounds differently.

We have not ported over the "Additional drivers" tab from software-properties-gtk to software-properties-qt, which can be used for installing additional CPU and graphics drivers. As a workaround, you can use the `ubuntu-drivers` command line tool.

## Issues with fixes

The default LibreOffice theme that ships on the ISOs is the default Adwaita theme, which is not consistent with the system theme. This will be fixed in version 1:6.1.2-0ubuntu2.

Trojitá has display issues with some emails related to a QtWebkit issue. This will be fixed in version 5.212.0~alpha2-12ubuntu2.

Both of the above fixes should come within the next week after release.

## Known issues

Trojitá will crash if sorted and resorted several times in succession (LP: #[1797665](https://bugs.launchpad.net/ubuntu/+source/trojita/+bug/1797665)).

Qterminal dropdown shortcut key does not consistently toggle visibility (LP: #[1795998](https://bugs.launchpad.net/ubuntu/+source/qterminal/+bug/1795998)).

# Would you like to help?

We can always use more help! **No matter your skill level or your technical experience, there's something you can help with that can make a huge difference in Lubuntu.** [Join](https://lubuntu.me/links/) us on our chat which is bridged three ways to Matrix, Telegram, and IRC and talk to us there. Whether you know another language, have some spare time to help us [test](https://phab.lubuntu.me/w/testing/) Lubuntu, are good at writing documentation, or just want to stay "in the know," that is the place to be.

Another great method to get involved is bug reporting. If you notice an issue please [file a bug](https://bugs.launchpad.net/lubuntu/+filebug) and tag it with "lubuntu".

Don't want to file a bug? [Let us know](https://lubuntu.me/links/) what the problem is (in detail, enough that we can reproduce it) and we can assist you in filing one.

# Stay Connected!

We [publish a newsletter](https://lubuntu.me/category/newsletter/) every so often which details the work that is currently happening in Lubuntu, including fixed bugs and additional ways you can help.

For the latest Lubuntu information and announcements follow us on [Twitter](https://twitter.com/LubuntuOfficial), [Mastodon](https://mastodon.technology/@lubuntu), or [Telegram](https://t.me/LubuntuOfficial). We have other social media pages and ways to stay connected which you can find [here](https://lubuntu.me/links/).

# Screenshots

As promised [on Twitter](https://twitter.com/LubuntuOfficial/status/1050068447000973312), users who tested Lubuntu and submitted their screenshots to us would be credited in the announcement. Here are the submissions:

<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="und" dir="ltr">❤️ <a href="https://t.co/lNBgQQD9kH">pic.twitter.com/lNBgQQD9kH</a></p>&mdash; GnuXero (@GnuXero26) <a href="https://twitter.com/GnuXero26/status/1050071135054905351?ref_src=twsrc%5Etfw">October 10, 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr">Learning to customize Lubuntu &lt;3 <a href="https://t.co/5sVYbG0B2R">pic.twitter.com/5sVYbG0B2R</a></p>&mdash; Leandro Ramos (@leandroembu) <a href="https://twitter.com/leandroembu/status/1051495186054991872?ref_src=twsrc%5Etfw">October 14, 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="und" dir="ltr"> <a href="https://t.co/gmleH5b6nw">pic.twitter.com/gmleH5b6nw</a></p>&mdash; N0um3n0 (@Cryptodata) <a href="https://twitter.com/Cryptodata/status/1051536066421944330?ref_src=twsrc%5Etfw">October 14, 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

And marneu, one of our newer [r/Lubuntu](https://www.reddit.com/r/Lubuntu/) moderators who uses Lubuntu 18.10 with the i3 window manager, submitted three screenshots: [one](https://i.imgur.com/ObmUloF.jpg), [two](https://i.imgur.com/r7yj5Wh.png), [three](https://i.imgur.com/A5WNmIM.png).

And of course, while it doesn't count, Dustin Krysak did give us an [Ubuntu Budgie](https://ubuntubudgie.org/blog/2018/10/18/18-10-ubuntu-budgie-released) screenshot:

<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr">Here is the best screenshot yet..... ha ha <a href="https://t.co/WanVi9IZNv">pic.twitter.com/WanVi9IZNv</a></p>&mdash; Dustin 🤖 Krysak (@Bashfulrobot) <a href="https://twitter.com/Bashfulrobot/status/1050254685498560512?ref_src=twsrc%5Etfw">October 11, 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Thank you to everyone who submitted screenshots!
