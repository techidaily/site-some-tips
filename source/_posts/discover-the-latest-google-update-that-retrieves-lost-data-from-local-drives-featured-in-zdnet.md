---
title: Discover the Latest Google Update That Retrieves Lost Data From Local Drives, Featured in ZDNet
date: 2024-12-20T16:55:33.604Z
updated: 2024-12-27T16:53:04.367Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/cloud/    https://www.zdnet.com/a/img/resize/11605a395ec8b3e2f636eb48afa4c955709bccd5/2023/12/11/a0d15279-54ca-4124-b358-f316518e220a/google-silgettyimages-1026614182.jpg?width=170&height=96&fit=crop&auto=webp
---

## Discover the Latest Google Update That Retrieves Lost Data From Local Drives, Featured in ZDNet

![google-silgettyimages-1026614182](https://www.zdnet.com/a/img/resize/fec48d129c5cfc8c9723c7e9d539f8ddf2e286d8/2023/12/11/a0d15279-54ca-4124-b358-f316518e220a/google-silgettyimages-1026614182.jpg?auto=webp&width=1280)

Anadolu/Getty Images

A few months ago, reports began surfacing that some Google Drive desktop app users had [apparently lost months worth of files](https://www.zdnet.com/article/some-google-drive-users-have-apparently-lost-months-worth-of-files/). Google support forums received numerous posts from panicked users, and the company itself wasn't offering much clarity into what happened, only suggesting that users refrain from moving any files.

**Also: [The top cloud storage services you can buy](https://www.zdnet.com/article/best-cloud-storage/)**

Now Google is explaining what happened, and offering up a way to restore the missing files. In [a post on the company's community support forum](https://support.google.com/drive/thread/245861992), two fixes were provided - one using the actual Drive app and one using a command line interface. While a temporary fix posted by a user in the support forum worked for some people, the Google suggestion seems to be working for everyone who tries it.

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

For the first method, Google says, start by making sure you have the latest version of the desktop app - 85.0.13.0 or higher. To see what version you're running, click on the settings gear in the desktop app, then "about." If you have the latest version, open Drive and then hold the shift key and click settings. From there, click Recover from backups.

While recovery is working, you'll see either a message that recovery has started, or one that says no backups found. If you see the former, you'll eventually see a message that says recovery is complete, in which case your files should be restored, or one that says not enough disk space. If you see the second message, you'll need to free up space and run the same operation again.

When that process is done, there should be a new desktop folder called [Google Drive](https://www.zdnet.com/home-and-office/work-life/how-to-organize-your-google-drive-5-tips-and-tricks-to-know/) Recovery containing the unsynced files. 

If you get the message that no backup is found, Google says to submit feedback through the app with the hashtag "#DFD84" and send diagnostic logs.

**Also: [How to organize your Google Drive: 5 tips and tricks to know](https://www.zdnet.com/home-and-office/work-life/how-to-organize-your-google-drive-5-tips-and-tricks-to-know/)**

The second method, using the command line, is useful if you have your [backup](https://www.zdnet.com/article/best-backup-software/) in another location or you want to restore the files to a specific location. 

To perform that recovery method in Windows, open the command prompt and run the command

> "C:\\Program Files\\Google\\Drive File Stream\\launch.bat" --recover\_from\_account\_backups." 

The tool will run silently, Google says, and you'll know it's done when GoogleDriveFS.exe is no longer running in Task Manager. As with the first method, a new folder will be created on the desktop with your missing files.

For the Mac version of the second method, open the terminal application and enter

> "/Applications/Google Drive.app/Contents/MacOS/Google Drive" --recover\_from\_account\_backups

If these methods still don't work, Google suggests [reaching out to support directly](https://support.google.com/drive/answer/4431192).

#### Google

[Everything announced at Made by Google 2024](https://www.zdnet.com/article/everything-announced-at-made-by-google-2024-pixel-9-pro-fold-gemini-watch-3-and-more/ "Everything announced at Made by Google 2024")

[Google's new Pixel 9 Pro Fold is here, but should you buy the cheaper Pixel Fold instead?](https://www.zdnet.com/article/google-pixel-9-pro-fold-vs-pixel-fold/ "Google's new Pixel 9 Pro Fold is here, but should you buy the cheaper Pixel Fold instead?")

[Pixel Buds Pro 2 vs. Pixel Buds Pro: Which Google earbuds are the best?](https://www.zdnet.com/article/pixel-buds-pro-2-vs-pixel-buds-pro-which-google-earbuds-are-the-best/ "Pixel Buds Pro 2 vs. Pixel Buds Pro: Which Google earbuds are the best?")

[I tested the Google Pixel 9 Pro's 'Add Me' feature and found it crazy clever](https://www.zdnet.com/article/the-google-pixel-9-pros-add-me-feature-is-an-ar-camera-tool-youll-actually-use/ "I tested the Google Pixel 9 Pro's 'Add Me' feature and found it crazy clever")

* [Everything announced at Made by Google 2024](https://www.zdnet.com/article/everything-announced-at-made-by-google-2024-pixel-9-pro-fold-gemini-watch-3-and-more/ "Everything announced at Made by Google 2024")
* [Google's new Pixel 9 Pro Fold is here, but should you buy the cheaper Pixel Fold instead?](https://www.zdnet.com/article/google-pixel-9-pro-fold-vs-pixel-fold/ "Google's new Pixel 9 Pro Fold is here, but should you buy the cheaper Pixel Fold instead?")
* [Pixel Buds Pro 2 vs. Pixel Buds Pro: Which Google earbuds are the best?](https://www.zdnet.com/article/pixel-buds-pro-2-vs-pixel-buds-pro-which-google-earbuds-are-the-best/ "Pixel Buds Pro 2 vs. Pixel Buds Pro: Which Google earbuds are the best?")
* [I tested the Google Pixel 9 Pro's 'Add Me' feature and found it crazy clever](https://www.zdnet.com/article/the-google-pixel-9-pros-add-me-feature-is-an-ar-camera-tool-youll-actually-use/ "I tested the Google Pixel 9 Pro's 'Add Me' feature and found it crazy clever")

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
<li><a href="https://youtube-blog.techidaily.com/ath-to-youtube-prosperity-unlocking-monetization-with-500plus-views/"><u>[New] Path to YouTube Prosperity Unlocking Monetization with 500+ Views</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-tackling-text-transformations-converting-xmlttml-for-voice-outputs/"><u>[New] Tackling Text Transformations Converting XML/TTML for Voice Outputs</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unveiling-the-secrets-to-download-youtubes-subtitles/"><u>[New] Unveiling the Secrets to Download YouTube's Subtitles</u></a></li>
<li><a href="https://snapchat-videos.techidaily.com/updated-in-2024-smart-sync-strategy-transferring-photos-from-iphone-to-snapchat-correctly/"><u>[Updated] In 2024, Smart Sync Strategy Transferring Photos From iPhone to Snapchat Correctly</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-top-kid-friendly-drone-models-for-first-flights/"><u>[Updated] Top Kid-Friendly Drone Models for First Flights</u></a></li>
<li><a href="https://article-helps.techidaily.com/2024-approved-essential-tools-for-motion-artwork/"><u>2024 Approved Essential Tools for Motion Artwork</u></a></li>
<li><a href="https://buynow-tips.techidaily.com/critical-insights-on-googles-pixel-slate-and-its-chromeos-woes/"><u>Critical Insights on Google's Pixel Slate and Its ChromeOS Woes</u></a></li>
<li><a href="https://change-location.techidaily.com/how-to-use-snapchat-location-spoofer-to-protect-your-privacy-on-infinix-note-30-5g-drfone-by-drfone-virtual-android/"><u>How to use Snapchat Location Spoofer to Protect Your Privacy On Infinix Note 30 5G? | Dr.fone</u></a></li>
<li><a href="https://review-topics.techidaily.com/how-to-y02t-get-deleted-pictures-back-with-ease-and-safety-by-fonelab-android-recover-pictures/"><u>How to Y02T Get Deleted Pictures Back with Ease and Safety?</u></a></li>
<li><a href="https://digital-screen-recording.techidaily.com/in-2024-discovering-androids-premier-mobas-ranked/"><u>In 2024, Discovering Android's Premier MOBAs Ranked</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unlock-professional-graphics-custom-templates-on-the-house/"><u>In 2024, Unlock Professional Graphics - Custom Templates on the House</u></a></li>
<li><a href="https://games-able.techidaily.com/post-shortage-whats-next-for-ps5-retail-costs/"><u>Post-Shortage, What's Next for PS5 Retail Costs?</u></a></li>
<li><a href="https://win11.techidaily.com/revamping-admin-oversight-of-chromium-and-microsoft-edge-browsing-experience/"><u>Revamping Admin-Oversight of Chromium & Microsoft Edge Browsing Experience</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/OZQJUTr44rA?si=ADA0nD1VnXjR_sH0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

