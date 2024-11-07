---
title: Two Simple Methods for Updating Applications on Your Mac OS - Insights
date: 2024-11-01T08:43:06.679Z
updated: 2024-11-06T16:23:34.380Z
tags:
  - apple
categories:
  - tech
thumbnail: https://thmb.techidaily.com/0e72ae7670739d2aa724a5c1676e3ea5eb7af36bcb7980843f57c620d01dbd2b.jpg
---

## Two Simple Methods for Updating Applications on Your Mac OS - Insights

![fullscreen-1-4-24-7-23pm](https://www.zdnet.com/a/img/resize/4d0754ca50eca284946b9049b2a02512354bb4c1/2024/01/05/f413ba01-74e1-4edb-8d1e-41b8aa539d45/fullscreen-1-4-24-7-23pm.jpg?auto=webp&width=1280)

Screen Sharing on MacOS Sonoma

Jason Perlow/ZDNET

Any time I see updates available for my MacOS machines, I immediately apply them. Why? Because those updates often contain security patches that keep my computers safe. Those updates might also contain new features for apps or performance and reliability improvements. Either way, I find these updates to be an essential part of [maintaining the security of my devices](https://www.zdnet.com/article/how-to-update-every-apple-device/) and keeping my mind at ease.

**Also: [How I purged over 175GB of files from my Mac in under a minute (and you can too)](https://www.zdnet.com/article/how-i-purged-over-175gb-of-files-from-my-mac-in-under-a-minute/)**

When I go to update a MacOS device, I know there's more than one way to approach the task -- from the App Store (via the MacOS GUI) or from the command line. Because I've spent decades [working with Linux](https://www.zdnet.com/article/thinking-about-switching-to-linux-things-you-need-to-know/), I'm 100% comfortable using the command line, so I will sometimes open the terminal app, check for upgrades, and then run them when they're available. Or, if I'm feeling a bit lazy, I'll just go the App Store route.

Let me show you both approaches.

>  Disclaimer: This post includes affiliate links
>
>  If you click on a link and make a purchase, I may receive a commission at no extra cost to you.
>

## How to update MacOS apps from the App Store

**What you'll need:** The only things you'll need are an Apple device (a MacBook or iMac) and a valid user account on the machine. That's it. Let's get to the updates.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135395/19272" target="_top" id="2135395">
  <img src="//a.impactradius-go.com/display-ad/19272-2135395" border="0" alt="https://techidaily.com" width="125" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135395/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## 1\. Open the App Store

The fastest way to check and see if there are any updates available is by clicking the Apple button in the upper-left corner, where you might see something like _2 updates_ listed (indicating you have two apps that have updates available). Click that entry to open the App Store.

I have two available updates on my MacBook Pro.

Screenshot by Jack Wallen/ZDNET

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

## 2\. Update your apps

When the App Store opens, you can either update the apps individually (by clicking the Update button associated with the app in question) or update them all at once (by clicking Update All). During the update process, you might be prompted to close an app (or even a related app) if it's blocking the update from continuing. Should that be the case, close the app in question, return to the App Store, and click Continue from the pop-up warning.

These two apps on my MacBook Pro have pending updates.

Screenshot by Jack Wallen/ZDNET

Once the update is completed, close the App Store and you're done.

## How to update MacOS apps from the command line

This is a bit more complicated, for two reasons: first, you have to find out what apps are available for updating, and, second -- as with Linux -- the app names are case-sensitive.

<!-- affiliate ads begin -->
<a href="https://laganoo.pxf.io/c/5597632/1484909/16446" target="_top" id="1484909">
  <img src="//a.impactradius-go.com/display-ad/16446-1484909" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://laganoo.pxf.io/i/5597632/1484909/16446" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## 1\. Open the Terminal app

To run commands, you must first open the terminal app, which can be done from the Launchpad. Click the Launchpad icon in your Dock and then type _terminal_. Click the launcher to open the Terminal app.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135408/19272" target="_top" id="2135408">
  <img src="//a.impactradius-go.com/display-ad/19272-2135408" border="0" alt="https://techidaily.com" width="120" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135408/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## 2\. Check for available updates

Next, you need to run the command to check for updates. The command in question is _softwareupdate_ and is used for both checking and running the updates. To check for available updates, issue the command:

sudo softwareupdate -l

You will be prompted for your sudo password (which is your MacOS user password). 

**Also: [How to update every Apple device (iPhone, iPad, Apple Watch, Mac, more)](https://www.zdnet.com/article/how-to-update-every-apple-device/)**

The -l option stands for _list_. This will print out any available app updates and, if required, it will inform you if a restart is needed to complete any recent OS updates. If you see such a warning, make sure to do the reboot to complete the process.

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2136626/26400" target="_top" id="2136626">
  <img src="//a.impactradius-go.com/display-ad/26400-2136626" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2136626/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## 3\. Update the apps

Let's say the command lists that Apple Mail has an update available, which should be listed as _Mail_ (remember, case sensitivity). Before you update the app, make sure to close it first. Once closed, update the app with a command like this:

sudo softwareupdate -i Mail

After successfully typing your sudo password, the update will proceed. When the update completes, you may or may not have to restart the machine. (You will be informed if a reboot is necessary.) You can then re-open the app you just updated and enjoy whatever fresh features or security patches the update applied.

**Also: [The Apple products you shouldn't buy this month](https://www.zdnet.com/article/the-apple-products-you-shouldnt-buy-this-month/)** 

This is about as simple a method as you'll find to help keep your MacOS machines running smoothly and securely. Never leave an app update lingering because it often contains security patches, which are required for the health and well-being of your operating system.

#### Apple

[iPhone 16 Pro upgrade: If you have a 3 year-old iPhone, here are all the new features you'll get](https://www.zdnet.com/article/iphone-16-pro-and-pro-max-hands-on/ "iPhone 16 Pro upgrade: If you have a 3 year-old iPhone, here are all the new features you'll get")

[My biggest regret with upgrading my iPhone to iOS 18 (and I'm not alone)](https://www.zdnet.com/article/my-biggest-regret-with-upgrading-my-iphone-to-ios-18-and-im-not-alone/ "My biggest regret with upgrading my iPhone to iOS 18 (and I'm not alone)")

[We've used every iPhone 16 model and here's our best buying advice for 2024](https://www.zdnet.com/article/iphone-16-pro-max-buying-advice-2024/ "We've used every iPhone 16 model and here's our best buying advice for 2024")

[6 iOS 18 settings I changed immediately - and why you should too](https://www.zdnet.com/article/6-ios-18-settings-i-changed-immediately-and-why-you-should-too/ "6 iOS 18 settings I changed immediately - and why you should too")

* [iPhone 16 Pro upgrade: If you have a 3 year-old iPhone, here are all the new features you'll get](https://www.zdnet.com/article/iphone-16-pro-and-pro-max-hands-on/ "iPhone 16 Pro upgrade: If you have a 3 year-old iPhone, here are all the new features you'll get")
* [My biggest regret with upgrading my iPhone to iOS 18 (and I'm not alone)](https://www.zdnet.com/article/my-biggest-regret-with-upgrading-my-iphone-to-ios-18-and-im-not-alone/ "My biggest regret with upgrading my iPhone to iOS 18 (and I'm not alone)")
* [We've used every iPhone 16 model and here's our best buying advice for 2024](https://www.zdnet.com/article/iphone-16-pro-max-buying-advice-2024/ "We've used every iPhone 16 model and here's our best buying advice for 2024")
* [6 iOS 18 settings I changed immediately - and why you should too](https://www.zdnet.com/article/6-ios-18-settings-i-changed-immediately-and-why-you-should-too/ "6 iOS 18 settings I changed immediately - and why you should too")

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
<li><a href="https://youtube-blog.techidaily.com/urchasing-options-choosing-premium-vs-standard-fixtures-and-whether-they-are-integrated-or-retrofit-options-can-alter-costs/"><u>[New] __Purchasing Options__ Choosing Premium Vs. Standard Fixtures and Whether They Are Integrated or Retrofit Options Can Alter Costs.</u></a></li>
<li><a href="https://article-helps.techidaily.com/new-mastering-audio-for-digital-unboxing-scenes/"><u>[New] Mastering Audio for Digital Unboxing Scenes</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-photo-magic-weaving-text-into-your-imagery-journey/"><u>[New] Photo Magic Weaving Text Into Your Imagery Journey</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-quest-for-optimal-video-viewing-vlcs-stand-against-mpc/"><u>[New] The Quest for Optimal Video Viewing VLC's Stand Against MPC</u></a></li>
<li><a href="https://facebook-video-recording.techidaily.com/new-ultimate-mp4-uploader-for-fb/"><u>[New] Ultimate MP4 Uploader for FB</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-top-digital-aids-to-supercharge-your-video-subtitles-accuracy/"><u>[Updated] Top Digital Aids to Supercharge Your Video Subtitles' Accuracy</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-complete-srt-reference-manual/"><u>2024 Approved The Complete SRT Reference Manual</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-transform-your-streams-best-4k-video-downloaders-summarized/"><u>2024 Approved Transform Your Streams Best 4K Video Downloaders Summarized</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-path-to-smooth-transitions-in-inshot-editing/"><u>In 2024, The Path to Smooth Transitions in Inshot Editing</u></a></li>
<li><a href="https://win-hot.techidaily.com/1728479471838-samsung/"><u>Samsung 資料夾移行時產生了什麼問題？深入探究克隆過程中的反應問題</u></a></li>
<li><a href="https://win11.techidaily.com/spinning-visuals-easy-6-tips-to-flip-image-on-your-pc/"><u>Spinning Visuals Easy: 6 Tips to Flip Image on Your PC</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-art-of-audio-integration-tunes-for-your-microsoft-slides-for-2024/"><u>The Art of Audio Integration Tunes for Your Microsoft Slides for 2024</u></a></li>
<li><a href="https://tech-renaissance.techidaily.com/ultimate-guide-merging-excel-columns-seamlessly/"><u>Ultimate Guide: Merging Excel Columns Seamlessly</u></a></li>
<li><a href="https://facebook-video-share.techidaily.com/vlogging-vs-micro-video-which-outperforms-for-2024-youtubes-shorts-or-tiktoks/"><u>Vlogging Vs. Micro-Video Which Outperforms for 2024 YouTubes Shorts or TikToks?</u></a></li>
<li><a href="https://blue-screen-error.techidaily.com/windows-11-driver-exception-pool-error-fixes-comprehensive-troubleshooting-techniques/"><u>Windows 11 Driver Exception Pool Error Fixes: Comprehensive Troubleshooting Techniques</u></a></li>
</ul></div>

