---
title: A Step-by-Step Guide to Transferring CustomActionData During WiX CustomAction Execution
date: 2024-10-01T19:11:47.035Z
updated: 2024-10-03T20:02:35.497Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes A Step-by-Step Guide to Transferring CustomActionData During WiX CustomAction Execution
thumbnail: https://thmb.techidaily.com/dbdd977fc03b6891cb3b7e84cceda70cd02add2f2e15c2683531919a3387ddeb.jpg
---

## A Step-by-Step Guide to Transferring CustomActionData During WiX CustomAction Execution

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

<!-- affiliate ads begin -->
<span id="1982508">
					<video width="576" height="240" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1982508.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1982508">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1982508.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1982508%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1982508/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<a href="https://aligracehair.sjv.io/c/5597632/2016129/19272" target="_top" id="2016129">
  <img src="//a.impactradius-go.com/display-ad/19272-2016129" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2016129/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to configure CustomActions with Advanced Installer?

If you use Advanced Installer to build and create your MSI, there is no need for an extra CustomAction to set the property of interest with the same name as the Deferred CustomAction.

All you need to do is specify the value of the CustomActionData property within the “ActionData” and Advanced Installer does the rest for you.

![Configure CustomActions](https://cdn.advancedinstaller.com/img/wix-pass-customactiondata-to-customaction/configure-custom-actions.png "Configure CustomActions")  

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Have a look at our [How to Use CustomActionData to Access Windows Installer Properties in Deferred CustomActions](https://tools.techidaily.com/advancedinstaller/products/) article to find out more about:- Why do you need CustomActionData- When can Deferred CustomActions go wrong- How you can pass CustomActionData to a CustomAction using Advanced Installer

<!-- affiliate ads begin -->
<a href="https://25home.pxf.io/c/5597632/2148643/16836" target="_top" id="2148643">
  <img src="//a.impactradius-go.com/display-ad/16836-2148643" border="0" alt="https://techidaily.com" width="300" height="75"/>
</a>
<img height="0" width="0" src="https://25home.pxf.io/i/5597632/2148643/16836" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<a href="https://bluettiit.sjv.io/c/5597632/2148129/17093" target="_top" id="2148129">
  <img src="//a.impactradius-go.com/display-ad/17093-2148129" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://bluettiit.sjv.io/i/5597632/2148129/17093" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://extra-hints.techidaily.com/new-converting-multimedia-scripts-transitioning-from-xmlssa-to-srt/"><u>[New] Converting Multimedia Scripts Transitioning From XML/SSA to SRT</u></a></li>
<li><a href="https://some-guidance.techidaily.com/new-the-ultimate-adobe-premiere-soundtrack-guide/"><u>[New] The Ultimate Adobe Premiere Soundtrack Guide</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/updated-acclaimed-melody-hub-for-android-devices/"><u>[Updated] Acclaimed Melody Hub for Android Devices</u></a></li>
<li><a href="https://some-tips.techidaily.com/customizing-windows-11-with-tailored-themes-and-styles/"><u>Customizing Windows 11 with Tailored Themes and Styles</u></a></li>
<li><a href="https://some-tips.techidaily.com/download-windows-11-insider-build-15031-resolve-initializing-issue-for-smooth-installation/"><u>Download Windows 11 Insider Build 15031? Resolve 'Initializing' Issue for Smooth Installation</u></a></li>
<li><a href="https://some-tips.techidaily.com/enabling-rdc-access-for-windows-11-comprehensive-tutorial-to-connect-remotely/"><u>Enabling RDC Access for Windows 11: Comprehensive Tutorial to Connect Remotely</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhance-your-pcs-safety-with-easy-restore-point-setup-in-windows-11/"><u>Enhance Your PC's Safety with Easy Restore Point Setup in Windows 11</u></a></li>
<li><a href="https://some-tips.techidaily.com/expert-tips-for-deleting-internet-trackers-and-cookies-in-googles-chrome-browser/"><u>Expert Tips for Deleting Internet Trackers & Cookies in Google's Chrome Browser</u></a></li>
<li><a href="https://win-answers.techidaily.com/fixes-for-metro-exodus-game-crash-issues-on-windows/"><u>Fixes for Metro Exodus Game Crash Issues on Windows</u></a></li>
<li><a href="https://location-social.techidaily.com/how-to-changeadd-location-filters-on-snapchat-for-your-motorola-moto-g-stylus-5g-2023-drfone-by-drfone-virtual-android/"><u>How to Change/Add Location Filters on Snapchat For your Motorola Moto G Stylus 5G (2023) | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/how-to-configure-remote-desktop-on-windows-11-a-step-by-step-guide/"><u>How to Configure Remote Desktop on Windows 11: A Step-by-Step Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/how-to-enable-and-create-restore-points-in-windows-10/"><u>How to Enable and Create Restore Points in Windows 10?</u></a></li>
<li><a href="https://android-transfer.techidaily.com/in-2024-best-3-software-to-transfer-files-tofrom-your-huawei-nova-y71-via-a-usb-cable-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>In 2024, Best 3 Software to Transfer Files to/from Your Huawei Nova Y71 via a USB Cable | Dr.fone</u></a></li>
<li><a href="https://fox-links.techidaily.com/in-2024-transforming-your-videography-from-monochrome-to-high-dynamic-range-masterpieces/"><u>In 2024, Transforming Your Videography From Monochrome to High-Dynamic Range Masterpieces</u></a></li>
<li><a href="https://meme-emoji.techidaily.com/new-how-to-record-and-edit-an-animoji-or-memoji-karaoke-music-video-for-2024/"><u>New How to Record and Edit an Animoji or Memoji Karaoke Music Video for 2024</u></a></li>
<li><a href="https://hardware-help.techidaily.com/quick-and-secure-geforce-gtx-460-drivers-downloading-guide-for-windows-users/"><u>Quick and Secure GeForce GTX 460 Drivers Downloading Guide for Windows Users</u></a></li>
</ul></div>

