---
title: "Guide to Generating Global Shortcut Keys via WiX: No Commercial Prompts Included"
date: 2024-09-21T07:31:19.770Z
updated: 2024-09-27T21:24:17.696Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Guide to Generating Global Shortcut Keys via WiX: No Commercial Prompts Included"
thumbnail: https://thmb.techidaily.com/5a94426a32501655e657a3254c012c85eb00e68b90f4fb83cdfc375f3ce534ef.jpg
---

## Guide to Generating Global Shortcut Keys via WiX: No Commercial Prompts Included

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

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1938721/19272" target="_top" id="1938721">
  <img src="//a.impactradius-go.com/display-ad/19272-1938721" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1938721/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### What is an advertised shortcut?

Advertised shortcuts are helpful for developers when making sure a software is installed and running as intended, without any missing pieces. 

When an advertised shortcut is launched, Windows Installer checks to see if all the components included in the same feature as the shortcut are installed on the device. If that’s not the case, the shortcut will automatically launch the MSI from which the program was installed and reinstall the .msi file missing resources.

### What is a non-advertised shortcut (Standard Shortcut)?

We call a non-advertised shortcut (Standard Shortcuts) a standard Windows shortcut. In this case, you can see the target field points to the executable that will be launched if you right-click on it. If this executable is missing for any reason, the application will immediately crash.

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
<a href="https://appsumo.8odi.net/c/5597632/2151868/7443" target="_top" id="2151868">
  <img src="//a.impactradius-go.com/display-ad/7443-2151868" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2151868/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://dhgate.sjv.io/c/5597632/2106658/12108" target="_top" id="2106658">
  <img src="//a.impactradius-go.com/display-ad/12108-2106658" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://dhgate.sjv.io/i/5597632/2106658/12108" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. In the shortcut’s properties, you can use the "_Advertised Shortcut"_ checkbox to make your shortcut an advertised one. (This option is unchecked by default, leave it as it is to create a **non-advertised shortcut**).

![Create Advertised Shorcut](https://cdn.advancedinstaller.com/img/wix-child-images/create-advertised-shortcut.png "Create Advertised Shorcut")  

3\. To place the shortcut on the Desktop go to the **Paths** section.

4\. Once in the Paths section, change the Shortcut folder option from **SHORTCUTDIR** to **DesktopFolder**.

![Change Shortcut Folder](https://cdn.advancedinstaller.com/img/wix-child-images/change-shortcut-folder.png "Change Shortcut Folder")  

<!-- affiliate ads begin -->
<a href="https://aidotcom.pxf.io/c/5597632/2129041/19576" target="_top" id="2129041">
  <img src="//a.impactradius-go.com/display-ad/19576-2129041" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aidotcom.pxf.io/i/5597632/2129041/19576" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

5\. To make sure that your setup package is ICE valid, go to: File - Settings - Package Validation

6\. In the **Build Settings** section, check the "_Enable ICE validation for MSI packages_” checkbox.

![Enable ICE Validation for MSI Packages](https://cdn.advancedinstaller.com/img/wix-child-images/enable-ice-validation-for-msi-packages.png "Enable ICE Validation for MSI Packages")  

Done!

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Check out Advanced Installer’s friendly GUI through our [30-day full featured trial](https://tools.techidaily.com/advancedinstaller/products/)**.** (No credit card required)

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2105874/7443" target="_top" id="2105874">
  <img src="//a.impactradius-go.com/display-ad/7443-2105874" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2105874/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://screen-activity-recording.techidaily.com/new-in-2024-mastering-marker-techniques-for-efficient-video-cutting/"><u>[New] In 2024, Mastering Marker Techniques for Efficient Video Cutting</u></a></li>
<li><a href="https://youtube-help.techidaily.com/new-streaming-success-updated-youtube-revenue-policies/"><u>[New] Streaming Success Updated YouTube Revenue Policies</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-streamlined-zoom-utilization-a-chromebook-perspective/"><u>[New] Streamlined Zoom Utilization A Chromebook Perspective</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unleashing-potential-with-the-vida-editing-suite/"><u>[Updated] Unleashing Potential with the Vida Editing Suite</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/2024-approved-integrating-soundscapes-with-fusion-studios-tips/"><u>2024 Approved Integrating Soundscapes with Fusion Studio's Tips</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-strategies-for-a-rising-number-of-youtubers-fans/"><u>2024 Approved Strategies for a Rising Number of Youtubers' Fans</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-tales-on-the-silver-screen-writing-for-cinema/"><u>2024 Approved Tales on the Silver Screen Writing for Cinema</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-future-of-editing-with-vita-a-complete-review/"><u>2024 Approved The Future of Editing with Vita - A Complete Review</u></a></li>
<li><a href="https://some-guidance.techidaily.com/effective-techniques-to-downsize-your-mov-videos-without-losing-quality/"><u>Effective Techniques to Downsize Your MOV Videos Without Losing Quality</u></a></li>
<li><a href="https://driver-download.techidaily.com/enhance-your-gameplay-update-nvidia-geforce-gtx-1660-ti-graphics-card-drivers/"><u>Enhance Your Gameplay: Update Nvidia GeForce GTX 1660 Ti Graphics Card Drivers</u></a></li>
<li><a href="https://solve-helper.techidaily.com/extract-your-dvd-content-for-mobile-playback-using-the-no-cost-winx-dvd-converter-mp4-avi-for-iphone-and-android/"><u>Extract Your DVD Content for Mobile Playback Using the No-Cost WinX DVD Converter (MP4, AVI) for iPhone and Android</u></a></li>
<li><a href="https://fox-that.techidaily.com/how-to-fix-a-broken-qr-code-scanner-on-your-iphone-with-these-10-tips/"><u>How to Fix a Broken QR Code Scanner on Your iPhone with These 10 Tips</u></a></li>
<li><a href="https://activate-lock.techidaily.com/in-2024-new-guide-how-to-check-icloud-activation-lock-status-from-your-iphone-12-pro-max-by-drfone-ios/"><u>In 2024, New Guide How To Check iCloud Activation Lock Status From Your iPhone 12 Pro Max</u></a></li>
<li><a href="https://some-tips.techidaily.com/optimal-energy-solutions-for-gopro-hero5-certified-and-third-party-for-2024/"><u>Optimal Energy Solutions for GoPro Hero5 Certified & Third-Party for 2024</u></a></li>
<li><a href="https://howto.techidaily.com/reasons-for-realme-narzo-60-5g-stuck-on-boot-screen-and-ways-to-fix-them-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Reasons for Realme Narzo 60 5G Stuck on Boot Screen and Ways To Fix Them | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/transform-your-images-proven-pixlr-strategies-for-2024/"><u>Transform Your Images Proven Pixlr Strategies for 2024</u></a></li>
</ul></div>

