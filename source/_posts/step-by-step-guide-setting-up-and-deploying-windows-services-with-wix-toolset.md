---
title: "Step-by-Step Guide: Setting Up & Deploying Windows Services with WiX Toolset"
date: 2024-09-24T10:34:07.518Z
updated: 2024-09-28T07:45:35.364Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Step-by-Step Guide: Setting Up & Deploying Windows Services with WiX Toolset"
thumbnail: https://thmb.techidaily.com/d0531d40b03cde46602b7231bfc17c15ddbf0815517f86ca0ac7f1e63b79d5ed.jpg
---

## Step-by-Step Guide: Setting Up & Deploying Windows Services with WiX Toolset

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

## How To Add Windows Services with WiX Installer

Written by [Horatiu Vladasel](https://tools.techidaily.com/advancedinstaller/products/) · June 7th, 2021

An important characteristic that we've highlighted in our series of posts about Windows Installer XML Toolset (WiX) is that it doesn't have a GUI. It builds the Windows Installer package with the information defined in the WiX source file (XML based). 

In this article, we will show you how to add a Windows Service to your MSI package using **WIX Installer**. 

### What are the main elements needed to define a Windows Service in XML?

When it comes to defining a Windows Service in your XML, there are two elements that are mandatory and connected to each other:

* [ServiceInstall](https://wixtoolset.org/docs/v3/xsd/wix/serviceinstall/) element – it is used to install a Windows Service.
* [ServiceControl](https://wixtoolset.org/docs/v3/xsd/wix/servicecontrol/) element – it is used to control Windows Service’s behavior once installed.

Apart from these two mandatory elements, you can also use[ServiceConfig](https://wixtoolset.org/docs/v3/xsd/wix/serviceconfig/) to configure a service that already exists, or is being installed by the current package.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)If you are not familiar with Windows Installer technology, we strongly recommend you to have a look at the corresponding MSI tables:[ServiceInstall](https://learn.microsoft.com/en-us/windows/win32/msi/serviceinstall-table), [ServiceControl](https://learn.microsoft.com/en-us/windows/win32/msi/servicecontrol-table), and [MSIServiceConfig](https://learn.microsoft.com/en-us/windows/win32/msi/msiserviceconfig-table).

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2082520/7443" target="_top" id="2082520">
  <img src="//a.impactradius-go.com/display-ad/7443-2082520" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2082520/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to Add a Windows Service to Your MSI?

Now that we know the main elements, we will go through how to add a Windows Service to your MSI. We will also configure the Windows Service created and set it to “Automatic (Delayed Start)”.

This way, you can ensure that the critical Windows Services get all the resources they need at the boot time, whilst the non-critical ones start a little bit later.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2049391/7443" target="_top" id="2049391">
  <img src="//a.impactradius-go.com/display-ad/7443-2049391" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2049391/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Defining the ServiceInstall element

First things first, we must define our**ServiceInstall** element:

<ServiceInstall Id="WindowsServicesSample" Name="WindowsServicesSample" DisplayName="WindowsServicesSample" Description="Example Windows Services" Start="auto" Type="ownProcess" ErrorControl="normal" Account="LocalSystem" Arguments="/ARGUMENTS LIST" Vital="yes" Interactive="no"/>

Copy

The **ServiceInstall** element comes with a set of mandatory attributes that I'm listing below:

* Name – Windows Service name.
* Start – specifies when the Windows Service should be started – allowed values: “autoyes” or “demand”.
* Type – Windows Service’s type – allowed values: “ownProcess” or “shareProcess”.
* ErrorControl – specifies the behavior of the system and what action should be taken if the Windows Service cannot be installed – allowed values: “ignore”, “normal” or “critical”.

Aside from the above, other common attributes include:

* Id – the unique identifier for the Windows Service configuration (if not defined, it will default to Name attribute).
* DisplayName – the localizable name of the Windows Service used by user interface programs to identify the Windows Service.
* Description – the description of the Windows Service.
* Vital – which specifies whether the overall installation of the package should be aborted if the Windows Service fails to install – allowed values: “yes” or “no”.
* Arguments – which specifies any command-line arguments required to run the Windows Service.
* Account – which specifies the account name under which the Windows Service will run.
* Interactive – which specifies whether the Windows Service should interact with the desktop – allowed values: “yes” or “no”.

### Setting the ServiceControl Element

After defining our **ServiceInstall** element, we can set the corresponding **ServiceControl** element.

<ServiceControl Id="WindowsServicesSample" Name="WindowsServicesSample" Start="install" Stop="both" Remove="uninstall" Wait="yes"/>

Copy

Just like ServiceInstall, the **ServiceControl** element comes with a set of mandatory attributes:

* Id – the unique identifier for the Windows Service configuration.
* Name – the Windows Service name.

Other attributes include:

* Start – which specifies whether the Windows Service should be started on install, uninstall or both – allowed values: “install”, “uninstall” or “both”.
* Stop – which specifies whether the Windows Service should be stopped on install, uninstall or both – allowed values: “install”, “uninstall” or “both”.
* Remove – which specifies whether the Windows Service should be removed on install, uninstall or both – allowed values: “install”, “uninstall” or “both”.
* Wait – which specifies whether or not to wait for Service Control Manager to report the Windows Service as complete (in “pending” state) before proceeding (maximum 30 seconds) – allowed values: “yes” or “no”.

<!-- affiliate ads begin -->
<a href="https://coinrule.sjv.io/c/5597632/1958378/18409" target="_top" id="1958378">
  <img src="//a.impactradius-go.com/display-ad/18409-1958378" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://coinrule.sjv.io/i/5597632/1958378/18409" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Determine the ServiceConfig Element

Additionally, we can now go and define the**ServiceConfig** element to configure our Windows Service.

<ServiceConfig ServiceName="WindowsServicesSample" OnInstall="yes" DelayedAutoStart="yes"/>

Copy

The **ServiceConfig** element comes with the following attributes:

* Id – the unique identifier for the Windows Service configuration.
* ServiceName – the Windows Service name.
* OnInstall – which specifies whether to configure the Windows Service on the install of the parent Component – allowed values: “Yes” or “No”.
* OnUninstall – which specifies whether to configure the Windows Service on uninstall of the parent Component – allowed values: “Yes” or “No”.
* OnReinstall – which specifies whether to configure the Windows Service on reinstall of the parent Component – allowed values: “Yes” or “No”.
* DelayedAutoStart – which specifies whether a Windows Service set to “Auto-Start” should delay its start – allowed values: “Yes”/”1” or “No”/”0”.
* FailureActionsWhen – which specifies when failure actions should be applied – allowed value: “failedToStop”/”0” and “failedToStopOrReturnedError”/”1”.
* PreShutdownDelay – which specifies the time that the Service Control Manager waits after reporting a system shutdown.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)**ServiceConfig** is only available starting with Windows Installer 5.0.

The complete listing for the WiX source file is as follows:

<?xml version="1.0" encoding="UTF-8"?>
<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
  <Product Id="{2D00166E-A14A-4F24-B94F-3D5E9ED21D65}" Name="MyApp" Language="1033" Version="1.0.0.0" Manufacturer="MyCompany" UpgradeCode="{8F800905-91E8-4234-AD80-A485F156FE1B}">
	<Package InstallerVersion="400" Compressed="yes" InstallScope="perMachine" />
	
	<Media Id='1' Cabinet='MyAppCAB.cab' EmbedCab='yes' />
 
	<Directory Id='TARGETDIR' Name='SourceDir'>
  	<Directory Id='ProgramFilesFolder'>
    	<Directory Id='MyCompany' Name='MyCompany'>
      	<Directory Id='INSTALLDIR' Name='MyApp'>
        	<Component Id='ReadmeComponent' Guid='{2D00166E-AAAA-4F24-B94F-3D5E9ED21D65}'>
          	<File Id="Readme" Name="Readme.txt" DiskId="1" Source="Readme.txt"/>
        	</Component>
        	<Component Id='WindowsServicesComponent' Guid='{3D00166E-AAAA-4F24-B94F-3D5E9ED21D66}'>
          	<File Id="WindowsServicesSample.exe" Name="WindowsServicesSample.exe" DiskId="1" Source="WindowsServicesSample.exe"/>
          	<ServiceInstall Id="WindowsServicesSample" Name="WindowsServicesSample" DisplayName="WindowsServicesSample" Description="Example Windows Services" Start="auto" Type="ownProcess" ErrorControl="normal" Account="LocalSystem" Arguments="/ARGUMENTS LIST" Vital="yes" Interactive="no"/>
          	<ServiceControl Id="WindowsServicesSample" Name="WindowsServicesSample" Start="install" Stop="both" Remove="uninstall" Wait="yes"/>
          	<ServiceConfig ServiceName="WindowsServicesSample" OnInstall="yes" DelayedAutoStart="yes"/>
         	</Component>
      	</Directory>
    	</Directory>
  	</Directory>
	</Directory>
 
	<Feature Id='MyFeature' Title='My 1st Feature' Level='1'>
     	<ComponentRef Id='ReadmeComponent' />
     	<ComponentRef Id='WindowsServicesComponent' />
	</Feature>
 
  </Product>
</Wix>

Copy

### Compiling and building the MSI

Once we've reached this step, all you need to do is:

Pre-process and compile the WiX source file (.wxs) into an object file (.wixobj) by running the following command:

candle <path to wsx file>

Copy

Process the object file (.wixobj) and build the Windows Installer package (.msi) by running the following command:

light <path to wixobj file> –out <path to msi file>

Copy

![Building msi package](https://cdn.advancedinstaller.com/img/wix-child-images/building-msi-package.png "Building MSI Package")  

And that’s it. Your MSI package is now built.

![Msi application](https://cdn.advancedinstaller.com/img/wix-child-images/msi-application.png "MSI App")  

If you install the newly created MSI package, your Windows Service should appear in the Service Control Manager and have the following details.

![Windows service details](https://cdn.advancedinstaller.com/img/wix-child-images/windows-service-details.png "Windows Services Details")  

<!-- affiliate ads begin -->
<span id="1374820">
					<video width="200" height="200" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1374820.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/15852-1374820">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1374820.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:125px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fthefitville.pxf.io%2Fc%2F5597632%2F1374820%2F15852'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1374820/15852" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

As shown in the image above, I was able to set my WindowsServiceSample service to “Automatic (Delayed Start) “using the ServiceConfig element in WiX.

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2137209/26400" target="_top" id="2137209">
  <img src="//a.impactradius-go.com/display-ad/26400-2137209" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2137209/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Windows Services in Advanced Installer

As you can see, the creation and configuration of a Windows Service using WiX are done via three elements () specifically designed for this purpose. Each element comes with its own attributes which could be a bit difficult to define, especially for those who are not that familiar with the WiX source file (XML) format.

Compared to WiX, Advanced Installer has its own dedicated GUI which you can use to create and configure a Windows Service. It is self-explanatory and it mainly consists in selecting the required configuration from a drop-down list, for each of the attributes of the 3 elements.

For more details, you could check our [Services Page](https://tools.techidaily.com/advancedinstaller/products/).

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
<li><a href="https://vp-tips.techidaily.com/new-2024-approved-tailor-topical-laughs/"><u>[New] 2024 Approved Tailor Topical Laughs</u></a></li>
<li><a href="https://remote-screen-capture.techidaily.com/new-in-2024-free-tools-make-screencapture-a-breeze-for-tv-lovers/"><u>[New] In 2024, Free Tools Make ScreenCapture a Breeze for TV Lovers</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-transform-your-youtube-views-with-smart-zoom-practices/"><u>[New] Transform Your YouTube Views with Smart Zoom Practices</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/updated-2024-approved-uncomplicated-steps-to-record-instagrams-story-feed/"><u>[Updated] 2024 Approved Uncomplicated Steps to Record Instagram's Story Feed</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-streaming-royalty-ranking-the-top-10-platforms-for-real-time-content/"><u>[Updated] Streaming Royalty Ranking the Top 10 Platforms for Real-Time Content</u></a></li>
<li><a href="https://facebook-record-videos.techidaily.com/updated-visionary-voices-triumph-online/"><u>[Updated] Visionary Voices Triumph Online</u></a></li>
<li><a href="https://screen-video-capture.techidaily.com/2024-approved-freezing-gameplay-essential-pc-screen-snaps/"><u>2024 Approved Freezing Gameplay Essential PC Screen Snaps</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unleash-creativity-with-a-diy-guide-to-haul-edits/"><u>2024 Approved Unleash Creativity with a DIY Guide to Haul Edits</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unlock-creative-expression-master-device-based-filters-and-effects/"><u>2024 Approved Unlock Creative Expression Master Device-Based Filters and Effects</u></a></li>
<li><a href="https://location-social.techidaily.com/in-2024-how-to-fake-snapchat-location-without-jailbreak-on-vivo-s17e-drfone-by-drfone-virtual-android/"><u>In 2024, How to Fake Snapchat Location without Jailbreak On Vivo S17e | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-route-to-richer-tiktok-bios-including-linktree-links/"><u>In 2024, The Route to Richer TikTok Bios Including Linktree Links</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unlock-the-best-live-stream-options-today/"><u>In 2024, Unlock the Best Live Stream Options Today</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/in-2024-what-to-do-if-your-apple-iphone-15-pro-max-has-bad-esn-or-blacklisted-imei-by-drfone-ios/"><u>In 2024, What to do if your Apple iPhone 15 Pro Max has bad ESN or blacklisted IMEI?</u></a></li>
<li><a href="https://win-answers.techidaily.com/overcoming-nvidia-gaming-overlay-problems-expert-strategies-for-a-smooth-experience/"><u>Overcoming NVIDIA Gaming Overlay Problems: Expert Strategies for a Smooth Experience</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/the-curious-case-of-instavideos-turned-sideways/"><u>The Curious Case of InstaVideos Turned Sideways</u></a></li>
</ul></div>

