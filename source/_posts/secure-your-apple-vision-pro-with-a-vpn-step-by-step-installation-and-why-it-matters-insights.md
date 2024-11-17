---
title: "Secure Your Apple Vision Pro With a VPN: Step-by-Step Installation & Why It Matters | Insights"
date: 2024-11-11T13:07:17.481Z
updated: 2024-11-17T07:05:38.455Z
tags:
  - apple
categories:
  - tech
thumbnail: https://thmb.techidaily.com/de901a9dfeb58de3e9633af24cac79c38827e6567ccf0cdebe9976885fce2e39.png
---

## Secure Your Apple Vision Pro With a VPN: Step-by-Step Installation & Why It Matters | Insights

![cover](https://www.zdnet.com/a/img/resize/2ae9bf524b9cea7e2db4f65c459804299201cd16/2024/04/10/5f3e713a-ccdc-4a7d-a2a1-b36b8f212cc8/cover.jpg?auto=webp&width=1280)

David Gewirtz/ZDNET

One of the killer apps for Apple's Vision Pro headset is using it while traveling, which also happens to be when you most want to use a VPN. I discussed this in a [previous article](https://www.zdnet.com/article/why-youll-need-a-vpn-for-the-vision-pro-and-other-xr-headsets/) \-- before I had access to a Vision Pro -- and did manage to dig around in the emulator and find a setting for VPNs, which boded well for eventual VPN capabilities.

**Also: [Itching to try Vision Pro's Travel Mode? Here's what to expect before you go](https://www.zdnet.com/article/itching-to-try-vision-pros-travel-mode-heres-what-to-expect-before-you-go/)**

Now that I have a headset, I'm happy to report that, yes, installing a VPN on the Vision Pro does work. In this article, I'll take you step by step through installing and configuring a VPN that runs entirely on the Vision Pro device.

>  Disclaimer: This post includes affiliate links
>
>  If you click on a link and make a purchase, I may receive a commission at no extra cost to you.
>

##  Before we begin

Two things are worth noting before we dig in. 

First: The VPN service I'm using is Proton VPN, which I [reviewed last year](https://www.zdnet.com/article/proton-vpn-review/). This article is _not_ a review of Proton VPN. It's an exploration of what's involved in setting up a VPN on the Vision Pro. Of the VPNs available to set up with Apple's headset, Proton was the one with which I was most familiar. So I reached out to their team for a test account.

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

Second: I need to acknowledge and explain the generally low quality of the screenshots. As I discussed in [my article about how to take Vision Pro screenshots](https://www.zdnet.com/article/apple-vision-pro-tricks-how-to-take-perfect-screenshots-and-recordings-and-avoid-weirdness/), the system only provides focused pixels on the small area your eyes are looking at and only takes 1920x1080 pixel images. 

As such, many of the screenshots below are less than stellar. In instances where I wanted you to see a small section of a particular screenshot, I zoomed in tight in Photoshop and used that to illustrate the process. 

Because the screenshot only captures a very small portion of the screen where eyes are focused, I had to take 72 images on the Vision Pro, including many shots of the same screen, in the hopes of getting one that was good enough. I wound up using 21\. Each screenshot in this article has a little expando-square in the upper-right corner. You'll probably want to hit that for most of these screenshots to be able to see the details.

**Also: [Apple Vision Pro tricks: How to take perfect screenshots and recordings (and avoid weirdness)](https://www.zdnet.com/article/apple-vision-pro-tricks-how-to-take-perfect-screenshots-and-recordings-and-avoid-weirdness/)**

I do not care for the Vision Pro's implementation of screenshots. If Apple wants us to tell you folks about how their new invention works, they _really_ need to improve how this is done and let us grab full-frame, full-resolution screenshots. 

With that observation out of the way, let's get started. 

##  Installing the apps

I'm going to install two apps: Proton's VPN and [Speed Test by Ookla](https://apps.apple.com/us/app/speedtest-by-ookla/id300704847). These are not native Vision Pro apps, but Apple allows developers to designate some of their iPad and iPhone apps as suitable for the Vision Pro. 

**Also: [Why you'll need a VPN for the Vision Pro (and other XR headsets)](https://www.zdnet.com/article/why-youll-need-a-vpn-for-the-vision-pro-and-other-xr-headsets/)**

When you open the App Store on the Vision Pro and do a search, you have the option of looking for VisionOS apps or iPad and iPhone apps. To get both of these apps, I told it to search the available iPad and iPhone apps. 

The speed test is the easiest way to see and prove the VPN is in operation. So that's what I installed first. 

I launched the App Store on the Vision Pro itself and searched for "speed test". 

This says "Open" instead of "Get" because I had already installed it on the Vision Pro in the past, but wanted to show you how it looks in the App Store for this article.

Screenshot by David Gewirtz/ZDNET

Next, I looked for the [Proton VPN app](https://apps.apple.com/us/app/proton-vpn-fast-secure/id1437005085) on the traditional apps side of the Vision Pro app store. Notice that it mentions in-app purchases. I didn't have to deal with this, because I'd already set up my account on my Mac. 

Screenshot by David Gewirtz/ZDNET

Once I hit Get, I had to give the App Store my password (which is not entirely enjoyable without a keyboard on the Vision Pro). I was then presented with a confirmation dialog. I pressed Install. 

Screenshot by David Gewirtz/ZDNET

I was then given one more opportunity to confirm the install by pressing the larger button at the top of the headset. 

Screenshot by David Gewirtz/ZDNET

##  Launching the apps

The Vision Pro has two separate structures for apps. Vision Pro native apps are displayed in the main app launcher. But non-native apps, those built for iPads and iPhones, are stored in their own Compatible Apps folder. 

Screenshot by David Gewirtz/ZDNET

The Proton VPN app is on the first page of the folder. 

The two blurred-out apps are icons for apps from developers who are still working on their projects and don't yet want them to be made public.

Screenshot by David Gewirtz/ZDNET

The Speed Test app was installed on the next page of the Compatible Apps folder. 

Screenshot by David Gewirtz/ZDNET

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135406/19272" target="_top" id="2135406">
  <img src="//a.impactradius-go.com/display-ad/19272-2135406" border="0" alt="https://techidaily.com" width="120" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135406/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  Running a local speed test

Once the two apps were installed, but before the VPN was enabled, I ran a local speed test. I wanted to see a baseline of what we were dealing with. Take a look at the following composite screenshot. There's a lot going on here. I overlayed measurements taken on my iPhone on the left side of the screen. 

Screenshot by David Gewirtz/ZDNET

The area marked (1) indicates the download and upload speed of the Vision Pro. The area marked (2) indicates the download and upload speed of the iPhone. The iPhone was a lot faster. These measurements tell you how long it will take to move a block of data like a file. 

The area marked (3) indicates the ping speeds for the Vision Pro, while the area marked (4) indicates the same thing on the iPhone. Ping speeds tell you how long it takes for a packet to go out and back to the network. You want low ping speeds if you're playing a fast game, because you want your target to still be in the same place by the time the network gets your data. 

**Also: [The best VPN services of 2024: Expert tested](https://www.zdnet.com/article/best-vpn/)**

Keep in mind that all of this is before the VPN had been activated or configured into the network stack of the Vision Pro. I was really quite surprised at how much better my four-year-old iPhone was compared to the brand-new $3,500 Vision Pro. 

And, just in case you're curious, here's what my desktop Mac Studio connected via Ethernet scored. It's a lot faster than Wi-Fi, regardless of which device you're measuring against. 

Screenshot by David Gewirtz/ZDNET

Before we move on to installing and testing the VPN, note that Speed Test correctly identified my location as the Pacific Northwest. I'm in Oregon. 

Screenshot by David Gewirtz/ZDNET

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2111967/7443" target="_top" id="2111967">
  <img src="//a.impactradius-go.com/display-ad/7443-2111967" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2111967/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  Installing the VPN

To get started, I went to the Compatible Apps folder and launched Proton VPN. It gave me the option to create an account or log in. 

Screenshot by David Gewirtz/ZDNET

I had previously prepared my account, so I signed in. 

Screenshot by David Gewirtz/ZDNET

Rather than deal with the dreaded floating keyboard, I used the Apple ecosystem's Universal Clipboard feature. I copied the Proton VPN username and password on my Mac, and pasted it on the Vision Pro. (Hint: Hold your thumb and forefinger together to paste.)

**Also: [How to select, copy, and paste on the Apple Vision Pro with hand gestures](https://www.zdnet.com/article/how-to-select-copy-and-paste-on-the-apple-vision-pro-with-hand-gestures/)**

The Proton VPN app gave me the opportunity to save the login information into the iCloud Keychain, which I did. 

Screenshot by David Gewirtz/ZDNET

The first thing I did was hit the Quick Connect button in Proton VPN. Unfortunately, you can't see it in the screenshot all that well because I struggle to get the Vision Pro to focus on items near the bottom of the screen. I'm still exploring why that is; it could have something to do with the shape of my eyes. 

Screenshot by David Gewirtz/ZDNET

As soon as I did that, the Vision Pro dropped out of the virtual environment and put me in passthrough mode, giving me this dialog: 

Yep, that's my Roku TV behind there.

Screenshot by David Gewirtz/ZDNET

This is the meat of the VPN. This is when Proton VPN is actually asking to hook into the Vision Pro's VPN subsystem. It's also showing in Settings, where the VPN is installed and enabled. 

Screenshot by David Gewirtz/ZDNET

You can control whether the VPN activates on demand, or only when you enable it by clicking the Info button. You can also uninstall the VPN using the same interface. 

Screenshot by David Gewirtz/ZDNET

And there you go. There's now a VPN on the Vision Pro. I've been testing using Proton VPN, but because these interfaces are part of VisionOS, it's fair to assume that any VPN app you use, if written properly, should install onto the Vision Pro in roughly the same way. 

**Also: [The best VPNs for iPhone and iPad: Expert tested](https://www.zdnet.com/article/best-iphone-vpn/)**

Next, let's check it out and see if it works.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2075475/7443" target="_top" id="2075475">
  <img src="//a.impactradius-go.com/display-ad/7443-2075475" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2075475/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  Testing the VPN

I'm on the West Coast of the United States, so it makes sense that Quick Connect dropped me into Los Angeles. 

Screenshot by David Gewirtz/ZDNET

When looking at the Speed Test results (it's difficult to see because of how the screenshots blur) and with a bit of resizing and Photoshop magic, you can see where the map says "City of Los Angeles," proving that Speed Test thinks the device being used is in LA, which confirms the VPN is running. 

Screenshot by David Gewirtz/ZDNET

The speed results themselves aren't breathtaking, but they're reasonable. The VPN did cost the network some performance, but at least with these tests, there's still more than enough bandwidth for video streaming. 

**Also: [What is a VPN and why do you need one? All your virtual private network questions answered](https://www.zdnet.com/article/what-is-a-vpn-and-why-do-you-need-one-all-your-virtual-private-network-questions-answered/)**

I did one more test, connecting to London. In Proton VPN, I searched for and found a London-based server. 

Screenshot by David Gewirtz/ZDNET

From there, I established a London connection. 

Screenshot by David Gewirtz/ZDNET

Interestingly, the performance connecting from Oregon to London was better than the connection from Oregon to LA, but not by much. 

Screenshot by David Gewirtz/ZDNET

<!-- affiliate ads begin -->
<a href="https://malaysia-healthcare-travel-council.pxf.io/c/5597632/1557742/17382" target="_top" id="1557742">
  <img src="//a.impactradius-go.com/display-ad/17382-1557742" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://malaysia-healthcare-travel-council.pxf.io/i/5597632/1557742/17382" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## What does it all mean?

One of the more interesting observations comes from this screenshot, showing which machine Speed Test thinks is running its app. 

Screenshot by David Gewirtz/ZDNET

Notice? Speed Test thinks the Apple Vision Pro is an 11-inch 3rd-generation iPad Pro, a tablet sold by Apple from May 2021 through October 2022\. Apps that don't yet know about the Vision Pro as a device seem to see the headset as an iPad. This is why we can run many existing iPad apps, unchanged, on the Vision Pro. 

In any case, the bottom line is that a VPN does, indeed, work on the Vision Pro. Proton VPN works well enough now, and will probably improve once the company optimizes it for the new hardware. 

**Also: [Proton VPN review: A very solid VPN with robust leak protection](https://www.zdnet.com/article/proton-vpn-review/)**

The door is definitely open for VPN use on the Vision Pro. For those using it while traveling, this is a very important capability indeed. 

Do you plan on traveling with your Vision Pro? Have you tried to use a VPN with it yet? Does this article help ease your concerns about being able to protect your data when traveling with a Vision Pro? Let us know in the comments below. 

---

_You can follow my day-to-day project updates on social media. Be sure to subscribe to [my weekly update newsletter](https://advancedgeekery.substack.com/), and follow me on Twitter/X at [@DavidGewirtz](https://twitter.com/davidgewirtz), on Facebook at [Facebook.com/DavidGewirtz](https://www.facebook.com/davidgewirtz), on Instagram at [Instagram.com/DavidGewirtz](https://www.instagram.com/DavidGewirtz/), and on YouTube at [YouTube.com/DavidGewirtzTV](https://www.youtube.com/user/DavidGewirtzTV)._

#### AR + VR

[I replaced my boring workouts with Meta Quest's Supernatural app, and can't imagine going back](https://www.zdnet.com/article/supernatural-on-meta-quest-hands-on/ "I replaced my boring workouts with Meta Quest's Supernatural app, and can't imagine going back")

[This Finnish startup's new VR headset rivals Apple's Vision Pro - and business users will love it](https://www.zdnet.com/article/this-finnish-startups-new-vr-headset-rivals-apples-vision-pro-and-business-users-will-love-it/ "This Finnish startup's new VR headset rivals Apple's Vision Pro - and business users will love it")

[Meta's $500 Quest 3 is the mainstream VR headset I've been waiting for, and it delivers](https://www.zdnet.com/article/meta-quest-3-review/ "Meta's $500 Quest 3 is the mainstream VR headset I've been waiting for, and it delivers")

[I tried Apple Vision Pro and it's far ahead of where I expected](https://www.zdnet.com/article/i-tried-apple-vision-pro-and-its-far-ahead-of-where-i-expected/ "I tried Apple Vision Pro and it's far ahead of where I expected")

[The best VR headsets right now (and they're not just from Meta)](https://www.zdnet.com/article/best-vr-headset/ "The best VR headsets right now (and they're not just from Meta)")

* [I replaced my boring workouts with Meta Quest's Supernatural app, and can't imagine going back](https://www.zdnet.com/article/supernatural-on-meta-quest-hands-on/ "I replaced my boring workouts with Meta Quest's Supernatural app, and can't imagine going back")
* [This Finnish startup's new VR headset rivals Apple's Vision Pro - and business users will love it](https://www.zdnet.com/article/this-finnish-startups-new-vr-headset-rivals-apples-vision-pro-and-business-users-will-love-it/ "This Finnish startup's new VR headset rivals Apple's Vision Pro - and business users will love it")
* [Meta's $500 Quest 3 is the mainstream VR headset I've been waiting for, and it delivers](https://www.zdnet.com/article/meta-quest-3-review/ "Meta's $500 Quest 3 is the mainstream VR headset I've been waiting for, and it delivers")
* [I tried Apple Vision Pro and it's far ahead of where I expected](https://www.zdnet.com/article/i-tried-apple-vision-pro-and-its-far-ahead-of-where-i-expected/ "I tried Apple Vision Pro and it's far ahead of where I expected")
* [The best VR headsets right now (and they're not just from Meta)](https://www.zdnet.com/article/best-vr-headset/ "The best VR headsets right now (and they're not just from Meta)")

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
<li><a href="https://youtube-lab.techidaily.com/024-approved-free-tools-for-effortless-video-image-retrieval/"><u>[New] 2024 Approved Free Tools for Effortless Video Image Retrieval</u></a></li>
<li><a href="https://video-capture.techidaily.com/new-netflixs-secret-ally-your-mac-for-recording-entertainment-for-2024/"><u>[New] Netflix's Secret Ally Your Mac for Recording Entertainment for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-complete-checklist-for-internet-broadcast-preservation/"><u>[New] The Complete Checklist for Internet Broadcast Preservation</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unlocking-success-the-essentials-of-crafting-great-reddit-threads/"><u>[New] Unlocking Success The Essentials of Crafting Great Reddit Threads</u></a></li>
<li><a href="https://fox-helps.techidaily.com/updated-delving-into-the-chronology-of-windows-movie-maker-editions/"><u>[Updated] Delving Into the Chronology of Windows Movie Maker Editions</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-ultimate-guide-to-stretched-seconds-capturing-slow-mo-videos-using-mobile-apps-and-internet-platforms/"><u>[Updated] The Ultimate Guide to Stretched Seconds Capturing Slow-Mo Videos Using Mobile Apps and Internet Platforms</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unveiling-cosmic-divides-metaverse-and-multiverse-explained/"><u>[Updated] Unveiling Cosmic Divides Metaverse and Multiverse Explained</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-best-budget-camera-stabilizers-for-youtube-stars/"><u>2024 Approved The Best Budget Camera Stabilizers for YouTube Stars</u></a></li>
<li><a href="https://fox-hovers.techidaily.com/embarking-on-the-av1-coding-journey/"><u>Embarking on the AV1 Coding Journey</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/explore-the-ultimate-selection-find-dells-greatest-deals-of-cyber-monday-across-best-buy-amazon-newegg-et-al-insights/"><u>Explore the Ultimate Selection: Find Dell's Greatest Deals of Cyber Monday Across Best Buy, Amazon, Newegg, Et Al. - Insights</u></a></li>
<li><a href="https://techidaily.com/how-to-factory-reset-nubia-red-magic-8s-proplus-without-losing-data-drfone-by-drfone-reset-android-reset-android/"><u>How to Factory Reset Nubia Red Magic 8S Pro+ without Losing Data | Dr.fone</u></a></li>
<li><a href="https://unlock-android.techidaily.com/in-2024-bypassing-google-account-with-vnrom-bypass-for-xiaomi-redmi-a2plus-by-drfone-android/"><u>In 2024, Bypassing Google Account With vnROM Bypass For Xiaomi Redmi A2+</u></a></li>
<li><a href="https://review-topics.techidaily.com/in-2024-does-airplane-mode-turn-off-gps-location-on-oppo-a38-drfone-by-drfone-virtual-android/"><u>In 2024, Does Airplane Mode Turn off GPS Location On Oppo A38? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-complete-guide-to-adding-powerful-narrations/"><u>In 2024, The Complete Guide to Adding Powerful Narrations</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-timing-translation-from-20mb-to-seconds-measurement/"><u>In 2024, Timing Translation From 20Mb to Seconds Measurement</u></a></li>
<li><a href="https://techno-recovery.techidaily.com/navigating-a-world-of-devices-how-edge-computing-impacts-job-prospects-insights-from-zdnet/"><u>Navigating a World of Devices: How Edge Computing Impacts Job Prospects - Insights From ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/unmatched-4k-hdtvs-for-intense-gaming-for-2024/"><u>Unmatched 4K HDTVs for Intense Gaming for 2024</u></a></li>
</ul></div>

