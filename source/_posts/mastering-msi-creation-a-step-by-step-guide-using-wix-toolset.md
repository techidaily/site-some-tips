---
title: "Mastering MSI Creation: A Step-by-Step Guide Using WiX Toolset"
date: 2024-09-27T01:21:11.976Z
updated: 2024-09-28T09:22:18.474Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Mastering MSI Creation: A Step-by-Step Guide Using WiX Toolset"
thumbnail: https://thmb.techidaily.com/d6abae0f7e3d8fb5f7c3d204845ee10283f20e49e0d3d6312bf5d54b51961985.jpg
---

## Mastering MSI Creation: A Step-by-Step Guide Using WiX Toolset

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

## How to create an MSI installer with WiX

Written by [Renato Ivanescu](https://tools.techidaily.com/advancedinstaller/products/) · June 20th, 2023

The **MSI format** is a widely recognized standard in the software industry for distributing software packages to Windows-based devices. MSI packages offer numerous advantages over alternative software installation methods, including enhanced reliability and improved performance. 

**WiX** is an open-source toolset to build MSI packages. It enables developers to create a software installation by writing XML that describes components, registry entries, and other resources.

In this article, I’ll show you **how to use WiX to create an MSI installer** for a Windows Forms application. Let’s dive in!

### Add the setup project to your application

Once you have created the Windows Forms application, the next step is to add the setup package to it.

1. _Right-click on the project solution_ → _Add_ → _New project._
2. From the project list, choose _Setup Project for WiX_. You will find this template only if you have the _Wix Toolset Visual Studio Extension_ installed. Need help installing it? We've got you – check out [this](https://tools.techidaily.com/advancedinstaller/products/) tutorial.

![Setup Project for WiX](https://cdn.advancedinstaller.com/img/create-msi-installer-with-wix/setup-project-for-wix.png "Setup Project for WiX")  

After creating the setup project, you should see it in _Solution Explore_r. The _Product.wxs_ file is the one containing the setup project logic.

![Solution Explorer - Product.wxs](https://cdn.advancedinstaller.com/img/create-msi-installer-with-wix/solution-explorer-product-wxs.png "Solution Explorer - Product.wxs")  

### Add project output to your setup project

Next, we need to include the deployable files in the setup project. To achieve this, we can use the Wix Setup Editor.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)**Wix Setup Editor** is an interactive GUI used to manage the setup files. It is available only if you have the Wax extension installed. If you want to see how to add the extension, you can also read [this](https://tools.techidaily.com/advancedinstaller/products/) article. 

To open the editor, go to _Tools_ → _WiX Setup Editor_. Here we have to make some configurations:

* Select the setup project in the ‘_Setup project to edit’_ section. In our case, it is _AppSetup_.
* For the ‘_Root directory’_, select _INSTALLFOLDER_.
* In the ‘_Projects to install_ section’, select your Window Forms application. We selected _MyApp,_ as this is our application.

![Wix Setup Editor](https://cdn.advancedinstaller.com/img/create-msi-installer-with-wix/wix-setup-editor.png "Wix Setup Editor")  

<!-- affiliate ads begin -->
<span id="1982456">
					<video width="576" height="240" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1982456.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1982456">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1982456.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1982456%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1982456/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

Make sure the files have the _resolved_ state like in the image above. If they have the _unmapped_ state as shown below, update it to _resolved_ by pressing the ‘+’ button under the warning sign.

![Add project output to your setup project](https://cdn.advancedinstaller.com/img/create-msi-installer-with-wix/add-project-output-to-your-setup-project.png "Add project output to your setup project")  

### How to edit product details

To modify the product details, navigate to the _Product.wxs_ file and make the necessary edits to the relevant fields. For example, we set the version to 1.2 and the manufacturer to Caphyon.

<Product Id="*" Name="My Application" Language="1033" Version="1.2" Manufacturer="Caphyon" UpgradeCode="be6d0f2f-6e81-4b75-a499-b5084d0e9a8f">
		<Package InstallerVersion="200" Compressed="yes" InstallScope="perMachine" />
		<MajorUpgrade DowngradeErrorMessage="A newer version of [ProductName] is already installed." />
		<MediaTemplate />
		<Feature Id="ProductFeature" Title="My Application" Level="1">
			<ComponentGroupRef Id="ProductComponents" />
		</Feature>
</Product>

Copy

<!-- affiliate ads begin -->
<a href="https://25home.pxf.io/c/5597632/2148646/16836" target="_top" id="2148646">
  <img src="//a.impactradius-go.com/display-ad/16836-2148646" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://25home.pxf.io/i/5597632/2148646/16836" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to create Shortcuts for your application?

In order to create a shortcut, we will need to make edits to the XML file since the Wix Setup Editor does not provide direct shortcut creation functionality.

Follow the next steps to add a shortcut on the Desktop and one in the Programs Menu:

1\. Define the directory structures.

<Directory Id="TARGETDIR" Name="SourceDir">
			<Directory Id="ProgramFilesFolder">
				<Directory Id="INSTALLFOLDER" Name="My Application" />
			</Directory>
			<Directory Id="ProgramMenuFolder">
				<Directory Id="MyAppFolder" Name="My Application"/>
			</Directory>
			<Directory Id="DesktopFolder" Name="Desktop" />
</Directory>

Copy

2\. Add the shortcuts to the installer package.

<DirectoryRef Id="MyAppFolder">
	<Component Id="ApplicationShortcut" Guid="e75a5c28-29d6-4d65-a5da-04363a176440">
		<Shortcut Id="ApplicationStartMenuShortcut"
						  Name="MyApp"
						  Description="MyApp"
						  Target="[INSTALLFOLDER]MyApp.exe"
						  WorkingDirectory="INSTALLFOLDER"/>
		<RemoveFolder Id="CleanUpShortCut" Directory="MyAppFolder" On="uninstall"/>
		<RegistryValue Root="HKCU" Key="Software\MyCompany\MyApp" Name="installed" Type="integer" Value="1" KeyPath="yes"/>
			</Component>
</DirectoryRef>
<DirectoryRef Id="DesktopFolder">
		<Component Id="ApplicationShortcutDesktop" Guid="cde1e030-eb64-49a5-b7b8-400b379c2d1a">
		<Shortcut Id="ApplicationDesktopShortcut" 
						  Name="MyApp" 
						  Description="MyApp" 
						  Target="[INSTALLFOLDER]MyApp.exe"
						  WorkingDirectory="INSTALLFOLDER" />
		<RegistryValue Root="HKCU" Key="Software\MyCompany\MyApp" Name="installed" Type="integer" Value="1" KeyPath="yes" />
		</Component>
</DirectoryRef>

Copy

3\. Tell Windows to install the shortcuts.

<Product Id="*" ….>
		<Feature Id="ProductFeature" Title="My Application" Level="1">
			….
			<ComponentRef Id="ApplicationShortcut" />
			<ComponentRef Id="ApplicationShortcutDesktop" />
		</Feature>
	</Product>

Copy

### How to add installation dialogues?

By default, when you create an installer package using WiX, it does not include a user interface (UI). However, if you wish to incorporate a minimal UI, you can follow the steps outlined below:

1\. _Right-click in the setup project_ → _Add_ → _Reference_s. In the _Add Reference_ dialog, look in the bin folder of the Wix toolset and add WinUiExtension.dll.

![add installation dialogues](https://cdn.advancedinstaller.com/img/create-msi-installer-with-wix/add-installation-dialogues.png "add installation dialogues")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1918684/19272" target="_top" id="1918684">
  <img src="//a.impactradius-go.com/display-ad/19272-1918684" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1918684/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. Go to the _Product.wsx_ file and add the next line inside the <_Product>_ element to reference the UI: 

<UIRef Id="WixUI_Minimal" />

Copy

### How to install your application?

Now, you can build the setup project. 

1. Go to the _bin_ folder inside the setup project folder to find the MSI file.
2. Run the file and install the application.
3. After the installation, you should find the shortcuts on the _Program Menu_ and _Desktop_.

![install your application](https://cdn.advancedinstaller.com/img/create-msi-installer-with-wix/install-your-application.png "install your application")  

<!-- affiliate ads begin -->
<a href="https://wigfever.sjv.io/c/5597632/2005196/22899" target="_top" id="2005196">
  <img src="//a.impactradius-go.com/display-ad/22899-2005196" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://wigfever.sjv.io/i/5597632/2005196/22899" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Conclusion

WiX toolset is a flexible tool for creating installer packages but when it comes to more complex packaging scenarios, it may require additional time and effort. The WiX Setup Editor offers limited functionalities, and you will often need to manually edit the XML file to configure most settings.

Alternatively, you can explore a GUI-based tool like Advanced Installer to create and manage installation packages. It has a user-friendly interface and is much easier to use. It provides a range of pre-built templates which simplify the process of creating MSIs. 

You can watch the tutorial below to see how easy it is to create an MSI with Advanced Installer.

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
<a href="https://aligracehair.sjv.io/c/5597632/1896541/19272" target="_top" id="1896541">
  <img src="//a.impactradius-go.com/display-ad/19272-1896541" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1896541/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://instagram-videos.techidaily.com/new-in-2024-the-art-of-affiliate-marketing-in-the-instagram-era/"><u>[New] In 2024, The Art of Affiliate Marketing in the Instagram Era</u></a></li>
<li><a href="https://visual-screen-recording.techidaily.com/new-prime-choices-for-valheims-agricultural-success/"><u>[New] Prime Choices for Valheim's Agricultural Success</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-quintessential-quest-for-quality-storytellers-top-8-institutions/"><u>[New] The Quintessential Quest for Quality Storytellers – Top 8 Institutions</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-ultimate-guide-top-7-superior-wet-proof-camcorders/"><u>[New] Ultimate Guide Top 7 Superior Wet-Proof Camcorders</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unlocking-true-tints-and-shades-in-photos/"><u>[New] Unlocking True Tints and Shades in Photos</u></a></li>
<li><a href="https://snapchat-videos.techidaily.com/updated-2024-approved-artistic-angles-a-selection-of-hot-snapchat-augments/"><u>[Updated] 2024 Approved Artistic Angles A Selection of Hot Snapchat Augments</u></a></li>
<li><a href="https://extra-skills.techidaily.com/updated-scene-reduction-unveiling-imovies-cropping-logic/"><u>[Updated] Scene Reduction Unveiling iMovie's Cropping Logic</u></a></li>
<li><a href="https://youtube-web.techidaily.com/ed-step-by-step-guide-to-a-distinctive-youtube-channel-url-for-2024/"><u>[Updated] Step-by-Step Guide to a Distinctive YouTube Channel URL for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-evolution-of-live-streaming-with-periscope/"><u>[Updated] The Evolution of Live Streaming with Periscope</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-transform-your-flip-to-flash-with-android/"><u>[Updated] Transform Your Flip to Flash with Android</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-text-trends-top-10-modern-effects/"><u>2024 Approved Text Trends Top 10 Modern Effects</u></a></li>
<li><a href="https://win-howtos.techidaily.com/how-to-play-and-convert-mov-videos-on-your-computer-or-device/"><u>How to Play and Convert MOV Videos on Your Computer or Device</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unveiling-the-ultimate-15-stop-motion-film-collection/"><u>In 2024, Unveiling the Ultimate 15 Stop-Motion Film Collection</u></a></li>
<li><a href="https://some-tips.techidaily.com/master-multitask-media-with-ease-expertly-using-netflixs-picture-in-picture-feature-for-2024/"><u>Master Multitask Media with Ease Expertly Using Netflix’s Picture-In-Picture Feature for 2024</u></a></li>
<li><a href="https://win11.techidaily.com/resolving-inoperative-windows-11-speech-recognition/"><u>Resolving Inoperative Windows 11 Speech Recognition</u></a></li>
<li><a href="https://tech-recovery.techidaily.com/step-by-step-tutorial-on-how-to-navigate-and-search-with-the-wayback-machine/"><u>Step-by-Step Tutorial on How to Navigate and Search with the Wayback Machine</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-ultimate-tutorial-for-lut-use-in-after-effects-for-2024/"><u>The Ultimate Tutorial for LUT Use in After Effects for 2024</u></a></li>
<li><a href="https://extra-information.techidaily.com/unlocking-obs-potential-incorporating-luts-seamlessly/"><u>Unlocking OBS' Potential Incorporating LUTs Seamlessly</u></a></li>
<li><a href="https://hardware-help.techidaily.com/update-your-visual-experience-with-geforce-gtx-1660-super-driver-downloads/"><u>Update Your Visual Experience with GeForce GTX 1660 Super Driver Downloads</u></a></li>
</ul></div>

