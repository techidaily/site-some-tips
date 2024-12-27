---
title: "Enhanced Container Capabilities in Red Hat Enterprise Linux 9.3: A Comprehensive Update From ZDNet"
date: 2024-12-25T17:14:35.857Z
updated: 2024-12-27T16:01:17.679Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/e1ce3f3e6442fac637b9a262af6a28dc4e5da35e5024ee062fdf9880b101f6b7.jpg
---

## Enhanced Container Capabilities in Red Hat Enterprise Linux 9.3: A Comprehensive Update From ZDNet

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
<li><a href="https://some-tips.techidaily.com/new-simplified-screen-switching-utilizing-pip-mode-on-netflix-for-smooth-viewing/"><u>[New] Simplified Screen Switching Utilizing PIP Mode on Netflix for Smooth Viewing</u></a></li>
<li><a href="https://article-knowledge.techidaily.com/updated-in-2024-maximize-your-youtube-srt-a-three-pronged-plan/"><u>[Updated] In 2024, Maximize Your Youtube SRT A Three-Pronged Plan</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unlocking-your-youtube-potential-through-brand-partnerships/"><u>[Updated] Unlocking Your YouTube Potential Through Brand Partnerships</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unveiling-the-potential-of-magix-music-maker-2024/"><u>[Updated] Unveiling the Potential of Magix Music Maker 2024</u></a></li>
<li><a href="https://youtube-stream.techidaily.com/2024-approved-from-long-winded-to-concise-the-art-of-youtube-trimming/"><u>2024 Approved From Long-Winded to Concise The Art of YouTube Trimming</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-transforming-education-with-instructional-videos/"><u>2024 Approved Transforming Education with Instructional Videos</u></a></li>
<li><a href="https://win11-tips.techidaily.com/how-to-optimize-group-and-admin-management-in-homes/"><u>How to Optimize Group and Admin Management in Homes</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/in-2024-read-this-guide-to-find-a-reliable-alternative-to-fake-gps-on-nokia-c12-plus-drfone-by-drfone-virtual-android/"><u>In 2024, Read This Guide to Find a Reliable Alternative to Fake GPS On Nokia C12 Plus | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-untangling-veiled-feedback-mechanisms-in-video-sites/"><u>In 2024, Untangling Veiled Feedback Mechanisms in Video Sites</u></a></li>
<li><a href="https://screen-video-capture.techidaily.com/in-game-recorder-faceoff-for-2024/"><u>In-Game Recorder Faceoff for 2024</u></a></li>
<li><a href="https://buynow-help.techidaily.com/marvels-avengers-review-marvelous-mediocrity/"><u>Marvel’s Avengers Review: Marvelous Mediocrity</u></a></li>
<li><a href="https://techtrends.techidaily.com/no-more-waiting-speeding-through-windows-11-update-processes-efficiently/"><u>No More Waiting: Speeding Through Windows 11 Update Processes Efficiently</u></a></li>
<li><a href="https://youtube-webster.techidaily.com/al-youtube-playback-adjusting-speed-settings/"><u>Optimal YouTube Playback Adjusting Speed Settings</u></a></li>
<li><a href="https://fix-guide.techidaily.com/reasons-for-oppo-a79-5g-stuck-on-boot-screen-and-ways-to-fix-them-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Reasons for Oppo A79 5G Stuck on Boot Screen and Ways To Fix Them | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/streamline-your-workflow-with-leading-tts-apps-for-mac-users-for-2024/"><u>Streamline Your Workflow with Leading TTS Apps for Mac Users for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveiling-asmrs-benefits-a-health-perspective-for-2024/"><u>Unveiling ASMR’s Benefits A Health Perspective for 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/SgRVYjqB70s?si=My_2cDvJVdincQRu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

