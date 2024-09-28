---
title: "Building Universal Shortcuts Without Ads Using the WiX Toolset: A Step-by-Step Guide"
date: 2024-09-21T16:55:32.660Z
updated: 2024-09-28T00:27:56.878Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Building Universal Shortcuts Without Ads Using the WiX Toolset: A Step-by-Step Guide"
thumbnail: https://thmb.techidaily.com/14b0662c78e5872a3461f2dbc1feb1f76e4bd1f2823265595248b4cc420c76ab.jpg
---

## Building Universal Shortcuts Without Ads Using the WiX Toolset: A Step-by-Step Guide

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

## How to create non-advertised shortcuts for all users / per machine with WiX Toolset

When you define shortcuts in WiX Toolset, their default installation is **non-advertised (Standard Shortcuts)**. 

Even though this characteristic shouldn’t be a serious issue, it can be a source of ICE errors in some instances (for example, when you define components that have both per-user and per-machine data, with a per-machine keypath).

This article will show you how to fix ICE errors when creating non-advertised shortcuts using the WiX Toolset.

### Advertised vs. Non-advertised shortcuts

### What is an advertised shortcut?

Advertised shortcuts are helpful for developers when making sure a software is installed and running as intended, without any missing pieces. 

When an advertised shortcut is launched, Windows Installer checks to see if all the components included in the same feature as the shortcut are installed on the device. If that’s not the case, the shortcut will automatically launch the MSI from which the program was installed and reinstall the .msi file missing resources.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2082538/7443" target="_top" id="2082538">
  <img src="//a.impactradius-go.com/display-ad/7443-2082538" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2082538/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### What is a non-advertised shortcut (Standard Shortcut)?

We call a non-advertised shortcut (Standard Shortcuts) a standard Windows shortcut. In this case, you can see the target field points to the executable that will be launched if you right-click on it. If this executable is missing for any reason, the application will immediately crash.

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2137220/26400" target="_top" id="2137220">
  <img src="//a.impactradius-go.com/display-ad/26400-2137220" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2137220/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to create non-advertised shortcuts?

