---
title: Mastering WiX Toolset Update Deployment Strategies for Seamless Software Modifications
date: 2024-09-29T18:32:34.438Z
updated: 2024-10-03T20:00:59.205Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Mastering WiX Toolset Update Deployment Strategies for Seamless Software Modifications
thumbnail: https://thmb.techidaily.com/d68b2c77d9bc6992a97b4d45a79ba7275bc346cfc58c9a3e57e1e4c2f555ef0b.jpg
---

## Mastering WiX Toolset Update Deployment Strategies for Seamless Software Modifications

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

## How To Implement Updates Using WiX Toolset Installer

Written by [Radu Popescu](https://tools.techidaily.com/advancedinstaller/products/) · June 7th, 2021

In this post, we will address installer updates with a focus on the most common scenarios you may encounter when performing a small, minor, or major upgrade.

First, we will see what is inside your WiX Toolset base application and move on to the different types of updates that you can execute for your WiX installers. 

<!-- affiliate ads begin -->
<a href="https://bluettius.sjv.io/c/5597632/2139116/17108" target="_top" id="2139116">
  <img src="//a.impactradius-go.com/display-ad/17108-2139116" border="0" alt="https://techidaily.com" width="250" height="90"/>
</a>
<img height="0" width="0" src="https://bluettius.sjv.io/i/5597632/2139116/17108" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### What Is Inside Your WiX Toolset Base Application?

To better understand how an application upgrade works, we should first know what its components are and how they interact with each other. 

For the scenarios presented in this article, we are using WiX Toolset version 3.11.2\. Our base sample application contains **an executable file** “CMtrace.exe” and a **text file**“guide.txt” which has the information shown below.

![Text file base application](https://cdn.advancedinstaller.com/img/wix-child-images/text-file-base-application.png "Base application containing a text file")  

 Take note of the **ProductID**,**UpgradeCode**, and **PackageID** in the code below. It will be helpful for future references since they are the ones that are modified through the upgrading process.

Our base application has the following code inside the WiX installer project.

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

### What Are The Main Types of WiX Update Installers?

#### Small Updates

**Small Updates** are used to perform small alterations to one or a few files without changing the product version (major.minor.build) or Product ID GUID.

If you look at our example below, you can observe that the only modification to the package is the text inside the guide.txt file. Since this is a quick fix, you can consider Small Update as a hotfix.

![Text file small update](https://cdn.advancedinstaller.com/img/wix-child-images/text-file-small-update.png "The txt file after the small update")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135402/19272" target="_top" id="2135402">
  <img src="//a.impactradius-go.com/display-ad/19272-2135402" border="0" alt="https://techidaily.com" width="336" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135402/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

In this case, the element changed in the code is: **Package GUID**

<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
<Product Id="A0174BDA-E73A-4238-802E-6C8D5E427668" UpgradeCode="8127636F-6291-4D43-8CC9-AB702A631C3B" 
Name="SampleApp" Version="1.0.0.0" Manufacturer="Caphyon" Language="1033">
<PackageId="487E2D11-D57C-4365-85EF-4DB9330DD3AA" InstallerVersion="200" Compressed="yes" Comments="Test sample app installer"
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

#### Minor Updates

Minor Updates are used to perform minor changes to a package increasing its version.

Since the product remains the same, you don't need to change the **Product GUID**.

The only elements changed in the code are the **Version attribute** and **Package GUID**. 

<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
<Product Id="A0174BDA-E73A-4238-802E-6C8D5E427668" UpgradeCode="8127636F-6291-4D43-8CC9-AB702A631C3B" 
Name="SampleApp" Version="1.1.0.0" Manufacturer="Caphyon" Language="1033">
<PackageId="487E2D11-D57C-4365-85EF-4DB9330DD3AA" InstallerVersion="200" Compressed="yes" Comments="Test sample app installer"/>
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

#### Major Updates

 Major Updates are used to perform crucial changes to a package, upgrading them from the full version to another.

Let’s assume we perform a Major Upgrade to our application which has the main executable CmTrace2.exe and the 1.0.0 version. Once the upgrade is done, and the functionality is added, the application version will also change to 2.0.0.

 The elements changed in the code compared to our base application are **Version attribute**, **Product**, and **Package GUID**.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)As a best practice, the UpgradeCode should also be changed every time you make a Major upgrade to your package.

<!-- affiliate ads begin -->
<span id="1983472">
					<video width="576" height="240" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1983472.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1983472">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1983472.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1983472%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1983472/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
<Product Id="95EF64F6-3CF6-4F3A-9854-CBBE0A7338F5" UpgradeCode="7806A6DF-7FEF-4788-B871-261903DE0381" 
Name="SampleApp" Version="2.0.0.0" Manufacturer="Caphyon" Language="1033">
<PackageId="487E2D11-D57C-4365-85EF-4DB9330DD3AA" InstallerVersion="200" Compressed="yes" Comments="Test sample app installer"/>
<MediaTemplate />
<Directory Id="TARGETDIR" Name="SourceDir">
<Directory Id="ProgramFilesFolder">
<Directory Id="INSTALLDIR" Name="SampleApp">
<Component Id="Files" Guid="11111111-2222-3333-4444-555555555555">
<File Id="File1" Source="CMTrace2.exe"/>
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

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)You can check the types of upgrades and the differences between them in our article on [Updates Deployment](https://tools.techidaily.com/advancedinstaller/products/).

### How to Implement WiX Installer Upgrades - Common Scenarios

Updates are meant to keep track of changes performed to previous versions. No matter what scenario you follow, you should always have the UpgradeCode from the previous version in hand. 

Here are some of the common scenarios we will encounter when implementing WiX installer updates.

#### Detecting and Replacing Files and Versions

In this scenario, we want our new package to**detect** the previous version and **include the additional files** that we added to our new package. 

To do this, we need to add the section below to the code: 

<Upgrade Id='8127636F-6291-4D43-8CC9-AB702A631C3B'>
    <UpgradeVersion OnlyDetect='yes'
        Minimum='1.0.0' IncludeMinimum='yes'
        Maximum='1.0.1' IncludeMaximum='yes' />
</Upgrade>

Copy

**Upgrade Id** should have the value of**UpgradeCode** from our base application (the one mentioned at the beginning of this article). 

**OnlyDetect** must be set to yes. If set to no, it will remove the previous version.

**Minimum** and **maximum** attributes define the version range in which the update will be applied (if found).

#### Detecting and Replacing the Previous Version Completely

Here, we want our package to remove the previous version. Also, the package can be installed as a standalone. This is mostly used for Major Upgrades.

The only change here is the **OnlyDetect** value and the maximum value, since now our version range is different (our new application is now version 2.0).

The code should now look like this:

<Upgrade Id='8127636F-6291-4D43-8CC9-AB702A631C3B'>
    <UpgradeVersion OnlyDetect='no'
        Minimum='1.0.0' IncludeMinimum='yes'
        Maximum='2.0.0' IncludeMaximum='yes' /> 
</Upgrade>

Copy

**More about WiX Toolset**: We have a [dedicated resource page about the WiX Toolset](https://tools.techidaily.com/advancedinstaller/products/), which includes various topics related to your installer, using [custom actions](https://tools.techidaily.com/advancedinstaller/products/) in WiX, and [setting a WiX installer build to the current version](https://tools.techidaily.com/advancedinstaller/products/).

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
<a href="https://aligracehair.sjv.io/c/5597632/1896532/19272" target="_top" id="1896532">
  <img src="//a.impactradius-go.com/display-ad/19272-1896532" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1896532/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://fox-links.techidaily.com/new-essential-audio-interface-guide-for-podcasters-for-2024/"><u>[New] Essential Audio Interface Guide for Podcasters for 2024</u></a></li>
<li><a href="https://facebook-video-footage.techidaily.com/new-in-2024-boost-views-with-your-own-youtube-thumbnail-design/"><u>[New] In 2024, Boost Views with Your Own YouTube Thumbnail Design</u></a></li>
<li><a href="https://screen-capture.techidaily.com/new-in-2024-easy-onboarding-for-webinar-logging-in-microsoft-operating-systems/"><u>[New] In 2024, Easy Onboarding for Webinar Logging in Microsoft Operating Systems</u></a></li>
<li><a href="https://visual-screen-recording.techidaily.com/updated-2024-approved-essential-videography-the-leading-screen-recorder-apps/"><u>[Updated] 2024 Approved Essential Videography The Leading Screen Recorder Apps</u></a></li>
<li><a href="https://youtube-webster.techidaily.com/ed-2024-approved-experience-the-future-of-learning-with-these-channels/"><u>[Updated] 2024 Approved Experience the Future of Learning with These Channels</u></a></li>
<li><a href="https://fox-info.techidaily.com/updated-in-2024-best-cameras-to-capture-slow-motion-videos/"><u>[Updated] In 2024, Best Cameras to Capture Slow Motion Videos</u></a></li>
<li><a href="https://some-tips.techidaily.com/1-protect-your-privacy-why-you-should-avoid-sharing-your-personal-email-with-businesses/"><u>1. Protect Your Privacy: Why You Should Avoid Sharing Your Personal Email with Businesses</u></a></li>
<li><a href="https://location-social.techidaily.com/how-to-hidefake-snapchat-location-on-your-lava-storm-5g-drfone-by-drfone-virtual-android/"><u>How to Hide/Fake Snapchat Location on Your Lava Storm 5G | Dr.fone</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/in-2024-which-pokemon-can-evolve-with-a-moon-stone-for-lava-blaze-2-drfone-by-drfone-virtual-android/"><u>In 2024, Which Pokémon can Evolve with a Moon Stone For Lava Blaze 2? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/samsung-galaxy-z-flip-enhanced-innovation-in-the-next-gen-foldable-phone/"><u>Samsung Galaxy Z Flip: Enhanced Innovation in the Next-Gen Foldable Phone</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-evolution-of-the-google-pixel-lineup-a-look-at-the-pixel-6-pro-after-three-years/"><u>The Evolution of the Google Pixel Lineup: A Look at the Pixel 6 Pro After Three Years</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-secret-behind-my-familys-effortless-coordination-why-we-cant-live-without-cozi/"><u>The Secret Behind My Family's Effortless Coordination: Why We Can't Live Without Cozi</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-ultimate-guide-to-the-oneplus-11-insights-from-a-yearlong-experience-for-pricing-similarity/"><u>The Ultimate Guide to the OnePlus 11 – Insights From a Yearlong Experience (for Pricing Similarity)</u></a></li>
<li><a href="https://some-tips.techidaily.com/this-week-in-digital-discoveries-unveiling-new-windows-laptops-and-exclusive-spotify-secrets/"><u>This Week in Digital Discoveries: Unveiling New Windows Laptops and Exclusive Spotify Secrets</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveiling-the-secrets-behind-the-google-pixel-tablets-impressive-performance/"><u>Unveiling the Secrets Behind the Google Pixel Tablet's Impressive Performance!</u></a></li>
<li><a href="https://vp-tips.techidaily.com/1725285083782-winx-dvd-ripper-for-mac/"><u>WinX DVD Ripper for Mac: 解決方案與答案 - 在線用戶支持</u></a></li>
<li><a href="https://some-tips.techidaily.com/your-weekly-tech-update-unpacking-the-atandt-security-leak-and-exciting-releases-from-samsung/"><u>Your Weekly Tech Update: Unpacking the AT&T Security Leak & Exciting Releases From Samsung</u></a></li>
</ul></div>

