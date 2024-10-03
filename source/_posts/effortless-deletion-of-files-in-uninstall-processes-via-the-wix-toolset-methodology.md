---
title: Effortless Deletion of Files in Uninstall Processes via the WiX Toolset Methodology
date: 2024-09-27T18:39:30.318Z
updated: 2024-10-03T19:46:06.913Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Effortless Deletion of Files in Uninstall Processes via the WiX Toolset Methodology
thumbnail: https://thmb.techidaily.com/773b13fe6e17412a9b5b64d4e711163f73a0c0700089624569da26ef89b36362.jpg
---

## Effortless Deletion of Files in Uninstall Processes via the WiX Toolset Methodology

[Versus](https://tools.techidaily.com/advancedinstaller/products/)

[![Inno Setup](https://cdn.advancedinstaller.com/svg/versus/iconInnoSetup.svg "Inno Setup")Inno Setup](https://www.advancedinstaller.com/versus/wix-toolset/../inno-setup.html)[![WiX Toolset](https://cdn.advancedinstaller.com/svg/versus/iconWiXToolset.svg "WiX Toolset")WiX Toolset](https://tools.techidaily.com/advancedinstaller/products/)[![InstallShield](https://cdn.advancedinstaller.com/svg/versus/iconInstallShield.svg "InstallShield")InstallShield](https://www.advancedinstaller.com/versus/wix-toolset/../installshield/adminstudio.html)[![MSIX Packaging Tool](https://cdn.advancedinstaller.com/svg/versus/iconMSIXPackagingTool.svg "MSIX Packaging Tool")MSIX Packaging Tool](https://www.advancedinstaller.com/versus/wix-toolset/../msix-packaging-tool-vs-advanced-installer.html)

![icon subscribe mail](https://www.advancedinstaller.com/svg/blog/spotSubscribeSidebar.svg "icon subscribe mail")

Check your inbox and confirm the  
 subscription

Exclusive Newsletter![Exclusive Newsletter](https://www.advancedinstaller.com/svg/versus/iconDemo.svg)

![Exclusive Newsletter](https://www.advancedinstaller.com/svg/versus/iconDemo.svg)Exclusive Newsletter

Get the latest WiX insights direct to your inbox. Subscribe now!

>  Disclaimer: This post includes affiliate links
>
>  If you click on a link and make a purchase, I may receive a commission at no extra cost to you.
>

## How to Remove Files on Uninstall Using WiX Toolset

When uninstalling an application, Windows Installer removes by default only the files that were created during the installation process. But, how about the files that are created after the installation? 

In this article, we will see how to remove the files created after the installation using WiX Toolset.

### How to remove files by adding a new component to an existing Component Group in WiX Toolset?

First, you need to add a new Component in an existing Component Group or create a new Component Group altogether – which will need to be referenced in one of the installer’s features.

Let’s imagine that you want to delete a file (sample.txt) that was created by the application in the Install Folder. To delete it, you have to add a new Component to the component group that manages the **Install Folder**. 

<Component Id="DeleteSample" Guid="*">
	<RemoveFile Id="Sample File" On="uninstall" Name="sample.txt"/>
</Component>

Copy

For this code to work, you have to replace the wildcard from the Guid property with a brand new Guid.

Alternatively, you can replace both the name and the extension of the file, in the Name property, with wildcards, making the installer delete the following:

* only the files having a certain name, by replacing the extension with a wildcard
* only the files having a certain extension, by replacing the name with a wildcard
* all the files, by replacing both the name and the extension with wildcards

The **RemoveFile** element removes a file if the parent component is selected for removal.

### How to remove files on uninstall using Advanced Installer?

Here is how you can remove the files created after the installation with Advanced Installer.

1\. Go to the **Files and Folders page**, and add a new File Removal.

![Add New File Removal](https://cdn.advancedinstaller.com/img/wix-child-images/add-new-file-removal.png "Add New File Removal")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2094480/7443" target="_top" id="2094480">
  <img src="//a.impactradius-go.com/display-ad/7443-2094480" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2094480/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)To use the [**File Operations**](https://tools.techidaily.com/advancedinstaller/products/) feature in Advanced Installer, you need to have a Professional license or higher. Start with our [30-day full feature trial](https://tools.techidaily.com/advancedinstaller/products/).

<!-- affiliate ads begin -->
<a href="https://wigfever.sjv.io/c/5597632/2014854/22899" target="_top" id="2014854">
  <img src="//a.impactradius-go.com/display-ad/22899-2014854" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://wigfever.sjv.io/i/5597632/2014854/22899" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. In the New File Removal Dialog, fill in the **Name** field with the name of the file you want to be deleted. 

3\. For the **Component** field, you can choose any component you want.

4\. In the **Remove On** field, choose the Component uninstall option 

5\. And for the **Condition** field, use the REMOVE=”ALL” condition.

![Remove All Condition](https://cdn.advancedinstaller.com/img/wix-child-images/remove-all-condition.png "Remove All Condition")  

That’s it!

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2037474/7443" target="_top" id="2037474">
  <img src="//a.impactradius-go.com/display-ad/7443-2037474" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2037474/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Conclusion

As you see, you can choose between two different approaches when it comes to deleting files during the uninstall process. It is up to you to decide. 

If you prefer to configure your packages through the use of XML, you should go with the WiX Toolset. But if you want a fast and efficient solution, then the option of using the GUI that comes with Advanced Installer is for you.

Advanced Installer #1 alternative to the WiX Toolset

We decided to focus on our main goal to save precious time of our developers.

HANS-LEO TEULINGS   
 PHD – CEO, NEUROSCRIPT, LLC

You might find useful:

* [CAB Embedding Options in MSI](https://tools.techidaily.com/advancedinstaller/products/)
* [Updated installers in WiX Toolset](https://tools.techidaily.com/advancedinstaller/products/)
* [Custom Actions In WiX Toolset](https://tools.techidaily.com/advancedinstaller/products/)
* [Windows Services with WiX Installer](https://tools.techidaily.com/advancedinstaller/products/)
* [Set WiX Installer Version to the Current Build Version](https://tools.techidaily.com/advancedinstaller/products/)
* [Remove Files and Folders when Uninstalling with WiX](https://tools.techidaily.com/advancedinstaller/products/)
* [How to set a WiX Toolset custom action to run only on uninstall](https://tools.techidaily.com/advancedinstaller/products/)
* [How to create non-advertised shortcuts for all users / per machine with WiX Toolset](https://tools.techidaily.com/advancedinstaller/products/)
* [How to Remove Files on Uninstall Using WiX Toolset](https://tools.techidaily.com/advancedinstaller/products/)
* [How to create major upgrades for MSI packages using WiX Toolset](https://tools.techidaily.com/advancedinstaller/products/)
* [How to pass CustomActionData to a CustomAction using WiX](https://tools.techidaily.com/advancedinstaller/products/)
* [How to build an installer without a license page using WiX Toolset](https://tools.techidaily.com/advancedinstaller/products/)
* [How to create a WiX KeyPath attribute](https://tools.techidaily.com/advancedinstaller/products/)
* [How to Create a Desktop Shortcut using WiX Toolset](https://tools.techidaily.com/advancedinstaller/products/)
* [How to Use WiX MSI to Update an Installed Application](https://tools.techidaily.com/advancedinstaller/products/)
* [How to correctly set the install folder in Wix](https://tools.techidaily.com/advancedinstaller/products/)
* [WiX Toolset Visual Studio Extension](https://tools.techidaily.com/advancedinstaller/products/)
* [How to create a custom dialog in WiX for user input](https://tools.techidaily.com/advancedinstaller/products/)
* [How to create an MSI installer with WiX](https://tools.techidaily.com/advancedinstaller/products/)
* [How to use WIX MSI to do a silent install or uninstall of a web app](https://tools.techidaily.com/advancedinstaller/products/)

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135356/19272" target="_top" id="2135356">
  <img src="//a.impactradius-go.com/display-ad/19272-2135356" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135356/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Get the most from packaging with Advanced Installer

Try the 30-day fully-featured edition absolutely free!

[Download Free Trial](https://tools.techidaily.com/advancedinstaller/products/)

No credit card required

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
<li><a href="https://youtube-videos.techidaily.com/new-auditory-artistry-access-to-excellent-dj-video-samples/"><u>[New] Auditory Artistry Access to Excellent DJ Video Samples</u></a></li>
<li><a href="https://video-capture.techidaily.com/new-in-2024-the-premier-webcam-lineup-for-next-gen-windows-pcs/"><u>[New] In 2024, The Premier Webcam Lineup for Next-Gen Windows PCs</u></a></li>
<li><a href="https://youtube-lab.techidaily.com/ed-2024-approved-your-ultimate-yt-shorts-companion/"><u>[Updated] 2024 Approved Your Ultimate YT Shorts Companion</u></a></li>
<li><a href="https://youtube-docs.techidaily.com/ed-easy-and-speed-share-youtube-playlists-now-for-2024/"><u>[Updated] Easy & Speed Share YouTube Playlists Now for 2024</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/updated-uncovering-the-ultimate-screen-recorder-compare-and-choose-obsfraps/"><u>[Updated] Uncovering the Ultimate Screen Recorder Compare and Choose (OBS/Fraps)</u></a></li>
<li><a href="https://some-tips.techidaily.com/achieve-superior-outcomes-mastering-dall-e-2-in-5-steps/"><u>Achieve Superior Outcomes: Mastering DALL-E 2 in 5 Steps</u></a></li>
<li><a href="https://some-tips.techidaily.com/advancements-in-ai-communication-exploring-the-improved-conversational-capabilities-of-chatgpts-gpt-4/"><u>Advancements in AI Communication: Exploring the Improved Conversational Capabilities of ChatGPT's GPT-4</u></a></li>
<li><a href="https://some-tips.techidaily.com/ai-powered-youtubes-new-feature-quick-video-previews-and-summaries/"><u>AI Powered YouTube's New Feature: Quick Video Previews & Summaries</u></a></li>
<li><a href="https://some-tips.techidaily.com/boost-your-linux-skills-with-tips-from-chatgpt-a-personal-experience/"><u>Boost Your Linux Skills with Tips From ChatGPT - A Personal Experience</u></a></li>
<li><a href="https://some-tips.techidaily.com/discover-cutting-edge-results-with-our-latest-ai-enhanced-google-search/"><u>Discover Cutting-Edge Results with Our Latest AI-Enhanced Google Search</u></a></li>
<li><a href="https://some-tips.techidaily.com/electric-vehicle-charging-issues-unraveling-the-top-8-causes-of-connection-failures/"><u>Electric Vehicle Charging Issues: Unraveling the Top 8 Causes of Connection Failures</u></a></li>
<li><a href="https://some-tips.techidaily.com/electrifying-news-volkswagen-adopts-tesla-compatible-charging-stations-for-future-models/"><u>Electrifying News: Volkswagen Adopts Tesla-Compatible Charging Stations for Future Models</u></a></li>
<li><a href="https://some-tips.techidaily.com/embracing-the-reality-electric-vehicle-ranges-may-remain-stable-for-now/"><u>Embracing the Reality: Electric Vehicle Ranges May Remain Stable for Now</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/enhancing-tiktok-profiles-with-linktree-features/"><u>Enhancing TikTok Profiles with Linktree Features</u></a></li>
<li><a href="https://techidaily.com/full-guide-to-hard-reset-your-motorola-defy-2-drfone-by-drfone-reset-android-reset-android/"><u>Full Guide to Hard Reset Your Motorola Defy 2 | Dr.fone</u></a></li>
<li><a href="https://ai-vdieo-software.techidaily.com/in-2024-free-download-filmora-13-video-editing-made-easy/"><u>In 2024, Free Download Filmora 13 Video Editing Made Easy</u></a></li>
<li><a href="https://win11.techidaily.com/microsofts-innovation-unveiled-ai-companion-for-windows-11-enhanced-productivity/"><u>Microsoft's Innovation Unveiled: AI Companion for Windows 11 Enhanced Productivity</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-drone-picks-unveiling-the-ultimate-flyers-of-2024/"><u>Top Drone Picks: Unveiling the Ultimate Flyers of 2024</u></a></li>
<li><a href="https://sound-issues.techidaily.com/top-solutions-for-restoring-audio-on-your-toshiba-laptop/"><u>Top Solutions for Restoring Audio on Your Toshiba Laptop</u></a></li>
</ul></div>

