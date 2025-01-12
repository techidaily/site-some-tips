---
title: How to Retrieve Vanished Documents on Your PC with Google Drive's New Feature | Tech Analysis by ZDNet
date: 2025-01-11T18:40:56.272Z
updated: 2025-01-12T18:33:20.837Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/cloud/    https://www.zdnet.com/a/img/resize/11605a395ec8b3e2f636eb48afa4c955709bccd5/2023/12/11/a0d15279-54ca-4124-b358-f316518e220a/google-silgettyimages-1026614182.jpg?width=170&height=96&fit=crop&auto=webp
---

## How to Retrieve Vanished Documents on Your PC with Google Drive's New Feature | Tech Analysis by ZDNet

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
<li><a href="https://youtube-blog.techidaily.com/n-2024-cool-climates-cozy-cinematics-selecting-winter-backgrounds/"><u>[New] In 2024, Cool Climates, Cozy Cinematics Selecting Winter Backgrounds</u></a></li>
<li><a href="https://screen-video-capture.techidaily.com/new-in-2024-prime-zero-dollar-clip-maker-program/"><u>[New] In 2024, Prime Zero-Dollar Clip Maker Program</u></a></li>
<li><a href="https://youtube-webster.techidaily.com/ed-advanced-techniques-for-youtube-editing-via-finalcut-pro-for-2024/"><u>[Updated] Advanced Techniques for YouTube Editing via FinalCut Pro for 2024</u></a></li>
<li><a href="https://some-techniques.techidaily.com/updated-from-concept-to-completion-utilizing-luts-effectively-in-premiere-pro/"><u>[Updated] From Concept to Completion Utilizing LUTs Effectively in Premiere Pro</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/updated-going-back-in-time-your-android-movie-method/"><u>[Updated] Going Back in Time Your Android Movie Method</u></a></li>
<li><a href="https://fox-info.techidaily.com/updated-in-2024-becoming-a-whatsapp-pro-uncovering-invaluable-tips-and-tricks/"><u>[Updated] In 2024, Becoming a WhatsApp Pro Uncovering Invaluable Tips and Tricks</u></a></li>
<li><a href="https://discord-videos.techidaily.com/2024-approved-crafting-chat-aesthetics-the-definitive-guide-to-discord-formatting/"><u>2024 Approved Crafting Chat Aesthetics The Definitive Guide to Discord Formatting</u></a></li>
<li><a href="https://novels-ebooks.techidaily.com/211441845--cannabis-y-espiritualidad/"><u>Cannabis y espiritualidad | Free Book</u></a></li>
<li><a href="https://fake-location.techidaily.com/in-2024-5-easy-ways-to-change-location-on-youtube-tv-on-tecno-spark-10-4g-drfone-by-drfone-virtual-android/"><u>In 2024, 5 Easy Ways to Change Location on YouTube TV On Tecno Spark 10 4G | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/mastering-google-pixel-watchs-new-protective-feature-a-step-by-step-guide-to-enabling-fall-detection-smartwatch-security-with-zdnet/"><u>Mastering Google Pixel Watch’s New Protective Feature: A Step-by-Step Guide to Enabling Fall Detection | Smartwatch Security with ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/maximizing-productivity-with-top-tools-and-techniques-to-streamline-your-daily-routine-expert-tips-by-zdnet/"><u>Maximizing Productivity with Top Tools & Techniques to Streamline Your Daily Routine | Expert Tips by ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/navigating-through-chaos-leveraging-google-docs-versioning-for-data-safety-and-recovery/"><u>Navigating Through Chaos: Leveraging Google Docs Versioning for Data Safety and Recovery</u></a></li>
<li><a href="https://some-tips.techidaily.com/overcoming-google-drive-hurdles-a-comprehensive-guide-to-successful-file-downloads/"><u>Overcoming Google Drive Hurdles: A Comprehensive Guide to Successful File Downloads</u></a></li>
<li><a href="https://some-tips.techidaily.com/revolutionizing-home-comfort-top-alternatives-to-ecobee-and-amazons-offerings-in-smart-thermostats-unveiled-by-zdnet/"><u>Revolutionizing Home Comfort: Top Alternatives to Ecobee and Amazon's Offerings in Smart Thermostats Unveiled by ZDNET</u></a></li>
<li><a href="https://some-tips.techidaily.com/stop-overlooking-crucial-emails-with-simple-gmail-notification-tweaks-expert-guide/"><u>Stop Overlooking Crucial Emails with Simple Gmail Notification Tweaks – Expert Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-rated-protective-covers-for-your-google-pixel-7a-the-latest-selection-you-cant-miss/"><u>Top-Rated Protective Covers for Your Google Pixel 7A: The Latest Selection You Can't Miss!</u></a></li>
<li><a href="https://some-tips.techidaily.com/zdnets-ultimate-guide-to-the-premier-google-pixel-phones-of-2024-expertly-tested-and-reviewed/"><u>ZDNet's Ultimate Guide to the Premier Google Pixel Phones of 2024 - Expertly Tested and Reviewed</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/9ECz3oZ8NrQ?si=86vkwkDJo9HQXpzt" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

