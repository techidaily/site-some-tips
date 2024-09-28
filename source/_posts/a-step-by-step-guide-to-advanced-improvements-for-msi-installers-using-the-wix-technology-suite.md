---
title: A Step-by-Step Guide to Advanced Improvements for MSI Installers Using the WiX Technology Suite
date: 2024-09-22T00:32:38.113Z
updated: 2024-09-28T11:24:49.308Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes A Step-by-Step Guide to Advanced Improvements for MSI Installers Using the WiX Technology Suite
thumbnail: https://thmb.techidaily.com/2fabafc66fe8d6c738eceaf2d94bef9969abb79ce6dfc7f79cdd9561a56a5238.jpg
---

## A Step-by-Step Guide to Advanced Improvements for MSI Installers Using the WiX Technology Suite

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

## How to create major upgrades for MSI packages using WiX Toolset

Deploying major upgrades for an MSI package created with WiX Toolset is simple. However, there are a few boxes you need to check to make sure you're doing it properly. We'll share them with you in this article!

### What makes major upgrades different from patches?

Unlike patches, major upgrades require a complete reinstallation of the application. When the application is upgraded, the old version is completely removed from the system, and then the new version is installed.

Every major version of an application is treated as a separate application by the OS, and according to Windows Installer standards, its MSI **must have a unique product code**.

### How to implement a major upgrade using WiX Toolset

To implement a major upgrade in WiX Toolset, you need to keep some things in mind.

1\. In the Product element, the **ID** should remain a wildcard. This ensures that the MSI package will generate a different product code each time we build it.

2\. The **UpgradeCode** should remain constant, in order to correctly link the different versions of the package.

Here is an example of a proper Product element:

<Product Id="*" Name="Sample Application" Language="1033" Version="1.0.0.0" Manufacturer="Caphyon" UpgradeCode="ca61b68b-a4ca-452f-9cd7-5ffcd2558b5d">
…………………………
</Product>

Copy

3\. To handle changing any version of the product, you have to add the **MajorUpgrade** element in the Product element, as follows:

<MajorUpgrade AllowSameVersionUpgrades="yes" DowngradeErrorMessage="A newer version of [ProductName] is already installed." />

Copy

This addition ensures that even version 1.0.0.1 is going to be perceived as a major upgrade. Otherwise, you may see multiple side by side installations of your application in Programs and Features.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1997662/19272" target="_top" id="1997662">
  <img src="//a.impactradius-go.com/display-ad/19272-1997662" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1997662/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Using Advanced Installer Approach to Handle Major Upgrades

WiX toolset approach to perform a major upgrade to an MSI package requires adding new code to your XML file.

But, if you want to make this process smoother, Advanced Installer enables you to do that directly from its GUI without writing any code. Here's how you can achieve it:

Before getting started, make sure you have a **backup copy of the project file** before beginning to edit the.AIP project. This is known as the "old.AIP Project." 

1\. Increment the "Version" from the "Product Details" section by going to the "Product Details" page:

![Increment Version](https://cdn.advancedinstaller.com/img/wix-child-images/increment-version.png "Increment Version")  

2\. Customize the new version of your software by making the necessary changes to the Installer Project.

![Important](https://cdn.advancedinstaller.com/svg/common/IconMessageInfo.svg)Keep in mind that the resources of the new version are all of your application's resources, not just those that are modified by this upgrade installation.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2151873/7443" target="_top" id="2151873">
  <img src="//a.impactradius-go.com/display-ad/7443-2151873" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2151873/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

3\. Generate a new Product Code by clicking “Generate new”

![Generate New Product Code](https://cdn.advancedinstaller.com/img/wix-child-images/generate-new-product-code.png "Generate New Product Code")  

<!-- affiliate ads begin -->
<a href="https://unicoeye.pxf.io/c/5597632/2134241/18498" target="_top" id="2134241">
  <img src="//a.impactradius-go.com/display-ad/18498-2134241" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://unicoeye.pxf.io/i/5597632/2134241/18498" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

And you’re done.

Watch the video below to learn how you can complete this task more easily with Advanced Installer:

### Conclusion

As you can see, WiX offers you the capability to handle major upgrades by using the **MajorUpgrade** element within the XML-based definition file. But that is error-prone.

If you need an easier and foolproof solution, then you can use Advanced Installer’s GUI.

Which one do you prefer? Let us know in the comments.

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
<a href="https://unicoeye.pxf.io/c/5597632/2134233/18498" target="_top" id="2134233">
  <img src="//a.impactradius-go.com/display-ad/18498-2134233" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://unicoeye.pxf.io/i/5597632/2134233/18498" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://screen-capture.techidaily.com/new-2024-approved-mitigating-high-bitrate-in-obs-outputs/"><u>[New] 2024 Approved Mitigating High-Bitrate in OBS Outputs</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-sharpen-your-shots-canon-offers-freepaid-lut-edits/"><u>[New] Sharpen Your Shots Canon Offers Free/Paid LUT Edits</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-superior-script-architect-space/"><u>[Updated] Superior Script Architect Space</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-proper-way-to-link-zoom-and-your-gmail-accounts/"><u>[Updated] The Proper Way to Link Zoom and Your Gmail Accounts</u></a></li>
<li><a href="https://location-social.techidaily.com/does-nokia-c110-have-find-my-friends-drfone-by-drfone-virtual-android/"><u>Does Nokia C110 Have Find My Friends? | Dr.fone</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/free-and-open-source-video-capturing-tools-for-2024/"><u>Free & Open Source Video Capturing Tools for 2024</u></a></li>
<li><a href="https://ios-pokemon-go.techidaily.com/in-2024-hacks-to-do-pokemon-go-trainer-battles-for-apple-iphone-15-pro-drfone-by-drfone-virtual-ios/"><u>In 2024, Hacks to do pokemon go trainer battles For Apple iPhone 15 Pro | Dr.fone</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/in-2024-ipogo-will-be-the-new-ispoofer-on-tecno-pop-7-pro-drfone-by-drfone-virtual-android/"><u>In 2024, iPogo will be the new iSpoofer On Tecno Pop 7 Pro? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-ultimate-resource-50plus-no-fee-visual-effects-websites-reviewed-for-2024/"><u>The Ultimate Resource 50+ No-Fee Visual Effects Websites Reviewed for 2024</u></a></li>
</ul></div>

