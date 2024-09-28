---
title: "Step-by-Step Guide: Generating a WiX Installer's KeyPath Property"
date: 2024-09-25T23:44:16.460Z
updated: 2024-09-28T04:41:23.664Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Step-by-Step Guide: Generating a WiX Installer's KeyPath Property"
thumbnail: https://thmb.techidaily.com/07be777ce45c307461ad22ca534398f5c53e5285da087031d4c184f1389088d2.jpg
---

## Step-by-Step Guide: Generating a WiX Installer's KeyPath Property

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

## How to create a WiX KeyPath attribute

Written by [Horatiu Vladasel](https://tools.techidaily.com/advancedinstaller/products/) · October 4th, 2022

One of the main benefits of using Windows Installer to build your software installer is the "self-repair" or "self-healing" capability. This option is particularly useful when keypaths are missing or broken.

How do you trigger the self-repair mechanism?

The most common way to trigger this feature is to launch an advertised shortcut. The way it works is that when this advertised shortcut is launched, Windows Installer checks the keypaths for all the components included within the same feature as the advertised shortcut. If any of them is missing or broken, it prompts the self-repair mechanism.

In this article we will go into how you can set a KeyPath in WiX.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1948905/19272" target="_top" id="1948905">
  <img src="//a.impactradius-go.com/display-ad/19272-1948905" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1948905/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to create a WiX Keypath?

1\. To get started, you must set the **KeyPath attribute** of the Component element to “yes”.

By doing this, the Directory of the Component is used as a keypath.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)If you want to set a File or a Registry value as a keypath for the Component, then you must set the Keypath attribute of the File or Registry element to “yes”.

<!-- affiliate ads begin -->
<a href="https://25home.pxf.io/c/5597632/2148648/16836" target="_top" id="2148648">
  <img src="//a.impactradius-go.com/display-ad/16836-2148648" border="0" alt="https://techidaily.com" width="468" height="60"/>
</a>
<img height="0" width="0" src="https://25home.pxf.io/i/5597632/2148648/16836" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

<Component Id='MyShortcutComponent' Guid='{2D00166E-AAAA-4F24-B94F-3D5E9ED21D65}'>
          		<File Id="Readme" Name="Readme.txt" DiskId="1" Source="Readme.txt"  KeyPath="yes">
			</File>			
		</Component>
		<Component Id='MyRegComponent' Guid='*'>
			<RegistryValue Root="HKCU" Key="Software\MyCompany\MyApp" Type="string" Value="Installed" KeyPath="yes" />
		</Component>

Copy

2\. Now, you must declare the shortcut element and ensure that it has the “Advertise” attribute set to “yes”.

<Shortcut Id="MyApp" Directory="ProgramMenuFolder" Name="MyApp" WorkingDirectory="INSTALLDIR" Advertise="yes" />

Copy

3\. And that’s it. You have fully declared an advertised shortcut which triggers the **self-repair mechanism** when the component keypath is either missing or broken.

The **complete listing for the WiX source file** should look like the one below:

<?xml version="1.0" encoding="UTF-8"?>        
<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
  <Product Id="{2D00166E-A14A-4F24-B94F-3D5E9ED21D65}" Name="MyApp" Language="1033" Version="1.0.0.0" Manufacturer="MyCompany" UpgradeCode="{8F800905-91E8-4234-AD80-A485F156FE1B}">
	<Package InstallerVersion="400" Compressed="yes" InstallScope="perMachine" />
	<Media Id='1' Cabinet='MyAppCAB.cab' EmbedCab='yes' />
	<Directory Id='TARGETDIR' Name='SourceDir'>
	<Directory Id='ProgramMenuFolder'/>
  	<Directory Id='ProgramFilesFolder'>
    	<Directory Id='MyCompany' Name='MyCompany'>
      	<Directory Id='INSTALLDIR' Name='MyApp'>
        	<Component Id='MyShortcutComponent' Guid='*'>
          		<File Id="Readme" Name="Readme.txt" DiskId="1" Source="Readme.txt"  KeyPath="yes">
				 <Shortcut Id="MyApp" Directory="ProgramMenuFolder" Name="MyApp" WorkingDirectory="INSTALLDIR" Advertise="yes" />
			</File>			
		</Component>
		<Component Id='MyRegComponent' Guid='*'>
			<RegistryValue Root="HKCU" Key="Software\MyCompany\MyApp" Type="string" Value="Installed" KeyPath="yes" />
		</Component>
      	</Directory>
    	</Directory>
  	</Directory>
	</Directory>
	<Feature Id='MyFeature' Title='My 1st Feature' Level='1'>
     	<ComponentRef Id='MyShortcutComponent' />
	<ComponentRef Id='MyRegComponent' />
	</Feature>
  </Product>
