---
title: Mastering WiX Toolset Update Deployment Strategies for Seamless Software Modifications
date: 2024-09-26T14:49:00.031Z
updated: 2024-09-27T20:14:34.936Z
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
<a href="https://review-au.sjv.io/c/5597632/2135315/14409" target="_top" id="2135315">
  <img src="//a.impactradius-go.com/display-ad/14409-2135315" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://review-au.sjv.io/i/5597632/2135315/14409" style="position:absolute;visibility:hidden;" border="0" />
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

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2144282/7443" target="_top" id="2144282">
  <img src="//a.impactradius-go.com/display-ad/7443-2144282" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2144282/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2049383/7443" target="_top" id="2049383">
  <img src="//a.impactradius-go.com/display-ad/7443-2049383" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2049383/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<a href="https://aligracehair.sjv.io/c/5597632/2087248/19272" target="_top" id="2087248">
  <img src="//a.impactradius-go.com/display-ad/19272-2087248" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2087248/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://snapchat-videos.techidaily.com/new-in-2024-social-media-showdown-2021-tiktok-vs-snapchat-whos-winning/"><u>[New] In 2024, Social Media Showdown 2021 TikTok vs Snapchat - Who’s Winning?</u></a></li>
<li><a href="https://screen-recording.techidaily.com/updated-digital-dream-team-best-screen-capture-software-online/"><u>[Updated] Digital Dream Team Best Screen Capture Software Online</u></a></li>
<li><a href="https://youtube-zero.techidaily.com/ed-in-2024-comic-crafting-mastering-7-cheeky-content-strategies/"><u>[Updated] In 2024, Comic Crafting Mastering 7 Cheeky Content Strategies</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/updated-navigating-instagrams-reel-downloads-with-ease-and-versatility/"><u>[Updated] Navigating Instagram's Reel Downloads with Ease and Versatility</u></a></li>
<li><a href="https://vp-tips.techidaily.com/wi-fi2024/"><u>【Wi-Fi無し、通信エリア外でも聞ける】2024新着無料ミュージックアプリ - すぐに使える最高の選択</u></a></li>
<li><a href="https://article-posts.techidaily.com/2024-approved-cheap-sky-expeditions-under-500-drone-highlights/"><u>2024 Approved Cheap Sky Expeditions Under $500 Drone Highlights</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-ultimate-guide-to-iphone-silhouette-photos/"><u>2024 Approved The Ultimate Guide to iPhone Silhouette Photos</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-transform-and-edit-videos-like-a-pro-with-these-iphonepc-tools/"><u>2024 Approved Transform and Edit Videos Like a Pro With These iPhone/PC Tools</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-transform-video-quality-on-tiktok-2-ways/"><u>2024 Approved Transform Video Quality on TikTok (2 Ways)</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-eternal-gallery-of-commons-artworks-online/"><u>In 2024, The Eternal Gallery of Commons Artworks Online</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-pros-guide-to-efficient-win11-use/"><u>In 2024, The Pro's Guide to Efficient Win11 Use</u></a></li>
<li><a href="https://screen-capture.techidaily.com/ps5-elite-gaming-screens-top-5-hdmi-21-ultra-high-res-monitors-for-2024/"><u>PS5 Elite Gaming Screens Top 5 HDMI 2.1 Ultra High-Res Monitors for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-2019-game-changer-in-vegaspro-for-2024/"><u>The 2019 Game-Changer in VegasPro for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-30-pro-windows-10-secrets-revealed-for-2024/"><u>Top 30 Pro Windows 10 Secrets Revealed for 2024</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/updated-noctua-nh-d15-g2-features-enhanced-silence-with-increased-heatpipes-and-modernized-offset-framework/"><u>Updated Noctua NH-D15 G2 Features Enhanced Silence with Increased Heatpipes & Modernized Offset Framework</u></a></li>
</ul></div>

