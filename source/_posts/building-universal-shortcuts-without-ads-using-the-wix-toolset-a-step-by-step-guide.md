---
title: "Building Universal Shortcuts Without Ads Using the WiX Toolset: A Step-by-Step Guide"
date: 2024-09-27T17:55:16.117Z
updated: 2024-10-03T17:49:43.785Z
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

### What is a non-advertised shortcut (Standard Shortcut)?

We call a non-advertised shortcut (Standard Shortcuts) a standard Windows shortcut. In this case, you can see the target field points to the executable that will be launched if you right-click on it. If this executable is missing for any reason, the application will immediately crash.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135400/19272" target="_top" id="2135400">
  <img src="//a.impactradius-go.com/display-ad/19272-2135400" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135400/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<span id="1160850">
					<video width="576" height="324" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1160850.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/14559-1160850">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1160850.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fpropmoneyinc.pxf.io%2Fc%2F5597632%2F1160850%2F14559'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1160850/14559" style="position:absolute;visibility:hidden;" border="0" />
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

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1880927/19272" target="_top" id="1880927">
  <img src="//a.impactradius-go.com/display-ad/19272-1880927" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1880927/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. In the shortcut’s properties, you can use the "_Advertised Shortcut"_ checkbox to make your shortcut an advertised one. (This option is unchecked by default, leave it as it is to create a **non-advertised shortcut**).

![Create Advertised Shorcut](https://cdn.advancedinstaller.com/img/wix-child-images/create-advertised-shortcut.png "Create Advertised Shorcut")  

3\. To place the shortcut on the Desktop go to the **Paths** section.

4\. Once in the Paths section, change the Shortcut folder option from **SHORTCUTDIR** to **DesktopFolder**.

![Change Shortcut Folder](https://cdn.advancedinstaller.com/img/wix-child-images/change-shortcut-folder.png "Change Shortcut Folder")  

5\. To make sure that your setup package is ICE valid, go to: File - Settings - Package Validation

6\. In the **Build Settings** section, check the "_Enable ICE validation for MSI packages_” checkbox.

![Enable ICE Validation for MSI Packages](https://cdn.advancedinstaller.com/img/wix-child-images/enable-ice-validation-for-msi-packages.png "Enable ICE Validation for MSI Packages")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2002018/7443" target="_top" id="2002018">
  <img src="//a.impactradius-go.com/display-ad/7443-2002018" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2002018/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

Done!

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Check out Advanced Installer’s friendly GUI through our [30-day full featured trial](https://tools.techidaily.com/advancedinstaller/products/)**.** (No credit card required)

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2151893/7443" target="_top" id="2151893">
  <img src="//a.impactradius-go.com/display-ad/7443-2151893" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2151893/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://video-capture.techidaily.com/new-2024-approved-turn-on-google-meet-grids-to-see-all-attendees/"><u>[New] 2024 Approved Turn On Google Meet Grids to See All Attendees</u></a></li>
<li><a href="https://youtube-web.techidaily.com/rom-raw-to-masterpiece-the-premier-free-mobile-editors-for-android-for-2024/"><u>[New] From Raw to Masterpiece The Premier Free Mobile Editors for Android for 2024</u></a></li>
<li><a href="https://fox-links.techidaily.com/new-in-2024-13-best-ways-to-make-money-on-reddit-no-experience-needed/"><u>[New] In 2024, 13 Best Ways to Make Money on Reddit - No Experience Needed</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/updated-revolutionary-process-to-blend-gopro-videos-into-360-degree-panoramas/"><u>[Updated] Revolutionary Process to Blend GoPro Videos Into 360-Degree Panoramas</u></a></li>
<li><a href="https://mondly-stories.techidaily.com/10-reasons-why-you-should-learn-afrikaans/"><u>10 Reasons Why You Should Learn Afrikaans</u></a></li>
<li><a href="https://extra-tips.techidaily.com/2024-approved-basic-equipment-for-travel-video-creators/"><u>2024 Approved Basic Equipment for Travel Video Creators</u></a></li>
<li><a href="https://win11.techidaily.com/crack-the-ms-pc-manager-install-issue-on-windows-xp/"><u>Crack the MS PC Manager Install Issue on Windows XP</u></a></li>
<li><a href="https://some-tips.techidaily.com/navigating-tomorrow-cosmic-as-your-gateway-to-the-next-gen-linux-experience/"><u>Navigating Tomorrow: COSMIC as Your Gateway to the Next-Gen Linux Experience</u></a></li>
<li><a href="https://buynow-help.techidaily.com/sonoss-outdoor-audio-triumph-a-compreran-report/"><u>Sonos's Outdoor Audio Triumph: A Compreran Report</u></a></li>
<li><a href="https://techtrends.techidaily.com/step-by-step-tutorial-configuring-macs-network-drive-access/"><u>Step-by-Step Tutorial: Configuring Mac's Network Drive Access</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-8-essential-steps-for-optimizing-your-new-windows-pc/"><u>Top 8 Essential Steps for Optimizing Your New Windows PC</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-9-methods-for-accessing-powershell-on-windows-10/"><u>Top 9 Methods for Accessing PowerShell on Windows 10</u></a></li>
<li><a href="https://some-tips.techidaily.com/transitioning-kodi-the-shift-from-debian-packages-to-flatpak-on-linux-systems/"><u>Transitioning Kodi: The Shift From Debian Packages to Flatpak on Linux Systems</u></a></li>
<li><a href="https://some-tips.techidaily.com/ultimate-selection-premium-mac-screens-and-monitors/"><u>Ultimate Selection: Premium Mac Screens and Monitors</u></a></li>
<li><a href="https://some-tips.techidaily.com/uncover-hidden-gems-essential-yet-overlooked-windows-shortcuts/"><u>Uncover Hidden Gems: Essential Yet Overlooked Windows Shortcuts</u></a></li>
<li><a href="https://some-tips.techidaily.com/understanding-batch-files-a-comprehensive-guide-on-what-they-are-and-how-to-access-them/"><u>Understanding Batch Files: A Comprehensive Guide on What They Are & How To Access Them</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/unlocking-performance-secrets-toms-equipment-rundown/"><u>Unlocking Performance Secrets - Tom's Equipment Rundown</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-the-secrets-13-quick-methods-to-access-windows-10-settings/"><u>Unlocking the Secrets: 13 Quick Methods to Access Windows 10 Settings</u></a></li>
<li><a href="https://some-tips.techidaily.com/your-comprehensive-guide-to-all-the-top-highlights-from-apples-worldwide-developers-conference-2024/"><u>Your Comprehensive Guide to All the Top Highlights From Apple's Worldwide Developers Conference 2024</u></a></li>
</ul></div>

