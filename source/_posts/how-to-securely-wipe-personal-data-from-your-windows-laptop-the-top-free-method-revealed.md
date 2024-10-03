---
title: "How to Securely Wipe Personal Data From Your Windows Laptop: The Top Free Method Revealed"
date: 2024-09-28T19:43:22.105Z
updated: 2024-10-03T19:08:22.412Z
tags:
  - work-life
categories:
  - tech
thumbnail: https://thmb.techidaily.com/ced9cab3bb4f4b670e0a461fa0277071d0fe6cc512c46ece52a065d147ecc37a.jpg
---

## How to Securely Wipe Personal Data From Your Windows Laptop: The Top Free Method Revealed

![erasing files concept](https://www.zdnet.com/a/img/resize/102940ee04276089e5835b4815e51ce84ae69967/2024/08/15/42fdba14-32ac-49f1-bfab-83e55f8c70b0/gettyimages-1311072873.jpg?auto=webp&width=1280)

Westend61/Getty Images

When you replace your old but still functional Windows PC with a shiny new model, you have several options for that gently used device. You can give it away to a friend or family member. You can donate it to a charitable organization like Goodwill (which partners with [Dell Reconnect](https://shop-links.co/link/?exclusive=1&publisher_slug=itechdaily19598&url=https%3A%2F%2Fwww.dell.com%2Fen-us%2Fdt%2Fcorporate%2Fsocial-impact%2Fadvancing-sustainability%2Fhow-to-recycle%2Ffaq.htm%23tab0%3D1)). You can even trade it in for credit or sell it on a third-party site like [Swappa](https://swappa.com/sell/laptop) or [Back Market](https://www.awin1.com/awclick.php?mid=18275&id=423585&clickref=zd-%5F%5FCOM%5FCLICK%5FID%5F%5F-dtp&ued=https%3A%2F%2Fwww.backmarket.com%2Fen-us%2Fbuyback%2Fhome). 

**Also: [You can upgrade your old PC to Windows 11 - even if Microsoft says it's 'incompatible'. Here's how](https://www.zdnet.com/article/yes-you-can-upgrade-your-old-pc-to-windows-11-even-if-microsoft-says-its-incompatible/)**

Whichever course of action you take, though, your most important task is to **_permanently delete all your personal files_** from that PC before you pass it along. With a desktop PC, that might be as easy as swapping out the system drive for a new one. But that's usually not an option with a laptop, where replacing storage can be impossible or prohibitively expensive. 

For laptops and for desktops where you aren't replacing the system drive, the simplest route is to reset the PC, choosing the option to remove personal files and reinstall Windows. On a PC running Windows 10, go to Settings > Update & Security > Recovery. On a Windows 11 device, the Reset PC option is under Settings > System > Recovery. Make sure you choose the Remove Everything option, as shown here.

When you're resetting a PC to give away or sell, be sure to choose the Remove Everything option.

Screenshot by Ed Bott/ZDNET

It takes several prompts before you get to the actual reset option (you don't want to do this accidentally, after all) and if you dig through the settings you can find a Clean Disk option designed to remove all data in addition to removing your files. As an alternative, you can boot from Windows installation media, remove all existing disk partitions, and then perform a clean install.

**Also: [Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how](https://www.zdnet.com/home-and-office/work-life/wi-fi-problems-add-a-wired-network-to-your-home-without-ethernet-cable-heres-how/)**

Either option removes existing personal files, but Microsoft's documentation cautions that "the data erasure functionality is targeted at consumers and does not meet government and industry data erasure standards." As a result, it's possible that someone with advanced technical skills could use forensic tools or data recovery software to access some of the deleted information.

On modern systems with solid-state drives, you can often find a management utility that includes a Secure Erase command. For Samsung SSDs, use the [Samsung Magician](https://shop-links.co/link/?exclusive=1&publisher_slug=itechdaily19598&url=https%3A%2F%2Fsemiconductor.samsung.com%2Fconsumer-storage%2Fmagician%2F) program. For Intel SSDs, download and install the [Intel Memory and Storage Tool](https://www.intel.com/content/www/us/en/download/19543/intel-memory-and-storage-tool-gui.html?v=t). SSDs from Crucial use the [Crucial Storage Executive utility](https://www.crucial.com/support/storage-executive). Microsoft Surface devices support a custom tool called the [Microsoft Surface Data Eraser](https://learn.microsoft.com/en-us/surface/surface-it-toolkit-data-eraser); check the download links in that article to determine whether you need the newer IT Toolkit or the Legacy version for older Surface devices.

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

Some third-party partition management tools include the option to wipe a disk completely. My favorite for this task is [MiniTool Partition Wizard](https://www.partitionwizard.com/), which includes the Wipe Disk option in free and paid versions.

**Also: [The best laptops of 2024: Expert tested and reviewed](https://www.zdnet.com/article/best-laptop/)**

You also can use Windows' built-in encryption tools to ensure that the entire system drive, including unused disk space, is encrypted before performing a clean install. That extra step requires some additional time, but it ensures that any data recovered from anywhere on the drive will be unreadable. And you don't need any third-party software to get the job done.

Your system drive is fully encrypted by default if you've signed in to Windows with a Microsoft account on a modern device that supports BitLocker Device Encryption (BDE). To confirm that your device supports BDE, run the System Information utility (Msinfo32.exe) as an administrator and check the Device Encryption Support entry at the bottom of the System Summary page.

On a system running Windows 10 Pro or Windows 11 Pro, you can use the Manage BitLocker utility (type BitLocker in the search box to find it) to encrypt the system drive and any data drives. Be sure to choose the option to encrypt the entire drive and not just the space that currently contains data.

**Also: [The Windows 10 clock is ticking: 5 ways to save your old PC in 2025 (most are free)](https://www.zdnet.com/article/the-windows-10-clock-is-ticking-5-ways-to-save-your-old-pc-in-2025-most-are-free/)**

If Device Encryption isn't available, open a command prompt using the Run As Administrator option and enter this command:

**Cipher /W:C:\\**

That command "zeroes out" unused disk space, overwriting it so that it can't be recovered. This process can take a long time, so consider letting it run overnight while you concentrate on more important tasks.

#### Featured

[Labor Day weekend and sales are here. Here's what to know, and the best deals of the weekend](https://www.zdnet.com/article/labor-day-deals-everything-to-know-09-02-2024/ "Labor Day weekend and sales are here. Here's what to know, and the best deals of the weekend")

[Still have a Windows 10 PC? You have 5 options before support ends next year](https://www.zdnet.com/article/still-have-a-windows-10-pc-you-have-5-options-before-support-ends-next-year/ "Still have a Windows 10 PC? You have 5 options before support ends next year")

[This Samsung phone is the one I recommend to most people (and it's not a flagship)](https://www.zdnet.com/article/this-samsung-phone-is-the-one-i-recommend-to-most-people-and-its-not-a-flagship/ "This Samsung phone is the one I recommend to most people (and it's not a flagship)")

[Which programming languages are most popular now (and what does that even mean)?](https://www.zdnet.com/article/the-most-popular-programming-languages-in-2024-and-what-that-even-means/ "Which programming languages are most popular now (and what does that even mean)?")

* [Labor Day weekend and sales are here. Here's what to know, and the best deals of the weekend](https://www.zdnet.com/article/labor-day-deals-everything-to-know-09-02-2024/ "Labor Day weekend and sales are here. Here's what to know, and the best deals of the weekend")
* [Still have a Windows 10 PC? You have 5 options before support ends next year](https://www.zdnet.com/article/still-have-a-windows-10-pc-you-have-5-options-before-support-ends-next-year/ "Still have a Windows 10 PC? You have 5 options before support ends next year")
* [This Samsung phone is the one I recommend to most people (and it's not a flagship)](https://www.zdnet.com/article/this-samsung-phone-is-the-one-i-recommend-to-most-people-and-its-not-a-flagship/ "This Samsung phone is the one I recommend to most people (and it's not a flagship)")
* [Which programming languages are most popular now (and what does that even mean)?](https://www.zdnet.com/article/the-most-popular-programming-languages-in-2024-and-what-that-even-means/ "Which programming languages are most popular now (and what does that even mean)?")

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
<li><a href="https://video-capture.techidaily.com/new-2024-approved-the-finest-11-streaming-sound-recorders/"><u>[New] 2024 Approved The Finest 11 Streaming Sound Recorders</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-art-of-iphone-podcast-listening/"><u>[New] The Art of iPhone Podcast Listening</u></a></li>
<li><a href="https://article-posts.techidaily.com/updated-leading-edge-photography-the-best-4k-mirrorless-cameras/"><u>[Updated] Leading Edge Photography The Best 4K Mirrorless Cameras</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-toolwiz-revolutionizes-camera-use-a-comprehensive-review-for-photographers/"><u>2024 Approved Toolwiz Revolutionizes Camera Use - A Comprehensive Review for Photographers</u></a></li>
<li><a href="https://extra-resources.techidaily.com/finding-the-best-free-subtitle-conversion-services/"><u>Finding the Best Free Subtitle Conversion Services</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/how-to-evade-tips-on-avoiding-edgenuity-video-lessons-with-finesse/"><u>How to Evade Tips on Avoiding Edgenuity Video Lessons with Finesse</u></a></li>
<li><a href="https://fox-helps.techidaily.com/in-2024-reflect-your-vision-affordable-personalization-of-professional-logo-designs-free/"><u>In 2024, Reflect Your Vision Affordable Personalization of Professional Logo Designs (Free)</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-top-virtual-reality-vr-bikes-to-check-out/"><u>In 2024, Top Virtual Reality (VR) Bikes to Check Out</u></a></li>
<li><a href="https://some-tips.techidaily.com/transform-the-way-you-view-web-content-using-ms-edges-split-screen-functionality-for-2024/"><u>Transform the Way You View Web Content Using MS Edge's Split Screen Functionality for 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://25home.pxf.io/c/5597632/2148638/16836" target="_top" id="2148638">
  <img src="//a.impactradius-go.com/display-ad/16836-2148638" border="0" alt="https://techidaily.com" width="160" height="90"/>
</a>
<img height="0" width="0" src="https://25home.pxf.io/i/5597632/2148638/16836" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

