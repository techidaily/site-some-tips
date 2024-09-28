---
title: "1. Create Personalized Extensions with WiX Toolset: Your Step-by-Step Guide"
date: 2024-09-21T17:26:00.020Z
updated: 2024-09-28T10:36:23.049Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes 1. Create Personalized Extensions with WiX Toolset: Your Step-by-Step Guide"
thumbnail: https://thmb.techidaily.com/f86055b0c210c48b3bc87c8b80af070af1138eb8ba02388288320b33c5951f16.jpeg
---

## 1. Create Personalized Extensions with WiX Toolset: Your Step-by-Step Guide

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

## How To Add Custom Actions in WiX Toolset

Written by [Horatiu Vladasel](https://tools.techidaily.com/advancedinstaller/products/) · June 7th, 2021

We have a list of Wix-related articles meant to help developers navigate through the tool in a seamless way. From [implementing upgrades](https://tools.techidaily.com/advancedinstaller/products/) with WiX to[embedding CAB options in MSI](https://tools.techidaily.com/advancedinstaller/products/) \- you can find a lot of helpful materials on our main WiX page.

This article is all about Custom Actions in the Windows Installer XML Toolset (WiX), and by the end of it, you should be able to add any Custom Actions using the tool. Let's go through it together. 

Unlike other packaging tools, Windows Installer XML Toolset (WiX) doesn't have a GUI – it builds the Windows Installer package based on the information defined within the WiX source file (XML based).

When it comes to Custom Actions, there are two elements that are connected to each other, and you will have to keep both of them in mind when defining your XML. These two elements are:

1\. The [Custom Action](https://wixtoolset.org/docs/v3/xsd/wix/customaction/) element – which comes with various attributes that correspond to different [Custom Action types](https://learn.microsoft.com/en-us/windows/win32/msi/summary-list-of-all-custom-action-types).

2\. The Sequences element - which could be any of these: [AdminExecuteSequence](https://wixtoolset.org/docs/v3/xsd/wix/adminexecutesequence/), [AdminUISequence](https://wixtoolset.org/docs/v3/xsd/wix/adminuisequence/), [AdvertiseExecuteSequence](https://wixtoolset.org/docs/v3/xsd/wix/advertiseexecutesequence/), [InstallExecuteSequence](https://wixtoolset.org/docs/v3/xsd/wix/installexecutesequence/) or [InstallUISequence](https://wixtoolset.org/docs/v3/xsd/wix/installuisequence/) and is used to schedule a Custom Action within the corresponding table in the MSI. It also allows setting the condition for determining if a Custom Action gets executed or not.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1938698/19272" target="_top" id="1938698">
  <img src="//a.impactradius-go.com/display-ad/19272-1938698" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1938698/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How To Add a Custom Action to Your Package Using WiX Toolset?

Let’s suppose you want to add two Custom Actions to your MSI package with the following characteristics:

* One Custom Action to create a file at the time the package gets installed.
* Another Custom Action to remove the same file at the time the package gets uninstalled.

In the following example, we will show you how to add a Custom Action to your MSI package using the WiX Toolset. We will also go through the most common conditions used for Custom Actions.

First, we must define our Custom Action element:

<CustomAction Id="CreateFileCA" BinaryKey="CreateFile.vbs" Execute="deferred" VBScriptCall='' Impersonate="no" Return="check"/>
<CustomAction Id="DeleteFileCA" BinaryKey="DeleteFile.vbs" Execute="deferred" VBScriptCall='' Impersonate="no" Return="check"/>

Copy

As you can see, the **BinaryKey** attribute contains a reference to a Binary element. This is because I opted for my Custom Action source code to be stored in the Binary table. The next step in our example is to define the Binary element.

<Binary Id="CreateFile.vbs" SourceFile="CreateFile.vbs"/>
<Binary Id="DeleteFile.vbs" SourceFile="DeleteFile.vbs"/>

Copy

Now that our Custom Action element is defined, we can set the corresponding InstallExecuteSequence element.

<InstallExecuteSequence>
  	<Custom Action='CreateFileCA' Before='InstallFinalize'>NOT Installed</Custom>
  	<Custom Action='DeleteFileCA' Before='CreateFolders'>Installed AND (REMOVE = "ALL" OR AI_INSTALL_MODE = "Remove") AND NOT UPGRADINGPRODUCTCODE</Custom>
</InstallExecuteSequence>

Copy

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)The inner text of a [Custom element](https://wixtoolset.org/docs/v3/xsd/wix/custom/) specifies the condition of the Custom Action.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2037345/7443" target="_top" id="2037345">
  <img src="//a.impactradius-go.com/display-ad/7443-2037345" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2037345/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
        	<Component Id='MyComponent' Guid='{2D00166E-AAAA-4F24-B94F-3D5E9ED21D65}'>
          	<File Id="Readme" Name="Readme.txt" DiskId="1" Source="Readme.txt"/>
        	</Component>
      	</Directory>
    	</Directory>
  	</Directory>
	</Directory>
 
	<Feature Id='MyFeature' Title='My 1st Feature' Level='1'>
     	<ComponentRef Id='MyComponent' />
	</Feature>
 
	<Binary Id="CreateFile.vbs" SourceFile="CreateFile.vbs"/>
	<Binary Id="DeleteFile.vbs" SourceFile="DeleteFile.vbs"/>
 
	<CustomAction Id="CreateFileCA" BinaryKey="CreateFile.vbs" Execute="deferred" VBScriptCall='' Impersonate="no" Return="check"/>
	<CustomAction Id="DeleteFileCA" BinaryKey="DeleteFile.vbs" Execute="deferred" VBScriptCall='' Impersonate="no" Return="check"/>
 
	<InstallExecuteSequence>
  	<Custom Action='CreateFileCA' Before='InstallFinalize'>NOT Installed</Custom>
  	<Custom Action='DeleteFileCA' Before='CreateFolders'>Installed AND (REMOVE = "ALL" OR AI_INSTALL_MODE = "Remove") AND NOT UPGRADINGPRODUCTCODE</Custom>
	</InstallExecuteSequence>
 
  </Product>
 
</Wix>

Copy

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1880940/19272" target="_top" id="1880940">
  <img src="//a.impactradius-go.com/display-ad/19272-1880940" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1880940/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to Set Custom Action Conditions?

Conditions are set depending on your specific needs and can be easily customized to a great extent. They can include references to installer properties, environment variables, installation folders, state/action of a component/feature, etc.

Below, you can find a list of the most common conditions:

* NOT Installed – evaluates to TRUE during the MSI installation only
* NOT Installed OR REINSTALL – evaluates to TRUE during the MSI installation and repair
* REMOVE = "ALL" – evaluates to TRUE during the MSI uninstallation and upgrade
* (REMOVE = "ALL") AND NOT UPGRADINGPRODUCTCODE – evaluates to TRUE during the MSI uninstallation only

### Compile and Build the MSI Package Containing the Custom Actions

After following the previous steps and taking notes of what each condition is and how to add Custom Actions in WiX, we have reached the final step of this process: Building the MSI package.

To do this, we have to: 

1\. Pre-process and compile the WiX source file (.wxs) into an object file (.wixobj) by running the following command:

candle <path to wsx file>

Copy

2\. Process the object file (.wixobj) and build the Windows Installer package (.msi) by running the following command:

light <path to wixobj file> –out <path to msi file>

Copy

![Build msi package](https://cdn.advancedinstaller.com/img/wix-child-images/build-msi-package.png "Build MSI Package")  

And that’s it. Your MSI package is now built.

![Msi package](https://cdn.advancedinstaller.com/img/wix-child-images/msi-package.png "MSI Package")  

<!-- affiliate ads begin -->
<span id="1834903">
					<video width="864" height="1536" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1834903.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/16836-1834903">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1834903.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:540px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2F25home.pxf.io%2Fc%2F5597632%2F1834903%2F16836'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1834903/16836" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How Do Custom Actions Work in Advanced Installer

Now, with your project completely configured you can build your setup package directly from Visual Studio or Azure DevOps.

Windows Installer comes with a lot of Standard Actions which are enough to install and configure the application. However, there are scenarios where developers or IT Pros need to extend the standard capabilities offered by Windows Installer and include Custom Actions.

As you can see, WiX does not have any GUI and is purely based on the information defined within the WiX source file (XML) which can be a bit difficult.

On the other hand, tools like Advanced Installer come with a dedicated GUI for adding a Custom Action which makes the job a lot easier and straightforward. 

If you want to give it a try, you can check it out for free through the [Advanced Installer 30-day full-feature trial](https://tools.techidaily.com/advancedinstaller/products/) and have a look at our [Custom Actions page](https://tools.techidaily.com/advancedinstaller/products/). Additionally, Advanced Installer comes with a list of predefined [Custom Action](https://tools.techidaily.com/advancedinstaller/products/) which you can use.

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
<li><a href="https://desktop-recording.techidaily.com/new-perfected-approaches-to-capturing-remote-training-sessions-for-2024/"><u>[New] Perfected Approaches to Capturing Remote Training Sessions for 2024</u></a></li>
<li><a href="https://extra-skills.techidaily.com/updated-premium-timepieces-for-your-dream-wedding-on-smartphones/"><u>[Updated] Premium Timepieces for Your Dream Wedding on Smartphones</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unlocking-the-potential-of-windows-movie-maker-in-windows-8-environments/"><u>[Updated] Unlocking the Potential of Windows Movie Maker in Windows 8 Environments</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unlocking-the-secrets-of-youtube-video-comments/"><u>[Updated] Unlocking the Secrets of YouTube Video Comments</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-7-ideas-to-improve-the-unboxing-experience/"><u>2024 Approved 7 Ideas to Improve the Unboxing Experience</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-master-iphones-artistic-capabilities-capturing-movement-blur/"><u>2024 Approved Master iPhone's Artistic Capabilities Capturing Movement Blur</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-experts-list-of-top-vector-stock-portals/"><u>2024 Approved The Expert's List of Top Vector Stock Portals</u></a></li>
<li><a href="https://youtube-video-recordings.techidaily.com/breaking-into-livestrances-a-gamers-guide-to-youtube-success/"><u>Breaking Into Livestrances A Gamers' Guide to YouTube Success</u></a></li>
<li><a href="https://vp-tips.techidaily.com/comparacao-detalhada-o-que-diferencia-o-formato-de-video-wmv-do-mp4/"><u>Comparação Detalhada: O Que Diferencia O Formato De Vídeo WMV Do MP4?</u></a></li>
<li><a href="https://twitter-videos.techidaily.com/end-audio-blackout-vocalize-tweet-videos-for-2024/"><u>End Audio Blackout Vocalize Tweet Videos for 2024</u></a></li>
<li><a href="https://android-transfer.techidaily.com/how-to-transfer-photos-from-tecno-spark-20-pro-to-new-android-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>How to Transfer Photos from Tecno Spark 20 Pro to New Android? | Dr.fone</u></a></li>
<li><a href="https://article-posts.techidaily.com/in-2024-cutting-edge-drone-footage-for-movies-and-tv/"><u>In 2024, Cutting-Edge Drone Footage for Movies and TV</u></a></li>
<li><a href="https://location-social.techidaily.com/in-2024-edit-and-send-fake-location-on-telegram-for-your-vivo-y78-5g-in-3-ways-drfone-by-drfone-virtual-android/"><u>In 2024, Edit and Send Fake Location on Telegram For your Vivo Y78 5G in 3 Ways | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-streamline-strategies-softwares-versus-hardware-harmony/"><u>In 2024, Streamline Strategies Softwares Versus Hardware Harmony?</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/is-fake-gps-location-spoofer-a-good-choice-on-honor-100-drfone-by-drfone-virtual-android/"><u>Is Fake GPS Location Spoofer a Good Choice On Honor 100? | Dr.fone</u></a></li>
<li><a href="https://win-howtos.techidaily.com/resolving-the-missing-openal32dll-file-issue-a-comprehensive-guide/"><u>Resolving the Missing openAL32.dll File Issue: A Comprehensive Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/tailoring-visual-quality-choose-aspect-ratios-wisely-for-2024/"><u>Tailoring Visual Quality Choose Aspect Ratios Wisely for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-ultimate-editors-guide-to-top-10-fcp-plug-ins-for-2024/"><u>The Ultimate Editor's Guide to Top 10 FCP Plug-Ins for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-ultimate-guide-to-instagram-stardom-unleash-your-potential-with-9-key-strategies-for-2024/"><u>The Ultimate Guide to Instagram Stardom - Unleash Your Potential with 9 Key Strategies for 2024</u></a></li>
</ul></div>

