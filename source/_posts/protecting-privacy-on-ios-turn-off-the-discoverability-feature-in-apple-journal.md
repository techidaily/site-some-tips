---
title: Protecting Privacy on iOS - Turn Off the Discoverability Feature in Apple Journal
date: 2024-10-13T18:42:25.632Z
updated: 2024-10-20T16:34:24.784Z
tags:
  - apple
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/apple/    https://www.zdnet.com/a/img/resize/e1c97a372d50219ebfe746bcad0e0906a6a53076/2024/04/05/ca836ca2-489f-4333-9b63-1e09daf1dc4a/journal.jpg?width=170&height=96&fit=crop&auto=webp
---

## Discover the True Condition of Your Apple Watch's Battery - Unveiling Unexpected Insights

![apple-watch-series-7-3.jpg](https://www.zdnet.com/a/img/resize/fb1894cec95b042794453fab1fd1bbdd5feecd86/2021/11/02/3fb8411f-1bcc-47cd-99e2-bb3fb393f34b/apple-watch-series-7-3.jpg?auto=webp&width=1280)

The Series 7 in Midnight and Blue. 

Jason Cipriani/ZDNet

OK, so the other day we looked at how to tell how worn your iPhone battery is, and we also looked at some of the [weird lies the "battery health" screen tells you](https://www.zdnet.com/article/your-iphone-battery-is-lying-to-you-in-weird-ways/).

That led to the inevitable question -- how worn is the battery in my Apple Watch?

>  Disclaimer: This post includes affiliate links
>
>  If you click on a link and make a purchase, I may receive a commission at no extra cost to you.
>

### See also

* [You can already use the Apple Watch's double-tap feature. Here's how](https://www.zdnet.com/article/you-can-already-use-the-apple-watchs-double-tap-feature-heres-how/)
* [Apple Watch Fall Detection: How and why to enable it](https://www.zdnet.com/article/apple-watch-fall-detection-how-and-why-to-enable-it/)
* [How to set up an Apple Watch](https://www.zdnet.com/article/how-to-set-up-an-apple-watch/)
* [How to chat with ChatGPT right on your Apple Watch. Meet Petey AI](https://www.zdnet.com/article/how-to-chat-with-chatgpt-right-on-your-apple-watch-meet-petey-ai/)

This seems to be something that worries Apple Watch owners. After all, this is a device that seems to need to be charged daily, and it's got a pretty small battery, and as such, users feel there's not much wiggle room once the battery is worn.

Also, it's not tricky to find somewhere that will change the battery in your iPhone, but with the Apple Watch you're a lot more limited. 

Probably your best answer here is to [pay the $69 and let Apple do it](https://support.apple.com/watch/repair/service).

But other than finding your Apple Watch dying on your arm in the middle of the day, how do you tell how much life it has left?

Well, it's a similar process to [figuring out how worn the iPhone's battery](https://www.zdnet.com/article/your-iphone-battery-is-lying-to-you-in-weird-ways/) is. 

Fire up your iPhone and go to **Settings > Privacy**, then scroll to the bottom and tap on **Analytics & Improvements**.

Then you need to click on **Analytics Data**. This setting only exists if you have **Share iPhone & Watch Analytics** enabled. If it's not enabled, you'll need to enable it and wait a day or so for the iPhone to collect the data.

Yes, the information is only logged if you choose to share it with Apple. But oddly, Apple doesn't make it easy for you to look at it.

If **Analytics Data** is enabled, then tap on it, and you'll be presented with what looks like a wall of files.

Wall of analytics files

Don't panic!

You need to scroll until you find a file starting with the name **log-aggregated**. There's likely to be a bunch of them with dates in the name.

<!-- affiliate ads begin -->
<a href="https://imp.i357552.net/c/5597632/1061528/11832" target="_top" id="1061528">
  <img src="//a.impactradius-go.com/display-ad/11832-1061528" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://imp.i357552.net/i/5597632/1061528/11832" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### **ZDNET** Recommends

[The best smartwatches Apple, Samsung, and others battle for your wrist.  Read now](https://www.zdnet.com/article/best-smartwatch/)

The latest one will be at the bottom of the list. Oh, but if you have an Apple Watch paired with the iPhone, then there will be a similar file for that too. To tell the difference, tap on it to open up the file, scroll to the top and look for it to mention **Watch OS** and not **iPhone OS**.

And going through this data on the iPhone itself is a pain (although it can be done if you're patient and do a copy and paste into an app like **Notes**).

What I do is I tap the Share button and email the file to myself so I can open it at my leisure on a Mac or PC (you could always AirDrop it to yourself).

**Also:** [How to AirDrop](https://www.zdnet.com/home-and-office/how-to-airdrop/)

The file contains a lot of information, so once you have it open in a text editor, you can start looking for specific information.

Apple Watch battery cycle count

Here I'm looking for one specific entry:

**<key>com.apple.power.battery.CycleCount</key>**

 **<integer>163</integer>**

That number between the **<integer>** tags is the battery cycle count, which is the number of times the battery has been fully recharged. This means that if one day you take your Apple Watch down to 50% before recharging it, and 50% the next day, those two recharges count as one recharge cycle.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2123727/7443" target="_top" id="2123727">
  <img src="//a.impactradius-go.com/display-ad/7443-2123727" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2123727/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## How worn is my Apple Watch battery?

Now, I took delivery of my [Apple Watch Series 7](https://apple.sjv.io/c/159047/435031/7613?&sharedId=zdnet&u=https%3A%2F%2Fwww.apple.com%2Fapple-watch-series-7%2F&subId1=zd-%5F%5FCOM%5FCLICK%5FID%5F%5F-dtp) in mid-October 2021, and I've worn it constantly since then. With this in mind, I'm quite surprised that it has only been through 163 recharge cycles, which means I'm on track for about 217 recharge cycles during the first year of ownership.

But how many recharge cycles can the battery endure before Apple considers it worn?

This is where I got another surprise!

According to [Apple](https://www.apple.com/batteries/service-and-recycling/), the battery in the Apple Watch "is designed to retain up to 80 percent of its original capacity at 1000 complete charge cycles." That's twice the number of charge cycles that the iPhone can do and still retain 80 percent of its charge capacity.

That means the battery is good for at least 3.5 to 4 years, which is pretty impressive. 

#### More how-tos

[How to download YouTube videos for free, plus two other methods](https://www.zdnet.com/article/how-to-download-youtube-videos-for-free-plus-two-other-methods/ "How to download YouTube videos for free, plus two other methods")

[Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how](https://www.zdnet.com/article/ditch-the-wi-fi-how-to-add-a-wired-network-to-your-home-without-ethernet-cable/ "Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how")

[Wiping a Windows laptop? Here's the safest free way to erase your personal data](https://www.zdnet.com/article/wiping-a-windows-laptop-heres-the-safest-free-way-to-erase-your-personal-data/ "Wiping a Windows laptop? Here's the safest free way to erase your personal data")

[How to connect a PS4 controller to a smartphone](https://www.zdnet.com/article/how-to-connect-a-ps4-controller-to-a-smartphone/ "How to connect a PS4 controller to a smartphone")

* [How to download YouTube videos for free, plus two other methods](https://www.zdnet.com/article/how-to-download-youtube-videos-for-free-plus-two-other-methods/ "How to download YouTube videos for free, plus two other methods")
* [Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how](https://www.zdnet.com/article/ditch-the-wi-fi-how-to-add-a-wired-network-to-your-home-without-ethernet-cable/ "Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how")
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
<li><a href="https://some-tips.techidaily.com/new-strategies-for-winning-on-spotifys-ad-platform/"><u>[New] Strategies for Winning on Spotify's Ad Platform</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-essentials-navigating-whatsapp-call-functionality/"><u>[New] The Essentials Navigating WhatsApp Call Functionality</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-top-11-windows-11-secrets-unveiled/"><u>[New] Top 11 Windows 11 Secrets Unveiled</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unveiling-the-secrets-of-gopro-timelapse-photography/"><u>[New] Unveiling the Secrets of GoPro Timelapse Photography</u></a></li>
<li><a href="https://facebook-video-content.techidaily.com/updated-in-2024-the-ultimate-playlist-to-share-on-fb-stories/"><u>[Updated] In 2024, The Ultimate Playlist to Share on FB Stories</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-streamlined-playback-import-tunes-into-inshot/"><u>[Updated] Streamlined Playback Import Tunes Into InShot</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-ultimate-lg-4k-display-a-comprehensive-overview/"><u>[Updated] Ultimate LG 4K Display A Comprehensive Overview</u></a></li>
<li><a href="https://youtube-data.techidaily.com/approved-light-up-the-screen-techniques-for-stunning-youtube-visuals/"><u>2024 Approved Light Up the Screen Techniques for Stunning YouTube Visuals</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-top-ringtones-for-game-of-thrones-enthusiasts-online-listings/"><u>2024 Approved Top Ringtones for Game of Thrones Enthusiasts - Online Listings</u></a></li>
<li><a href="https://common-error.techidaily.com/fixing-the-resolved-halo-4-ue4-critical-bug-leading-to-system-failure/"><u>Fixing the [Resolved]: Halo 4 UE4 Critical Bug Leading to System Failure</u></a></li>
<li><a href="https://win-solutions.techidaily.com/how-to-resolve-the-recurring-freezing-and-crashing-problem-with-warzone-version-20-on-desktop/"><u>How to Resolve the Recurring Freezing and Crashing Problem with Warzone Version 2.0 on Desktop</u></a></li>
<li><a href="https://article-tips.techidaily.com/in-2024-bring-a-smile-simple-meme-creation-with-kapwing/"><u>In 2024, Bring a Smile Simple Meme Creation With Kapwing</u></a></li>
<li><a href="https://android-transfer.techidaily.com/in-2024-how-to-use-phone-clone-to-migrate-your-tecno-camon-20-data-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>In 2024, How to Use Phone Clone to Migrate Your Tecno Camon 20 Data? | Dr.fone</u></a></li>
<li><a href="https://technical-tips.techidaily.com/playstation-4-gaming-screenshots-and-recordings-made-easy/"><u>PlayStation 4 Gaming Screenshots and Recordings Made Easy</u></a></li>
<li><a href="https://fox-that.techidaily.com/reviving-the-functionality-of-your-iphone-volume-keys-7-proven-strategies/"><u>Reviving the Functionality of Your iPhone Volume Keys - 7 Proven Strategies</u></a></li>
<li><a href="https://article-knowledge.techidaily.com/step-by-step-crafting-your-own-android-ringtones-and-sounds/"><u>Step-By-Step Crafting Your Own Android Ringtones and Sounds</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-10-essential-gratuitous-lut-downloads-of-the-year-for-2024/"><u>Top 10 Essential, Gratuitous LUT Downloads of the Year for 2024</u></a></li>
<li><a href="https://win-amazing.techidaily.com/toshiba-printer-driver-downloads-for-windows-pcs/"><u>Toshiba Printer Driver Downloads for Windows PCs</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveil-the-subject-background-removal-techniques-in-photopea-for-2024/"><u>Unveil the Subject Background Removal Techniques in Photopea for 2024</u></a></li>
</ul></div>