</Wix>

Copy

At last, you can go and compile the WiX source file and process the resulting WiX object tile to build your MSI package.

<!-- affiliate ads begin -->
<a href="https://bluetties.sjv.io/c/5597632/2141688/17094" target="_top" id="2141688">
  <img src="//a.impactradius-go.com/display-ad/17094-2141688" border="0" alt="https://techidaily.com" width="120" height="90"/>
</a>
<img height="0" width="0" src="https://bluetties.sjv.io/i/5597632/2141688/17094" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to Create a Keypath in Advanced Installer?

When you build and create your Windows Installer MSI package with Advanced Installer, you will see that the process is fairly straightforward and easy to follow.

All you need to do is to ensure that the **“Advertised shortcut” box is checked.**

![Check Advertised Shortcut Box](https://cdn.advancedinstaller.com/img/create-wix-keypath-attribute/check-advertised-shortcut-box.png "Check Advertised Shortcut Box")  

And that’s it! Advanced Installer follows Microsoft's best practices when it organizes your resources in features and components. It automatically sets keypaths for all the components.

If for any reason you need to reorganize your resources or change a keypath, then you can do that from the [Organization page](https://tools.techidaily.com/advancedinstaller/products/).

Do you want to create a WiX Keypath without writing code? Try Advanced Installer’s [free 30-day full featured trial](https://tools.techidaily.com/advancedinstaller/products/) and do it in one-click.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1934138/19272" target="_top" id="1934138">
  <img src="//a.impactradius-go.com/display-ad/19272-1934138" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1934138/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Conclusion

Setting up keypaths for the components within your installer is mandatory if you want to take advantage of the “self-healing” feature.

If you are using Advanced Installer, that can be done very easily, with just a few clicks.

Hope you enjoyed this article! If you have any other questions on WiX, write them in the comments below.

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
<li><a href="https://some-tips.techidaily.com/new-streamline-overload-efficiently-editing-oversized-tiktok-drafts/"><u>[New] Streamline Overload Efficiently Editing Oversized TikTok Drafts</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/new-unleashing-potential-a-deep-dive-into-the-ion-air-pro-3-review/"><u>[New] Unleashing Potential A Deep Dive Into the ION Air Pro 3 Review</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-streamlining-360-degree-video-editing-workflow-in-premiere-pro/"><u>[Updated] Streamlining 360-Degree Video Editing Workflow in Premiere Pro</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-transforming-pedagogy-through-vr-innovation/"><u>[Updated] Transforming Pedagogy Through VR Innovation</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unveiling-the-perfect-gaming-experience-kinemaster-on-android/"><u>2024 Approved Unveiling the Perfect Gaming Experience KineMaster on Android</u></a></li>
<li><a href="https://win-able.techidaily.com/expert-tips-to-solve-football-manager-2021-stuck-loading-screen-and-get-playing-asap/"><u>Expert Tips to Solve Football Manager 2021 Stuck Loading Screen and Get Playing ASAP</u></a></li>
<li><a href="https://tech-savvy.techidaily.com/gpt-vs-bert-dissecting-modern-nlp-giants-distinctions/"><u>GPT vs BERT: Dissecting Modern NLP Giants' Distinctions</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-restore-a-bricked-realme-narzo-n55-back-to-operation-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Restore a Bricked Realme Narzo N55 Back to Operation | Dr.fone</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/in-2024-design-thinking-for-content-creators-crafting-impactful-facebook-reels/"><u>In 2024, Design Thinking for Content Creators Crafting Impactful Facebook Reels</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-strategies-for-swiftly-locating-forgotten-reddit-threads/"><u>In 2024, Strategies for Swiftly Locating Forgotten Reddit Threads</u></a></li>
<li><a href="https://fox-info.techidaily.com/mastering-video-conferencing-a-complete-guide-to-zoom-on-android-for-2024/"><u>Mastering Video Conferencing A Complete Guide to Zoom on Android for 2024</u></a></li>
<li><a href="https://tech-revival.techidaily.com/winxdvd-solution-hub-your-go-to-resource-for-dvd-extraction-and-mobile-media-transfer/"><u>WinXDVD Solution Hub – Your Go-To Resource for DVD Extraction and Mobile Media Transfer</u></a></li>
</ul></div>

