At 2:15 AM Central US Time, the Lubuntu Team was informed by our hosting provider, Altispeed Technologies, that there had been a problem with the server we use for Lubuntu's infrastructure, including Phabricator, Weblate, Jenkins, the IRC bridge and other services. This resulted in complete data loss for all of the aforementioned services. Below is a statement from Altispeed Technologies regarding the incident:

```
In an effort to demonstrate good stewardship of Linux and open source, Altispeed Technologies donates the server, storage space, and bandwidth for hosting many of the Lubuntu resources. During a migration effort last night, the virtual machine that stores production data for the Lubuntu Phabricator instance (among other services) was inadvertently destroyed. Despite having backups enabled, our VPS provider was unable to recover the data and it has been permanently lost.

Our team is working to re-provision the system and we have signed an agreement with a datacenter to run our services under our control. All Lubuntu resources hosted by Altispeed will be moved at that time. We apologize for any inconvenience this may have caused and will continue to work towards giving back to the community.
```

We still have complete access to the Git repositories hosted on the Phabricator instance, as they have been mirrored to GitHub, however, all of the tasks on our Phabricator instance as well as the wiki and login information for all users has been lost.

We sincerely apologize for the inconvenience, and expect services to be back up before the end of the day Central US time. On a positive note, starting anew has allowed us to refine the way the services are organized on the server, to offer a faster and more secure experience going forward.
