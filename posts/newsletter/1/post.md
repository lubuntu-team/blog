At Lubuntu we decided it was a good idea to create a weekly newsletter detailing the work that has been happening. So, here we are. :)

NOTICE

# Changes

## General

 * We're preparing to participate in the Final Beta. At the moment, we're aware of two showstopper bugs affecting Lubuntu:
    * [https://bugs.launchpad.net/ubuntu/+source/ubiquity/+bug/1754174](https://bugs.launchpad.net/ubuntu/+source/ubiquity/+bug/1754174)
        * This affects installing Lubuntu while selecting the option straight away from booting (when selecting "Install Lubuntu" from the boot menu).
    * [https://bugs.launchpad.net/ubuntu/+source/partman-auto-crypto/+bug/1759732](https://bugs.launchpad.net/ubuntu/+source/partman-auto-crypto/+bug/1759732)
        * This makes encrypted LVM installs unable to work due to the fact that we have zram support in the live image. A simple workaround is to umount the zram partitions, but we would like this properly fixed for users.

We expect these bugs to be fixed before we release the final ISO, if not the Final Beta.

## Lubuntu Next

 * The Lubuntu Next images as of 20180401 no longer ask for you to select a window manager, and while some default settings still need to be set, it is usable now.
   * This was fixed, but regressed when the changes were accidentally dropped after SDDM 0.17 was introduced into the archive. This upload fixes it: [https://launchpad.net/ubuntu/+source/sddm/0.17.0-1ubuntu2](https://launchpad.net/ubuntu/+source/sddm/0.17.0-1ubuntu2)
   * The new Featherpad release was synced to Bionic: [https://launchpad.net/ubuntu/+source/featherpad/0.8-1](https://launchpad.net/ubuntu/+source/featherpad/0.8-1)
   * While these are not things that happened solely over the past week, we have made a few changes in the Lubuntu Next ISOs:
     * It now ships with Arc as the LXQt and Openbox themes. Thanks to the Artwork Team for the hard work!
     * The default applications that ship with Lubuntu Next are now decided on. The goal now is to work on perfecting default settings that will ship with these applications, and to get them set properly.
     * Working with Kubuntu and KDE Neon, we are going to move to Calamares as the default installer for Lubuntu Next. We believe that this is the right decision going forward for users to provide a robust, flexible, and modular installer. As Lubuntu Next is the first flavor (in at least a decade, from our estimates) that has switched their graphical installer (and is not a Canonical-led project), we expect some bumps in the road going forward. The goal is, alongside Kubuntu, to ship 18.10 with Calamares being the only graphical installer.

## Infrastructure and Project Changes

As noted in previous announcements, we now have a [Phabricator instance](https://phab.lubuntu.me/) that is graciously hosted by our friends over at Altispeed Technologies, the major code that Lubuntu works on is now [mirrored on our official GitHub page](https://github.com/lubuntu-team/) (we're working on mirroring more useful repositories, stay tuned!), all of our official web presences (meaning, Lubuntu.me and subdomains, because Lubuntu.net is no longer under the control of the Lubuntu project (we can't say more at this time except that we are in no way affiliated with FOSSASIA)) now have HTTPS, and we have [many more ways you can contact us](https://lubuntu.me/links/). But, there are some more infrastructure and project changes which we have done that haven't quite been announced yet:

 1. [The CSS](https://github.com/lubuntu-team/cdimage-css) for [the Lubuntu pages under cdimage.ubuntu.com](http://cdimage.ubuntu.com/lubuntu/daily/current/) has been updated with a refreshed look, thanks to the Artwork Team. We have documented this process for other flavors, which is available [here](https://wiki.ubuntu.com/ReleaseTeam/FlavorCSSChanges).
 1. The logo has changed to reflect the move towards LXQt. There are some places which will still contain the old logo, but in general, the Lubuntu logo is changing (and has already changed in many places) to the following:

![Lubuntu's logo](https://pbs.twimg.com/profile_images/965283049968689152/8iy34E_U_200x200.jpg)

You can find usage terms for our new logo and brand [here](https://github.com/lubuntu-team/lubuntu-identity). As explained there, it is licensed under the [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/) unless you receive explicit permission from [the Lubuntu Team](https://launchpad.net/~lubuntu-admins).

# Roadmap

The rest of the Bionic roadmap is [laid out pretty clearly](https://wiki.ubuntu.com/BionicBeaver/ReleaseSchedule); we will participate in the Final Beta to be released on Thursday (assuming the two showstopper bugs are fixed), then in two weeks we get the release candidates, and one week after that, Lubuntu 18.04 is released.

Lubuntu 18.04 will ship as an LTS with three years of support. The LXDE desktop will continue to be the default throughout the duration of the LTS, and it will ship with the same applications we have shipped in 17.10.

Lubuntu Next will continue to be an early adopter's preview, because our focus as a team right now is on polishing Lubuntu 18.04 and making it a solid LTS. If you install Lubuntu Next 18.04 (which you can grab a daily ISO of right now but won't actually be released), **a lot of things won't work well quite yet** (of course, you can get it to work with some modifications, but we are not confident enough in the state of the ISO that we are willing to ship it). It will stay **unofficially** supported, and the packages will only be supported in the Ubuntu archive for nine months after the release. After that, you need to update to 18.10 to receive the latest updates.

We frequently get a question along the lines of "Why aren't you shipping LXQt as the default yet?" The answer to these questions is that while we are working towards it (and progress is being made), we don't want to jeopardize our userbase by shipping something that isn't quite perfect yet. We welcome help with making Lubuntu Next a solid experience, regardless of your experience level, so feel free to get in contact with us.

# Contact us

Feel free to [get in touch with us](https://lubuntu.me/links/).
