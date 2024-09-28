---
title: "Step-by-Step Guide: Integrating .CAB Files Into Your Windows Installer Packages"
date: 2024-09-27T05:31:58.545Z
updated: 2024-09-28T15:14:57.042Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Step-by-Step Guide: Integrating .CAB Files Into Your Windows Installer Packages"
thumbnail: https://thmb.techidaily.com/3e64ab7fbedf01adf094c0f7a07b62ec8466f937073c7188969d1624a01e5f53.jpg
---

## Step-by-Step Guide: Integrating .CAB Files Into Your Windows Installer Packages

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

## How To Embed CAB Files in MSI

Written by [Alex Marin](https://tools.techidaily.com/advancedinstaller/products/) · June 7th, 2021

One of the most asked questions in the industry is related to CAB files and what embedding options these have within the WiX Toolset. 

Let's see how CAB embedding works within WiX Toolset, what differences are there when using different versions and how you can use Advanced Installer to manage your CAB files in your MSI.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2144284/7443" target="_top" id="2144284">
  <img src="//a.impactradius-go.com/display-ad/7443-2144284" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2144284/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How CAB Embedding Works In WiX Toolset

To control CAB embedding within your Wix Toolset project, you will need to use the following option:

<MediaTemplate EmbedCab="yes"/>

Copy

Just set the EmbedCab value to “yes” or “no” according to your needs - and you're ready to start.

To see how CAB embedding works, let's create a simple MSI with WiX Toolset. 

For this example, we added a single file called “Trace32.exe” in the package.

The code for the WSX file is as follows:

<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
<Product Id="*" UpgradeCode="12345678-1111-2222-3333-666666666666"
 
Name="My First Installer" Version="1.0.0.0" Manufacturer="My Company" Language="1033">
<Package InstallerVersion="200" Compressed="yes" Comments="Hello, this is my first installer"/>
<MediaTemplate EmbedCab="yes" />

 
<Directory Id="TARGETDIR" Name="SourceDir">
<Directory Id="ProgramFilesFolder">
<Directory Id="INSTALLDIR" Name="MyFirstInstaller">
<Component Id="Files" Guid="11111111-2222-3333-4444-555555555555">
<File Id="File1" Source="Trace32.exe"/>
</Component>
</Directory>
</Directory>
</Directory>
 
<Feature Id="Feature1" Level="1" Title="First feature" Description="This is the one and only feature in this installation">
<ComponentRef Id="Files"/>
</Feature>
</Product>
</Wix>

Copy

 Once we have the MSI configured as needed, it's time to build it: 

1\. Create a new batch file in the same folder along with the **example.wsx** file. 

2\. Save it as**make\_msi.bat**.

3\. Inside the batch file, paste the following code:

"C:\Program Files (x86)\WiX Toolset v3.11\bin\candle.exe" example.wxs
"C:\Program Files (x86)\WiX Toolset v3.11\bin\light.exe" example.wixobj
@pause

Copy

When everything is ready, execute the **make\_msi.bat** file - this quick build will result in the **example.msi** that will appear in the folder.

![Execute bat file](https://cdn.advancedinstaller.com/img/wix-child-images/execute-bat-file.gif "Executing the make_msi.bat file")  

After executing the .bat file, the CAB file was embedded inside the MSI. If you don’t want the CAB file to be embedded, change the following line within the example.wsx:

<MediaTemplate EmbedCab="no"/>

Copy

If you change it and run the **make\_msi.bat** again, a CAB archive named “cab1.cab” will be created next to your MSI.

![Create cab file](https://cdn.advancedinstaller.com/img/wix-child-images/create-cab-file.png "Creating CAB file")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2137412/7443" target="_top" id="2137412">
  <img src="//a.impactradius-go.com/display-ad/7443-2137412" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2137412/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2105864/7443" target="_top" id="2105864">
  <img src="//a.impactradius-go.com/display-ad/7443-2105864" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2105864/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### What Are The Differences When Embedding CAB Files In Different WiX Versions?

Before WiX version 3.8, the MediaTemplate element did not exist and CAB files had to be declared independently:

<Media Id="1" Cabinet="cab1.cab" EmbedCab="yes"/>

Copy

This method still works after version 3.8, but if you want to use it, the WSX file should use this code:

<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
<Product Id="*" UpgradeCode="12345678-1111-2222-3333-666666666666"
 
Name="My First Installer" Version="1.0.0.0" Manufacturer="My Company" Language="1033">
<Package InstallerVersion="200" Compressed="yes" Comments="Hello, this is my first installer"/>
<Media Id="1" Cabinet="product.cab" EmbedCab="Yes"/>

Copy

Keep in mind that if you are using a WiX version higher than 3.8, you can't use MediaTemplate and Media elements at the same time. Either you declare a template which will be used across all the CAB files (as seen in the first example), or you declare each CAB manually and define if it’s embedded or not.

### Using Advanced Installer's GUI to Manage CAB Files Within Your MSIs

 Advanced Installer offers multiple options to handle CAB files within your MSI. Watch our tutorial video to see how it works. 

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)If you want to see a comparison between WiX and Advanced Installer, check our article titled [Bundles-WiX vs. Advanced Installer](https://tools.techidaily.com/advancedinstaller/products/), where we discuss the basics of WiX - such as where to get it, how to install it, and how to create a bundle of two MSI applications with it.

I hope you found this information helpful and easy to implement.

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
<a href="https://appsumo.8odi.net/c/5597632/2129738/7443" target="_top" id="2129738">
  <img src="//a.impactradius-go.com/display-ad/7443-2129738" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2129738/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://some-tips.techidaily.com/new-strategy-cradle-nurturing-market-gains/"><u>[New] Strategy Cradle Nurturing Market Gains</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unleashing-potential-the-easy-path-to-blending-linktree-with-tiktok-bios/"><u>[New] Unleashing Potential The Easy Path to Blending Linktree with TikTok Bios</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/updated-elevating-your-craft-top-camera-optics-for-professional-videos/"><u>[Updated] Elevating Your Craft Top Camera Optics for Professional Videos</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-top-20-free-public-domain-pubg-screenshot-slideshows/"><u>[Updated] Top 20 Free Public Domain PUBG Screenshot Slideshows</u></a></li>
<li><a href="https://twitter-videos.techidaily.com/2024-approved-amazonprimes-winning-tweets-of-the-year-2023/"><u>2024 Approved AmazonPrime's Winning Tweets of the Year 2023</u></a></li>
<li><a href="https://fox-links.techidaily.com/2024-approved-flash-and-fly-gaming-top-10-speedy-apps-on-desktopmobile/"><u>2024 Approved Flash & Fly Gaming Top 10 Speedy Apps on Desktop/Mobile</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unveiling-magixs-image-organizer-insights/"><u>2024 Approved Unveiling MAGIX's Image Organizer Insights</u></a></li>
<li><a href="https://fox-that.techidaily.com/cant-get-texts-on-your-iphone-fix-apples-cross-platform-sms-problem-with-ease/"><u>Can't Get Texts on Your iPhone? Fix Apple's Cross-Platform SMS Problem with Ease</u></a></li>
<li><a href="https://tech-haven.techidaily.com/comprehensive-guide-to-superfetch-unlocking-the-full-potential/"><u>Comprehensive Guide to SuperFetch: Unlocking the Full Potential</u></a></li>
<li><a href="https://buynow-tips.techidaily.com/conquer-new-worlds-with-stellaris-the-ultimate-intergalactic-empire-guide/"><u>Conquer New Worlds with Stellaris - The Ultimate Intergalactic Empire Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-mastering-windows-colors-expertise-for-viewing-and-editing-hd-video/"><u>In 2024, Mastering Windows Colors Expertise for Viewing & Editing HD Video</u></a></li>
<li><a href="https://android-location-track.techidaily.com/in-2024-top-9-realme-narzo-n55-monitoring-apps-for-parental-controls-drfone-by-drfone-virtual-android/"><u>In 2024, Top 9 Realme Narzo N55 Monitoring Apps for Parental Controls | Dr.fone</u></a></li>
<li><a href="https://tech-hub.techidaily.com/inside-openais-incentive-system-for-cybersecurity-testing-a-step-by-step-participant-guide/"><u>Inside OpenAI’s Incentive System for Cybersecurity Testing: A Step-by-Step Participant Guide</u></a></li>
<li><a href="https://extra-support.techidaily.com/navigating-through-vlc-features-settings-and-troubleshooting-mac-for-2024/"><u>Navigating Through VLC Features, Settings & Troubleshooting (Mac) for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-potential-with-magix-paint-pro-for-2024/"><u>Unlocking Potential with MAGIX Paint Pro for 2024</u></a></li>
</ul></div>

