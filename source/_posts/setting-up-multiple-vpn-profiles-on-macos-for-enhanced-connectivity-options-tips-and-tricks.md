---
title: Setting Up Multiple VPN Profiles on macOS for Enhanced Connectivity Options | Tips & Tricks
date: 2024-10-22T17:11:23.545Z
updated: 2024-10-26T16:25:32.833Z
tags:
  - apple
categories:
  - tech
thumbnail: https://thmb.techidaily.com/f68ad44dfce4596bff961c8c73128e503881dbfbd95e5f1787a78426eec3f375.jpg
---

## Setting Up Multiple VPN Profiles on macOS for Enhanced Connectivity Options | Tips & Tricks

![MacOS Ventura](https://www.zdnet.com/a/img/resize/f9b803b11abf24ef89a80e3eab2b456c1d35293a/2022/07/11/47775a46-83d9-4a0e-a1e0-bac36bb3c798/macos-ventura-apple-hero.jpg?auto=webp&width=1280)

Apple

I connect to a lot of different networks. At home, I have three different LANs to choose from, which I use depending on my needs. For example, I have a general-purpose network and one that I use for the deployment of containers and the like. 

>  Disclaimer: This post includes affiliate links
>
>  If you click on a link and make a purchase, I may receive a commission at no extra cost to you.
>

### **ZDNET** Recommends

[The best Macs Apple's Mac lineup can be confusing as the company transitions from Intel processors to its own Apple Silicon processors. But we're here to help.  Read now](https://www.zdnet.com/article/best-mac/)

For the general-purpose network, I can just have MacOS accept an IP address from the DHCP server. However, for the container network, I prefer assigning a static IP address.

Is this possible?

It certainly is. With the help of MacOS Network Locations, you can assign specific configurations for specific networks (or locations) and even define a particular network you want to connect to within a location.

Let me show you how it works.

**Also:** [**How to manage SSH connections on MacOS with Termius**](https://www.zdnet.com/article/how-to-manage-ssh-connections-on-macos-with-termius/) 

## How to create different network locations in MacOS

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2111964/7443" target="_top" id="2111964">
  <img src="//a.impactradius-go.com/display-ad/7443-2111964" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2111964/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## Requirements

The only thing you'll need is a device running an updated version of MacOS. This feature works with both wired and wireless connections.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2137394/7443" target="_top" id="2137394">
  <img src="//a.impactradius-go.com/display-ad/7443-2137394" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2137394/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## 1\. Open System Preferences

Click the Apple menu at the top right of your display and select System Preferences from the menu.

## 2\. Open Network

From within System Preferences, click the Network icon to open the Network section.

<!-- affiliate ads begin -->
<a href="https://bluettide.pxf.io/c/5597632/2141684/17092" target="_top" id="2141684">
  <img src="//a.impactradius-go.com/display-ad/17092-2141684" border="0" alt="https://techidaily.com" width="120" height="90"/>
</a>
<img height="0" width="0" src="https://bluettide.pxf.io/i/5597632/2141684/17092" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## 3\. Create a new network location

From the Location drop-down, select Edit Locations. In the resulting pop-up, click + (the plus sign). You will be prompted to name the location, so type a new name and hit Enter on your keyboard, and then click Done.

Creating a new Network Location in MacOS Monterey.

Image: Jack Wallen

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2094479/7443" target="_top" id="2094479">
  <img src="//a.impactradius-go.com/display-ad/7443-2094479" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2094479/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## 4\. Configure the new location

Make sure to select the new location you created from the Location drop-down. Click Advanced to open the location configuration window, where you can configure the location to meet your specific needs. For example, you can select the network to be used and then configure that network for a static IP address using the Cloudflare DNS servers.

Configuring a network for the new location in MacOS.

Image: Jack Wallen

Once you've configured the location exactly how you need it, click Apply to save everything.

## Switching to a different Network Location

After you've created all of the network locations you need, MacOS makes it very easy to switch between them. All you have to do is click the Apple menu > Location > \[Location name\] (select the name of the location you want to use).

Switching between network locations is a few mouse clicks away.

Image: Jack Wallen

And that's all there is to creating and using network locations in MacOS. If you need to get specific with how your MacOS device interacts with a network, this is a great way to go. Just remember, however, if you move from the current location, you'll want to select another. For example, if you have [one location for home and one for work](https://www.zdnet.com/article/hybrid-workers-dont-want-to-return-to-the-office-but-soon-they-might-have-to/), your machine might have trouble connecting to that work LAN with the home settings.

  
Fortunately, you are now empowered to more easily make that switch.

#### Jack Wallen: Here's how to...

[How to get true window snapping in MacOS](https://www.zdnet.com/article/how-to-get-true-window-snapping-in-macos/ "How to get true window snapping in MacOS")

[The AGM 5 Pro might be the loudest Android phone ever](https://www.zdnet.com/article/the-agm-5-pro-might-be-the-loudest-android-phone-ever/ "The AGM 5 Pro might be the loudest Android phone ever")

[Nitrux 2.4 Linux distro shows promise](https://www.zdnet.com/article/nitrux-2-4-linux-distribution-shows-promise-but-seems-rough-around-the-edges/ "Nitrux 2.4 Linux distro shows promise")

[Tired of being tracked online? DuckDuckGo's Email Protection can help](https://www.zdnet.com/article/tired-of-being-tracked-online-duckduckgos-email-protection-can-help/ "Tired of being tracked online? DuckDuckGo's Email Protection can help")

* [How to get true window snapping in MacOS](https://www.zdnet.com/article/how-to-get-true-window-snapping-in-macos/ "How to get true window snapping in MacOS")
* [The AGM 5 Pro might be the loudest Android phone ever](https://www.zdnet.com/article/the-agm-5-pro-might-be-the-loudest-android-phone-ever/ "The AGM 5 Pro might be the loudest Android phone ever")
* [Nitrux 2.4 Linux distro shows promise](https://www.zdnet.com/article/nitrux-2-4-linux-distribution-shows-promise-but-seems-rough-around-the-edges/ "Nitrux 2.4 Linux distro shows promise")
* [Tired of being tracked online? DuckDuckGo's Email Protection can help](https://www.zdnet.com/article/tired-of-being-tracked-online-duckduckgos-email-protection-can-help/ "Tired of being tracked online? DuckDuckGo's Email Protection can help")

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
<li><a href="https://some-tips.techidaily.com/new-the-secret-to-love-in-video-editing-filmoras-best-aspects/"><u>[New] The Secret to Love in Video Editing Filmora's Best Aspects</u></a></li>
<li><a href="https://some-skills.techidaily.com/new-top-ranked-audio-respeeders-mobile-desktop/"><u>[New] Top-Ranked Audio Respeeders (Mobile, Desktop)</u></a></li>
<li><a href="https://tiktok-videos.techidaily.com/updated-enhance-your-vision-a-compreeved-guide-to-tiktok-video-captioning/"><u>[Updated] Enhance Your Vision A Compreeved Guide to TikTok Video Captioning</u></a></li>
<li><a href="https://fox-access.techidaily.com/updated-in-2024-mastering-iphone-photo-blurring-4-techniques-explored/"><u>[Updated] In 2024, Mastering iPhone Photo Blurring 4 Techniques Explored</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-iphone-tips-bringing-out-the-best-with-hdr-photography/"><u>[Updated] IPhone Tips Bringing Out the Best with HDR Photography</u></a></li>
<li><a href="https://facebook-videos.techidaily.com/updated-tips-for-troubled-feed-viewers-reveal-hidden-fb-videos-for-2024/"><u>[Updated] Tips for Troubled Feed Viewers Reveal Hidden FB Videos for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unraveling-best-practices-for-effective-fb-healthcare-promos/"><u>[Updated] Unraveling Best Practices for Effective FB Healthcare Promos</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/updated-veiled-vocal-vaults-top-6-under-the-radar-mobile-apps/"><u>[Updated] Veiled Vocal Vaults Top 6 Under-the-Radar Mobile Apps</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/2024-approved-liveoutnow-an-in-depth-look-at-effortless-podcast-live-streaming/"><u>2024 Approved LiveOutNow An In-Depth Look at Effortless Podcast Live Streaming</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unveil-clearer-visuals-essential-tips-for-zooming-on-snapchat/"><u>2024 Approved Unveil Clearer Visuals Essential Tips for Zooming on Snapchat</u></a></li>
<li><a href="https://win-howtos.techidaily.com/fixing-boot-issues-how-to-get-your-computer-to-properly-shutdown-windows-10/"><u>Fixing Boot Issues: How To Get Your Computer To Properly Shutdown Windows 10</u></a></li>
<li><a href="https://android-location-track.techidaily.com/how-to-track-nubia-red-magic-8s-proplus-by-phone-number-drfone-by-drfone-virtual-android/"><u>How to Track Nubia Red Magic 8S Pro+ by Phone Number | Dr.fone</u></a></li>
<li><a href="https://fox-access.techidaily.com/the-future-of-drone-control-with-syma-x8c-for-2024/"><u>The Future of Drone Control with Syma X8C for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlock-photo-editing-potential-with-these-clever-pixlr-techniques-for-2024/"><u>Unlock Photo Editing Potential with These Clever Pixlr Techniques for 2024</u></a></li>
</ul></div>

