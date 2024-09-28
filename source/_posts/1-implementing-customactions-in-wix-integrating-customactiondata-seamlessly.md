---
title: "1. Implementing CustomActions in WiX: Integrating CustomActionData Seamlessly"
date: 2024-09-24T20:07:53.671Z
updated: 2024-09-28T02:55:58.065Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes 1. Implementing CustomActions in WiX: Integrating CustomActionData Seamlessly"
thumbnail: https://thmb.techidaily.com/d9427c61032284cb88ab156d6c103f9d31f7d2686f689f4e79141572fa04ae5d.jpg
---

## 1. Implementing CustomActions in WiX: Integrating CustomActionData Seamlessly

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

## How to pass CustomActionData to a CustomAction using WiX

Written by [Horatiu Vladasel](https://tools.techidaily.com/advancedinstaller/products/) · September 9th, 2022

Do you want to transfer CustomActionData to a CustomAction in WiX? We'll show you how in this article.

When adding CustomActions using WiX, there are two elements that you need to use:

* the CustomAction element;
* the Sequence element.

The CustomAction element specifies the custom action that will be added to the MSI CustomAction table. 

On the other hand, the Sequence element is used to schedule the CustomAction within the corresponding table (AdminExecuteSequence, AdminUISequence, AdvertiseExecuteSequence, InstallExecuteSequence) and set any condition, if needed.

Each condition is evaluated separately, and the corresponding CustomAction is run only if the condition is set as True. Otherwise, the CustomAction gets skipped. If the condition syntax is invalid, then the sequence ends and returns **iesBadActionData**.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Get more details about WiX CustomActions from our [How To Add Custom Actions in WiX Toolset](https://tools.techidaily.com/advancedinstaller/products/) article.

What is the challenge when you want to pass a property to a **Deferred CustomAction**?

A **Deferred CustomAction** doesn't have any information about the original session handle and property data (Session.Property(\[PROPERTY\])). This is because the script generated for it is executed outside of the installation process. Instead, you will need to use CustomActionData (Session.Property("CustomActionData")) .

### How to use CustomActions with WiX?

Let's suppose we need to add a script that takes the value of the SERVERPATH property as an input (passed to the installer via command line) and writes it into the registry. The CustomAction script should look like the one below:

First, we must define our CustomAction elements:

<CustomAction Id="SetServerPath" BinaryKey="SetServerPath.vbs" Execute="deferred" VBScriptCall='' Impersonate="no" Return="check"/>
<CustomAction Id="SetServerPathProperty" Property="SetServerPath" Value="[SERVERPATH]"/>

Copy

Let’s understand what **SetServerPathProperty** and **SetServerPath CustomAction** are:

* The **SetServerPath CustomAction** is the Deferred CustomAction and it references the VBScript defined above, which is stored in the Binary table.
* The **SetServerPathProperty** is the SetProperty CustomAction which is used to set the property of interest (SERVERPATH) property to a property with the same name as the Deferred CustomAction (SetServerPath).

We also need to define the Binary element because the VBScript referenced by the SetServerPath CustomAction is stored in the Binary table.

<Binary Id="SetServerPath.vbs" SourceFile="SetServerPath.vbs"/>

Copy

Once the CustomAction and Binary elements are defined, we can set the corresponding InstallExecuteSequence elements – one for each of the two CustomActions.

<InstallExecuteSequence>
     <Custom Action='SetServerPath' Before='InstallFinalize'>NOT Installed</Custom>
     <Custom Action='SetServerPathProperty' Before='SetServerPath'>NOT Installed</Custom>
</InstallExecuteSequence>

Copy

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)When scheduling the two CustomAction in the InstallExecuteSequence table, the **SetProperty CustomAction** ('SetServerPathProperty) should be scheduled before the Deferred CustomAction (SetServerPath).

<!-- affiliate ads begin -->
<span id="1993647">
					<video width="128" height="480" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1993647.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1993647">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1993647.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:80px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1993647%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1993647/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

**SetProperty CustomAction** ('SetServerPathProperty) is used to set the property of interest to a property with the same name as the Deferred CustomAction.

The complete listing for the WiX source file (.wxs) should look like the one below:

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
	<Binary Id="SetServerPath.vbs" SourceFile="SetServerPath.vbs"/>	
	<CustomAction Id="SetServerPath" BinaryKey="SetServerPath.vbs" Execute="deferred" VBScriptCall='' Impersonate="no" Return="check"/>
	<CustomAction Id="SetServerPathProperty" Property="SetServerPath" Value="[SERVERPATH]"/>
	<InstallExecuteSequence>
  	<Custom Action='SetServerPath' Before='InstallFinalize'>NOT Installed</Custom>
  	<Custom Action='SetServerPathProperty' Before='SetServerPath'>NOT Installed</Custom>
	</InstallExecuteSequence>
  </Product>
</Wix>

Copy

Now, all we need to do is to:

* Pre-process and compile the WiX source file into a WiX object file.
* Process the WiX object file compiled previously and build the Windows Installer (MSI package).

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2105874/7443" target="_top" id="2105874">
  <img src="//a.impactradius-go.com/display-ad/7443-2105874" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2105874/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to configure CustomActions with Advanced Installer?

If you use Advanced Installer to build and create your MSI, there is no need for an extra CustomAction to set the property of interest with the same name as the Deferred CustomAction.

All you need to do is specify the value of the CustomActionData property within the “ActionData” and Advanced Installer does the rest for you.

![Configure CustomActions](https://cdn.advancedinstaller.com/img/wix-pass-customactiondata-to-customaction/configure-custom-actions.png "Configure CustomActions")  

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2136619/26400" target="_top" id="2136619">
  <img src="//a.impactradius-go.com/display-ad/26400-2136619" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2136619/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Have a look at our [How to Use CustomActionData to Access Windows Installer Properties in Deferred CustomActions](https://tools.techidaily.com/advancedinstaller/products/) article to find out more about:- Why do you need CustomActionData- When can Deferred CustomActions go wrong- How you can pass CustomActionData to a CustomAction using Advanced Installer

### Conclusion

WiX does not have a GUI and it builds the Windows Installer packages based solely on the information defined within the WiX source file (wxs). This makes it difficult to use, especially for people who have little or no experience.

On the other hand, Advanced Installer comes with a dedicated GUI for adding a CustomAction and passing the CustomActionData property to it which makes the job a lot easier and very intuitive.

Try out Advanced Installer’s dedicated GUI for CustomAction through our [30-day full feature trial](https://tools.techidaily.com/advancedinstaller/products/).

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
<a href="https://aligracehair.sjv.io/c/5597632/1934138/19272" target="_top" id="1934138">
  <img src="//a.impactradius-go.com/display-ad/19272-1934138" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1934138/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://facebook-videos.techidaily.com/new-in-2024-a-day-in-the-life-on-facebook-enhancing-participation/"><u>[New] In 2024, A Day in the Life on Facebook Enhancing Participation</u></a></li>
<li><a href="https://vp-tips.techidaily.com/new-joyjingles-where-to-find-hilarious-ringtone-links/"><u>[New] JoyJingles Where to Find Hilarious Ringtone Links</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-ultimate-2024-rendition-of-audiofreex-insight/"><u>[New] The Ultimate 2024 Rendition of AudioFreex Insight</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-ultimate-frames-per-second-for-languid-visuals/"><u>[New] Ultimate Frames Per Second for Languid Visuals</u></a></li>
<li><a href="https://remote-screen-capture.techidaily.com/updated-leading-8-capture-tools-without-lag-for-2024/"><u>[Updated] Leading 8 Capture Tools Without Lag for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-pixelpunmatic-device/"><u>[Updated] PixelPunmatic Device</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-top-10-hidden-gems-for-enhancing-canva-images/"><u>[Updated] Top 10 Hidden Gems for Enhancing Canva Images</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/best-srt-mods-ultimate-upgrades-for-macwindows/"><u>Best SRT Mods Ultimate Upgrades for Mac/Windows</u></a></li>
<li><a href="https://data-safeguard.techidaily.com/easy-steps-to-retrieve-lost-information-from-your-iphone-exclusive-buy-now-offer/"><u>Easy Steps to Retrieve Lost Information From Your iPhone – Exclusive Buy-Now Offer</u></a></li>
<li><a href="https://fake-location.techidaily.com/how-can-i-use-a-fake-gps-without-mock-location-on-samsung-galaxy-s23-fe-drfone-by-drfone-virtual-android/"><u>How Can I Use a Fake GPS Without Mock Location On Samsung Galaxy S23 FE? | Dr.fone</u></a></li>
<li><a href="https://techidaily.com/how-to-soft-reset-oppo-find-n3-flip-phone-drfone-by-drfone-reset-android-reset-android/"><u>How to Soft Reset Oppo Find N3 Flip phone? | Dr.fone</u></a></li>
<li><a href="https://android-location.techidaily.com/in-2024-10-free-location-spoofers-to-fake-gps-location-on-your-poco-f5-pro-5g-drfone-by-drfone-virtual/"><u>In 2024, 10 Free Location Spoofers to Fake GPS Location on your Poco F5 Pro 5G | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-all-you-need-to-know-about-upgrading-to-macos-11-big-sur/"><u>In 2024, All You Need to Know About Upgrading to macOS 11 Big Sur</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-top-flight-tech-best-drone-gimbals/"><u>In 2024, Top Flight Tech Best Drone Gimbals</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unseen-battles-umbraheroes-black-versus-luminaryheroes-silver/"><u>In 2024, Unseen Battles Umbraheroes (Black) Versus Luminaryheroes (Silver)</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-eye-opening-journey-with-q500-for-2024/"><u>The Eye-Opening Journey with Q500 for 2024</u></a></li>
<li><a href="https://screen-video-capture.techidaily.com/the-ultimate-user-friendly-guide-to-starting-an-effective-group-chat-on-skype-across-multiple-platforms-for-2024/"><u>The Ultimate User-Friendly Guide to Starting an Effective Group Chat on Skype Across Multiple Platforms for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unbelievable-judgment-and-backup-recommendations-for-2024/"><u>Unbelievable Judgment & Backup Recommendations for 2024</u></a></li>
<li><a href="https://os-tips.techidaily.com/unstick-your-idevice-from-update-process-with-easy-troubleshooting-techniques/"><u>Unstick Your iDevice From Update Process with Easy Troubleshooting Techniques</u></a></li>
</ul></div>

