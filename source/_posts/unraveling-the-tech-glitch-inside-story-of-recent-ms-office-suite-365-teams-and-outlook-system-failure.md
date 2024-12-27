---
title: "Unraveling the Tech Glitch: Inside Story of Recent MS Office Suite (365, Teams, and Outlook) System Failure"
date: 2024-12-20T16:28:56.455Z
updated: 2024-12-27T16:54:34.950Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/add496faff3567ece40d0c0a25d683b37093fb191cb1e756a607d3720738205f.png
---

## Unraveling the Tech Glitch: Inside Story of Recent MS Office Suite (365, Teams, and Outlook) System Failure

![pc-bored](https://www.zdnet.com/a/img/resize/408ebd0e8ee60ec9b60791f812c680a6417e28b6/2023/01/30/0efaa9c7-ad12-450b-a636-40239ea5be7e/pc-bored.jpg?auto=webp&width=1280)

Image: Getty Images

Microsoft says an update on a router was behind a huge multi-hour outage affecting the Microsoft Wide Area Network (WAN) that made Azure, Microsoft 365 apps, and Power Platform inaccessible to customers across the globe last week. 

The [multi-hour outage last Wednesday](https://www.zdnet.com/article/microsoft-365-outage-hits-teams-and-outlook-users-what-we-know-so-far/) impacted Microsoft Teams, Exchange Online, Outlook, SharePoint Online, OneDrive for Business, Microsoft Graph, PowerBi, M365 Admin Portal, Microsoft Intune, Microsoft Defender for Cloud Apps, and Microsoft Defender for Identity. 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/htnQWyEOCgc?si=fy86hi8_hTtbWAnw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

### Cloud

* [​What is digital transformation? Everything you need to know](https://www.zdnet.com/article/what-is-digital-transformation-everything-you-need-to-know-about-how-technology-is-reshaping/)
* [The best cloud providers compared: AWS, Azure, Google Cloud, and more](https://www.zdnet.com/article/the-top-cloud-providers-of-2021-aws-microsoft-azure-google-cloud-hybrid-saas/)
* [The top 6 cheap web hosting services: Find an affordable option](https://www.zdnet.com/article/best-cheap-web-hosting/)
* [What is cloud computing? Here's everything you need to know](https://www.zdnet.com/article/what-is-cloud-computing-everything-you-need-to-know-about-the-cloud/)

Prior to the outage, Microsoft had warned customers that a planned update might cause latency or timeouts from 07:05 UTC on Wednesday when customers attempted to connect to Azure resources in Public Azure regions, Microsoft 365, and Power BI. But as workers in Europe started the day, the update caused more than latency issues and started impacting network devices across the Microsoft WAN, which dropped connections between services in data centers as well as connections on ExpressRoute, Microsoft's private network for customers to transfer data between data centers. 

Microsoft says in its [preliminary post-incident review](https://status.azure.com/en-us/status/history/#:~:text=Preliminary%20Post%20Incident%20Review%20%28PIR%29%20%E2%80%93%20Azure%20Networking%20%E2%80%93%20Global%20WAN%20issues%20%28Tracking%20ID%20VSG1-B90%29) that most regions and services had recovered by 09:00 UTC on Wednesday, but they were not fully recovered until 12:43 UTC on 25 January. The outage also affected Azure Government cloud services that were dependent on Azure public cloud, according to Microsoft.

**Also: [The best cloud storage services: Are free ones worth it?](https://www.zdnet.com/article/best-cloud-storage/)**

"We determined that a change made to the Microsoft Wide Area Network (WAN) impacted connectivity between clients on the internet to Azure, connectivity across regions, as well as cross-premises connectivity via ExpressRoute," Microsoft says in its report first spotted [by Bleeping Computer](https://www.bleepingcomputer.com/news/microsoft/massive-microsoft-365-outage-caused-by-wan-router-ip-change/).

"As part of a planned change to update the IP address on a WAN router, a command given to the router caused it to send messages to all other routers in the WAN, which resulted in all of them recomputing their adjacency and forwarding tables. During this re-computation process, the routers were unable to correctly forward packets traversing them. The command that caused the issue has different behaviors on different network devices, and the command had not been vetted using our full qualification process on the router on which it was executed."

Microsoft's monitoring systems detected domain name service (DNS) and WAN issues at 07:12 UTC. After reviewing recent changes, while automatic recovery was happening at 08:20 UTC, engineers discovered the "problematic command" behind the issues.

**Also: [Technology spending will rise in 2023\. And this old favorite is still a top priority](https://www.zdnet.com/article/technology-spending-will-rise-next-year-and-this-old-favourite-is-still-a-top-priority/)**

"Due to the WAN impact, our automated systems for maintaining the health of the WAN were paused, including the systems for identifying and removing unhealthy devices, and the traffic engineering system for optimizing the flow of data across the network," Microsoft said. 

"Due to the pause in these systems, some paths in the network experienced increased packet loss from 09:35 UTC until those systems were manually restarted, restoring the WAN to optimal operating conditions. This recovery was completed at 12:43 UTC."

Microsoft says it has now "blocked highly impactful commands from getting executed on the devices" to mitigate future occurrences. It's also now requiring all command execution on the networks devices to follow safe change guidelines. 

Microsoft plans to publish a final post-incident report within the next two weeks. 

#### Featured

[How to disable ACR (and greatly reduce ads) on every TV model - and why you should](https://www.zdnet.com/article/how-to-disable-acr-and-greatly-reduce-ads-on-every-tv-model-and-why-you-should/ "How to disable ACR (and greatly reduce ads) on every TV model - and why you should")

[I replaced my Samsung Galaxy S24 Ultra with the Pixel 9 Pro XL for two weeks - and can't go back](https://www.zdnet.com/article/i-replaced-my-samsung-galaxy-s24-ultra-with-the-pixel-9-pro-xl-for-two-weeks-and-cant-go-back/ "I replaced my Samsung Galaxy S24 Ultra with the Pixel 9 Pro XL for two weeks - and can't go back")

[Linus Torvalds talks AI, Rust adoption, and why the Linux kernel is 'the only thing that matters'](https://www.zdnet.com/article/linus-torvalds-talks-ai-rust-adoption-and-why-the-linux-kernel-is-the-only-thing-that-matters/ "Linus Torvalds talks AI, Rust adoption, and why the Linux kernel is 'the only thing that matters'")

[The best mini PCs you can buy: Expert recommended](https://www.zdnet.com/article/best-mini-pc/ "The best mini PCs you can buy: Expert recommended")

* [How to disable ACR (and greatly reduce ads) on every TV model - and why you should](https://www.zdnet.com/article/how-to-disable-acr-and-greatly-reduce-ads-on-every-tv-model-and-why-you-should/ "How to disable ACR (and greatly reduce ads) on every TV model - and why you should")
* [I replaced my Samsung Galaxy S24 Ultra with the Pixel 9 Pro XL for two weeks - and can't go back](https://www.zdnet.com/article/i-replaced-my-samsung-galaxy-s24-ultra-with-the-pixel-9-pro-xl-for-two-weeks-and-cant-go-back/ "I replaced my Samsung Galaxy S24 Ultra with the Pixel 9 Pro XL for two weeks - and can't go back")
* [Linus Torvalds talks AI, Rust adoption, and why the Linux kernel is 'the only thing that matters'](https://www.zdnet.com/article/linus-torvalds-talks-ai-rust-adoption-and-why-the-linux-kernel-is-the-only-thing-that-matters/ "Linus Torvalds talks AI, Rust adoption, and why the Linux kernel is 'the only thing that matters'")
* [The best mini PCs you can buy: Expert recommended](https://www.zdnet.com/article/best-mini-pc/ "The best mini PCs you can buy: Expert recommended")

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
<li><a href="https://youtube-tips.techidaily.com/024-approved-decoding-youtubes-algorithm-the-role-of-keyword-optimization/"><u>[New] 2024 Approved Decoding YouTube's Algorithm The Role of Keyword Optimization</u></a></li>
<li><a href="https://fox-access.techidaily.com/new-champions-of-cutting-edge-vr-creation/"><u>[New] Champions of Cutting-Edge VR Creation</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/new-elite-8-video-grabber-utilities/"><u>[New] Elite 8 Video Grabber Utilities</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-top-10-timeless-family-adventures-on-screen-this-season/"><u>[Updated] Top 10 Timeless Family Adventures on Screen This Season</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-transforming-images-into-engaging-animation-projects/"><u>[Updated] Transforming Images Into Engaging Animation Projects</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/2024-approved-principles-of-documentary-storytelling/"><u>2024 Approved Principles of Documentary Storytelling</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-ultimate-roundup-unleashing-the-best-5-online-title-makers/"><u>2024 Approved The Ultimate Roundup Unleashing the Best 5 Online Title Makers</u></a></li>
<li><a href="https://pokemon-go-android.techidaily.com/all-you-need-to-know-about-mega-greninja-for-honor-magic-vs-2-drfone-by-drfone-virtual-android/"><u>All You Need To Know About Mega Greninja For Honor Magic Vs 2 | Dr.fone</u></a></li>
<li><a href="https://hardware-help.techidaily.com/get-the-newest-amd-graphics-driver-for-win-11107-free-downloads-now/"><u>Get the Newest AMD Graphics Driver for Win 11/10/7 - Free Downloads Now!</u></a></li>
<li><a href="https://techidaily.com/how-to-reset-a-infinix-hot-40-phone-that-is-locked-drfone-by-drfone-reset-android-reset-android/"><u>How to Reset a Infinix Hot 40 Phone That Is Locked | Dr.fone</u></a></li>
<li><a href="https://fox-friendly.techidaily.com/in-2024-ideal-episodic-unveiling-schedule/"><u>In 2024, Ideal Episodic Unveiling Schedule</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-complete-guide-to-cd-conversion-and-burning-with-wmp/"><u>In 2024, The Complete Guide to CD Conversion & Burning with WMP</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-premier-pro-essentials-accessible-for-all-editors/"><u>In 2024, The Premier Pro Essentials - Accessible for All Editors</u></a></li>
<li><a href="https://fox-glue.techidaily.com/in-2024-top-11-best-dji-phantom-4-accessories-to-buy/"><u>In 2024, Top 11 Best DJI Phantom 4 Accessories to Buy</u></a></li>
<li><a href="https://youtube-help.techidaily.com/in-2024-transform-your-channels-look-for-free/"><u>In 2024, Transform Your Channel's Look for Free</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-understanding-auto-hdr-techniques-in-modern-cameras/"><u>In 2024, Understanding Auto HDR Techniques in Modern Cameras</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unveiling-the-basics-of-digital-imagery-sizes/"><u>In 2024, Unveiling the Basics of Digital Imagery Sizes</u></a></li>
<li><a href="https://some-tips.techidaily.com/supreme-creation-studio-test-for-2024/"><u>Supreme Creation Studio Test for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-tune-tracker-and-manager-android-companion-for-2024/"><u>Top Tune Tracker & Manager, Android Companion for 2024</u></a></li>
</ul></div>

