---
title: Setting Up Various Virtual LANs in macOS to Expand Your Connection Portfolio
date: 2024-10-27T08:11:51.658Z
updated: 2024-11-01T02:06:14.527Z
tags:
  - apple
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/9d62ebaae5cde110de337e500298a1dd86cc5b2c/2022/07/11/47775a46-83d9-4a0e-a1e0-bac36bb3c798/macos-ventura-apple-hero.jpg?width=278&height=156&fit=crop&auto=webp
---

## Enhancing Your macOS Connectivity by Configuring Various Network Places | Expert Advice

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

<!-- affiliate ads begin -->
<a href="https://wigfever.sjv.io/c/5597632/2014850/22899" target="_top" id="2014850">
  <img src="//a.impactradius-go.com/display-ad/22899-2014850" border="0" alt="https://techidaily.com" width="320" height="90"/>
</a>
<img height="0" width="0" src="https://wigfever.sjv.io/i/5597632/2014850/22899" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## How to create different network locations in MacOS

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1915825/19272" target="_top" id="1915825">
  <img src="//a.impactradius-go.com/display-ad/19272-1915825" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1915825/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## Requirements

The only thing you'll need is a device running an updated version of MacOS. This feature works with both wired and wireless connections.

## 1\. Open System Preferences

Click the Apple menu at the top right of your display and select System Preferences from the menu.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1884002/19272" target="_top" id="1884002">
  <img src="//a.impactradius-go.com/display-ad/19272-1884002" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1884002/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## 2\. Open Network

From within System Preferences, click the Network icon to open the Network section.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1948891/19272" target="_top" id="1948891">
  <img src="//a.impactradius-go.com/display-ad/19272-1948891" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1948891/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## 3\. Create a new network location

From the Location drop-down, select Edit Locations. In the resulting pop-up, click + (the plus sign). You will be prompted to name the location, so type a new name and hit Enter on your keyboard, and then click Done.

Creating a new Network Location in MacOS Monterey.

Image: Jack Wallen

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
<li><a href="https://facebook-video-files.techidaily.com/new-2024-approved-top-five-new-facebook-features-you-should-know/"><u>[New] 2024 Approved Top Five New Facebook Features You Should Know</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/new-filmforge-editors-review-complete-overview/"><u>[New] FilmForge Editor's Review – Complete Overview</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-jaunt-vr-journey-explained/"><u>[New] The Jaunt VR Journey Explained</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-ultimate-sierra-icloud-document-and-desktop-guide/"><u>[New] The Ultimate Sierra iCloud Document & Desktop Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-best-professional-template-pack-for-premiere-pro/"><u>[Updated] The Best Professional Template Pack for Premiere Pro</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-top-budget-friendly-sites-for-stunning-fx-on-videos/"><u>[Updated] Top Budget-Friendly Sites For Stunning FX on Videos</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-understanding-luts-to-amplify-your-photo-quality/"><u>[Updated] Understanding LUTs to Amplify Your Photo Quality</u></a></li>
<li><a href="https://fake-location.techidaily.com/apply-these-techniques-to-improve-how-to-detect-fake-gps-location-on-honor-magic-v2-drfone-by-drfone-virtual-android/"><u>Apply These Techniques to Improve How to Detect Fake GPS Location On Honor Magic V2 | Dr.fone</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/experience-luxury-with-our-expert-guide-on-the-gorgeous-dell-xps-13-7390-convertible-laptop/"><u>Experience Luxury with Our Expert Guide on the Gorgeous Dell XPS 13 7390 Convertible Laptop</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/gratis-webm-to-vob-konverter-mooyavi-online-tool/"><u>Gratis Webm-to-Vob Konverter - Mooyavi Online Tool</u></a></li>
<li><a href="https://techidaily.com/how-to-transfer-data-from-apple-iphone-15-to-other-iphone-14-devices-drfone-by-drfone-transfer-data-from-ios-transfer-data-from-ios/"><u>How To Transfer Data From Apple iPhone 15 To Other iPhone 14 devices? | Dr.fone</u></a></li>
<li><a href="https://ios-pokemon-go.techidaily.com/pokemon-go-cooldown-chart-on-apple-iphone-xs-drfone-by-drfone-virtual-ios/"><u>Pokémon Go Cooldown Chart On Apple iPhone XS | Dr.fone</u></a></li>
<li><a href="https://fox-blue.techidaily.com/the-complete-seo-strategy-for-podcast-growth-for-2024/"><u>The Complete Seo Strategy for Podcast Growth for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-15-nba-live-stream-techniques-for-2024/"><u>Top 15 NBA LIVE STREAM Techniques for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-tier-image-manipulations-for-2024/"><u>Top-Tier Image Manipulations for 2024</u></a></li>
<li><a href="https://youtube-lab.techidaily.com/king-youtube-top-rated-pc-and-mobile-video-extractors-for-2024/"><u>Unlocking YouTube Top-Rated PC & Mobile Video Extractors for 2024</u></a></li>
</ul></div>

