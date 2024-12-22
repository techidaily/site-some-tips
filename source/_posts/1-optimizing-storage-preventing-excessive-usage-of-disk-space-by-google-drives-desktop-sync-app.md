---
title: "1. Optimizing Storage: Preventing Excessive Usage of Disk Space by Google Drive's Desktop Sync App"
date: 2024-12-20T01:33:16.614Z
updated: 2024-12-22T03:05:23.991Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/dab2ef0415897bd2885169e6ea9bd44d0885cdc86df8bf517d1ad2126bf71ef1.jpg
---

## 1. Optimizing Storage: Preventing Excessive Usage of Disk Space by Google Drive's Desktop Sync App

Once upon a time, I installed the Google Drive desktop client on my [MacBook Pro](https://apple.sjv.io/c/159047/435031/7613?&sharedId=zdnet&u=https%3A%2F%2Fwww.apple.com%2Fmacbook-pro%2F&subId1=zd-%5F%5FCOM%5FCLICK%5FID%5F%5F-dtp), only to discover shortly after that it had filled up my local storage on the laptop. That was my original, Intel-based MacBook that only had a 500GB SSD drive. It took me no time to figure out what exactly had gobbled up my storage on the device and even less time to resolve the problem. Had I not been able to put that two-and-two together quickly, I'd have run into some problems with that laptop. Fortunately, that was not the case.

Since then, I've been very careful about how the Google Drive Desktop client is configured on my laptops. Now it's time that I pass that information on to you, so you can avoid the same storage problem I once had.

I will assume that you already have the Google Drive Desktop Client installed on either [macOS](https://dl.google.com/drive-file-stream/GoogleDrive.dmg) or [Windows](https://dl.google.com/drive-file-stream/GoogleDriveSetup.exe) (please, Google, create an official client for Linux!) and have it linked to your Google Drive account. The desktop client installation is very simple for both platforms, so you shouldn't have any trouble getting it up and running and connected to Google Drive.

With that taken care of, let's see how we can avoid a storage nightmare.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/AQn0MYjIfyI?si=rIdjT-qMRpjpJXXa" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## Streaming vs mirroring

You must understand this most important concept for protecting your storage space with the Google Drive Client. Google offers two different types of sync with the client, which are:

* **Stream files:** all files are stored on Google Drive cloud only unless you open a file or make it available offline. All files that are either opened or made available offline will be stored in a virtual drive in your local storage.
* **Mirror files:** files are stored on both Google Drive and local storage and are all made available offline.

At this point, I'm certain you know what happened with that earlier installation. I connected Google Drive (via the Desktop Client) to my MacBook by way of mirroring the files, which synced every file in my Drive account to local storage. And given I paid for[2TB of Google Drive storage](https://one.google.com/about/plans), you can bet that consumed every bit of space on my drive. Do that, and the operating system will slow to a crawl.

Here's what I had to do to fix that.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/JAkb8Bv3AU4?si=2rHwnZYTzTLieKgY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## How to configure the Google Drive client for streaming

Before I take you down this road, know that the Google Drive client does default to the stream option. However, during my original installation, I opted (for whatever reason) to go with the mirror option. Because I'm absolutely paranoid about my files and folders on Google Drive, I took the safest route possible and first uninstalled the Google Drive client from my MacBook Pro. Once the app was uninstalled, I double-checked to ensure all of my directories and files were safe on Google Drive. They were. Whew.

When you opt to stream files, they are saved in a virtual drive that can be mounted and unmounted. However, when you go with the mirror option, those files are saved in /Users/USERNAME/My Drive (Where USERNAME is your macOS username). Once you've uninstalled the Google Drive Client (and you've checked to verify all of your directories and files still exist on your Google Drive cloud account), delete that My Drive directory. Once you've done that, you've freed up the space Google Drive consumed and should be back to a more management disk. 

Re-install the Google Drive client on your machine, and then you can ensure you configure it to stream and not mirror files. Here's how you do that.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/XIUatTFH0Zw?si=ZCtoBtIy18y2F5Vc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

### 1\. Open preferences

Click on the Google Drive desktop client icon in the macOS topbar and click the gear icon in the resulting popup (**Figure 1**).

**Figure 1:** Accessing the Google Drive Desktop Client preferences.

Image: Jack Wallen

In the next popup menu (**Figure 2**), click Preferences.

**Figure 2:** The Google Drive Desktop Client popup menu gives you access to the Preferences entry.

Image: Jack Wallen

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/K7fATC_lI7o?si=UFotPJqflDRZr-mv" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<li><a href="https://screen-recording.techidaily.com/new-2024-approved-essential-quicktime-lapse-maker-5/"><u>[New] 2024 Approved Essential Quicktime-Lapse Maker #5</u></a></li>
<li><a href="https://video-capture.techidaily.com/new-2024-approved-how-to-record-and-save-voices-on-iphone-efficiently/"><u>[New] 2024 Approved How to Record & Save Voices on iPhone Efficiently</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/new-dive-into-quality-tips-for-shooting-crystal-clear-gopro-video-below-the-surface/"><u>[New] Dive Into Quality Tips for Shooting Crystal Clear GoPro Video Below the Surface</u></a></li>
<li><a href="https://video-screen-grab.techidaily.com/new-rapid-pause-video-snapshot-manual/"><u>[New] Rapid Pause Video Snapshot Manual</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-evolved-2023-samsung-bd-j5900-a-deep-dive/"><u>[New] The Evolved 2023 Samsung BD-J5900 A Deep Dive</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unwrapping-utopia-creating-magical-unboxing-moments/"><u>2024 Approved Unwrapping Utopia Creating Magical Unboxing Moments</u></a></li>
<li><a href="https://android-frp.techidaily.com/how-to-bypass-google-frp-lock-on-realme-11-pro-devices-by-drfone-android/"><u>How to Bypass Google FRP Lock on Realme 11 Pro Devices</u></a></li>
<li><a href="https://review-topics.techidaily.com/in-2024-does-life360-notify-when-you-log-out-on-apple-iphone-15-plus-drfone-by-drfone-virtual-ios/"><u>In 2024, Does Life360 Notify When You Log Out On Apple iPhone 15 Plus? | Dr.fone</u></a></li>
<li><a href="https://pokemon-go-android.techidaily.com/in-2024-latest-way-to-get-shiny-meltan-box-in-pokemon-go-mystery-box-on-realme-c55-drfone-by-drfone-virtual-android/"><u>In 2024, Latest way to get Shiny Meltan Box in Pokémon Go Mystery Box On Realme C55 | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-nailing-the-perfect-shot-expert-tips-for-android-time-lapse-videography/"><u>In 2024, Nailing the Perfect Shot Expert Tips for Android Time-Lapse Videography</u></a></li>
<li><a href="https://some-tips.techidaily.com/streamline-your-viewing-experience-how-to-use-floating-window-on-netflix-for-2024/"><u>Streamline Your Viewing Experience How To Use Floating Window on Netflix for 2024</u></a></li>
<li><a href="https://fox-http.techidaily.com/the-ultimate-combo-guide-zooming-into-facebook-streaming/"><u>The Ultimate Combo Guide Zooming Into Facebook Streaming</u></a></li>
<li><a href="https://pokemon-go-android.techidaily.com/ultimate-guide-to-get-the-meltan-box-pokemon-go-for-honor-90-lite-drfone-by-drfone-virtual-android/"><u>Ultimate guide to get the meltan box pokemon go For Honor 90 Lite | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/unheard-voices-on-youtube-livestream-success-beyond-1000-supporters-for-2024/"><u>Unheard Voices on YouTube Livestream Success Beyond 1000 Supporters for 2024</u></a></li>
</ul></div>

