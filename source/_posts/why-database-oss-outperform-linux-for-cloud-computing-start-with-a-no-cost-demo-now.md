---
title: Why Database OSs Outperform Linux for Cloud Computing – Start with a No-Cost Demo Now!
date: 2024-12-19T16:07:56.256Z
updated: 2024-12-21T16:36:11.527Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/cloud/    https://www.zdnet.com/a/img/resize/69453a09be65cd6830fe7f6859ed923600c9d900/2024/03/19/fc60cdb3-9886-46f8-bc56-50f329e893dd/wavybluegettyimages-1455951980.jpg?width=170&height=96&fit=crop&auto=webp
---

## Why Database OSs Outperform Linux for Cloud Computing – Start with a No-Cost Demo Now!

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
<li><a href="https://instagram-videos.techidaily.com/new-2024-approved-boosting-social-impact-with-the-combined-force-of-youtube-and-instagram-stories/"><u>[New] 2024 Approved Boosting Social Impact with the Combined Force of YouTube and Instagram Stories</u></a></li>
<li><a href="https://youtube-stream.techidaily.com/new-how-to-safeguard-against-youtube-prohibitions/"><u>[New] How to Safeguard Against Youtube Prohibitions</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-sync-audio-to-powerpoint-presentations/"><u>[New] Sync Audio to PowerPoint Presentations</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-guide-to-procuring-and-utilizing-free-visual-frame-content/"><u>[New] The Guide to Procuring and Utilizing Free Visual Frame Content</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-total-gaze-coverage-camera-analysis/"><u>[New] Total Gaze Coverage Camera Analysis</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-transform-avi-files-into-gifs-with-filmora-on-windowsmacos/"><u>[New] Transform AVI Files Into GIFs with Filmora on Windows/MacOS</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/updated-2024-approved-innovative-screen-capture-tools-review-top-10-free-selections/"><u>[Updated] 2024 Approved Innovative Screen Capture Tools Review Top 10 Free Selections</u></a></li>
<li><a href="https://fox-glue.techidaily.com/updated-in-2024-how-to-shoot-vertical-panorama-photos-with-your-smartphone-androidios/"><u>[Updated] In 2024, How to Shoot Vertical Panorama Photos with Your Smartphone Android/iOS</u></a></li>
<li><a href="https://discover-guides.techidaily.com/complete-guide-to-recovering-lost-data-on-windows-11-10-8-and-7/"><u>Complete Guide to Recovering Lost Data on Windows 11, 10, 8 & 7</u></a></li>
<li><a href="https://some-techniques.techidaily.com/evaluating-lg-bp350-ergonomics-design-and-display-quality-for-2024/"><u>Evaluating LG BP350 - Ergonomics, Design & Display Quality for 2024</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-i-transferred-messages-from-oppo-k11x-to-iphone-12xs-max-in-seconds-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>How I Transferred Messages from Oppo K11x to iPhone 12/XS (Max) in Seconds | Dr.fone</u></a></li>
<li><a href="https://android-unlock.techidaily.com/in-2024-forgotten-the-voicemail-password-of-vivo-y77t-try-these-fixes-by-drfone-android/"><u>In 2024, Forgotten The Voicemail Password Of Vivo Y77t? Try These Fixes</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-top-tier-eyeball-enticer-author/"><u>In 2024, Top-Tier Eyeball Enticer Author</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unlock-the-potential-tutorial-on-enabling-speech-transcription-in-powerpoint/"><u>In 2024, Unlock the Potential Tutorial on Enabling Speech Transcription in PowerPoint</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-journey-of-personalized-instagram-notification-creation-for-2024/"><u>The Journey of Personalized Instagram Notification Creation for 2024</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/the-ultimate-guide-to-selecting-the-best-workstation-cpus-of-2024/"><u>The Ultimate Guide to Selecting the Best Workstation CPUs of 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-6-premium-video-translation-tools-for-2024/"><u>Top 6 Premium Video Translation Tools for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-7-sites-for-swapping-outringtone-files-on-snapchat-for-2024/"><u>Top 7 Sites for Swapping Outringtone Files on Snapchat for 2024</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/ultimate-guide-to-get-the-meltan-box-pokemon-go-for-zte-nubia-flip-5g-drfone-by-drfone-virtual-android/"><u>Ultimate guide to get the meltan box pokemon go For ZTE Nubia Flip 5G | Dr.fone</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/9Jfq2Wx1Bcs?si=YQrYpTy0g4aV5QaO" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

