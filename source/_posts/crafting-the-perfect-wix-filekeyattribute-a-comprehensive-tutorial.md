---
title: Crafting the Perfect WiX FileKeyAttribute – A Comprehensive Tutorial
date: 2024-09-25T14:24:53.077Z
updated: 2024-09-27T16:58:57.206Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Crafting the Perfect WiX FileKeyAttribute – A Comprehensive Tutorial
thumbnail: https://thmb.techidaily.com/e5cf76fbd383eaf326a40e9f47ba567bbfc7a691177fb2bbb8430f5442ba8e06.jpg
---

## Crafting the Perfect WiX FileKeyAttribute – A Comprehensive Tutorial

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

### How to create a WiX Keypath?

1\. To get started, you must set the **KeyPath attribute** of the Component element to “yes”.

By doing this, the Directory of the Component is used as a keypath.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)If you want to set a File or a Registry value as a keypath for the Component, then you must set the Keypath attribute of the File or Registry element to “yes”.

<!-- affiliate ads begin -->
<a href="https://laganoo.pxf.io/c/5597632/1528681/16446" target="_top" id="1528681">
  <img src="//a.impactradius-go.com/display-ad/16446-1528681" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://laganoo.pxf.io/i/5597632/1528681/16446" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://appsumo.8odi.net/c/5597632/2105882/7443" target="_top" id="2105882">
  <img src="//a.impactradius-go.com/display-ad/7443-2105882" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2105882/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to Create a Keypath in Advanced Installer?

When you build and create your Windows Installer MSI package with Advanced Installer, you will see that the process is fairly straightforward and easy to follow.

All you need to do is to ensure that the **“Advertised shortcut” box is checked.**

![Check Advertised Shortcut Box](https://cdn.advancedinstaller.com/img/create-wix-keypath-attribute/check-advertised-shortcut-box.png "Check Advertised Shortcut Box")  

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2137229/26400" target="_top" id="2137229">
  <img src="//a.impactradius-go.com/display-ad/26400-2137229" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2137229/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

And that’s it! Advanced Installer follows Microsoft's best practices when it organizes your resources in features and components. It automatically sets keypaths for all the components.

If for any reason you need to reorganize your resources or change a keypath, then you can do that from the [Organization page](https://tools.techidaily.com/advancedinstaller/products/).

Do you want to create a WiX Keypath without writing code? Try Advanced Installer’s [free 30-day full featured trial](https://tools.techidaily.com/advancedinstaller/products/) and do it in one-click.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2043594/7443" target="_top" id="2043594">
  <img src="//a.impactradius-go.com/display-ad/7443-2043594" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2043594/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://video-screen-grab.techidaily.com/updated-cutting-edge-strategies-for-efficient-speech-translation-with-google/"><u>[Updated] Cutting Edge Strategies for Efficient Speech Translation with Google</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-understanding-film-a-beginners-guide-to-essential-shots/"><u>[Updated] Understanding Film A Beginner's Guide to Essential Shots</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-streamlining-virtual-meetings-in-google-mail/"><u>2024 Approved Streamlining Virtual Meetings in Google Mail</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-top-video-editors-aiding-in-app-dev-creation/"><u>2024 Approved Top Video Editors Aiding in App Dev Creation</u></a></li>
<li><a href="https://pokemon-go-android.techidaily.com/best-pokemons-for-pvp-matches-in-pokemon-go-for-honor-magic-6-drfone-by-drfone-virtual-android/"><u>Best Pokemons for PVP Matches in Pokemon Go For Honor Magic 6 | Dr.fone</u></a></li>
<li><a href="https://techidaily.com/how-do-i-reset-my-tecno-spark-20c-phone-without-technical-knowledge-drfone-by-drfone-reset-android-reset-android/"><u>How do I reset my Tecno Spark 20C Phone without technical knowledge? | Dr.fone</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/in-2024-revolutionize-your-harvest-stardews-top-7-upgrades/"><u>In 2024, Revolutionize Your Harvest Stardew's Top 7 Upgrades</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-ultimate-audio-and-video-showcase-excellent-webcams-for-podcasts/"><u>In 2024, Ultimate Audio & Video Showcase Excellent Webcams for Podcasts</u></a></li>
<li><a href="https://vp-tips.techidaily.com/quality-cameras-on-a-shoestring-budget/"><u>Quality Cameras on a Shoestring Budget</u></a></li>
<li><a href="https://win-blog.techidaily.com/resolved-how-to-fix-concurrent-accidents-in-your-computer-system/"><u>Resolved: How to Fix Concurrent Accidents in Your Computer System</u></a></li>
<li><a href="https://youtube-sure.techidaily.com/k-the-potential-of-your-video-platform-growth-for-2024/"><u>Unlock the Potential of Your Video Platform Growth for 2024</u></a></li>
</ul></div>

