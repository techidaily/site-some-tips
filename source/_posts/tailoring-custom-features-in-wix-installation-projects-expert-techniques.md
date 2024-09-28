---
title: "Tailoring Custom Features in WiX Installation Projects: Expert Techniques"
date: 2024-09-21T11:14:19.900Z
updated: 2024-09-28T12:07:13.072Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Tailoring Custom Features in WiX Installation Projects: Expert Techniques"
thumbnail: https://thmb.techidaily.com/dbece127b3474bfee03fecc83648c4194241691bdbde80d7fc24eae5256f2a38.jpg
---

## Tailoring Custom Features in WiX Installation Projects: Expert Techniques

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
<a href="https://aligracehair.sjv.io/c/5597632/1896555/19272" target="_top" id="1896555">
  <img src="//a.impactradius-go.com/display-ad/19272-1896555" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1896555/19272" style="position:absolute;visibility:hidden;" border="0" />
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

### How to Set Custom Action Conditions?

Conditions are set depending on your specific needs and can be easily customized to a great extent. They can include references to installer properties, environment variables, installation folders, state/action of a component/feature, etc.

Below, you can find a list of the most common conditions:

* NOT Installed – evaluates to TRUE during the MSI installation only
* NOT Installed OR REINSTALL – evaluates to TRUE during the MSI installation and repair
* REMOVE = "ALL" – evaluates to TRUE during the MSI uninstallation and upgrade
* (REMOVE = "ALL") AND NOT UPGRADINGPRODUCTCODE – evaluates to TRUE during the MSI uninstallation only

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2037474/7443" target="_top" id="2037474">
  <img src="//a.impactradius-go.com/display-ad/7443-2037474" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2037474/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135395/19272" target="_top" id="2135395">
  <img src="//a.impactradius-go.com/display-ad/19272-2135395" border="0" alt="https://techidaily.com" width="125" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135395/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

And that’s it. Your MSI package is now built.

![Msi package](https://cdn.advancedinstaller.com/img/wix-child-images/msi-package.png "MSI Package")  

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

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2087408/7443" target="_top" id="2087408">
  <img src="//a.impactradius-go.com/display-ad/7443-2087408" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2087408/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://some-tips.techidaily.com/new-shaping-tomorrow-celebrating-the-top-6-in-nft-artistry/"><u>[New] Shaping Tomorrow Celebrating the Top 6 in NFT Artistry</u></a></li>
<li><a href="https://youtube-zero.techidaily.com/ed-2024-approved-essential-tactics-for-youtube-success-in-25-ways/"><u>[Updated] 2024 Approved Essential Tactics for YouTube Success in 25 Ways</u></a></li>
<li><a href="https://facebook-record-videos.techidaily.com/updated-learn-to-record-save-and-share-youtube-content-a-cost-free-approach/"><u>[Updated] Learn to Record, Save, & Share YouTube Content A Cost-Free Approach</u></a></li>
<li><a href="https://video-screen-grab.techidaily.com/updated-premium-selection-of-webinar-technologies-for-2024/"><u>[Updated] Premium Selection of Webinar Technologies for 2024</u></a></li>
<li><a href="https://instagram-video-recordings.techidaily.com/updated-quickening-instagram-video-streams-on-mobile-devices/"><u>[Updated] Quickening Instagram Video Streams on Mobile Devices</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-swift-steps-to-personalize-your-in-game-sonic-presence-in-pubg/"><u>[Updated] Swift Steps to Personalize Your In-Game Sonic Presence in PUBG</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-transform-your-footage-with-the-ideal-dimension-proportion/"><u>2024 Approved Transform Your Footage with the Ideal Dimension Proportion</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-transform-your-movie-grading-skills-using-cg-centrals-luts/"><u>2024 Approved Transform Your Movie Grading Skills Using CG Central's Luts</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unleashing-creative-potential-with-pixiz-for-photo-videos/"><u>2024 Approved Unleashing Creative Potential with Pixiz for Photo Videos</u></a></li>
<li><a href="https://win-dash.techidaily.com/download-hp-universal-printer-drivers-on-windows-pcs-easy-guide/"><u>Download HP Universal Printer Drivers on Windows PCs - Easy Guide</u></a></li>
<li><a href="https://howto.techidaily.com/fix-nokia-c210-android-system-webview-crash-2024-issue-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Fix Nokia C210 Android System Webview Crash 2024 Issue | Dr.fone</u></a></li>
<li><a href="https://youtube-data.techidaily.com/24-streaming-success-gamers-software/"><u>In 2024, Streaming Success Gamers' Software</u></a></li>
<li><a href="https://article-tips.techidaily.com/newbies-manual-to-vector-art-grasping-different-kinds-and-software/"><u>Newbie’s Manual to Vector Art Grasping Different Kinds & Software</u></a></li>
<li><a href="https://win-able.techidaily.com/solving-the-issue-mp4-videos-playing-only-sound/"><u>Solving the Issue: MP4 Videos Playing Only Sound</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-balancing-act-managing-your-off-facebook-activity-displays-for-2024/"><u>The Balancing Act Managing Your Off-Facebook Activity Displays for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/united-creatives-brands-meet-youtube-for-2024/"><u>United Creatives Brands Meet YouTube for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-smooth-authentication-on-iphone-x-mending-face-id-for-2024/"><u>Unlocking Smooth Authentication on iPhone X Mending Face ID for 2024</u></a></li>
</ul></div>

