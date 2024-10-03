---
title: "Setting Your WiX Installer's Version Number: Match It with the Latest Build"
date: 2024-10-01T18:24:50.409Z
updated: 2024-10-03T20:04:07.220Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Setting Your WiX Installer's Version Number: Match It with the Latest Build"
thumbnail: https://thmb.techidaily.com/26fc91ea31b084d9024cbf2c3260379dfbc09b55f5ef939a3a4cdd1934973c13.jpeg
---

## Setting Your WiX Installer's Version Number: Match It with the Latest Build

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

## How To Set WiX Installer Version to the Current Build Version

Written by [Radu Popescu](https://tools.techidaily.com/advancedinstaller/products/) · June 7th, 2021

Do you need your installer to keep its current build version? In this article, will go through all the steps you need to set your WiX installer version to the current build version.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2111981/7443" target="_top" id="2111981">
  <img src="//a.impactradius-go.com/display-ad/7443-2111981" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2111981/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Start with Your Base Application

We will use a hypothetical scenario using WiX Toolset version 3.11.2 to help illustrate how to set a WiX installer version to the current build version. 

For this example, the first thing we have to do is create a sample basic application containing **an executable file** called “CMtrace.exe” and a **text file** called “guide.txt” that includes the information shown below.

![Text file](https://cdn.advancedinstaller.com/img/wix-child-images/text-file.png "Text file")  

<!-- affiliate ads begin -->
<a href="https://bluettide.pxf.io/c/5597632/2141683/17092" target="_top" id="2141683">
  <img src="//a.impactradius-go.com/display-ad/17092-2141683" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://bluettide.pxf.io/i/5597632/2141683/17092" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

It is important to look inside the WiX installer project code since it will be the one modified through the updating version process. 

<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
<Product Id="A0174BDA-E73A-4238-802E-6C8D5E427668" UpgradeCode="8127636F-6291-4D43-8CC9-AB702A631C3B" 
Name="SampleApp" Version="1.0.0.0" Manufacturer="Caphyon" Language="1033">
<PackageId="075454EB-3FD5-4FA9-9701-1AA510A1D56F" InstallerVersion="200" Compressed="yes" Comments="Test sample app installer"/>
<MediaTemplate />
<Directory Id="TARGETDIR" Name="SourceDir">
<Directory Id="ProgramFilesFolder">
<Directory Id="INSTALLDIR" Name="SampleApp">
<Component Id="Files" Guid="11111111-2222-3333-4444-555555555555">
<File Id="File1" Source="CMTrace.exe"/>
<File Id="File2" Source="guide.txt"/>
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

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2118306/7443" target="_top" id="2118306">
  <img src="//a.impactradius-go.com/display-ad/7443-2118306" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2118306/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Using Binder Variables to Pass the Product Version of the Current Build Version

If we take a look in our code, we see that the <Product \[...\] Version=”1.0.0.0”> and the version value is hardcoded. What we want to achieve is to update the version of our main executable file to the actual Product Version.

Doing that is pretty simple, we just need to use **Binder Variables**. 

Binder Variables are properties that are not available until the linker is about to generate or bind the final output. The supported binder variables are   _All Versioned Files, Assemblies, Properties, Package Properties, Localization Variables_, and_Custom Binder Variables_. 

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)For an in-depth description of supported binder variables and examples, you can consult this [article](https://wixtoolset.org/docs/v3/overview/light/). 

First, we have to pass the version of our CMTrace.exe file to our Product. For that, we need to take a look at our file declaration section.

<File Id="File1" Source="CMTrace.exe"/> 

Copy

For this example, we are using the **“All Versioned Files” “bind.fileVersion.FileID”** binder variable, where FileID is the value of our CMtrace.exe File Id and is equal to “File1”.

 Now, all we need to do is replace the hard coded version from the <Product \[...\] Version=”1.0.0.0”> section, with the following syntax: 

 <Product [...] Version="!(bind.FileVersion.File1)" 

Copy

This is how our code should look like:

<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
<Product Id="A0174BDA-E73A-4238-802E-6C8D5E427668" UpgradeCode="8127636F-6291-4D43-8CC9-AB702A631C3B" 
Name="SampleApp" Version=”!(bind.FileVersion.File1)” Manufacturer="Caphyon" Language="1033">
<PackageId="075454EB-3FD5-4FA9-9701-1AA510A1D56F" InstallerVersion="200" Compressed="yes" Comments="Test sample app installer"/>
<MediaTemplate />
<Directory Id="TARGETDIR" Name="SourceDir">
<Directory Id="ProgramFilesFolder">
<Directory Id="INSTALLDIR" Name="SampleApp">
<Component Id="Files" Guid="11111111-2222-3333-4444-555555555555">
<File Id="File1" Source="CMTrace.exe"/>
<File Id="File2" Source="guide.txt"/>
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

And, that's it! You can now set the WiX Installer version to the current build version.

For more useful guides and tutorials, make sure to check our[dedicated page to the WiX open-source technology](https://tools.techidaily.com/advancedinstaller/products/), where you can find everything from the basic principles of the WiX Toolset to more advanced tips for developers and IT Pros.

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
<a href="https://bluettius.sjv.io/c/5597632/2139113/17108" target="_top" id="2139113">
  <img src="//a.impactradius-go.com/display-ad/17108-2139113" border="0" alt="https://techidaily.com" width="320" height="90"/>
</a>
<img height="0" width="0" src="https://bluettius.sjv.io/i/5597632/2139113/17108" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://fox-links.techidaily.com/updated-in-2024-content-calendar-for-successful-instagram-filmmaking/"><u>[Updated] In 2024, Content Calendar for Successful Instagram Filmmaking</u></a></li>
<li><a href="https://youtube-web.techidaily.com/ed-in-2024-unveiling-the-leading-10-no-cost-youtube-channels-for-stunning-visuals/"><u>[Updated] In 2024, Unveiling the Leading 10 No-Cost YouTube Channels for Stunning Visuals</u></a></li>
<li><a href="https://fox-helps.techidaily.com/updated-in-search-of-alternatives-to-vlc-media-player-for-2024/"><u>[Updated] In Search of Alternatives to VLC Media Player for 2024</u></a></li>
<li><a href="https://android-location-track.techidaily.com/3-solutions-to-find-your-oppo-a1-5g-current-location-of-a-mobile-number-drfone-by-drfone-virtual-android/"><u>3 Solutions to Find Your Oppo A1 5G Current Location of a Mobile Number | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/comparing-fingerprint-scanners-optical-vs-ultrasonic-technology/"><u>Comparing Fingerprint Scanners: Optical Vs. Ultrasonic Technology</u></a></li>
<li><a href="https://some-tips.techidaily.com/comprehensive-evaluation-is-googles-pixel-8a-series-at-its-final-chapter/"><u>Comprehensive Evaluation: Is Google's Pixel 8A Series at Its Final Chapter?</u></a></li>
<li><a href="https://youtube-videos.techidaily.com/demystifying-creator-studio-a-practical-handbook-for-2024/"><u>Demystifying Creator Studio A Practical Handbook for 2024</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/1722711118624-gather-primary-and-secondary-data/"><u>Gather Primary and Secondary Data:</u></a></li>
<li><a href="https://unlock-android.techidaily.com/how-to-unlock-tecno-camon-20-premier-5g-pattern-lock-if-forgotten-6-ways-by-drfone-android/"><u>How to Unlock Tecno Camon 20 Premier 5G Pattern Lock if Forgotten? 6 Ways</u></a></li>
<li><a href="https://some-tips.techidaily.com/imessage-prompts-understanding-the-reason-behind-contact-check-in-requests-and-easy-fixes/"><u>IMessage Prompts: Understanding the Reason Behind Contact Check-In Requests and Easy Fixes</u></a></li>
<li><a href="https://some-guidance.techidaily.com/in-2024-the-art-of-memes-9-essential-elements-for-gif-perfection/"><u>In 2024, The Art of Memes 9 Essential Elements for GIF Perfection</u></a></li>
<li><a href="https://some-tips.techidaily.com/innovative-possibilities-my-wishlist-for-the-new-ipad-mini-7/"><u>Innovative Possibilities: My Wishlist for the New iPad Mini 7</u></a></li>
<li><a href="https://article-tips.techidaily.com/sensory-engaging-e-commerce-platforms-for-2024/"><u>Sensory Engaging E-Commerce Platforms for 2024</u></a></li>
</ul></div>

