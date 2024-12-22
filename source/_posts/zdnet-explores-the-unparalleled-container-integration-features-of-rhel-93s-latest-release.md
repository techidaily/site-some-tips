---
title: ZDNet Explores the Unparalleled Container Integration Features of RHEL 9.3'S Latest Release
date: 2024-12-16T17:04:15.411Z
updated: 2024-12-22T01:30:40.732Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/cloud/    https://www.zdnet.com/a/img/resize/3bd1c9914f7b38396bfbfbca03488e78f9688761/2023/11/15/739bcb98-61a6-4850-a003-6b6559fbcef2/container-newgettyimages-1210376262.jpg?width=170&height=96&fit=crop&auto=webp
---

## ZDNet Explores the Unparalleled Container Integration Features of RHEL 9.3'S Latest Release

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
<li><a href="https://youtube-docs.techidaily.com/rowing-engagement-ethically-youtube-success-stories/"><u>[New] Growing Engagement Ethically YouTube Success Stories</u></a></li>
<li><a href="https://facebook-record-videos.techidaily.com/new-in-2024-dive-deep-10-immersive-youtube-videos-for-vr-enthusiasts/"><u>[New] In 2024, Dive Deep 10 Immersive YouTube Videos for VR Enthusiasts</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-synergizing-brands-on-video-platforms/"><u>[New] Synergizing Brands on Video Platforms</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unhackable-blueprint-for-inserting-your-tiktok-links/"><u>[New] Unhackable Blueprint for Inserting Your TikTok Links</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-negative-narratives-of-virtual-reality-tech/"><u>2024 Approved The Negative Narratives of Virtual Reality Tech</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-tricks-to-simulate-historical-alterations/"><u>2024 Approved Tricks to Simulate Historical Alterations</u></a></li>
<li><a href="https://data-safeguard.techidaily.com/guide-recovery-of-deletion-damaged-data-from-ios-devices-using-stellar/"><u>Guide: Recovery of Deletion-Damaged Data From iOS Devices Using Stellar</u></a></li>
<li><a href="https://iphone-unlock.techidaily.com/in-2024-apple-iphone-13-pro-max-backup-password-never-set-but-still-asking-heres-the-fix-drfone-by-drfone-ios/"><u>In 2024, Apple iPhone 13 Pro Max Backup Password Never Set But Still Asking? Heres the Fix | Dr.fone</u></a></li>
<li><a href="https://extra-guidance.techidaily.com/in-2024-iron-out-instability-in-iphone-videography-effortlessly/"><u>In 2024, Iron Out Instability in iPhone Videography Effortlessly</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-art-of-mastering-funimate/"><u>In 2024, The Art of Mastering Funimate</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-ultimate-guide-altering-voices-for-a-competitive-edge-in-free-fire/"><u>In 2024, The Ultimate Guide Altering Voices for a Competitive Edge in Free Fire</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-ultimate-guide-to-vr-game-engine-picks-2023/"><u>In 2024, The Ultimate Guide to VR Game Engine Picks, 2023</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-ultimate-pathway-best-7-platforms-turning-art-into-nfts/"><u>In 2024, The Ultimate Pathway Best 7 Platforms Turning Art Into NFTs</u></a></li>
<li><a href="https://youtube-blog.techidaily.com/24-the-ultimate-roadmap-to-mastering-your-youtube-video-editing-skills/"><u>In 2024, The Ultimate Roadmap to Mastering Your YouTube Video Editing Skills</u></a></li>
<li><a href="https://pokemon-go-android.techidaily.com/preparation-to-beat-giovani-in-pokemon-go-for-honor-80-pro-straight-screen-edition-drfone-by-drfone-virtual-android/"><u>Preparation to Beat Giovani in Pokemon Go For Honor 80 Pro Straight Screen Edition | Dr.fone</u></a></li>
<li><a href="https://win11.techidaily.com/resetting-admin-controlled-features-in-windows-11-systems/"><u>Resetting Admin-Controlled Features in Windows 11 Systems</u></a></li>
<li><a href="https://android-unlock.techidaily.com/top-4-sim-location-trackers-to-easily-find-your-lost-motorola-moto-g73-5g-device-by-drfone-android/"><u>Top 4 SIM Location Trackers To Easily Find Your Lost Motorola Moto G73 5G Device</u></a></li>
<li><a href="https://tech-savvy.techidaily.com/understanding-eus-ai-policy-on-gpt-tech/"><u>Understanding EU's AI Policy on GPT Tech</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlock-your-podcast-potential-advanced-techniques-for-idevice-audio-recording-for-2024/"><u>Unlock Your Podcast Potential Advanced Techniques for iDevice Audio Recording for 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/_O8m9KphYzs?si=jITthzeyX_Kmt9X2" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

