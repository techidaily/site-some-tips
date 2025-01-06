---
title: "Unraveling the Reasons Behind the Major Outage in Microsoft 365, Teams & Outlook: An In-Depth Analysis by ZDNet"
date: 2025-01-01T22:08:19.184Z
updated: 2025-01-05T20:56:10.248Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/b89ffcd4bf4187d5ce782fa255f3d31e70eba20fbf846963d325dce5a6f79e5f.jpg
---

## Unraveling the Reasons Behind the Major Outage in Microsoft 365, Teams & Outlook: An In-Depth Analysis by ZDNet

![pc-bored](https://www.zdnet.com/a/img/resize/408ebd0e8ee60ec9b60791f812c680a6417e28b6/2023/01/30/0efaa9c7-ad12-450b-a636-40239ea5be7e/pc-bored.jpg?auto=webp&width=1280)

Image: Getty Images

Microsoft says an update on a router was behind a huge multi-hour outage affecting the Microsoft Wide Area Network (WAN) that made Azure, Microsoft 365 apps, and Power Platform inaccessible to customers across the globe last week. 

The [multi-hour outage last Wednesday](https://www.zdnet.com/article/microsoft-365-outage-hits-teams-and-outlook-users-what-we-know-so-far/) impacted Microsoft Teams, Exchange Online, Outlook, SharePoint Online, OneDrive for Business, Microsoft Graph, PowerBi, M365 Admin Portal, Microsoft Intune, Microsoft Defender for Cloud Apps, and Microsoft Defender for Identity. 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/iPCr_bxZjMQ?si=ubOsoq5umPEXL9xL" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<li><a href="https://some-techniques.techidaily.com/new-from-beginner-to-star-top-25-vlogging-ideas/"><u>[New] From Beginner to Star Top 25 Vlogging Ideas</u></a></li>
<li><a href="https://facebook-record-videos.techidaily.com/updated-in-2024-enhancing-visibility-popularize-your-youtube-short-videos/"><u>[Updated] In 2024, Enhancing Visibility Popularize Your YouTube Short Videos</u></a></li>
<li><a href="https://youtube-blog.techidaily.com/ed-in-2024-essential-youtube-seo-techniques-for-enhanced-video-rankings/"><u>[Updated] In 2024, Essential YouTube SEO Techniques for Enhanced Video Rankings</u></a></li>
<li><a href="https://some-approaches.techidaily.com/updated-unlocking-10plus-top-free-subtitle-converter-websites/"><u>[Updated] Unlocking 10+ Top Free Subtitle Converter Websites</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/can-t-view-hevc-h-265-content-on-xiaomi-13-ultra-by-aiseesoft-video-converter-play-hevc-video-on-android/"><u>Can’t view HEVC H.265 content on Xiaomi 13 Ultra</u></a></li>
<li><a href="https://some-tips.techidaily.com/expand-your-digital-space-apple-introduces-new-6tb-and-12tb-icloudplus-plans-for-just-30-60month-discover-more-on-zdnet/"><u>Expand Your Digital Space: Apple Introduces New 6TB & 12TB iCloud+ Plans for Just $30-$60/Month – Discover More on ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/explore-how-database-operating-systems-thrive-in-the-cloud-unlike-linux-get-your-free-trial-today/"><u>Explore How Database Operating Systems Thrive in the Cloud Unlike Linux – Get Your Free Trial Today!</u></a></li>
<li><a href="https://some-tips.techidaily.com/exploring-awss-latest-industry-moves-unveiled-at-the-reinvent-2021-conference-zdnet-analysis/"><u>Exploring AWS's Latest Industry Moves Unveiled at the Re:Invent 2021 Conference | ZDNet Analysis</u></a></li>
<li><a href="https://review-topics.techidaily.com/in-2024-how-to-change-netflix-location-to-get-more-country-version-on-vivo-y200-drfone-by-drfone-virtual-android/"><u>In 2024, How to Change Netflix Location to Get More Country Version On Vivo Y200 | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/launching-sbom-capabilities-with-codenotary-for-enhanced-kubernetes-security-insights-on-zdnet/"><u>Launching SBOM Capabilities with Codenotary for Enhanced Kubernetes Security - Insights on ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/next-gen-ai-integration-boosts-google-clouds-developer-resources-and-analytical-power-according-to-zdnet/"><u>Next-Gen AI Integration Boosts Google Cloud's Developer Resources & Analytical Power, According to ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/quick-and-simple-steps-to-set-up-your-own-cloud-service-at-home-within-one-hour-insights-from-zdnet/"><u>Quick and Simple Steps to Set Up Your Own Cloud Service at Home Within One Hour - Insights From ZDNet</u></a></li>
<li><a href="https://youtube-webster.techidaily.com/y-streamers-the-creme-de-la-cuisine/"><u>Savory Streamers The Crème De La Cuisine</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-critical-role-of-active-oversight-in-cloud-security-management/"><u>The Critical Role of Active Oversight in Cloud Security Management</u></a></li>
<li><a href="https://some-tips.techidaily.com/understanding-the-cause-behind-the-major-microsoft-365-teams-and-outlook-disruption-an-insightful-breakdown/"><u>Understanding the Cause Behind the Major Microsoft 365, Teams & Outlook Disruption: An Insightful Breakdown</u></a></li>
<li><a href="https://fox-glue.techidaily.com/unlock-the-world-of-vr-with-your-phone-in-minutes-for-2024/"><u>Unlock the World of VR with Your Phone in Minutes for 2024</u></a></li>
<li><a href="https://fox-hovers.techidaily.com/vivavideo-review-the-users-perspective-for-2024/"><u>VivaVideo Review The User's Perspective for 2024</u></a></li>
</ul></div>