According to [ICE43](https://learn.microsoft.com/en-us/windows/win32/msi/ice43 "ICE43"), Microsoft recommends using separate registry keys in the HKCU (HKEY\_CURRENT\_USER) as keypaths of the non-advertised shortcuts.

To implement this method, you only need to create a new component where you will build the shortcut and the registry value that will serve as the shortcut’s keypath.

This method is actually very simple to implement. All you need to do is create a new component where you will build the shortcut and the registry value that will serve as the shortcut’s keypath.

<Component>
      <Shortcut Id="NonAdShortApp" Directory="DesktopFolder"     Name="NonAdShortApp.exe" WorkingDirectory="INSTALLFOLDER" Target="[#NonAdShortApp.exe]"/> 
      <RegistryValue Root="HKCU" Key="Software\[Manufacturer]\[ProductName]" Type="string" Value="" KeyPath="yes" />
</Component>

Copy

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Keep in mind that his method forces you to add registry entries in your setup package, which may not be as practical in a multi-user scenario. This means that if a user uninstalls the application, all the other users will have orphaned registry entries in their respective HKCU hives.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1938693/19272" target="_top" id="1938693">
  <img src="//a.impactradius-go.com/display-ad/19272-1938693" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1938693/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

A major difference between advertised and non-advertised shortcuts is the use of files (that are already installed per machine) as keypaths – which is not possible for non-advertised shortcuts.

To overcome this situation, we will turn an advertised shortcut into a non-advertised one.

Let’s get started!

First, **declare the shortcut** using the following lines:

<Component Id="NonAdShortApp.exe" Guid="4f4d8d47-72a3-4e00-b959-ccae259837df">
	<File Id="NonAdShortApp.exe" Name="NonAdShortApp.exe" Source="$(var.NonAdShortApp_TargetDir)NonAdShortApp.exe" KeyPath="yes">
		<Shortcut Id="NonAdShortApp" Directory="DesktopFolder" Name="NonAdShortApp.exe" WorkingDirectory="INSTALLFOLDER" Advertise="yes"/>
	</File>
</Component>

Copy

We have created a new advertised shortcut in our component which uses a file as a KeyPath. 

Now, we will use the DISABLEADVTSHORTCUTS property to **turn our advertised shortcut** into a **non-advertised** one, bypassing the ICE43 condition.

<Property Id="DISABLEADVTSHORTCUTS" Value="1" />

Copy

That’s it! By adding this line of code into your WiX project, you can turn any advertised shortcut into a non-advertised one without declaring additional registry entries for each shortcut.

### How to create a non-advertised shortcut with Advanced Installer

Through Advanced Installer’s GUI, you have a straightforward way to generate non-advertised shortcuts without using any code.

1\. Go to the **Shortcuts Page** and create a new shortcut for an installed file.

![Create New Shortcut](https://cdn.advancedinstaller.com/img/wix-child-images/create-new-shortcut.png "Create New Shortcut")  

2\. In the shortcut’s properties, you can use the "_Advertised Shortcut"_ checkbox to make your shortcut an advertised one. (This option is unchecked by default, leave it as it is to create a **non-advertised shortcut**).

![Create Advertised Shorcut](https://cdn.advancedinstaller.com/img/wix-child-images/create-advertised-shortcut.png "Create Advertised Shorcut")  

<!-- affiliate ads begin -->
<span id="1983539">
					<video width="576" height="240" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1983539.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1983539">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1983539.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1983539%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1983539/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

3\. To place the shortcut on the Desktop go to the **Paths** section.

4\. Once in the Paths section, change the Shortcut folder option from **SHORTCUTDIR** to **DesktopFolder**.

![Change Shortcut Folder](https://cdn.advancedinstaller.com/img/wix-child-images/change-shortcut-folder.png "Change Shortcut Folder")  

5\. To make sure that your setup package is ICE valid, go to: File - Settings - Package Validation

6\. In the **Build Settings** section, check the "_Enable ICE validation for MSI packages_” checkbox.

![Enable ICE Validation for MSI Packages](https://cdn.advancedinstaller.com/img/wix-child-images/enable-ice-validation-for-msi-packages.png "Enable ICE Validation for MSI Packages")  

Done!

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Check out Advanced Installer’s friendly GUI through our [30-day full featured trial](https://tools.techidaily.com/advancedinstaller/products/)**.** (No credit card required)

<!-- affiliate ads begin -->
<a href="https://unicoeye.pxf.io/c/5597632/2134498/18498" target="_top" id="2134498">
  <img src="//a.impactradius-go.com/display-ad/18498-2134498" border="0" alt="https://techidaily.com" width="720" height="90"/>
</a>
<img height="0" width="0" src="https://unicoeye.pxf.io/i/5597632/2134498/18498" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Conclusion

Now we know how to avoid ICE errors by creating non-advertised shortcuts with the WiX Toolset.

Of course, you can always choose a tool that doesn't require any code to create non-advertised shortcuts, such as Advanced Installer.

We hope you found this article useful.

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
<li><a href="https://facebook-clips.techidaily.com/new-igniting-online-trends-crafting-viral-facebook-posts-for-2024/"><u>[New] Igniting Online Trends Crafting Viral Facebook Posts for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-simplify-viewing-incorporating-subtitles-into-wmp/"><u>[New] Simplify Viewing Incorporating Subtitles Into WMP</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-ultimate-productivity-playlist-podcast-inspired-tasks/"><u>[New] The Ultimate Productivity Playlist Podcast-Inspired Tasks</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-ultimate-playlist-of-timeless-anime-themes/"><u>[Updated] The Ultimate Playlist of Timeless Anime Themes</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-scripting-for-success-filmmakers-secrets/"><u>2024 Approved Scripting for Success Filmmaker's Secrets</u></a></li>
<li><a href="https://win-answers.techidaily.com/1726027457688-dvd/"><u>市販DVDの高品位データコピー法：効率よく・即座に・完全無損失</u></a></li>
<li><a href="https://program-issues.techidaily.com/1723007174158-call-of-duty-wwii-troubleshooting-navigating-past-error-code-4128-easily/"><u>Call of Duty WWII Troubleshooting - Navigating Past Error Code 지 4128 Easily</u></a></li>
<li><a href="https://hardware-updates.techidaily.com/easy-download-updated-epson-l3150-driver-for-optimal-printing-on-windows-11-8-or-7-systems/"><u>Easy Download: Updated Epson L3150 Driver for Optimal Printing on Windows 11, 8 or 7 Systems</u></a></li>
<li><a href="https://win-howtos.techidaily.com/how-to-overcome-the-update-error-dealing-with-windows-1ves-0x80240034-troubleshooting-guide/"><u>How to Overcome the Update Error: Dealing with Windows 1Ve's 0X80240034 Troubleshooting Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-workings-of-drones-an-introduction-for-beginners/"><u>In 2024, The Workings of Drones An Introduction for Beginners</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/leading-downloader-software-facebooks-top-choices-5-for-2024/"><u>Leading Downloader Software Facebook's Top Choices #5 for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlock-your-potential-for-green-screen-excellence-in-kinemaster-for-2024/"><u>Unlock Your Potential for Green Screen Excellence in Kinemaster for 2024</u></a></li>
<li><a href="https://tech-revival.techidaily.com/unlocking-potential-with-usechamgext-gpt-copilot-a-comprehensive-guide/"><u>Unlocking Potential with UseChamgext GPT Copilot: A Comprehensive Guide</u></a></li>
<li><a href="https://smart-video-creator.techidaily.com/updated-2024-approved-top-online-video-editing-tools-for-vertical-content/"><u>Updated 2024 Approved Top Online Video Editing Tools for Vertical Content</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/your-gateway-to-classic-games-best-in-class-5gb-advance-emulators-compatible-with-pcs/"><u>Your Gateway to Classic Games Best-in-Class 5GB Advance Emulators Compatible with PCs</u></a></li>
</ul></div>

