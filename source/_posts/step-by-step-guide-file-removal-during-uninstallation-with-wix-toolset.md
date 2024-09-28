---
title: "Step-by-Step Guide: File Removal During Uninstallation with WiX Toolset"
date: 2024-09-25T08:07:57.685Z
updated: 2024-09-27T20:31:48.600Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Step-by-Step Guide: File Removal During Uninstallation with WiX Toolset"
thumbnail: https://thmb.techidaily.com/acfc08d56b4206022979b3dc0ecd7952203549957dd5b874ab0b46f7e315b993.jpg
---

## Step-by-Step Guide: File Removal During Uninstallation with WiX Toolset

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

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1959707/19272" target="_top" id="1959707">
  <img src="//a.impactradius-go.com/display-ad/19272-1959707" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1959707/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2137227/26400" target="_top" id="2137227">
  <img src="//a.impactradius-go.com/display-ad/26400-2137227" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2137227/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to remove files on uninstall using Advanced Installer?

Here is how you can remove the files created after the installation with Advanced Installer.

1\. Go to the **Files and Folders page**, and add a new File Removal.

![Add New File Removal](https://cdn.advancedinstaller.com/img/wix-child-images/add-new-file-removal.png "Add New File Removal")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135374/19272" target="_top" id="2135374">
  <img src="//a.impactradius-go.com/display-ad/19272-2135374" border="0" alt="https://techidaily.com" width="468" height="60"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135374/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)To use the [**File Operations**](https://tools.techidaily.com/advancedinstaller/products/) feature in Advanced Installer, you need to have a Professional license or higher. Start with our [30-day full feature trial](https://tools.techidaily.com/advancedinstaller/products/).

<!-- affiliate ads begin -->
<a href="https://dhgate.sjv.io/c/5597632/1172027/12108" target="_top" id="1172027">
  <img src="//a.impactradius-go.com/display-ad/12108-1172027" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://dhgate.sjv.io/i/5597632/1172027/12108" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. In the New File Removal Dialog, fill in the **Name** field with the name of the file you want to be deleted. 

3\. For the **Component** field, you can choose any component you want.

4\. In the **Remove On** field, choose the Component uninstall option 

5\. And for the **Condition** field, use the REMOVE=”ALL” condition.

![Remove All Condition](https://cdn.advancedinstaller.com/img/wix-child-images/remove-all-condition.png "Remove All Condition")  

That’s it!

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
<li><a href="https://instagram-clips.techidaily.com/new-in-2024-get-the-most-out-of-instagram-photos-with-these-apps/"><u>[New] In 2024, Get the Most Out of Instagram Photos with These Apps</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-superior-editing-software-tailored-to-dji-filmmaking/"><u>[New] Superior Editing Software Tailored to DJi Filmmaking</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-editors-toolkit-maximizing-the-impact-of-gopro-videos/"><u>[New] The Editor's Toolkit Maximizing the Impact of GoPro Videos</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-skys-playground-discovering-the-husqvarna-x4-fpv/"><u>[New] The Sky's Playground Discovering the Husqvarna X4 FPV</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-top-live-broadcast-tech-for-industry-experts/"><u>[New] Top Live Broadcast Tech for Industry Experts</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/updated-2024-approved-prime-pick-top-10-streamers-for-cutting-edge-tv-content/"><u>[Updated] 2024 Approved Prime Pick Top 10 Streamers for Cutting-Edge TV Content</u></a></li>
<li><a href="https://youtube-docs.techidaily.com/ed-growing-presence-in-video-platforms-via-short-films-for-2024/"><u>[Updated] Growing Presence in Video Platforms via Short Films for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-roadmap-to-fame-unleashing-instagrams-9-powerful-techniques/"><u>[Updated] The Roadmap to Fame Unleashing Instagram's #9 Powerful Techniques</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-transformative-video-creation-harness-the-trio-of-windows-photos-and-storyremix/"><u>[Updated] Transformative Video Creation Harness the Trio of Windows, Photos, and StoryRemix</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-transitioning-artistry-in-inshot-videos/"><u>[Updated] Transitioning Artistry in Inshot Videos</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unraveling-whatsapps-voice-transmission-techniques/"><u>[Updated] Unraveling WhatsApp's Voice Transmission Techniques</u></a></li>
<li><a href="https://techidaily.com/full-guide-to-hard-reset-your-vivo-y100i-drfone-by-drfone-reset-android-reset-android/"><u>Full Guide to Hard Reset Your Vivo Y100i | Dr.fone</u></a></li>
<li><a href="https://fake-location.techidaily.com/in-2024-5-best-route-generator-apps-you-should-try-on-apple-iphone-12-drfone-by-drfone-virtual-ios/"><u>In 2024, 5 Best Route Generator Apps You Should Try On Apple iPhone 12 | Dr.fone</u></a></li>
<li><a href="https://youtube-sure.techidaily.com/24-effortless-guide-to-share-your-videos-as-shorts-on-computers-and-phones/"><u>In 2024, Effortless Guide to Share Your Videos as Shorts on Computers & Phones</u></a></li>
<li><a href="https://games-able.techidaily.com/slowdown-simplicity-discover-idles/"><u>Slowdown Simplicity: Discover Idles</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-comprehensive-guide-to-metaverse-promotion-for-2024/"><u>The Comprehensive Guide to Metaverse Promotion for 2024</u></a></li>
<li><a href="https://some-guidance.techidaily.com/unlocking-sound-capture-on-windows-10-for-2024/"><u>Unlocking Sound Capture on Windows 10 for 2024</u></a></li>
<li><a href="https://tech-recovery.techidaily.com/verizon-5g-unveiled-a-glimpse-at-the-telecommunications-revolution/"><u>Verizon 5G Unveiled: A Glimpse at the Telecommunications Revolution</u></a></li>
<li><a href="https://video-capture.techidaily.com/zooming-into-success-a-complete-guide-to-podcast-audio-capture/"><u>Zooming Into Success A Complete Guide to Podcast Audio Capture</u></a></li>
</ul></div>

