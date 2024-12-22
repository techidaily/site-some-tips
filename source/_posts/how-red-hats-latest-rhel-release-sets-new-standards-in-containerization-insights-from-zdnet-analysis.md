---
title: How Red Hat's Latest RHEL Release Sets New Standards in Containerization - Insights From ZDNet Analysis
date: 2024-12-16T19:24:45.421Z
updated: 2024-12-20T23:45:21.464Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/cloud/    https://www.zdnet.com/a/img/resize/3bd1c9914f7b38396bfbfbca03488e78f9688761/2023/11/15/739bcb98-61a6-4850-a003-6b6559fbcef2/container-newgettyimages-1210376262.jpg?width=170&height=96&fit=crop&auto=webp
---

## How Red Hat's Latest RHEL Release Sets New Standards in Containerization - Insights From ZDNet Analysis

![container-newgettyimages-1210376262](https://www.zdnet.com/a/img/resize/7944b72f060a6e10643cb56625413038ed6f5096/2023/11/15/739bcb98-61a6-4850-a003-6b6559fbcef2/container-newgettyimages-1210376262.jpg?auto=webp&width=1280)

Abstract Aerial Art/Getty Images

In a significant update to its flagship operating system, [Red Hat](https://www.redhat.com/en) has announced the release of [Red Hat Enterprise Linux (RHEL) 9.3](https://access.redhat.com/documentation/en-us/red%5Fhat%5Fenterprise%5Flinux/6/html/installation%5Fguide/sn-welcome-x86). This latest version brings a host of new features and improvements. The ones that caught my eye focus on enhancing the developer experience, bolstering security, and expanding its ability to run containers. 

While many of us still use Linux for running servers, lately -- as [IDC Research](https://www.idc.com/) predicts -- Linux will be used more and more often as the launching pad for containers and cloud-native computing. [IDC forecasts this software market will grow to $5.57 billion by 2027](https://www.idc.com/getdoc.jsp?containerId=US49244823), with a compound annual growth rate (CAGR) of 23.4%. 

**Also: [How to choose the right Linux desktop distribution for you](https://www.zdnet.com/article/how-to-choose-the-right-linux-desktop-distribution-for-you/)**

Red Hat wants RHEL 9.3 to be this tech trend's foundation. As Gunnar Hellekson, Red Hat's RHEL VP and general manager, said, "The latest versions of RHEL continue to support current IT needs while creating a smoother pathway to future innovations without requiring a wholesale change in skills, tools or workflows." 

To make RHEL 9.3 more cloud-friendly, all RHEL subscriptions now include [Red Hat Insights](https://www.redhat.com/en/technologies/management/insights), a suite of hosted expert system services for developing and managing Linux platforms at scale. Insights can alert you to potential system issues and help you mitigate them. It also can help streamline operational tasks such as building standardized images, patching systems, and optimizing resources. 

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

Specifically for containers, Red Hat is recommending [Podman](https://podman.io/), its daemonless tool for deploying, running, building, and sharing Linux containers. Now, Podman has been around for some time, but with RHEL 9.3, Podman becomes more deeply integrated with RHEL 

For example, RHEL 9.3 includes pre-configured sets of [Ansible](https://www.ansible.com/) roles and modules to streamline specific Podman system operations. The RHEL system role for Podman also now supports [Quadlet](https://www.redhat.com/sysadmin/quadlet-podman), a tool for simplifying the process of running containers with [systemd](https://systemd.io/). 

Besides the container goodness, RHEL 9.3 also has several updates aimed at developers. These include:

**Also: [How AlmaLinux stays Red Hat Enterprise Linux compatible without Red Hat code](https://www.zdnet.com/article/how-almalinux-stays-red-hat-enterprise-linux-compatible-without-red-hat-code/)**

* **Updated programming languages and tools:** The platform now includes the latest versions of popular programming languages and tools. Apache HTTP Server 2.4.57, Redis 7, GCC 13, Rust 1.71, and LLVM 16 are some of the notable inclusions, offering developers up-to-date resources for their projects.
* **Enhanced toolsets and compilers:** The update brings GCC compiler 13.1.1, which includes numerous bug fixes and enhancements. Rust 1.71 addresses a security vulnerability and introduces a more efficient Cargo sparse protocol. LLVM 16, now built with C++ 17 by default, adds support for new CPU extensions and optimized instruction sets.
* **Go 1.20:** The new version of Go includes several changes, such as a new crypto/ecdh package, optimizations in the garbage collector, and support for profile-guided optimization.

RHEL 9.3 also, of course, comes with several security updates. The most important of these has to do -- to no one's surprise -- with containers and [edge computing](https://www.zdnet.com/article/red-hat-goes-to-the-edge/). [Keylime](https://keylime.dev/) provides a highly scalable remote boot attestation and runtime integrity measurement solution. With it, you can monitor remote nodes using a hardware-based cryptographic root of trust.

**Also: [Heavy metal Linux 6.6 has arrived](https://www.zdnet.com/article/heavy-metal-linux-linux-6-6-arrives/)**

Under all this, core RHEL relies on the [RHEL 9.3 kernel, version 5.14.0-362.8.1](https://access.redhat.com/documentation/en-us/red%5Fhat%5Fenterprise%5Flinux/9/html-single/9.3%5Frelease%5Fnotes/index). This includes updates to the [perf performance analysis tool](http://perf.wiki.kernel.org/) and the crash utility and support for [thin provisioned logical System Roles](https://access.redhat.com/documentation/en-us/red%5Fhat%5Fenterprise%5Flinux/8/html/configuring%5Fand%5Fmanaging%5Flogical%5Fvolumes/creating-and-managing-thin-provisioned-volumes%5Fconfiguring-and-managing-logical-volumes).

Finally, RHEL 9.3 also offers full support for [Stratis](https://stratis-storage.github.io/), a Linux storage system. Stratis helps simplify storage administration and amplify efficiency by integrating existing Linux storage capabilities into a more streamlined, user-friendly interface. This makes storage configuration and management accessible to both novice and experienced users. 

Overall, RHEL 9.3 represents a significant step forward in providing a secure, stable, and developer-friendly platform for enterprise applications, from the good old physical server in your closet to cloud and edge deployments.

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
<li><a href="https://some-tips.techidaily.com/new-uniquely-branding-podcasts-expert-led-logo-insights/"><u>[New] Uniquely Branding Podcasts Expert-Led Logo Insights</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unleash-superior-hd-videos-on-android-devices/"><u>[New] Unleash Superior HD Videos on Android Devices</u></a></li>
<li><a href="https://extra-skills.techidaily.com/updated-leveraging-predictive-analytics-anticipating-future-consumer-trends/"><u>[Updated] Leveraging Predictive Analytics Anticipating Future Consumer Trends</u></a></li>
<li><a href="https://facebook-video-recording.techidaily.com/updated-realizing-your-potential-in-360-video-streams-for-social-media/"><u>[Updated] Realizing Your Potential in 360 Video Streams for Social Media</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-ultimate-guide-for-crafting-top-charting-youtube-titles/"><u>[Updated] Ultimate Guide for Crafting Top-Charting YouTube Titles</u></a></li>
<li><a href="https://instagram-video-recordings.techidaily.com/2024-approved-unlock-the-full-potential-of-your-videos-on-instagram-platform/"><u>2024 Approved Unlock the Full Potential of Your Videos on Instagram Platform</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-utilizing-volume-decrease-effects-within-audacity/"><u>2024 Approved Utilizing Volume Decrease Effects Within Audacity</u></a></li>
<li><a href="https://driver-error.techidaily.com/bluetooth-driver-update-for-lenovo-on-windows-11/"><u>Bluetooth Driver Update for Lenovo on Windows 11</u></a></li>
<li><a href="https://sound-issues.techidaily.com/expert-tips-for-repairing-a-malfunctioning-sound-blaster-mic/"><u>Expert Tips for Repairing a Malfunctioning Sound Blaster Mic</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-uniting-platforms-the-seamless-addition-of-linktree-to-tiktok/"><u>In 2024, Uniting Platforms The Seamless Addition of Linktree to TikTok</u></a></li>
<li><a href="https://win-reviews.techidaily.com/revive-your-aging-pc-with-these-5-cost-free-tricks-for-windows-11-users-insights-from-zdnet/"><u>Revive Your Aging PC with These 5 Cost-Free Tricks for Windows 11 Users - Insights From ZDNet</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/DBMTAJBx-X4?si=sje5pFJXiHzJJGbP" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

