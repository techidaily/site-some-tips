---
title: "Tutorial: How to Include and Use .CAB Archives Within MSI Setup Files"
date: 2024-09-21T04:21:25.846Z
updated: 2024-09-28T10:02:46.640Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Tutorial: How to Include and Use .CAB Archives Within MSI Setup Files"
thumbnail: https://thmb.techidaily.com/880ddd263e214c3b4ae0eb5fd84c0b63be50232aa4ce3a994c19ff834b47aa92.jpg
---

## Tutorial: How to Include and Use .CAB Archives Within MSI Setup Files

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
<a href="https://appsumo.8odi.net/c/5597632/2111965/7443" target="_top" id="2111965">
  <img src="//a.impactradius-go.com/display-ad/7443-2111965" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2111965/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://aligracehair.sjv.io/c/5597632/1938721/19272" target="_top" id="1938721">
  <img src="//a.impactradius-go.com/display-ad/19272-1938721" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1938721/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Using Advanced Installer's GUI to Manage CAB Files Within Your MSIs

 Advanced Installer offers multiple options to handle CAB files within your MSI. Watch our tutorial video to see how it works. 

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)If you want to see a comparison between WiX and Advanced Installer, check our article titled [Bundles-WiX vs. Advanced Installer](https://tools.techidaily.com/advancedinstaller/products/), where we discuss the basics of WiX - such as where to get it, how to install it, and how to create a bundle of two MSI applications with it.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1997717/19272" target="_top" id="1997717">
  <img src="//a.impactradius-go.com/display-ad/19272-1997717" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1997717/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<a href="https://appsumo.8odi.net/c/5597632/2144283/7443" target="_top" id="2144283">
  <img src="//a.impactradius-go.com/display-ad/7443-2144283" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2144283/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://some-skills.techidaily.com/new-symbolizing-success-crafting-effective-podcast-logos/"><u>[New] Symbolizing Success Crafting Effective Podcast Logos</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-understanding-the-transformations-in-vegaspro-19/"><u>[New] Understanding the Transformations in VegasPro '19</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unmatched-audio-and-video-elite-webcams-for-podcasting/"><u>[New] Unmatched Audio & Video Elite Webcams for Podcasting</u></a></li>
<li><a href="https://fox-hovers.techidaily.com/buzzing-the-net-with-humor-your-comprehensive-guide-to-9gag/"><u>Buzzing the Net with Humor Your Comprehensive Guide to 9GAG</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/expert-analysis-jackery-powerbar-portable-charger-with-integrated-ac-output/"><u>Expert Analysis: Jackery PowerBar Portable Charger with Integrated AC Output</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-restore-deleted-htc-u23-pro-pictures-an-easy-method-explained-by-fonelab-android-recover-pictures/"><u>How to Restore Deleted HTC U23 Pro Pictures An Easy Method Explained.</u></a></li>
<li><a href="https://review-topics.techidaily.com/how-to-unlock-nokia-g310-without-password-by-drfone-android-unlock-android-unlock/"><u>How to Unlock Nokia G310 Without Password?</u></a></li>
<li><a href="https://unlock-android.techidaily.com/in-2024-how-to-unlock-honor-90-pro-phone-with-broken-screen-by-drfone-android/"><u>In 2024, How to Unlock Honor 90 Pro Phone with Broken Screen</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-maximizing-your-designs-with-free-clip-art/"><u>In 2024, Maximizing Your Designs with FREE Clip Art</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-swiftly-assemble-a-stunning-google-image-mosaic-with-ease/"><u>In 2024, Swiftly Assemble a Stunning Google Image Mosaic with Ease</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-experts-method-for-timestamping-your-youtube-videos/"><u>In 2024, The Expert's Method for Timestamping Your YouTube Videos</u></a></li>
<li><a href="https://techidaily.com/simple-ways-to-get-lost-videos-back-from-g24-power-by-fonelab-android-recover-video/"><u>Simple ways to get lost videos back from G24 Power</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-10-sci-fi-vr-adventures-new-realms-unveiled-for-2024/"><u>Top 10 Sci-Fi VR Adventures New Realms Unveiled for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-potential-the-right-propeller-match-in-fpv-flight-for-2024/"><u>Unlocking Potential The Right Propeller Match in FPV Flight for 2024</u></a></li>
<li><a href="https://techidaily.com/video-file-repair-how-to-fix-corrupted-video-files-of-gt-5-by-stellar-video-repair-mobile-video-repair/"><u>Video File Repair - How to Fix Corrupted video files of GT 5?</u></a></li>
</ul></div>

