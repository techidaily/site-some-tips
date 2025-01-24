---
title: Efficient File Removal Techniques with Windows PowerShell Commands
date: 2025-01-17T17:36:25.307Z
updated: 2025-01-24T16:18:49.470Z
tags:
  - desktop
categories:
  - tech
thumbnail: https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/10/52880885757_aff84061b0_o-1.jpg
---

## Efficient File Removal Techniques with Windows PowerShell Commands

### Quick Links

* [Before You Begin: How to Find a File or Folder’s Full Path](https://extra-lessons.techidaily.com/navigate-iphones-dual-task-capabilities-effortlessly/)
* [How to Delete a Specific File Using PowerShell](https://youtube-video-recordings.techidaily.com/new-5-inspirational-winter-bgs-to-heat-your-videos/)
* [How to Delete a Specific Folder Using PowerShell](https://screen-mirror.techidaily.com/in-2024-how-can-honor-magic-5-litemirror-share-to-pc-drfone-by-drfone-android/)
* [How to Delete All Files in a Folder But Keep the Folder](https://extra-skills.techidaily.com/new-pushing-creative-boundaries-with-these-top-7-film-color-techniques/)
* [How to Delete All Files From a Folder and Its Subfolders](https://win-able.techidaily.com/how-i-finally-managed-to-start-rocket-league-after-persistent-problems/)
* [How to Delete Files With Wildcards](https://extra-lessons.techidaily.com/new-gamer-era-starts-djis-mavic-air-versus-spark-battle/)

### Key Takeaways

* To delete a file or folder, use the "Remove-Item PATH" cmdlet in PowerShell. In this command, replace "PATH" with the full path to the file or folder you want to remove.
* To delete all files in a folder but keep the folder, use the "Remove-Item PATH\\\*.\*" command, where "PATH" is the full path to the folder.
* To remove all files from a folder and its subfolders, use the "Remove-Item PATH -Recurse -Include \*.\*" command, replacing "PATH" with the full path to your parent folder.

 PowerShell offers a straightforward way to delete files and folders on your Windows 11 or Windows 10 PC. You can remove folders, all files inside a folder, specific files from the specified directory, and so on using just a few commands. Here's how to do that.

##  Before You Begin: How to Find a File or Folder’s Full Path

 To remove files or folders from your Windows PC, you’ll need the item’s full path. If you know [how to get file or folder paths](https://fox-links.techidaily.com/updated-2024-approved-unparalleled-screenplay-craftsmanship-across-varied-fields/), skip to the relevant section below. If you aren't sure how to copy a file or folder’s full path, we’ll show you how.

 First, [open a File Explorer window](https://pokemon-go-android.techidaily.com/how-to-get-and-use-pokemon-go-promo-codes-on-realme-c67-4g-drfone-by-drfone-virtual-android/) and locate the file or folder whose path you want to find. Then, hold down the Shift key on your keyboard, right-click your file or folder, and choose "Copy as Path."

!['Copy as Path' highlighted in Windows' context menu.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/11/1-copy-file-folder-path-windows.jpg) 

 You’ve successfully copied the selected item’s path to your clipboard. You can now [paste this path](https://twitter-videos.techidaily.com/new-in-2024-gain-twitter-gifs-for-pc-download-made-simple/) (using Ctrl+V) wherever required within the PowerShell window.

##  How to Delete a Specific File Using PowerShell

 To remove a specific file from your PC, use PowerShell’s "Remove-Item" [cmdlet](https://extra-guidance.techidaily.com/new-prophotomaster-the-ai-enhanced-editing-edge/).

 Start by [opening a PowerShell window on your PC](https://techtrends.techidaily.com/what-are-the-stages-in-a-game-of-royal-match/). Here, type the following command, replace "PATH" with the full path to the item you want to delete, and press Enter:

Remove-Item PATH

 As an example, to delete a file named "Old-List.txt" on your desktop, you'd run:

Remove-Item "C:\Users\username\Desktop\Old-List.txt"

![The 'Remove-Item' cmdlet to delete a file in a PowerShell window.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/11/2-delete-file-powershell.jpg) 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/MmTJlcwgyrQ?si=x3hba82M0tT57fj7" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

 Note that the command won’t ask for a confirmation before deleting your file. If you’d like the command to do that, add the "Confirm" parameter as follows:

Remove-Item "C:\Users\username\Desktop\Old-List.txt" -Confirm

##  How to Delete a Specific Folder Using PowerShell

 You can use PowerShell’s "Remove-Item" cmdlet to remove any directory from your PC.

 Deleting a folder removes all the subfolders and files inside it.

 To start, launch PowerShell, type the following command, replace "PATH" with your directory’s full path, and press Enter:

Remove-Item PATH

 As an example, to delete a directory named "Old Files" from your desktop, you'd run:

Remove-Item "C:\Users\username\Desktop\Old Files"

![The 'Remove-Item' cmdlet to delete a folder in a PowerShell window.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/11/3-delete-folder-powershell.jpg) 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/15Ju8Cb4UZ8?si=5wdiQXdz1BOxIkDH" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/aYH0B2HqcIM?si=3fkoG85L6hAeB4ok" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

##  How to Delete All Files in a Folder But Keep the Folder

 If you want to remove all files from a folder but retain the folder, use the "Remove-Item" cmdlet as follows.

 In your PowerShell window, type the following command, replace "PATH" with the full path to the folder you want to empty, add "\\\*.\*" before the final quotation mark, and press Enter:

Remove-Item PATH\*.*

 For example, to delete all files from a folder named "Your Files" from the desktop, run:

Remove-Item "C:\Users\username\Desktop\Your Files\*.*"

![The 'Remove-Item' cmdlet to delete all files inside a folder on a PowerShell window.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/11/4-delete-all-files-retain-folder-powershell.jpg) 

 In this command, the first asterisk selects files with any name, and the second asterisk chooses files with any extension. This translates to selecting all the files in the specified folder.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/UJJbj1vbzs8?si=X3zd8thLJKprfuEa" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

##  How to Delete All Files From a Folder and Its Subfolders

 If you’re looking to remove all files from a folder and its subfolders, add the "Recurse" and "Include" parameters to the "Remove-Item" cmdlet.

 Open a PowerShell window, enter the following command, replace "PATH" with the full path to the folder, and press Enter:

Remove-Item PATH -Recurse -Include *.*

 Here, the "Recurse" parameter ensures the subfolders’ files are deleted as well. The "Include" parameter ensures files with any name and extension are removed.

 As an example, to remove all files from the "Downloads" folder and its subfolders on the desktop, run:

Remove-Item "C:\Users\username\Desktop\Downloads" -Recurse -Include *.*

![The 'Remove-Item' cmdlet to recursively delete items on a PowerShell window.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/11/5-delete-files-subfolders-powershell.jpg) 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/qmQjRcnaq9g?si=jadcGtXemUAlKOTa" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

##  How to Delete Files With Wildcards

 PowerShell offers wildcards, allowing you to delete various kinds of files by just specifying those file types in your command. In all the examples below, replace "PATH" with the full path to your folder.

 For example, if you want to remove all the [JPG](https://change-location.techidaily.com/ways-to-trade-pokemon-go-from-far-away-on-vivo-y27s-drfone-by-drfone-virtual-android/) files from a folder, use the following command:

Remove-Item PATH -Include *.jpg

 Another use of wildcards is to delete all but a specific file type from your directory. For example, to remove all files except for [PDF](https://extra-support.techidaily.com/new-obs-vs-wirecast-which-should-you-trust-for-live/) files from a folder, use the following command:

Remove-Item PATH -Exclude *.pdf

 Another advanced use of PowerShell is to remove all empty folders from the given directory. In this case, use the following command, replacing "PATH" with the full path to the directory:

Get-ChildItem -Recurse PATH | where { $_.PSISContainer -and @($_ | Get-ChildItem).Count -eq 0 } | Remove-Item

 And you're set.

---

 Now that you know how to delete items with PowerShell, you won't be stuck when File Explorer refuses to work. PowerShell offers more ways than File Explorer to help you remove content, like the ability to only remove specific files with a single command.

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
<li><a href="https://youtube-webster.techidaily.com/ed-leveraging-video-for-maximum-impact-with-these-5-youtube-strategies-for-2024/"><u>[Updated] Leveraging Video for Maximum Impact with These 5 YouTube Strategies for 2024</u></a></li>
<li><a href="https://screen-activity-recording.techidaily.com/updated-the-art-of-precision-introducing-an-obs-countdown-timer/"><u>[Updated] The Art of Precision Introducing an OBS Countdown Timer</u></a></li>
<li><a href="https://some-tips.techidaily.com/2023s-must-have-technology-picks-from-best-buy-featured-by-zdnet/"><u>2023'S Must-Have Technology Picks From Best Buy Featured by ZDNet</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/advanced-editing-perfecting-transitions-in-kinemaster-for-2024/"><u>Advanced Editing Perfecting Transitions in Kinemaster for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/apple-vision-pro-assessment-the-verdict-at-3500-comprehensive-insights-from-experts/"><u>Apple Vision Pro Assessment: The Verdict at $3,500 - Comprehensive Insights From Experts</u></a></li>
<li><a href="https://desktop-recording.techidaily.com/audio-recording-made-easy-free-x-recorder-for-pc-for-2024/"><u>Audio Recording Made Easy Free X-Recorder for PC for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/breaking-news-iphone-16s-camera-tech-sets-new-standards-eclipsing-historic-color-transition-according-to-latest-zdnet-analysis/"><u>Breaking News: IPhone 16'S Camera Tech Sets New Standards, Eclipsing Historic Color Transition According to Latest ZDNET Analysis</u></a></li>
<li><a href="https://some-tips.techidaily.com/cost-breakdown-for-apple-vision-pro-in-extended-reality-xr-investment-strategies-nextgentech-insights/"><u>Cost Breakdown for Apple Vision Pro in Extended Reality (XR) Investment Strategies | NextGenTech Insights</u></a></li>
<li><a href="https://fake-location.techidaily.com/dose-life360-notify-me-when-someone-checks-my-location-on-oppo-a79-5g-drfone-by-drfone-virtual-android/"><u>Dose Life360 Notify Me When Someone Checks My Location On Oppo A79 5G? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/escape-the-monotony-exploring-how-the-metaverse-may-revolutionize-your-future-job-opportunities-zdnet/"><u>Escape the Monotony: Exploring How the Metaverse May Revolutionize Your Future Job Opportunities | ZDNET</u></a></li>
<li><a href="https://some-tips.techidaily.com/exploring-the-disbelief-is-there-truth-to-reports-of-apples-upcoming-arvr-headset-a-zdnet-analysis/"><u>Exploring the Disbelief: Is There Truth to Reports of Apple's Upcoming AR/VR Headset? - A ZDNet Analysis</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/grizzly-introduces-revolutionary-phase-shifting-heat-pad-transforms-from-solid-to-liquid-at-45c/"><u>Grizzly Introduces Revolutionary Phase-Shifting Heat Pad: Transforms From Solid to Liquid at 45°C</u></a></li>
<li><a href="https://some-approaches.techidaily.com/how-to-swiftly-attach-a-soundtrack-to-your-mp4-file-in-minutes/"><u>How to Swiftly Attach a Soundtrack to Your MP4 File in Minutes</u></a></li>
<li><a href="https://android-location.techidaily.com/in-2024-for-people-wanting-to-mock-gps-on-vivo-y100t-devices-drfone-by-drfone-virtual/"><u>In 2024, For People Wanting to Mock GPS on Vivo Y100t Devices | Dr.fone</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/in-2024-how-to-cast-samsung-galaxy-xcover-7-to-computer-for-iphone-and-android-drfone-by-drfone-android/"><u>In 2024, How to Cast Samsung Galaxy XCover 7 to Computer for iPhone and Android? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/synergizing-progress-how-artificial-intelligence-and-5g-are-revolutionizing-technology/"><u>Synergizing Progress: How Artificial Intelligence & 5G Are Revolutionizing Technology</u></a></li>
<li><a href="https://some-tips.techidaily.com/why-i-switched-to-cost-effective-xr-headsets-over-apple-vision-pro-and-meta-quest-vee-expert-review-on-zdnet/"><u>Why I Switched to Cost-Effective XR Headsets Over Apple Vision Pro and Meta Quest Vee | Expert Review on ZDNET</u></a></li>
</ul></div>

