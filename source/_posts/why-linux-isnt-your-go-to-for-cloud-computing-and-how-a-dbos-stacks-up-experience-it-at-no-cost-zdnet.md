---
title: Why Linux Isn't Your Go-To for Cloud Computing and How a DBOS Stacks Up - Experience It at No Cost | ZDNet
date: 2025-01-09T19:33:11.612Z
updated: 2025-01-12T19:47:19.564Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/cloud/    https://www.zdnet.com/a/img/resize/69453a09be65cd6830fe7f6859ed923600c9d900/2024/03/19/fc60cdb3-9886-46f8-bc56-50f329e893dd/wavybluegettyimages-1455951980.jpg?width=170&height=96&fit=crop&auto=webp
---

## Why Linux Isn't Your Go-To for Cloud Computing and How a DBOS Stacks Up - Experience It at No Cost | ZDNet

![wavybluegettyimages-1455951980](https://www.zdnet.com/a/img/resize/cbbc573ce87707e4813dcece2dc5f07e89224a76/2024/03/19/fc60cdb3-9886-46f8-bc56-50f329e893dd/wavybluegettyimages-1455951980.jpg?auto=webp&width=1280)

Eugene Mymrin/Getty Images

For years, Linux has been responsible for powering servers in the cloud, but given how the cloud has grown exponentially, and that Linux wasn't designed specifically for the cloud, it became clear that something had to change.

**Also: [The best Linux distributions for beginners in 2024: Expert tested and reviewed](https://www.zdnet.com/article/best-linux-desktops-for-beginners/)**

That change might come by way of Michael Stonebraker (Ingres, PostgreSQL, and VoltDB) and Matei Zaharia (Apache Spark and co-founder/CTO of Databrisk) who have worked with a team from MIT to create a revolutionary operating system called DBOS, aka DataBase OS.

Work on DBOS began in 2022\. In an [initial blog post](https://dbos-project.github.io/blog/intro-blog.html), DBOS Inc. cofounders [Peter Craft](https://petereliaskraft.net) and [Qian Li](https://qianli.dev) stated, "We believe the next generation of operating systems should be database-oriented because databases are built to solve the hard problems of modern computing. Databases today can manage petabytes of data, are distributed and increasingly cloud-native, and can secure and govern data with fine-grained access control and provenance tracking. Equally important, modern distributed in-memory data stores like VoltDB and FoundationDB are becoming extremely fast, and we show later they are fast enough to efficiently run many OS services that traditional disk-based RDBMSs could not."

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
<li><a href="https://article-posts.techidaily.com/new-in-2024-choreographing-photography-and-filming-in-one-sweep/"><u>[New] In 2024, Choreographing Photography and Filming in One Sweep</u></a></li>
<li><a href="https://fox-access.techidaily.com/2024-approved-backswing-crafting-bundle/"><u>2024 Approved Backswing Crafting Bundle</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/holographic-horizons-trendsetting-wallpapers-for-2024/"><u>Holographic Horizons Trendsetting Wallpapers for 2024</u></a></li>
<li><a href="https://youtube-web.techidaily.com/24-editors-assistant-top-5-portable-devices-for-vfx-artists/"><u>In 2024, Editor's Assistant Top 5 Portable Devices for VFX Artists</u></a></li>
<li><a href="https://facebook-video-recording.techidaily.com/master-the-art-of-converting-fb-to-mp4-720p1080p-without-paying-for-2024/"><u>Master the Art of Converting FB to MP4, 720P/1080p, Without Paying for 2024</u></a></li>
<li><a href="https://video-screen-grab.techidaily.com/mastering-video-calls-discover-the-top-10-apps-for-your-phone/"><u>Mastering Video Calls Discover the Top 10 Apps for Your Phone</u></a></li>
<li><a href="https://some-tips.techidaily.com/meta-quest-3-crowned-top-tech-by-zdnet-the-surprising-contender/"><u>Meta Quest 3 Crowned Top Tech by ZDNet - The Surprising Contender!</u></a></li>
<li><a href="https://some-tips.techidaily.com/navigating-the-marvel-disney-multiverse-how-your-role-shapes-the-story-zdnet-insights/"><u>Navigating the Marvel-Disney Multiverse: How Your Role Shapes the Story | ZDNet Insights</u></a></li>
<li><a href="https://some-tips.techidaily.com/revolutionizing-home-care-discover-how-dysons-advanced-ar-assistance-guarantees-a-spot-free-vacuum-zdnet-insight/"><u>Revolutionizing Home Care: Discover How Dyson's Advanced AR Assistance Guarantees a Spot-Free Vacuum | ZDNET Insight</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-myth-of-budget-friendly-vision-pro-glasses-by-apple-a-closer-look-at-the-speculation-storm/"><u>The Myth of Budget-Friendly Vision Pro Glasses by Apple – A Closer Look at the Speculation Storm</u></a></li>
<li><a href="https://some-tips.techidaily.com/three-essential-actions-apple-needs-to-revitalize-the-visual-experience-with-to-rescue-the-vision-pro/"><u>Three Essential Actions Apple Needs to Revitalize the Visual Experience with To Rescue the Vision Pro</u></a></li>
<li><a href="https://extra-resources.techidaily.com/video-to-image-easily-separate-and-save-pics-from-movies-windows-10/"><u>Video to Image Easily Separate and Save Pics From Movies (Windows 10)</u></a></li>
<li><a href="https://novels-ebooks.techidaily.com/210133694-9781953791207-wellness/"><u>WELLNESS | Free Book</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/f3PFn06LijE?si=zHrmlTOzrKxXe-k4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

