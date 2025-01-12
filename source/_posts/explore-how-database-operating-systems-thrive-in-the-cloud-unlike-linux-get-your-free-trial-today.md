---
title: Explore How Database Operating Systems Thrive in the Cloud Unlike Linux – Get Your Free Trial Today!
date: 2025-01-10T17:30:38.884Z
updated: 2025-01-12T16:03:38.944Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/cloud/    https://www.zdnet.com/a/img/resize/69453a09be65cd6830fe7f6859ed923600c9d900/2024/03/19/fc60cdb3-9886-46f8-bc56-50f329e893dd/wavybluegettyimages-1455951980.jpg?width=170&height=96&fit=crop&auto=webp
---

## Explore How Database Operating Systems Thrive in the Cloud Unlike Linux – Get Your Free Trial Today!

![wavybluegettyimages-1455951980](https://www.zdnet.com/a/img/resize/cbbc573ce87707e4813dcece2dc5f07e89224a76/2024/03/19/fc60cdb3-9886-46f8-bc56-50f329e893dd/wavybluegettyimages-1455951980.jpg?auto=webp&width=1280)

Eugene Mymrin/Getty Images

For years, Linux has been responsible for powering servers in the cloud, but given how the cloud has grown exponentially, and that Linux wasn't designed specifically for the cloud, it became clear that something had to change.

**Also: [The best Linux distributions for beginners in 2024: Expert tested and reviewed](https://www.zdnet.com/article/best-linux-desktops-for-beginners/)**

That change might come by way of Michael Stonebraker (Ingres, PostgreSQL, and VoltDB) and Matei Zaharia (Apache Spark and co-founder/CTO of Databrisk) who have worked with a team from MIT to create a revolutionary operating system called DBOS, aka DataBase OS.

Work on DBOS began in 2022\. In an [initial blog post](https://dbos-project.github.io/blog/intro-blog.html), DBOS Inc. cofounders [Peter Craft](https://petereliaskraft.net) and [Qian Li](https://qianli.dev) stated, "We believe the next generation of operating systems should be database-oriented because databases are built to solve the hard problems of modern computing. Databases today can manage petabytes of data, are distributed and increasingly cloud-native, and can secure and govern data with fine-grained access control and provenance tracking. Equally important, modern distributed in-memory data stores like VoltDB and FoundationDB are becoming extremely fast, and we show later they are fast enough to efficiently run many OS services that traditional disk-based RDBMSs could not."

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

They went on to propose building a database-oriented OS that centered around two principles:

* All applications and OS states are stored in tables in a distributed database.
* States could only be accessed through database transactions.

Their OS consisted of four levels:

* User applications
* File system/scheduler/IPC/other OS services
* Distributed DBMS
* Microkernel services

**Also: [Thinking about switching to Linux? 10 things you need to know](https://www.zdnet.com/article/thinking-about-switching-to-linux-things-you-need-to-know/)**

With DBOS, operating system services are coded in SQL on the distributed DBMS, which is quite different than the traditional method of running the database management system within the user space on top of the operating system.

Once they had created a successful prototype of DBOS, they secured funding for DBOS, Inc., and, now, the operating system is available to [try for free](https://www.dbos.dev/pricing) or you can [contact sales for a custom plan](https://www.dbos.dev/contact). You can create a new account by signing in with your Google account. Once you've signed in, you'll see a Getting Started page that instructs you to:

* Download the SDK and run a "Hello, Database!" application on your computer: [SDK Quickstart](https://docs.dbos.dev/getting-started/quickstart)
* Deploy your application to the cloud: [Cloud Quickstart](https://docs.dbos.dev/getting-started/quickstart-cloud)

You can install the DBOS SDK on Ubuntu Linux, MacOS, or Windows (WSL). It does require Node.js 20 or later and then uses Docker to deploy the app to the OS.

**Also: [Why I use multiple operating systems to get my work done](https://www.zdnet.com/article/why-i-use-multiple-operating-systems-to-get-my-work-done/)**

One of the biggest benefits of DBOS is reliable execution, so if an application is interrupted, it will automatically resume right where it left off. 

The big question is: Will companies be interested in shrugging off their dependency on Linux for a radically new approach to cloud-centric operating systems?

#### Featured

[The fastest VPNs: Expert tested and reviewed](https://www.zdnet.com/article/fastest-vpn/ "The fastest VPNs: Expert tested and reviewed")

[Google Pixel 9 Pro XL vs. Samsung Galaxy S24 Ultra: I tested both and here are the key differences](https://www.zdnet.com/article/google-pixel-9-pro-xl-vs-samsung-galaxy-s24-ultra/ "Google Pixel 9 Pro XL vs. Samsung Galaxy S24 Ultra: I tested both and here are the key differences")

[How to upgrade your 'incompatible' Windows 10 PC to Windows 11](https://www.zdnet.com/article/how-to-upgrade-your-incompatible-windows-10-pc-to-windows-11/ "How to upgrade your 'incompatible' Windows 10 PC to Windows 11")

[Your Android phone is getting an anti-theft upgrade, thanks to AI. How it works](https://www.zdnet.com/article/your-android-phone-is-getting-an-anti-theft-upgrade-thanks-to-ai-how-it-works/ "Your Android phone is getting an anti-theft upgrade, thanks to AI. How it works")

* [The fastest VPNs: Expert tested and reviewed](https://www.zdnet.com/article/fastest-vpn/ "The fastest VPNs: Expert tested and reviewed")
* [Google Pixel 9 Pro XL vs. Samsung Galaxy S24 Ultra: I tested both and here are the key differences](https://www.zdnet.com/article/google-pixel-9-pro-xl-vs-samsung-galaxy-s24-ultra/ "Google Pixel 9 Pro XL vs. Samsung Galaxy S24 Ultra: I tested both and here are the key differences")
* [How to upgrade your 'incompatible' Windows 10 PC to Windows 11](https://www.zdnet.com/article/how-to-upgrade-your-incompatible-windows-10-pc-to-windows-11/ "How to upgrade your 'incompatible' Windows 10 PC to Windows 11")
* [Your Android phone is getting an anti-theft upgrade, thanks to AI. How it works](https://www.zdnet.com/article/your-android-phone-is-getting-an-anti-theft-upgrade-thanks-to-ai-how-it-works/ "Your Android phone is getting an anti-theft upgrade, thanks to AI. How it works")

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
<li><a href="https://desktop-recording.techidaily.com/new-in-2024-itop-screen-recorder-essential-or-excessive/"><u>[New] In 2024, ITop Screen Recorder - Essential or Excessive?</u></a></li>
<li><a href="https://desktop-recording.techidaily.com/new-soundsreview-insight/"><u>[New] SoundsReview Insight</u></a></li>
<li><a href="https://fox-http.techidaily.com/updated-in-2024-the-ultimate-strategy-for-professional-gopro-filming/"><u>[Updated] In 2024, The Ultimate Strategy for Professional Gopro Filming</u></a></li>
<li><a href="https://extra-skills.techidaily.com/updated-quick-tips-for-altering-video-speed-on-netflix-devices/"><u>[Updated] Quick Tips for Altering Video Speed on Netflix Devices</u></a></li>
<li><a href="https://fox-that.techidaily.com/1721468869423-experiencing-tardy-sms-notifications-on-iphone-discover-9-reliable-remedies-now/"><u>Experiencing Tardy SMS Notifications on iPhone? Discover 9 Reliable Remedies Now!</u></a></li>
<li><a href="https://win-blog.techidaily.com/free-online-conversion-transforming-rmvb-files-into-avi-format-with-ease-moveavewizard/"><u>Free Online Conversion: Transforming RMVB Files Into AVI Format with Ease - Moveavewizard</u></a></li>
<li><a href="https://youtube-help.techidaily.com/in-2024-mastering-channels-on-the-fly-tubebuddy-essentials/"><u>In 2024, Mastering Channels on the Fly - TubeBuddy Essentials</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/in-2024-thinking-about-changing-your-netflix-region-without-a-vpn-on-zte-nubia-flip-5g-drfone-by-drfone-virtual-android/"><u>In 2024, Thinking About Changing Your Netflix Region Without a VPN On ZTE Nubia Flip 5G? | Dr.fone</u></a></li>
<li><a href="https://discover-blog.techidaily.com/transformer-sans-frais-de-lanimation-gif-au-fichier-image-statique-jpeg/"><u>Transformer Sans Frais : De L'animation GIF Au Fichier Image Statique JPEG</u></a></li>
<li><a href="https://some-tips.techidaily.com/unboxing-the-dji-mini-3-pro-silent-flight-and-compact-design-showcase-an-in-depth-review-by-zdnet/"><u>Unboxing the DJI Mini 3 Pro: Silent Flight and Compact Design Showcase - An In-Depth Review by ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-the-future-of-home-security-my-experience-testing-an-innovative-facial-recognition-smart-lock-insights-from-zdnet/"><u>Unlocking the Future of Home Security: My Experience Testing an Innovative Facial Recognition Smart Lock - Insights From ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveiling-the-revolutionary-trio-camera-drone-how-it-changes-aerial-photography-zdnet-exclusive/"><u>Unveiling the Revolutionary Trio-Camera Drone: How It Changes Aerial Photography - ZDNet Exclusive</u></a></li>
<li><a href="https://some-tips.techidaily.com/watching-an-eclipse-safely-with-homemade-pinhole-projector-a-step-by-step-camera-obscura-build-guide/"><u>Watching an Eclipse Safely with Homemade Pinhole Projector - A Step-by-Step Camera Obscura Build Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/why-the-waterproof-blink-mini-2-outshines-wyze-cams-a-top-tier-smart-home-surveillance-option/"><u>Why the Waterproof Blink Mini 2 Outshines Wyze Cams: A Top-Tier Smart Home Surveillance Option</u></a></li>
<li><a href="https://some-tips.techidaily.com/zdnet-review-the-unforeseen-delights-of-using-the-ring-spotlight-cam-pro-a-users-perspective/"><u>ZDNet Review: The Unforeseen Delights of Using the Ring Spotlight Cam Pro - A User's Perspective</u></a></li>
<li><a href="https://some-tips.techidaily.com/zdnet-review-why-the-ecoflow-river-ticks-all-boxes-as-a-top-pick-for-beginners-in-portable-power/"><u>ZDNet Review: Why the EcoFlow River Ticks All Boxes as a Top Pick for Beginners in Portable Power</u></a></li>
<li><a href="https://some-tips.techidaily.com/zdnets-expert-review-the-surprisingly-stellar-performance-of-the-ring-spotlight-cam-pro/"><u>ZDNet's Expert Review: The Surprisingly Stellar Performance of the Ring Spotlight Cam Pro</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/tPgf_wSdhS8?si=BHoH1ryaxmwk-8FV" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

