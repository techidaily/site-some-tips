---
title: "Understanding the Cause Behind the Major Microsoft 365, Teams & Outlook Disruption: An Insightful Breakdown"
date: 2025-01-11T21:07:14.220Z
updated: 2025-01-12T17:28:47.169Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/3f74865abe3cde83f5178213b8f2028e6688a23ca37959ec467d0c79369ad79b.jpg
---

## Understanding the Cause Behind the Major Microsoft 365, Teams & Outlook Disruption: An Insightful Breakdown

![pc-bored](https://www.zdnet.com/a/img/resize/408ebd0e8ee60ec9b60791f812c680a6417e28b6/2023/01/30/0efaa9c7-ad12-450b-a636-40239ea5be7e/pc-bored.jpg?auto=webp&width=1280)

Image: Getty Images

Microsoft says an update on a router was behind a huge multi-hour outage affecting the Microsoft Wide Area Network (WAN) that made Azure, Microsoft 365 apps, and Power Platform inaccessible to customers across the globe last week. 

The [multi-hour outage last Wednesday](https://www.zdnet.com/article/microsoft-365-outage-hits-teams-and-outlook-users-what-we-know-so-far/) impacted Microsoft Teams, Exchange Online, Outlook, SharePoint Online, OneDrive for Business, Microsoft Graph, PowerBi, M365 Admin Portal, Microsoft Intune, Microsoft Defender for Cloud Apps, and Microsoft Defender for Identity. 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/epKTCSREjhI?si=Ez_hObK1FZrmEE7f" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<li><a href="https://facebook-record-videos.techidaily.com/new-in-2024-crafting-a-youtube-empire-26-successful-techniques/"><u>[New] In 2024, Crafting a YouTube Empire 26 Successful Techniques</u></a></li>
<li><a href="https://youtube-lab.techidaily.com/n-2024-from-template-to-trendsetter-gamer-channel-banners-guide/"><u>[New] In 2024, From Template to Trendsetter Gamer Channel Banners Guide</u></a></li>
<li><a href="https://techtrends.techidaily.com/1-free-online-tool-simple-and-effortless-audio-separation-from-videodvd-files/"><u>1. Free Online Tool: Simple and Effortless Audio Separation From Video/DVD Files</u></a></li>
<li><a href="https://howto.techidaily.com/9-solutions-to-fix-poco-x5-system-crash-issue-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>9 Solutions to Fix Poco X5 System Crash Issue | Dr.fone</u></a></li>
<li><a href="https://win-excellent.techidaily.com/die-ultimative-losung-fur-apricorn-ssd-klonen-mit-dem-kloon-toolkit-eine-detaillierte-anleitung-und-unverzichtbare-alternativen-verstehen/"><u>Die Ultimative Lösung Für Apricorn SSD Klonen Mit Dem Kloon Toolkit - Eine Detaillierte Anleitung Und Unverzichtbare Alternativen Verstehen</u></a></li>
<li><a href="https://some-tips.techidaily.com/discover-the-ultimate-list-2023s-finest-solar-lighting-solutions-on-zdnet/"><u>Discover the Ultimate List: 2023'S Finest Solar Lighting Solutions on ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/discover-the-ultimate-pick-2022s-leading-pellet-grills-compared-zdnet-exclusive/"><u>Discover the Ultimate Pick: 2022'S Leading Pellet Grills Compared | ZDNET Exclusive</u></a></li>
<li><a href="https://some-tips.techidaily.com/discover-why-zdnet-ranks-the-ecoflow-river-3-as-a-must-have-in-our-pick-for-top-beginners-portable-battery-pack/"><u>Discover Why ZDNet Ranks the EcoFlow River 3 as a Must-Have in Our Pick for Top Beginner's Portable Battery Pack!</u></a></li>
<li><a href="https://some-tips.techidaily.com/electric-bicycle-and-compact-grill-bundle-offer-from-zdnet-ride-and-bbq/"><u>Electric Bicycle and Compact Grill Bundle Offer From ZDNet – Ride and BBQ!</u></a></li>
<li><a href="https://some-tips.techidaily.com/elevate-your-relaxation-game-with-our-choice-of-the-finest/"><u>Elevate Your Relaxation Game with Our Choice of the Finest</u></a></li>
<li><a href="https://some-tips.techidaily.com/elevate-your-security-with-the-waterproof-blink-mini-2-the-ultimate-alternative-to-wyze-cameras-zdnets-expert-review/"><u>Elevate Your Security with the Waterproof Blink Mini 2 - The Ultimate Alternative to Wyze Cameras | ZDNET's Expert Review</u></a></li>
<li><a href="https://win11-tips.techidaily.com/empower-your-pc-configure-mobile-connectivity-with-win-11/"><u>Empower Your PC: Configure Mobile Connectivity with Win 11</u></a></li>
<li><a href="https://some-tips.techidaily.com/essential-tools-and-tips-for-a-flourishing-garden-insights-from-zdnet/"><u>Essential Tools and Tips for a Flourishing Garden: Insights From ZDNET</u></a></li>
<li><a href="https://unlock-android.techidaily.com/how-to-unlock-honor-magic-6-phone-with-broken-screen-by-drfone-android/"><u>How to Unlock Honor Magic 6 Phone with Broken Screen</u></a></li>
<li><a href="https://extra-hints.techidaily.com/premium-data-buffering-unit-for-sony-a7s-ii/"><u>Premium Data Buffering Unit for Sony A7S II</u></a></li>
<li><a href="https://tech-renaissance.techidaily.com/the-ultimate-fix-for-when-system-cant-find-java-vm-missing-jvmdll/"><u>The Ultimate Fix for When System Can’t Find Java VM (Missing JVM.DLL)</u></a></li>
</ul></div>

