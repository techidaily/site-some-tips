---
title: Implementing Significant Enhancements in MSI Packages with the Help of WiX Toolset
date: 2024-09-21T22:04:35.317Z
updated: 2024-09-28T02:07:13.865Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Implementing Significant Enhancements in MSI Packages with the Help of WiX Toolset
thumbnail: https://thmb.techidaily.com/7b420d51a7e917d12325acc7124ce448649fcdb3a71e7a06fbd4b66d64319f0c.jpg
---

## Implementing Significant Enhancements in MSI Packages with the Help of WiX Toolset

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

## How to create major upgrades for MSI packages using WiX Toolset

Deploying major upgrades for an MSI package created with WiX Toolset is simple. However, there are a few boxes you need to check to make sure you're doing it properly. We'll share them with you in this article!

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2130870/7443" target="_top" id="2130870">
  <img src="//a.impactradius-go.com/display-ad/7443-2130870" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2130870/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### What makes major upgrades different from patches?

Unlike patches, major upgrades require a complete reinstallation of the application. When the application is upgraded, the old version is completely removed from the system, and then the new version is installed.

Every major version of an application is treated as a separate application by the OS, and according to Windows Installer standards, its MSI **must have a unique product code**.

### How to implement a major upgrade using WiX Toolset

To implement a major upgrade in WiX Toolset, you need to keep some things in mind.

1\. In the Product element, the **ID** should remain a wildcard. This ensures that the MSI package will generate a different product code each time we build it.

2\. The **UpgradeCode** should remain constant, in order to correctly link the different versions of the package.

Here is an example of a proper Product element:

<Product Id="*" Name="Sample Application" Language="1033" Version="1.0.0.0" Manufacturer="Caphyon" UpgradeCode="ca61b68b-a4ca-452f-9cd7-5ffcd2558b5d">
…………………………
</Product>

Copy

3\. To handle changing any version of the product, you have to add the **MajorUpgrade** element in the Product element, as follows:

<MajorUpgrade AllowSameVersionUpgrades="yes" DowngradeErrorMessage="A newer version of [ProductName] is already installed." />

Copy

This addition ensures that even version 1.0.0.1 is going to be perceived as a major upgrade. Otherwise, you may see multiple side by side installations of your application in Programs and Features.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135402/19272" target="_top" id="2135402">
  <img src="//a.impactradius-go.com/display-ad/19272-2135402" border="0" alt="https://techidaily.com" width="336" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135402/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Using Advanced Installer Approach to Handle Major Upgrades

WiX toolset approach to perform a major upgrade to an MSI package requires adding new code to your XML file.

But, if you want to make this process smoother, Advanced Installer enables you to do that directly from its GUI without writing any code. Here's how you can achieve it:

Before getting started, make sure you have a **backup copy of the project file** before beginning to edit the.AIP project. This is known as the "old.AIP Project." 

1\. Increment the "Version" from the "Product Details" section by going to the "Product Details" page:

![Increment Version](https://cdn.advancedinstaller.com/img/wix-child-images/increment-version.png "Increment Version")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2151872/7443" target="_top" id="2151872">
  <img src="//a.impactradius-go.com/display-ad/7443-2151872" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2151872/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. Customize the new version of your software by making the necessary changes to the Installer Project.

![Important](https://cdn.advancedinstaller.com/svg/common/IconMessageInfo.svg)Keep in mind that the resources of the new version are all of your application's resources, not just those that are modified by this upgrade installation.

3\. Generate a new Product Code by clicking “Generate new”

![Generate New Product Code](https://cdn.advancedinstaller.com/img/wix-child-images/generate-new-product-code.png "Generate New Product Code")  

And you’re done.

Watch the video below to learn how you can complete this task more easily with Advanced Installer:

### Conclusion

As you can see, WiX offers you the capability to handle major upgrades by using the **MajorUpgrade** element within the XML-based definition file. But that is error-prone.

If you need an easier and foolproof solution, then you can use Advanced Installer’s GUI.

Which one do you prefer? Let us know in the comments.

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
<span id="1304648">
					<video width="200" height="200" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1304648.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/15852-1304648">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1304648.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:125px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fthefitville.pxf.io%2Fc%2F5597632%2F1304648%2F15852'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1304648/15852" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://video-capture.techidaily.com/new-5-ultimate-map-quests-for-precious-in-game-finds-for-2024/"><u>[New] 5 Ultimate Map Quests for Precious In-Game Finds for 2024</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/new-iphones-unlocked-smart-tips-for-saving-and-playing-gifs/"><u>[New] IPhones Unlocked Smart Tips for Saving & Playing GIFs</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-ultimate-quick-route-from-srt-to-text-txt-files/"><u>[New] The Ultimate, Quick Route From SRT to Text (TXT) Files</u></a></li>
<li><a href="https://visual-screen-recording.techidaily.com/new-top-10-educator-approved-video-capture-apps-for-2024/"><u>[New] Top 10 Educator-Approved Video Capture Apps for 2024</u></a></li>
<li><a href="https://youtube-lab.techidaily.com/nlock-potential-the-best-hr-vlogs-1-10-for-2024/"><u>[New] Unlock Potential The Best HR Vlogs #1-10 for 2024</u></a></li>
<li><a href="https://facebook-videos.techidaily.com/updated-2024-approved-instantly-access-fb-videos-on-your-apple-entertainment-center/"><u>[Updated] 2024 Approved Instantly Access FB Videos on Your Apple Entertainment Center</u></a></li>
<li><a href="https://vp-tips.techidaily.com/updated-2024-approved-upgrade-your-iphone-cinematic-experience-must-have-equipment/"><u>[Updated] 2024 Approved Upgrade Your iPhone Cinematic Experience Must-Have Equipment</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-artisans-guide-to-backdrop-free-image-perfection-with-photopea/"><u>[Updated] The Artisan's Guide to Backdrop-Free Image Perfection with Photopea</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-ultimate-iphone-strategies-for-flawless-audio-downloads/"><u>[Updated] Ultimate iPhone Strategies for Flawless Audio Downloads</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-rotate-iphone-photos-learn-the-art-of-inversion/"><u>2024 Approved Rotate iPhone Photos Learn the Art of Inversion</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-tomorrows-reflection-varied-solutions/"><u>2024 Approved Tomorrow’s Reflection Varied Solutions</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-utilizing-snapchats-prominent-personalities-highlight/"><u>2024 Approved Utilizing Snapchat's Prominent Personalities Highlight</u></a></li>
<li><a href="https://win-howtos.techidaily.com/1723211734324-how-to-reactivate-disabled-internet-connection-on-your-pc-or-mobile-step-by-step-solution/"><u>How to Reactivate Disabled Internet Connection on Your PC or Mobile - Step by Step Solution</u></a></li>
<li><a href="https://facebook.techidaily.com/master-the-art-of-personal-data-update-on-fb/"><u>Master the Art of Personal Data Update on FB</u></a></li>
<li><a href="https://snapchat-videos.techidaily.com/quick-and-easy-capturing-the-perfect-mac-snapped-footage-for-2024/"><u>Quick & Easy Capturing the Perfect Mac-Snapped Footage for 2024</u></a></li>
</ul></div>

