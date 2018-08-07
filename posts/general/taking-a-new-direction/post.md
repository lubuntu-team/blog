During the transition to LXQt, we have received mixed feedback about Lubuntu's perceived direction going forward, so we decided it would be good to make a blog post explaining what's been happening during the transition, and where our focus will be.

NOTICE

Creating a Linux distribution which is specifically meant for older hardware is beginning to become a challenge. As time progresses, the definition of "older machines" has been changing. At one point, our rule of thumb was to support machines ten years old. If you look at computers that were released ten years ago, for example, a computer with the AMD Phenom X3 processor, you will note that computers, give or take, supported two gigabytes of RAM and two processor cores, and were also 64-bit at this time.

More Linux distributions today can run on the computer of ten years ago than Linux distributions made five years ago with a 15 year old computer.

As an example, on a fresh amd64 (64-bit) Kubuntu 18.04.1 install with two gigabytes of RAM and one CPU core (in QEMU), the idle usage with LibreOffice open and Firefox open to Lubuntu.me is about 1 GB of RAM and 6% idle CPU usage. With the same specifications/programs and an i386 (32-bit) install, 790 MB of RAM and 7% of idle CPU usage is used.

While there is something to be said about i386 resource usage and how much more efficient it can make a system, the point is that other distributions can now do what only Lubuntu was once able to do with ten year old hardware. You are welcome to also draw your own conclusions and leave them in the comments of this post.

Furthermore, imagine what these statistics will look like in 2021, when Lubuntu 18.04, which has kept our traditional focus, reaches its end of life phase.

These statistics brought much internal debate within the Lubuntu team, but we decided that going forward, we need to adapt for the current state of the market. Therefore, **our main focus is shifting from providing a distribution for old hardware to a functional yet modular distribution focused on getting out of the way and letting users use their computer**.

In essence, this is leveraging something we have always done with Lubuntu; providing an operating system which users can use to revive their old computers, but bringing this to the age of modern computing.

For the forseeable future, here are our core goals:

 - Lubuntu will leverage modern, Qt-based technologies and programs to give users a functional yet modular experience.
 - In collaboration with others, Lubuntu will continue to be a transparent and open distribution which makes it a priority to keep the community informed about the development when possible.
 - Lubuntu will create and maintain complete documentation which will be included by default in the operating system, and can guide anyone from beginner to expert on how to use Lubuntu to its full potential and contribute to the further development of it.
 - Lubuntu will keep a light experience by default but enable users to utilize more heavy and featureful components as desired.
 - Lubuntu will have the ability to be used in any language across the world, and enable contributors to easily translate all components of the operating system.

This means that Lubuntu will stay light, and for users with old systems, should still be usable. But we will no longer provide minimum system requirements and we will no longer **primarily** focus on older hardware.

This is a large endeavor as you might expect, and we're still working on catching up to other distributions in terms of feature parity, but with 18.10 being the first LXQt-only release and 20.04 being the first LTS LXQt-only release, we are confident that Lubuntu will be ready for whatever the future holds.

Thank you, and if you have any questions that were not answered here, let us know.
