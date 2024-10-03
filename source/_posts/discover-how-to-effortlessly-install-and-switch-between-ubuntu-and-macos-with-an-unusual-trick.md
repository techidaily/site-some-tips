---
title: Discover How to Effortlessly Install and Switch Between Ubuntu & macOS with an Unusual Trick !
date: 2024-10-02T18:49:13.947Z
updated: 2024-10-03T20:11:08.206Z
tags:
  - apple
categories:
  - tech
thumbnail: https://thmb.techidaily.com/41df33583a82ea2d9923ca08fb1de828ddad2dc59980553349e15164e2adbb30.jpg
---

## Discover How to Effortlessly Install and Switch Between Ubuntu & macOS with an Unusual Trick !

![xcode-download](https://www.zdnet.com/a/img/resize/72daf9c10a8cbb72018f54fd48d893e5c1fdc697/2024/02/20/72eff26e-8b49-4c53-8f95-e123371d2227/xcode-download.jpg?auto=webp&width=1280)

Screenshot by David Gewirtz/ZDNET

So, you want to install Linux on a Mac? Well, there's more than one way to get that done. Compared to what I'm going to show you below, there's a somewhat easier set of steps that my colleague [Adrian Kingsley-Hughes ran through](https://www.zdnet.com/article/how-to-install-kali-linux-on-apple-silicon-macs/) using an installer on the App Store and Kali Linux.

**Also: [How to install Ubuntu Linux (It's easy!)](https://www.zdnet.com/article/how-to-install-ubuntu-linux/)**

But I'm going full geek. Together, we're going to use Xcode and build our own sample app, which we'll then use to install the full distribution of the [latest Ubuntu release](https://www.zdnet.com/article/ubuntu-desktop-23-10-arrives-a-glimpse-into-ubuntu-linuxs-future/), Noble Numbat.

Once you've done this, you will have considerable bragging rights. There's a lot to cover, so let's dig in. 

>  Disclaimer: This post includes affiliate links
>
>  If you click on a link and make a purchase, I may receive a commission at no extra cost to you.
>

##  Download these first

You'll need to download these items before you get started setting up Linux: 

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

**Xcode:** You will need to download and install Xcode from the Mac App Store. Xcode is the primary development environment Apple wants developers to use to build Mac applications and mobile apps. It's free. Just open the App Store app and type "xcode" into the search field.

**The latest build of Ubuntu, for 64-bit Arm:** The Arm installer ISO isn't located on the main Ubuntu download site. Instead, point your browser to the [daily build page](https://cdimage.ubuntu.com/daily-live/current/) and scroll down until you see the desktop image for 64-bit ARM (standard download).

Screenshot by David Gewirtz/ZDNET

**GUILinuxVirtualMachineSampleApp:** [This is a sample app](https://developer.apple.com/documentation/virtualization/running%5Fgui%5Flinux%5Fin%5Fa%5Fvirtual%5Fmachine%5Fon%5Fa%5Fmac) that runs the virtual machine inside of Xcode. You'll need to download it and unzip it. 

Screenshot by David Gewirtz/ZDNET

Before you move on to the next step, be sure that Xcode is fully installed, that you have the Ubuntu .iso file, and that you have downloaded and unzipped the sample app. 

**Also: [Ubuntu Desktop 23.10 arrives: A glimpse into Ubuntu Linux's future](https://www.zdnet.com/article/ubuntu-desktop-23-10-arrives-a-glimpse-into-ubuntu-linuxs-future/)**

Once all of that is done, we can move on. 

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1886044/19272" target="_top" id="1886044">
  <img src="//a.impactradius-go.com/display-ad/19272-1886044" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1886044/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  Configure the VM hosting app in Xcode

Go ahead and open Xcode. You'll see a starter screen. Tell it to open up an existing project. 

Screenshot by David Gewirtz/ZDNET

From here, navigate inside the folder you created when you extracted the sample application, and look for a file ending in .xcodeproj. Click open. 

Screenshot by David Gewirtz/ZDNET

This will open the sample application. Well, actually, it will warn you that you're opening a project downloaded from the Internet. But since the project comes right off the Apple developer site, I think you're good. 

Screenshot by David Gewirtz/ZDNET

Now, you'll have the project open. You need to do a bit of housekeeping, and then you'll be good. 

In the left-most pane, click the top-level sample app (shown at 1). Then, click the Signing & Capabilities tab (shown at 2), and finally, click the Add Account button at the Team prompt (shown at 3). 

Screenshot by David Gewirtz/ZDNET

This will take you to your Accounts tab, where you'll just set yourself up as a team. 

Screenshot by David Gewirtz/ZDNET

Once you've done this, close the window, and you'll be ready to move on. Here, you can see my app is going to be signed by my personal account. This just tells MacOS that it's my app and I want to allow it to run.

Screenshot by David Gewirtz/ZDNET

You're ready to start running the VM. Hit the little arrow to build and run. 

Screenshot by David Gewirtz/ZDNET

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2130886/7443" target="_top" id="2130886">
  <img src="//a.impactradius-go.com/display-ad/7443-2130886" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2130886/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  Installing Ubuntu

Your Xcode app will open a blank black window and a file chooser. The file chooser (although it doesn't tell you this) is looking for the Ubuntu install .iso file. So navigate to that .iso, click it, and click Open. 

Screenshot by David Gewirtz/ZDNET

Next, GRUB (Grand Unified Bootloader) will show up in that black window. Select Try or Install Ubuntu and hit Enter. 

Screenshot by David Gewirtz/ZDNET

And let the magic commence! Ubuntu is getting settled into your Xcode app: 

Screenshot by David Gewirtz/ZDNET

And here you go. Start configuring your Ubuntu install. 

Screenshot by David Gewirtz/ZDNET

Go ahead and select Install Ubuntu since you're already installing into a VM and not directly onto your computer anyway. 

Screenshot by David Gewirtz/ZDNET

I did the full installation: 

Screenshot by David Gewirtz/ZDNET

**Also: [Fedora Linux now runs on all M-powered Macs - except one](https://www.zdnet.com/article/fedora-linux-now-runs-on-all-m-powered-macs-except-one/)**

Use the default, which is to allow the installer to erase the virtual disk and set up your virtual filesystem: 

Screenshot by David Gewirtz/ZDNET

<!-- affiliate ads begin -->
<a href="https://imp.i357552.net/c/5597632/1013424/11832" target="_top" id="1013424">
  <img src="//a.impactradius-go.com/display-ad/11832-1013424" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://imp.i357552.net/i/5597632/1013424/11832" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  Run Ubuntu

Ubuntu is ready to run. Just click Restart Now and go to town. 

Screenshot by David Gewirtz/ZDNET

Once you restart, you'll be in a standard environment, with a nice little virtual machine you can play with. 

Screenshot by David Gewirtz/ZDNET

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2016165/19272" target="_top" id="2016165">
  <img src="//a.impactradius-go.com/display-ad/19272-2016165" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2016165/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  Final thoughts

During the installation phase, the Virtualization framework generates a GUI Linux VM.bundle package within your home folder. This grows fairly quickly, so if you're space-constrained, you may want to delete it when you're done Ubuntuing. Mine is 68.72GB after only a few hours of tinkering. 

**Also: [Ubuntu 23.10 seems like the usual boring update - until you dig into it](https://www.zdnet.com/article/ubuntu-23-10-seems-like-the-usual-boring-update-until-you-dig-in/)**

While the example application is limited to operating a single VM concurrently, the MacOS virtualization framework itself is capable of handling several VMs at the same time. This is not controlled by the application we built, but developers can use this framework to build more powerful virtualization management consoles. 

What do you think? Did you go ahead and install Ubuntu inside Xcode? Are you going to tattoo "Ubuntu/Xcode Forever" on your shoulder? Are you going to sing glorious songs of your Xcode prowess to all who will listen? I mean, you could. If you're not going to belt out songs of Macs and Linux, perhaps you could leave us a few comments below. 

---

_You can follow my day-to-day project updates on social media. Be sure to subscribe to my weekly update newsletter [on Substack](https://advancedgeekery.substack.com/), and follow me on Twitter at [@DavidGewirtz](https://twitter.com/davidgewirtz), on Facebook at [Facebook.com/DavidGewirtz](https://www.facebook.com/davidgewirtz), on Instagram at [Instagram.com/DavidGewirtz](https://www.instagram.com/DavidGewirtz/), and on YouTube at [YouTube.com/DavidGewirtzTV](https://www.youtube.com/user/DavidGewirtzTV)._

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
<li><a href="https://article-tips.techidaily.com/new-longest-flight-drone-champions-unveiled-for-2024/"><u>[New] Longest Flight Drone Champions Unveiled for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-blueprint-to-surge-in-youtubers-popularity/"><u>2024 Approved The Blueprint to Surge in Youtubers' Popularity</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-top-6-video-downloaders-preserve-your-linkedin-media-masterfully/"><u>2024 Approved Top 6 Video Downloaders Preserve Your LinkedIn Media Masterfully</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unleash-creativity-in-videos-with-quick-trims-on-windows-11/"><u>2024 Approved Unleash Creativity in Videos with Quick Trims on Windows 11</u></a></li>
<li><a href="https://android-transfer.techidaily.com/in-2024-how-i-transferred-messages-from-oneplus-ace-2v-to-iphone-12xs-max-in-seconds-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>In 2024, How I Transferred Messages from OnePlus Ace 2V to iPhone 12/XS (Max) in Seconds | Dr.fone</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/in-2024-maximizing-play-in-apex-legends-without-cross-platform-limitations/"><u>In 2024, Maximizing Play in Apex Legends Without Cross-Platform Limitations</u></a></li>
<li><a href="https://extra-guidance.techidaily.com/in-2024-optimal-text-movement-collections/"><u>In 2024, Optimal Text Movement Collections</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-straightforward-approach-to-editing-age-on-tiktok/"><u>In 2024, The Straightforward Approach to Editing Age on TikTok</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-turnback-artisan-hub/"><u>In 2024, Turnback Artisan Hub</u></a></li>
<li><a href="https://review-topics.techidaily.com/remove-google-frp-lock-on-nokia-150-2023-by-drfone-android-unlock-remove-google-frp/"><u>Remove Google FRP lock on Nokia 150 (2023)</u></a></li>
<li><a href="https://tech-haven.techidaily.com/setting-up-codegpt-a-step-by-step-guide-for-visual-studio-code/"><u>Setting Up CodeGPT: A Step-by-Step Guide for Visual Studio Code</u></a></li>
<li><a href="https://win-able.techidaily.com/troubleshooting-freezing-in-call-of-duty-black-ops-cold-war-effective-strategies-and-solutions/"><u>Troubleshooting Freezing in Call of Duty: Black Ops Cold War - Effective Strategies and Solutions</u></a></li>
<li><a href="https://techtrends.techidaily.com/unlock-imessage-communication-for-android-a-step-by-step-guide/"><u>Unlock iMessage Communication for Android - A Step-by-Step Guide</u></a></li>
</ul></div>

