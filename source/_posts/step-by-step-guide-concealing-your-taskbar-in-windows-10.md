---
title: "Step-by-Step Guide: Concealing Your Taskbar in Windows 10"
date: 2025-01-20T19:50:41.722Z
updated: 2025-01-24T20:33:04.711Z
tags:
  - deals
categories:
  - tech
thumbnail: https://thmb.techidaily.com/0ca2747bace885998e167d601fb15c3166c8be683eacac54f4c7c14302087724.jpg
---

## Step-by-Step Guide: Concealing Your Taskbar in Windows 10

### Quick Links

* [Automatically Hide the Taskbar in Settings](https://screen-video-capture.techidaily.com/new-2024-approved-capturing-every-moment-with-switch-hd-tech/)
* [Automatically Hide the Taskbar Using Command Prompt](https://instagram-videos.techidaily.com/updated-in-2024-achieve-flawless-video-for-instagram-perfection/)
* [Hide Taskbar with a PowerShell Command](https://some-techniques.techidaily.com/updated-excellence-in-video-selecting-peak-frame-rates-for-slow-motion-effects/)

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/wNhKhWc0wLc?si=1XLYV0sXV52Xc0lu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

### Key Takeaways

* You can save screen space by automatically hiding the taskbar on Windows 10.
* To hide the taskbar, right-click empty space on your desktop, then go to Personalization > Taskbar, and enable the toggle next to "Automatically Hide."
* Alternatively, you can use the Command Prompt or PowerShell to toggle the auto-hide option.

 The [Windows taskbar](https://remote-screen-capture.techidaily.com/updated-your-essential-guide-to-unmissable-gaming-adventures-for-2024/) is great for quickly accessing frequently used applications on your computer. However, some users prefer to hide it in order to save screen space. Here's how to hide the taskbar on Windows 10.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/PUDdKOsEN74?si=tkZf-KVinjuwmgx9" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

##  Automatically Hide the Taskbar in Settings

 To automatically hide your taskbar, right-click anywhere on your PC's desktop and select "Personalize" from the pop-up menu.

![Right-click empty space on your desktop, then select 'Personalize.'](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/right-click-personalize.png) 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/PNw3Lb26wFA?si=5NR1XRVSp41EQYMy" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

 The "Settings" window will appear. In the left-hand pane, select "Taskbar." From here, toggle the slider to "On" under "Automatically Hide The Taskbar In Desktop Mode." If your PC is able to switch over to tablet mode, you can hide the taskbar by toggling that option to "On," as well.

![Select the 'Taskbar' tab, then enable 'Automatically hide the taskbar in desktop mode' and 'automatically hide the taskbar in tablet mode.'](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/taskbar-settings.png) 

 You can also right-click the taskbar and select "Taskbar Settings" to access the same Settings window, if you prefer that.

![Right-click the taskbar, then select 'Taskbar Settings.'](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/taskbar-settings-on-taskbar.png) 

 Your taskbar will now automatically hide. This means that, unless you get a notification from an app in the taskbar or you hover your mouse over where the taskbar should be, it won't show up.

**![GIF showing the taskbar auto hiding](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2020/06/GIF-showing-the-taskbar-auto-hiding.gif)** 

 You can undo these settings by toggling the sliders back to the "Off" position.

##  Automatically Hide the Taskbar Using Command Prompt

 If you're feeling like a hacker, you can also toggle the auto-hide option between on and off by running [commands using the Command Prompt](https://some-knowledge.techidaily.com/how-to-leverage-slug-lines-in-articles-for-2024/).

 First, [open the Command Prompt](https://android-frp.techidaily.com/in-2024-step-by-step-tutorial-how-to-bypass-oppo-a78-frp-by-drfone-android/) by typing "command prompt" in the Windows Search bar and then select the "Command Prompt" app from the search results.

![Search 'command prompt' in the Start menu search, then open the result.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/run-command-prompt.png) 

 In Command Prompt, run this command to toggle the taskbar automatically hide option to on:

powershell -command "&{$p='HKCU:SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\StuckRects3';$v=(Get-ItemProperty -Path $p).Settings;$v[8]=3;&Set-ItemProperty -Path $p -Name Settings -Value $v;&Stop-Process -f -ProcessName explorer}"

![toggle autohide option to on from command prompt](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2020/06/toggle-autohide-option-to-on-from-command-prompt.png) 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/xIP8ktrmOdg?si=zRnjbGzM6PDx2jCq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

 And to toggle the taskbar auto-hide option to off, run this command:

powershell -command "&{$p='HKCU:SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\StuckRects3';$v=(Get-ItemProperty -Path $p).Settings;$v[8]=2;&Set-ItemProperty -Path $p -Name Settings -Value $v;&Stop-Process -f -ProcessName explorer}"

![toggle autohide option to off from command prompt](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2020/06/toggle-autohide-option-to-off-from-command-prompt.png) 

##  Hide Taskbar with a PowerShell Command

 You may have noticed that the command we used in Command Prompt actually invoked PowerShell first. You can skip the middleman and just run it with PowerShell directly, if you want.

 Search for "PowerShell" in the Start menu search, then launch it. It doesn't need to be run as administrator, but it won't hurt anything if you do.

![Search for 'powershell' in the Start menu search bar, then click "Open' or 'Run as Administrator.'](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/launch-powershell.png) 

 To auto-hide your taskbar, copy and paste the following command into PowerShell:

$p='HKCU:SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\StuckRects3';$v=(Get-ItemProperty -Path $p).Settings;$v[8]=3;&Set-ItemProperty -Path $p -Name Settings -Value $v;&Stop-Process -f -ProcessName explorer

![The command to auto-hide the taskbar in PowerShell.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/powershell-command.png) 

 If you want to re-enable your taskbar, you need to change "$v\[8\]=3" to "$v\[8\]=2" instead. Your complete command will look like this:

$p='HKCU:SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\StuckRects3';$v=(Get-ItemProperty -Path $p).Settings;$v[8]=2;&Set-ItemProperty -Path $p -Name Settings -Value $v;&Stop-Process -f -ProcessName explorer

![Re-enable the taskbar through PowerShell.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/reenable.png) 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/_SbYznUy_zY?si=ThBkP934r3mizi48" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

 If you just don't like how the taskbar looks, you may want to try [customizing the taskbar](https://remote-screen-capture.techidaily.com/updated-your-essential-guide-to-unmissable-gaming-adventures-for-2024/) instead of hiding it. There are even third-party apps, like [Start11](https://www.stardock.com/products/start11/), that give you even more granular control.

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
<li><a href="https://youtube-tips.techidaily.com/ed-2024-approved-mastering-media-analysis-evaluating-your-vs-opponents-youtube-content/"><u>[Updated] 2024 Approved Mastering Media Analysis Evaluating Your Vs. Opponents' YouTube Content</u></a></li>
<li><a href="https://facebook-record-videos.techidaily.com/updated-are-there-restrictions-in-saving-youtube-videos-in-2024/"><u>[Updated] Are There Restrictions in Saving YouTube Videos, In 2024</u></a></li>
<li><a href="https://article-knowledge.techidaily.com/updated-in-2024-assessing-virtual-realitys-dual-facets-pros-and-cons/"><u>[Updated] In 2024, Assessing Virtual Reality’s Dual Facets Pros & Cons</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/updated-in-2024-beyond-clickbait-whats-real-about-instagram-reels/"><u>[Updated] In 2024, Beyond Clickbait What's Real About Instagram Reels?</u></a></li>
<li><a href="https://fox-links.techidaily.com/updated-in-2024-the-art-of-voice-manipulation-in-ps-console-titles/"><u>[Updated] In 2024, The Art of Voice Manipulation in PS Console Titles</u></a></li>
<li><a href="https://extra-support.techidaily.com/2024-approved-scrutinizing-hero5s-performance-throughout-day/"><u>2024 Approved Scrutinizing Hero5's Performance Throughout Day</u></a></li>
<li><a href="https://some-tips.techidaily.com/choosing-between-apples-latest-innovations-ultra-vs-series-8-find-your-perfect-match/"><u>Choosing Between Apple's Latest Innovations: Ultra Vs. Series 8 – Find Your Perfect Match!</u></a></li>
<li><a href="https://some-tips.techidaily.com/essential-tech-hacks-unveiling-top-10-ipad-shortcuts-and-settings-for-novice-users-and-experts-alike-insights-from-zdnet/"><u>Essential Tech Hacks: Unveiling Top 10 iPad Shortcuts & Settings for Novice Users & Experts Alike - Insights From ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-the-camera-shootout-battle-pixel-npro-xl-triumphs-over-iphone-15-pro-with-a-surprising-twist-detailed-review/"><u>In the Camera Shootout Battle, Pixel nPro XL Triumphs Over iPhone 15 Pro with a Surprising Twist - Detailed Review</u></a></li>
<li><a href="https://some-tips.techidaily.com/integrating-services-how-to-transfer-apple-music-playlists-between-apple-and-googles-streaming-platforms/"><u>Integrating Services: How to Transfer Apple Music Playlists Between Apple and Google's Streaming Platforms</u></a></li>
<li><a href="https://some-tips.techidaily.com/labor-day-savings-snag-a-24-discount-on-apple-airtags-walmart-exclusive-offerzdnet/"><u>Labor Day Savings: Snag a $24 Discount on Apple AirTags - Walmart Exclusive Offer![ZDNET]</u></a></li>
<li><a href="https://smart-video-editing.techidaily.com/new-elevate-learning-with-these-top-rated-animation-software-for-2024/"><u>New Elevate Learning with These Top-Rated Animation Software for 2024</u></a></li>
<li><a href="https://instagram-clips.techidaily.com/quick-tips-for-editing-igtv-content-to-stand-out-for-2024/"><u>Quick Tips for Editing IGTV Content to Stand Out for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/secure-your-copy-of-the-newly-released-apple-vision-pro-today-available-in-512gb-and-1tb-configurations-techspot/"><u>Secure Your Copy of the Newly Released Apple Vision Pro Today - Available in 512GB & 1TB Configurations | TechSpot</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-rated-mp3-audio-devices-a-comprehensive-review-by-zdnet/"><u>Top Rated MP3 Audio Devices : A Comprehensive Review by ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-rated-wireless-charging-pads-in-depth-review-by-tech-gurus/"><u>Top-Rated Wireless Charging Pads - In-Depth Review by Tech Gurus</u></a></li>
<li><a href="https://program-issues.techidaily.com/troubleshooting-guide-fixing-black-ops-cold-war-error-code-0xc0000005/"><u>Troubleshooting Guide: Fixing Black Ops Cold War Error Code 0xC0000005</u></a></li>
<li><a href="https://some-tips.techidaily.com/unleash-creativity-with-freeform-methods-a-powerful-approach-for-brainstorm-sessions/"><u>Unleash Creativity with Freeform Methods: A Powerful Approach for Brainstorm Sessions</u></a></li>
<li><a href="https://video-screen-grab.techidaily.com/windows-11-gamers-guide-to-immaculate-game-recording-for-2024/"><u>Windows 11 Gamers' Guide to Immaculate Game Recording for 2024</u></a></li>
</ul></div>

