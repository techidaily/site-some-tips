---
title: "Massive Disruption: Unraveling the Causes Behind the Recent Microsoft 365, Teams & Outlook Downtime"
date: 2025-01-08T16:04:15.837Z
updated: 2025-01-12T19:49:51.201Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/a340b32764d713af4f960a065c1dc4d886b3bb5db9f5a34232b56c8f050ef2ce.jpg
---

## Massive Disruption: Unraveling the Causes Behind the Recent Microsoft 365, Teams & Outlook Downtime

![pc-bored](https://www.zdnet.com/a/img/resize/408ebd0e8ee60ec9b60791f812c680a6417e28b6/2023/01/30/0efaa9c7-ad12-450b-a636-40239ea5be7e/pc-bored.jpg?auto=webp&width=1280)

Image: Getty Images

Microsoft says an update on a router was behind a huge multi-hour outage affecting the Microsoft Wide Area Network (WAN) that made Azure, Microsoft 365 apps, and Power Platform inaccessible to customers across the globe last week. 

The [multi-hour outage last Wednesday](https://www.zdnet.com/article/microsoft-365-outage-hits-teams-and-outlook-users-what-we-know-so-far/) impacted Microsoft Teams, Exchange Online, Outlook, SharePoint Online, OneDrive for Business, Microsoft Graph, PowerBi, M365 Admin Portal, Microsoft Intune, Microsoft Defender for Cloud Apps, and Microsoft Defender for Identity. 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/HaM818fFKXQ?si=ZZLA4lFSHSgCpSE0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<li><a href="https://eaxpv-info.techidaily.com/new-2024-approved-harnessing-online-platforms-beyond-youtube-to-30plus-communities/"><u>[New] 2024 Approved Harnessing Online Platforms Beyond YouTube to 30+ Communities</u></a></li>
<li><a href="https://fox-hovers.techidaily.com/2024-approved-the-quest-for-codec-perfection-is-av1-surpassing-vp9/"><u>2024 Approved The Quest for Codec Perfection Is AV1 Surpassing VP9?</u></a></li>
<li><a href="https://discover-advanced.techidaily.com/abema-pc6/"><u>ABEMA PC録画機能を活用した最高の6つのツール</u></a></li>
<li><a href="https://some-tips.techidaily.com/ace-your-gameplay-with-the-ideal-vpn-in-depth-comparison-and-reviews-by-experts-powered-by-zdnet/"><u>Ace Your Gameplay with the Ideal VPN: In-Depth Comparison & Reviews by Experts | Powered by ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/ace-your-privacy-with-our-pick-of-the-best-apple-tv-vpns-pcmag/"><u>Ace Your Privacy with Our Pick of the Best Apple TV VPNs | PCMag</u></a></li>
<li><a href="https://some-tips.techidaily.com/activate-google-ones-complimentary-vpn-service-on-android-a-step-by-step-guide/"><u>Activate Google One's Complimentary VPN Service on Android - A Step-by-Step Guide</u></a></li>
<li><a href="https://win11-tips.techidaily.com/bridging-the-gap-between-windows-and-photoshop-open-up-delays/"><u>Bridging the Gap Between Windows and PhotoShop Open-Up Delays</u></a></li>
<li><a href="https://some-tips.techidaily.com/choosing-the-right-vpn-nordvpn-vs-surfshark-the-ultimate-comparison-guide-zdnet/"><u>Choosing the Right VPN: NordVPN Vs. Surfshark - The Ultimate Comparison Guide (ZDNet)</u></a></li>
<li><a href="https://some-tips.techidaily.com/discover-the-most-exciting-discounts-on-vpn-services-today-insider-tips-and-tricks/"><u>Discover the Most Exciting Discounts on VPN Services Today - Insider Tips and Tricks!</u></a></li>
<li><a href="https://tech-haven.techidaily.com/easy-guide-transforming-mp4-file-formats-into-avi-without-hassle/"><u>Easy Guide: Transforming MP4 File Formats Into AVI Without Hassle</u></a></li>
<li><a href="https://some-tips.techidaily.com/elite-browser-protection-top-vpn-plugins-for-chrome-rigorously-evaluated-expert-insights-zdnet/"><u>Elite Browser Protection: Top VPN Plugins for Chrome Rigorously Evaluated - Expert Insights | ZDNET</u></a></li>
<li><a href="https://some-tips.techidaily.com/essential-vpn-services-ranked-perfect-match-for-entrepreneurs-and-home-office-it-zdnets-picks/"><u>Essential VPN Services Ranked: Perfect Match for Entrepreneurs & Home Office IT | ZDNet's Picks</u></a></li>
<li><a href="https://desktop-recording.techidaily.com/flawless-transcription-mastery-with-googles-ai-for-2024/"><u>Flawless Transcription Mastery with Google's AI for 2024</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/in-2024-will-pokemon-go-ban-the-account-if-you-use-pgsharp-on-motorola-razr-40-drfone-by-drfone-virtual-android/"><u>In 2024, Will Pokémon Go Ban the Account if You Use PGSharp On Motorola Razr 40 | Dr.fone</u></a></li>
<li><a href="https://instagram-clips.techidaily.com/rise-to-stardom-on-instagram-adopting-tiktoks-winning-strategies/"><u>Rise to Stardom on Instagram Adopting TikTok's Winning Strategies</u></a></li>
<li><a href="https://win-dash.techidaily.com/ultimate-fix-for-compatibility-updating-startech-driver-in-windows-operating-systems/"><u>Ultimate Fix for Compatibility: Updating StarTech Driver in Windows Operating Systems</u></a></li>
</ul></div>

