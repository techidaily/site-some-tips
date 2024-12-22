---
title: "Inside the Tech Meltdhrenous: Analyzing Factors of the Major Microsoft Suite Outage Event"
date: 2024-12-15T19:13:08.712Z
updated: 2024-12-21T04:08:55.159Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/845fcd5e3eadfdeed515b58ea51b6008ffc3adda0043bb6ffedd07e36277b4e8.jpg
---

## Inside the Tech Meltdhrenous: Analyzing Factors of the Major Microsoft Suite Outage Event

![pc-bored](https://www.zdnet.com/a/img/resize/408ebd0e8ee60ec9b60791f812c680a6417e28b6/2023/01/30/0efaa9c7-ad12-450b-a636-40239ea5be7e/pc-bored.jpg?auto=webp&width=1280)

Image: Getty Images

Microsoft says an update on a router was behind a huge multi-hour outage affecting the Microsoft Wide Area Network (WAN) that made Azure, Microsoft 365 apps, and Power Platform inaccessible to customers across the globe last week. 

The [multi-hour outage last Wednesday](https://www.zdnet.com/article/microsoft-365-outage-hits-teams-and-outlook-users-what-we-know-so-far/) impacted Microsoft Teams, Exchange Online, Outlook, SharePoint Online, OneDrive for Business, Microsoft Graph, PowerBi, M365 Admin Portal, Microsoft Intune, Microsoft Defender for Cloud Apps, and Microsoft Defender for Identity. 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/P6Wfzj6YNDM?si=WRZQD9zCdQ1_tW1b" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<li><a href="https://fox-cloud.techidaily.com/new-in-2024-effective-strategies-for-podcast-on-insta-story-and-posts/"><u>[New] In 2024, Effective Strategies for Podcast on Insta Story & Posts</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/new-in-2024-gaming-evolved-streaming-xbox-content-on-facebook/"><u>[New] In 2024, Gaming Evolved Streaming Xbox Content on Facebook</u></a></li>
<li><a href="https://fox-glue.techidaily.com/new-prime-color-balancer-suite-for-2024/"><u>[New] Prime Color Balancer Suite for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-supercharge-your-design-with-these-canva-insider-tips/"><u>[Updated] Supercharge Your Design with These Canva Insider Tips</u></a></li>
<li><a href="https://fox-http.techidaily.com/updated-symbolize-your-brand-exclusive-access-to-free-customizable-logos-for-2024/"><u>[Updated] Symbolize Your Brand Exclusive Access to Free, Customizable Logos for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-ultimate-list-of-iphone-selfie-perks-8/"><u>[Updated] The Ultimate List of IPhone Selfie Perks #8</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-ultimate-guide-9-essential-360-degree-recording-techniques/"><u>[Updated] Ultimate Guide 9 Essential 360-Degree Recording Techniques</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-ultimate-guide-9-premier-video-translators-for-accurate-global-communication/"><u>[Updated] Ultimate Guide 9 Premier Video Translators for Accurate Global Communication</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-understanding-and-applying-auto-hdr-a-windows-11-tutorial/"><u>[Updated] Understanding and Applying Auto HDR A Windows 11 Tutorial</u></a></li>
<li><a href="https://youtube-zero.techidaily.com/approved-nextgen-youtuber-tools-studio-vs-beta-version/"><u>2024 Approved NextGen YouTuber Tools Studio Vs. Beta Version</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-perfect-portrait-retouching-conceal-dont-deceive/"><u>2024 Approved Perfect Portrait Retouching Conceal, Don't Deceive</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-strategic-steps-for-a-million-viewing-video-masterpiece/"><u>2024 Approved Strategic Steps for a Million-Viewing Video Masterpiece</u></a></li>
<li><a href="https://win11-tips.techidaily.com/customize-mouse-indicator-for-a-unique-style/"><u>Customize Mouse Indicator for a Unique Style</u></a></li>
<li><a href="https://vp-tips.techidaily.com/dynamic-broadcasting-with-manycam-your-ultimate-solution-for-live-streams-and-remote-webcams/"><u>Dynamic Broadcasting with ManyCam: Your Ultimate Solution for Live Streams and Remote Webcams</u></a></li>
<li><a href="https://facebook.techidaily.com/englands-premier-footballers-pledge-no-more-online-presence-for-safety/"><u>England's Premier Footballers Pledge No More Online Presence for Safety</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-streaming-success-implementing-green-screen-innovations/"><u>In 2024, Streaming Success Implementing Green Screen Innovations</u></a></li>
<li><a href="https://easy-unlock-android.techidaily.com/in-2024-tips-and-tricks-for-setting-up-your-motorola-moto-g34-5g-phone-pattern-lock-by-drfone-android/"><u>In 2024, Tips and Tricks for Setting Up your Motorola Moto G34 5G Phone Pattern Lock</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-complete-how-to-for-mac-obs-plus-streamlabs-integration-for-2024/"><u>The Complete How-To for Mac OBS + Streamlabs Integration for 2024</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/what-is-a-sim-network-unlock-pin-get-your-motorola-edge-40-phone-network-ready-by-drfone-android/"><u>What Is a SIM Network Unlock PIN? Get Your Motorola Edge 40 Phone Network-Ready</u></a></li>
</ul></div>

