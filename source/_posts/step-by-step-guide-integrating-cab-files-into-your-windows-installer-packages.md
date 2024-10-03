---
title: "Step-by-Step Guide: Integrating .CAB Files Into Your Windows Installer Packages"
date: 2024-09-28T16:25:49.058Z
updated: 2024-10-03T18:01:08.980Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Step-by-Step Guide: Integrating .CAB Files Into Your Windows Installer Packages"
thumbnail: https://thmb.techidaily.com/3e64ab7fbedf01adf094c0f7a07b62ec8466f937073c7188969d1624a01e5f53.jpg
---

## Step-by-Step Guide: Integrating .CAB Files Into Your Windows Installer Packages

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

## How To Embed CAB Files in MSI

Written by [Alex Marin](https://tools.techidaily.com/advancedinstaller/products/) · June 7th, 2021

One of the most asked questions in the industry is related to CAB files and what embedding options these have within the WiX Toolset. 

Let's see how CAB embedding works within WiX Toolset, what differences are there when using different versions and how you can use Advanced Installer to manage your CAB files in your MSI.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1915865/19272" target="_top" id="1915865">
  <img src="//a.impactradius-go.com/display-ad/19272-1915865" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1915865/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How CAB Embedding Works In WiX Toolset

To control CAB embedding within your Wix Toolset project, you will need to use the following option:

<MediaTemplate EmbedCab="yes"/>

Copy

Just set the EmbedCab value to “yes” or “no” according to your needs - and you're ready to start.

To see how CAB embedding works, let's create a simple MSI with WiX Toolset. 

For this example, we added a single file called “Trace32.exe” in the package.

The code for the WSX file is as follows:

<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
<Product Id="*" UpgradeCode="12345678-1111-2222-3333-666666666666"
 
Name="My First Installer" Version="1.0.0.0" Manufacturer="My Company" Language="1033">
<Package InstallerVersion="200" Compressed="yes" Comments="Hello, this is my first installer"/>
<MediaTemplate EmbedCab="yes" />

 
<Directory Id="TARGETDIR" Name="SourceDir">
<Directory Id="ProgramFilesFolder">
<Directory Id="INSTALLDIR" Name="MyFirstInstaller">
<Component Id="Files" Guid="11111111-2222-3333-4444-555555555555">
<File Id="File1" Source="Trace32.exe"/>
</Component>
</Directory>
</Directory>
</Directory>
 
<Feature Id="Feature1" Level="1" Title="First feature" Description="This is the one and only feature in this installation">
<ComponentRef Id="Files"/>
</Feature>
</Product>
</Wix>

Copy

 Once we have the MSI configured as needed, it's time to build it: 

1\. Create a new batch file in the same folder along with the **example.wsx** file. 

2\. Save it as**make\_msi.bat**.

3\. Inside the batch file, paste the following code:

"C:\Program Files (x86)\WiX Toolset v3.11\bin\candle.exe" example.wxs
"C:\Program Files (x86)\WiX Toolset v3.11\bin\light.exe" example.wixobj
@pause

Copy

When everything is ready, execute the **make\_msi.bat** file - this quick build will result in the **example.msi** that will appear in the folder.

![Execute bat file](https://cdn.advancedinstaller.com/img/wix-child-images/execute-bat-file.gif "Executing the make_msi.bat file")  

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2137223/26400" target="_top" id="2137223">
  <img src="//a.impactradius-go.com/display-ad/26400-2137223" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2137223/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

After executing the .bat file, the CAB file was embedded inside the MSI. If you don’t want the CAB file to be embedded, change the following line within the example.wsx:

<MediaTemplate EmbedCab="no"/>

Copy

If you change it and run the **make\_msi.bat** again, a CAB archive named “cab1.cab” will be created next to your MSI.

![Create cab file](https://cdn.advancedinstaller.com/img/wix-child-images/create-cab-file.png "Creating CAB file")  

### What Are The Differences When Embedding CAB Files In Different WiX Versions?

Before WiX version 3.8, the MediaTemplate element did not exist and CAB files had to be declared independently:

<Media Id="1" Cabinet="cab1.cab" EmbedCab="yes"/>

Copy

This method still works after version 3.8, but if you want to use it, the WSX file should use this code:

<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
<Product Id="*" UpgradeCode="12345678-1111-2222-3333-666666666666"
 
Name="My First Installer" Version="1.0.0.0" Manufacturer="My Company" Language="1033">
<Package InstallerVersion="200" Compressed="yes" Comments="Hello, this is my first installer"/>
<Media Id="1" Cabinet="product.cab" EmbedCab="Yes"/>

Copy

Keep in mind that if you are using a WiX version higher than 3.8, you can't use MediaTemplate and Media elements at the same time. Either you declare a template which will be used across all the CAB files (as seen in the first example), or you declare each CAB manually and define if it’s embedded or not.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2130885/7443" target="_top" id="2130885">
  <img src="//a.impactradius-go.com/display-ad/7443-2130885" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2130885/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Using Advanced Installer's GUI to Manage CAB Files Within Your MSIs

 Advanced Installer offers multiple options to handle CAB files within your MSI. Watch our tutorial video to see how it works. 

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)If you want to see a comparison between WiX and Advanced Installer, check our article titled [Bundles-WiX vs. Advanced Installer](https://tools.techidaily.com/advancedinstaller/products/), where we discuss the basics of WiX - such as where to get it, how to install it, and how to create a bundle of two MSI applications with it.

I hope you found this information helpful and easy to implement.

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
<a href="https://appsumo.8odi.net/c/5597632/2043603/7443" target="_top" id="2043603">
  <img src="//a.impactradius-go.com/display-ad/7443-2043603" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2043603/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://article-posts.techidaily.com/new-2024-approved-peering-into-the-world-of-luts-and-their-effect-on-pixels/"><u>[New] 2024 Approved Peering Into the World of LUTs and Their Effect on Pixels</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/new-screencasting-app-performance-examination/"><u>[New] ScreenCasting App Performance Examination</u></a></li>
<li><a href="https://fox-http.techidaily.com/updated-uncomplicated-story-framework-for-2024/"><u>[Updated] Uncomplicated Story Framework for 2024</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/forgot-iphone-6-password-here-are-the-best-solutions-stellar-by-stellar-data-recovery-ios-iphone-data-recovery/"><u>Forgot iPhone 6 Password? – Here are the Best Solutions | Stellar</u></a></li>
<li><a href="https://android-unlock.techidaily.com/in-2024-lock-your-motorola-razr-40-ultra-phone-in-style-the-top-5-gesture-lock-screen-apps-by-drfone-android/"><u>In 2024, Lock Your Motorola Razr 40 Ultra Phone in Style The Top 5 Gesture Lock Screen Apps</u></a></li>
<li><a href="https://some-tips.techidaily.com/locating-your-apps-executable-in-no-time-a-fast-guide-for-windows-10-users/"><u>Locating Your App's Executable in No Time: A Fast Guide for Windows 10 Users</u></a></li>
<li><a href="https://some-tips.techidaily.com/maximize-productivity-convert-untapped-mac-keyboard-buttons-to-instant-shortcut-magic-using-our-simple-tool/"><u>Maximize Productivity: Convert Untapped Mac Keyboard Buttons to Instant Shortcut Magic Using Our Simple Tool</u></a></li>
<li><a href="https://some-tips.techidaily.com/migrating-applications-from-one-hard-drive-to-another-on-windows-11-a-step-by-step-guide/"><u>Migrating Applications From One Hard Drive to Another on Windows 11: A Step-by-Step Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/no-more-local-watches-netflix-abandons-windows-offline-download-feature/"><u>No More Local Watches? Netflix Abandons Windows Offline Download Feature</u></a></li>
<li><a href="https://some-tips.techidaily.com/revisiting-the-eco-friendly-era-the-case-for-apples-return-to-plastic-notebook-design/"><u>Revisiting the Eco-Friendly Era: The Case for Apple's Return to Plastic Notebook Design</u></a></li>
<li><a href="https://youtube-sure.techidaily.com/omplete-manual-for-creating-condensed-youtube-videos/"><u>The Complete Manual for Creating Condensed YouTube Videos</u></a></li>
</ul></div>

