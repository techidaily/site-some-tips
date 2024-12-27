---
title: "Game-Changing Secure Architecture: Exploring the Impact of Canonical's Distroless on Enterprise Linux Deployments | ZDNET"
date: 2024-12-25T17:12:44.342Z
updated: 2024-12-27T16:59:55.132Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/b75342051a1eed044885b06ddc777260c76924178d810e45fd7a89223f0c20e7.jpg
---

## Game-Changing Secure Architecture: Exploring the Impact of Canonical's Distroless on Enterprise Linux Deployments | ZDNET

![penguins running](https://www.zdnet.com/a/img/resize/6c3353325c28400d3d71674d8697b9333e2daf49/2024/06/28/5d16beeb-6f88-4f0f-ad37-e57b56373d4d/gettyimages-1498113740.jpg?auto=webp&width=1280)

Vicki Jauron, Babylon and Beyond Photography/Getty Images

Canonical has announced plans to offer customized Docker container Long Term Support (LTS) [Linux](https://www.zdnet.com/article/best-linux-desktops-for-beginners/) images via its Everything LTS service. These custom "distroless" Linux images are set to come with 12 years of security support for Linux, and any included open-source application or dependency within the container.

Canonical CEO Mark Shuttleworth didn't mince his words: "Everything LTS means CVE maintenance for your entire open-source dependency tree, including open source that is not already packaged as a deb in Ubuntu." This shift is a game-changer for enterprises and ISVs looking to meet stringent regulatory requirements with complex open-source stacks.

**Also: [Thinking about switching to Linux? 10 things you need to know](https://www.zdnet.com/article/thinking-about-switching-to-linux-things-you-need-to-know/)**

Shuttleworth said Canonical will deliver "distroless or Ubuntu-based Docker images to your spec, which we will support on RHEL, VMware, Ubuntu or major public cloud K8s. Our enterprise and ISV customers can now count on Canonical to meet regulatory maintenance requirements with any open source stack, no matter how large or complex, wherever they want to deploy it."

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

Although Shuttleworth implied Canonical, which is Ubuntu Linux's parent company, would support [Red Hat Enterprise Linux (RHEL)](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux), it appears he meant Canonical would support these new Linux images on Red Hat OpenShift as well as all other [Kubernetes distributions and cloud platforms](https://www.zdnet.com/article/what-is-kubernetes-and-why-is-it-so-important/). 

Specifically, Canonical will back its images on all of Canonical's Kubernetes offerings -- [MicroK8s](https://microk8s.io/) or [Charmed Kubernetes](https://ubuntu.com/kubernetes/charmed-k8s) \-- and support VMware on Tanzu Kubernetes Grid or vSphere with Kubernetes or Ubuntu virtual machines (VMs) on the vSphere cluster. On public clouds, Canonical plans to support containers on Azure, AWS, Google Cloud, IBM, and Oracle public cloud Kubernetes offerings.

**Also: [Sparky Linux is a blazing-fast distro that can keep your older machines running for years](https://www.zdnet.com/article/sparky-linux-is-a-blazing-fast-distro-that-can-keep-your-older-machines-running-for-years/)**

With these new Open Container Initiative images, Canonical is embracing the "distroless" container paradigm in which images contain just enough of the operating system and software to run a specific application. These hardened, minimal containers have a reduced attack surface, making them much more secure than conventional Linux VMs or containers. Distros that use this approach include Alpine Linux, Fedora CoreOS, and Wolfi.

These new ["chiseled" containers](https://ubuntu.com/containers/chiselled) are built on Ubuntu with [Chisel](https://documentation.ubuntu.com/rockcraft/en/latest/explanation/chisel/). This program chisels Debian packages into a file system containing only the minimal collections of files needed for the container to function properly.

**Also: [Why I use the Linux tree command daily - and what it can do for you](https://www.zdnet.com/article/why-i-use-the-linux-tree-command-daily-and-what-it-can-do-for-you/)**

Canonical says that [Ubuntu Pro](https://ubuntu.com/pro) subscriptions will include the right to run unlimited Everything LTS containers and that it will support VMware, OpenShift, and public cloud Kubernetes hosts at the same price as Ubuntu Pro hosts.

The [Ubuntu Pro](https://ubuntu.com/pro) service will now include thousands of new open-source upstream components, including the latest AI/ML dependencies and tools. Canonical plans to maintain the 2,000 widely used AI/ML libraries and tools, including heavy hitters such as [PyTorch](https://pytorch.org/), [TensorFlow](https://www.tensorflow.org/), and [Rapids](https://rapids.ai/), as source code instead of as [Debian/Ubuntu deb packages](https://ubuntu.com/about/packages).

Canonical has also partnered with Microsoft to create chiseled containers, which are a mere 100MB, for the .NET community. A self-contained .NET application runtime base image is only 6MB when compressed.

**Also: [Canonical turns 20: Shaping the Ubuntu Linux world](https://www.zdnet.com/article/canonical-turns-20-shaping-the-ubuntu-linux-world/)**

Canonical also promises its average time for fixing critical CVE security issues will take less than 24 hours. Canonical is positioning itself as the go-to partner for organizations that want rock-solid security and cutting-edge, open-source tech.

At the same time, Canonical appears to be distancing itself from its Ubuntu brand. Ubuntu is still key, but meeting customer demands for tiny, ultra-secure images is coming first. This is a bold move by Shuttleworth in the ever-evolving market for enterprise Linux and cloud computing.

#### Linux

[The best Linux laptops for consumers and developers](https://www.zdnet.com/article/best-linux-laptop/ "The best Linux laptops for consumers and developers")

[Want to save your aging computer? Try these 5 Linux distributions](https://www.zdnet.com/article/want-to-save-your-old-computer-try-these-5-linux-distributions/ "Want to save your aging computer? Try these 5 Linux distributions")

[The best distros for beginners](https://www.zdnet.com/article/best-linux-desktops-for-beginners/ "The best distros for beginners")

[How to enable Linux on your Chromebook (and why you should)](https://www.zdnet.com/article/how-to-enable-linux-on-your-chromebook-and-why-you-should/ "How to enable Linux on your Chromebook (and why you should)")

* [The best Linux laptops for consumers and developers](https://www.zdnet.com/article/best-linux-laptop/ "The best Linux laptops for consumers and developers")
* [Want to save your aging computer? Try these 5 Linux distributions](https://www.zdnet.com/article/want-to-save-your-old-computer-try-these-5-linux-distributions/ "Want to save your aging computer? Try these 5 Linux distributions")
* [The best distros for beginners](https://www.zdnet.com/article/best-linux-desktops-for-beginners/ "The best distros for beginners")
* [How to enable Linux on your Chromebook (and why you should)](https://www.zdnet.com/article/how-to-enable-linux-on-your-chromebook-and-why-you-should/ "How to enable Linux on your Chromebook (and why you should)")

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="8358498916"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>

<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://youtube-docs.techidaily.com/n-2024-virtual-studio-compiling-the-best-dj-visuals-for-download/"><u>[New] In 2024, Virtual Studio Compiling the Best DJ Visuals for Download</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-least-expensive-skyvault-service-for-big-files/"><u>[Updated] The Least Expensive SkyVault Service for Big Files</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unveiling-the-art-of-podcast-rss-mastery/"><u>[Updated] Unveiling the Art of Podcast RSS Mastery</u></a></li>
<li><a href="https://fox-blue.techidaily.com/2024-approved-perfecting-your-sound-palette-with-audacity-crossfading/"><u>2024 Approved Perfecting Your Sound Palette with Audacity Crossfading</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-pioneering-editing-snapseed-for-the-newcomer/"><u>2024 Approved Pioneering Editing Snapseed for the Newcomer</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unleashing-creative-stories-zoom-techniques-on-snapchat/"><u>2024 Approved Unleashing Creative Stories Zoom Techniques on Snapchat</u></a></li>
<li><a href="https://hardware-help.techidaily.com/asus-unleashes-stunning-oled-display-in-their-latest-laptop-a-comprehensive-review-by-a-seasoned-tech-expert/"><u>Asus Unleashes Stunning OLED Display in Their Latest Laptop: A Comprehensive Review by a Seasoned Tech Expert</u></a></li>
<li><a href="https://video-capture.techidaily.com/bass-brilliance-new-device-overview/"><u>Bass Brilliance New Device Overview</u></a></li>
<li><a href="https://buynow-help.techidaily.com/decision-guide-is-getting-an-ipad-worth-it/"><u>Decision Guide: Is Getting an iPad Worth It?</u></a></li>
<li><a href="https://tech-renaissance.techidaily.com/explore-the-ultimate-guide-discover-2022s-finest-outdoor-camping-chairs-as-endorsed-by-zdnet/"><u>Explore the Ultimate Guide: Discover 2022'S Finest Outdoor Camping Chairs, as Endorsed by ZDNet</u></a></li>
<li><a href="https://activate-lock.techidaily.com/in-2024-how-to-bypass-icloud-activation-lock-on-ipod-and-iphone-12-pro-the-right-way-by-drfone-ios/"><u>In 2024, How To Bypass iCloud Activation Lock On iPod and iPhone 12 Pro The Right Way</u></a></li>
<li><a href="https://fox-links.techidaily.com/in-2024-stealthy-sound-suppression-techniques-for-fade-out/"><u>In 2024, Stealthy Sound Suppression Techniques for Fade-Out</u></a></li>
<li><a href="https://article-tips.techidaily.com/optimal-outlooks-ideal-laptops-to-render-hd-videos-quickly/"><u>Optimal Outlooks Ideal Laptops to Render HD Videos Quickly</u></a></li>
<li><a href="https://some-tips.techidaily.com/quick-catch-up-effective-methods-for-skipping-edgenuity-courses-for-2024/"><u>Quick Catch-Up Effective Methods for Skipping Edgenuity Courses for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/tap-into-the-latest-gaming-and-app-splash-of-win11-for-2024/"><u>Tap Into the Latest Gaming and App Splash of Win11 for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-visual-clarity-bypassing-background-in-photopea-for-2024/"><u>Unlocking Visual Clarity Bypassing Background in Photopea for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unraveling-rtmp-streams-overcoming-premieres-export-hurdle-for-2024/"><u>Unraveling RTMP Streams Overcoming Premiere's Export Hurdle for 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/-yZKNLxj3po?si=-RbF6nCJEVlHWP-M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

