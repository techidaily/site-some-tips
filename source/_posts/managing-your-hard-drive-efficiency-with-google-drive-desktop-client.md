---
title: Managing Your Hard Drive Efficiency with Google Drive Desktop Client
date: 2024-12-25T16:32:54.961Z
updated: 2024-12-27T17:17:24.852Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/754b583168e903d52acb50085981161b3ac5f74f/2020/10/07/a32627ff-cfb0-40bc-8a4f-bb6bb026bcbd/istock-1159763172.jpg?width=278&height=156&fit=crop&auto=webp
---

## Managing Your Hard Drive Efficiency with Google Drive Desktop Client

Once upon a time, I installed the Google Drive desktop client on my [MacBook Pro](https://apple.sjv.io/c/159047/435031/7613?&sharedId=zdnet&u=https%3A%2F%2Fwww.apple.com%2Fmacbook-pro%2F&subId1=zd-%5F%5FCOM%5FCLICK%5FID%5F%5F-dtp), only to discover shortly after that it had filled up my local storage on the laptop. That was my original, Intel-based MacBook that only had a 500GB SSD drive. It took me no time to figure out what exactly had gobbled up my storage on the device and even less time to resolve the problem. Had I not been able to put that two-and-two together quickly, I'd have run into some problems with that laptop. Fortunately, that was not the case.

Since then, I've been very careful about how the Google Drive Desktop client is configured on my laptops. Now it's time that I pass that information on to you, so you can avoid the same storage problem I once had.

I will assume that you already have the Google Drive Desktop Client installed on either [macOS](https://dl.google.com/drive-file-stream/GoogleDrive.dmg) or [Windows](https://dl.google.com/drive-file-stream/GoogleDriveSetup.exe) (please, Google, create an official client for Linux!) and have it linked to your Google Drive account. The desktop client installation is very simple for both platforms, so you shouldn't have any trouble getting it up and running and connected to Google Drive.

With that taken care of, let's see how we can avoid a storage nightmare.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/O7ChChlyX2o?si=7pMKdN1NZig1kYek" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## Streaming vs mirroring

You must understand this most important concept for protecting your storage space with the Google Drive Client. Google offers two different types of sync with the client, which are:

* **Stream files:** all files are stored on Google Drive cloud only unless you open a file or make it available offline. All files that are either opened or made available offline will be stored in a virtual drive in your local storage.
* **Mirror files:** files are stored on both Google Drive and local storage and are all made available offline.

At this point, I'm certain you know what happened with that earlier installation. I connected Google Drive (via the Desktop Client) to my MacBook by way of mirroring the files, which synced every file in my Drive account to local storage. And given I paid for[2TB of Google Drive storage](https://one.google.com/about/plans), you can bet that consumed every bit of space on my drive. Do that, and the operating system will slow to a crawl.

Here's what I had to do to fix that.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/FLO5dwmJAVs?si=1OYH8rv8aPaMsCiU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## How to configure the Google Drive client for streaming

Before I take you down this road, know that the Google Drive client does default to the stream option. However, during my original installation, I opted (for whatever reason) to go with the mirror option. Because I'm absolutely paranoid about my files and folders on Google Drive, I took the safest route possible and first uninstalled the Google Drive client from my MacBook Pro. Once the app was uninstalled, I double-checked to ensure all of my directories and files were safe on Google Drive. They were. Whew.

When you opt to stream files, they are saved in a virtual drive that can be mounted and unmounted. However, when you go with the mirror option, those files are saved in /Users/USERNAME/My Drive (Where USERNAME is your macOS username). Once you've uninstalled the Google Drive Client (and you've checked to verify all of your directories and files still exist on your Google Drive cloud account), delete that My Drive directory. Once you've done that, you've freed up the space Google Drive consumed and should be back to a more management disk. 

Re-install the Google Drive client on your machine, and then you can ensure you configure it to stream and not mirror files. Here's how you do that.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/1rCjQ09iG7s?si=Si1fUBric8MH1VHI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

### 1\. Open preferences

Click on the Google Drive desktop client icon in the macOS topbar and click the gear icon in the resulting popup (**Figure 1**).

**Figure 1:** Accessing the Google Drive Desktop Client preferences.

Image: Jack Wallen

In the next popup menu (**Figure 2**), click Preferences.

**Figure 2:** The Google Drive Desktop Client popup menu gives you access to the Preferences entry.

Image: Jack Wallen

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/bofw6eJA7Bg?si=HM2gKZGH4L1otw3e" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

### 2\. Choose the Stream option

In the resulting window, click the Google Drive tab in the left sidebar (**Figure 3**).

**Figure 3:** The Google Drive Desktop Client Preferences window on macOS.

Image: Jack Wallen

You should then see the stream and mirror listing, where you can choose between the two (**Figure 4**).

**Figure 4:** The two syncing options available to the Google Drive Desktop Client.

Image: Jack Wallen

Make sure stream is selected. If not, select it, and the Drive Client should take care of the rest. 

And that is all there is to prevent the Google Drive Desktop Client from using up your precious hard drive space on your device. Enjoy that newly-freed storage space.

#### More how-tos

[How to download YouTube videos for free, plus two other methods](https://www.zdnet.com/article/how-to-download-youtube-videos-for-free-plus-two-other-methods/ "How to download YouTube videos for free, plus two other methods")

[Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how](https://www.zdnet.com/article/wi-fi-problems-how-to-add-a-wired-network-to-your-home-without-ethernet-cable/ "Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how")

[Wiping a Windows laptop? Here's the safest free way to erase your personal data](https://www.zdnet.com/article/wiping-a-windows-laptop-heres-the-safest-free-way-to-erase-your-personal-data/ "Wiping a Windows laptop? Here's the safest free way to erase your personal data")

[How to connect a PS4 controller to a smartphone](https://www.zdnet.com/article/how-to-connect-a-ps4-controller-to-a-smartphone/ "How to connect a PS4 controller to a smartphone")

* [How to download YouTube videos for free, plus two other methods](https://www.zdnet.com/article/how-to-download-youtube-videos-for-free-plus-two-other-methods/ "How to download YouTube videos for free, plus two other methods")
* [Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how](https://www.zdnet.com/article/wi-fi-problems-how-to-add-a-wired-network-to-your-home-without-ethernet-cable/ "Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how")
* [Wiping a Windows laptop? Here's the safest free way to erase your personal data](https://www.zdnet.com/article/wiping-a-windows-laptop-heres-the-safest-free-way-to-erase-your-personal-data/ "Wiping a Windows laptop? Here's the safest free way to erase your personal data")
* [How to connect a PS4 controller to a smartphone](https://www.zdnet.com/article/how-to-connect-a-ps4-controller-to-a-smartphone/ "How to connect a PS4 controller to a smartphone")

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
<li><a href="https://screen-activity-recording.techidaily.com/new-2024-approved-screen-capture-showdown-is-obs-better-than-fraps/"><u>[New] 2024 Approved Screen Capture Showdown Is OBS Better Than Fraps?</u></a></li>
<li><a href="https://fox-hovers.techidaily.com/new-optimal-cloud-vaults-recommended-solutions/"><u>[New] Optimal Cloud Vaults Recommended Solutions</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-future-of-display-technology-with-eizos-high-res-monitor/"><u>[New] The Future of Display Technology with EIZO's High-Res Monitor</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-transform-videos-for-free-leading-enhancement-pages/"><u>[New] Transform Videos for Free Leading Enhancement Pages</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-vanguard-designs-evaluation-studio-25-examined-current-year/"><u>[Updated] Vanguard Designs Evaluation Studio 25 Examined, Current Year</u></a></li>
<li><a href="https://article-knowledge.techidaily.com/in-2024-dive-into-tiktok-edits-a-comprehensible-guide-for-all/"><u>In 2024, Dive Into TikTok Edits A Comprehensible Guide for All</u></a></li>
<li><a href="https://snapchat-videos.techidaily.com/in-2024-how-to-reverse-a-video-on-snapchat/"><u>In 2024, How to Reverse a Video on Snapchat?</u></a></li>
<li><a href="https://games-able.techidaily.com/mojang-mayhem-five-friendly-multiplayer-mc-tactics/"><u>Mojang Mayhem: Five Friendly Multiplayer MC Tactics</u></a></li>
<li><a href="https://tech-renaissance.techidaily.com/starting-out-in-vr-learn-how-to-establish-your-oculus-quest-or-quest-2-identity-online/"><u>Starting Out in VR? Learn How to Establish Your Oculus Quest or Quest 2 Identity Online</u></a></li>
<li><a href="https://some-tips.techidaily.com/subtlety-in-sound-fading-out-effectively-in-logic-pro-for-2024/"><u>Subtlety In Sound Fading Out Effectively in Logic Pro for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-writers-workshop-for-podcast-creators-examples-included-for-2024/"><u>The Writers' Workshop for Podcast Creators (Examples Included) for 2024</u></a></li>
<li><a href="https://program-issues.techidaily.com/troubleshooting-steps-when-your-astro-a50-headset-is-unresponsive/"><u>Troubleshooting Steps When Your Astro A50 Headset Is Unresponsive</u></a></li>
<li><a href="https://android-location-track.techidaily.com/two-ways-to-track-my-boyfriends-nokia-c210-without-him-knowing-drfone-by-drfone-virtual-android/"><u>Two Ways to Track My Boyfriends Nokia C210 without Him Knowing | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/ultimate-digital-collage-creator-8x-for-2024/"><u>Ultimate Digital Collage Creator 8X for 2024</u></a></li>
<li><a href="https://smart-video-editing.techidaily.com/updated-2024-approved-best-5-free-tools-to-combine-mpeg-videos/"><u>Updated 2024 Approved Best 5 Free Tools to Combine MPEG Videos</u></a></li>
</ul></div>

