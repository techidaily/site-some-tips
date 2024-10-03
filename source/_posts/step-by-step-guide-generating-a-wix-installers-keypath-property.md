---
title: "Step-by-Step Guide: Generating a WiX Installer's KeyPath Property"
date: 2024-09-27T18:05:58.018Z
updated: 2024-10-03T18:08:38.640Z
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
<a href="https://unicoeye.pxf.io/c/5597632/2148771/18498" target="_top" id="2148771">
  <img src="//a.impactradius-go.com/display-ad/18498-2148771" border="0" alt="https://techidaily.com" width="350" height="90"/>
</a>
<img height="0" width="0" src="https://unicoeye.pxf.io/i/5597632/2148771/18498" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to create a WiX Keypath?

1\. To get started, you must set the **KeyPath attribute** of the Component element to “yes”.

By doing this, the Directory of the Component is used as a keypath.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)If you want to set a File or a Registry value as a keypath for the Component, then you must set the Keypath attribute of the File or Registry element to “yes”.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2082533/7443" target="_top" id="2082533">
  <img src="//a.impactradius-go.com/display-ad/7443-2082533" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2082533/7443" style="position:absolute;visibility:hidden;" border="0" />
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

### How to Create a Keypath in Advanced Installer?

When you build and create your Windows Installer MSI package with Advanced Installer, you will see that the process is fairly straightforward and easy to follow.

All you need to do is to ensure that the **“Advertised shortcut” box is checked.**

![Check Advertised Shortcut Box](https://cdn.advancedinstaller.com/img/create-wix-keypath-attribute/check-advertised-shortcut-box.png "Check Advertised Shortcut Box")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2087262/19272" target="_top" id="2087262">
  <img src="//a.impactradius-go.com/display-ad/19272-2087262" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2087262/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

And that’s it! Advanced Installer follows Microsoft's best practices when it organizes your resources in features and components. It automatically sets keypaths for all the components.

If for any reason you need to reorganize your resources or change a keypath, then you can do that from the [Organization page](https://tools.techidaily.com/advancedinstaller/products/).

Do you want to create a WiX Keypath without writing code? Try Advanced Installer’s [free 30-day full featured trial](https://tools.techidaily.com/advancedinstaller/products/) and do it in one-click.

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2137227/26400" target="_top" id="2137227">
  <img src="//a.impactradius-go.com/display-ad/26400-2137227" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2137227/26400" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://screen-video-capture.techidaily.com/new-document-your-days-with-xiaomis-state-of-the-art-screenshot-tool/"><u>[New] Document Your Days with Xiaomi's State-of-the-Art Screenshot Tool</u></a></li>
<li><a href="https://youtube-data.techidaily.com/n-2024-navigating-the-nuances-of-mukbang-filmmaking-techniques/"><u>[New] In 2024, Navigating the Nuances of Mukbang Filmmaking Techniques</u></a></li>
<li><a href="https://extra-support.techidaily.com/new-rise-to-the-top-livestreaming-on-youtube-no-matter-how-low-followers-are/"><u>[New] Rise to the Top - Livestreaming on YouTube, No Matter How Low Followers Are</u></a></li>
<li><a href="https://fox-direct.techidaily.com/updated-2024-approved-virtual-frontiers-current-trends-in-vr-tech/"><u>[Updated] 2024 Approved Virtual Frontiers Current Trends in VR Tech</u></a></li>
<li><a href="https://visual-screen-recording.techidaily.com/updated-from-live-to-legacy-preserving-facebook-events-for-2024/"><u>[Updated] From Live to Legacy Preserving Facebook Events for 2024</u></a></li>
<li><a href="https://youtube-blog.techidaily.com/ed-the-path-to-profitable-videography-starting-strong-for-2024/"><u>[Updated] The Path to Profitable Videography Starting Strong for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/best-video-transcoding-tools-for-ubuntu-users-top-8-picks/"><u>Best Video Transcoding Tools for Ubuntu Users: Top 8 Picks</u></a></li>
<li><a href="https://some-tips.techidaily.com/convert-avi-files-to-m4a-format-for-free-with-movavis-online-software/"><u>Convert AVI Files to M4A Format for Free with Movavi's Online Software</u></a></li>
<li><a href="https://some-tips.techidaily.com/descargar-convertidor-online-libre-para-cambiar-de-gif-a-png/"><u>Descargar Convertidor Online Libre Para Cambiar De GIF a PNG</u></a></li>
<li><a href="https://some-tips.techidaily.com/gratuissimo-convertidor-ogg-e-ape-em-linha-pelo-movavi/"><u>Gratuíssimo Convertidor OGG E APE Em Linha Pelo Movavi</u></a></li>
<li><a href="https://some-tips.techidaily.com/movavis-no-cost-media-transformation-easily-convert-m4ampeg-to-m4v-formats/"><u>Movavi's No-Cost Media Transformation: Easily Convert M4A/MPEG to M4V Formats</u></a></li>
<li><a href="https://some-tips.techidaily.com/movavis-web-based-free-service-for-changing-m4v-video-format-to-movie-mov/"><u>Movavi's Web-Based, Free Service for Changing M4V Video Format to Movie (MOV)</u></a></li>
<li><a href="https://data-wizards.techidaily.com/purchase-immediate-sky-high-video-fix/"><u>Purchase Immediate: Sky-High Video Fix</u></a></li>
<li><a href="https://tech-recovery.techidaily.com/ultimate-troubleshooting-tips-to-fix-stop-code-0x0000007b-and-end-those-bsod-issues/"><u>Ultimate Troubleshooting Tips to Fix STOP Code 0X0000007B and End Those BSOD Issues</u></a></li>
<li><a href="https://ai-video-tools.techidaily.com/updated-2024-approved-mp4-file-editor-for-pc-quickly-trim-cut-and-merge-videos/"><u>Updated 2024 Approved MP4 File Editor for PC Quickly Trim, Cut, and Merge Videos</u></a></li>
<li><a href="https://some-tips.techidaily.com/virtueel-verwerpen-van-arw-naar-png-gratuite-online-convertitie-processen-met-movavi/"><u>Virtueel Verwerpen Van ARW Naar PNG: Gratuite Online-Convertitie-Processen Met Movavi</u></a></li>
<li><a href="https://some-tips.techidaily.com/vob-mjpeg-online-movavi/"><u>VOB를 무료로 MJPEG로 바꾸는 Online 도구 - Movavi</u></a></li>
</ul></div>

