---
title: Implementing Significant Enhancements in MSI Packages with the Help of WiX Toolset
date: 2024-10-02T17:24:32.682Z
updated: 2024-10-03T17:39:43.485Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Implementing Significant Enhancements in MSI Packages with the Help of WiX Toolset
thumbnail: https://thmb.techidaily.com/7b420d51a7e917d12325acc7124ce448649fcdb3a71e7a06fbd4b66d64319f0c.jpg
---

## Implementing Significant Enhancements in MSI Packages with the Help of WiX Toolset

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
<a href="https://appsumo.8odi.net/c/5597632/2049382/7443" target="_top" id="2049382">
  <img src="//a.impactradius-go.com/display-ad/7443-2049382" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2049382/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Using Advanced Installer Approach to Handle Major Upgrades

WiX toolset approach to perform a major upgrade to an MSI package requires adding new code to your XML file.

But, if you want to make this process smoother, Advanced Installer enables you to do that directly from its GUI without writing any code. Here's how you can achieve it:

Before getting started, make sure you have a **backup copy of the project file** before beginning to edit the.AIP project. This is known as the "old.AIP Project." 

1\. Increment the "Version" from the "Product Details" section by going to the "Product Details" page:

![Increment Version](https://cdn.advancedinstaller.com/img/wix-child-images/increment-version.png "Increment Version")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1880944/19272" target="_top" id="1880944">
  <img src="//a.impactradius-go.com/display-ad/19272-1880944" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1880944/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. Customize the new version of your software by making the necessary changes to the Installer Project.

![Important](https://cdn.advancedinstaller.com/svg/common/IconMessageInfo.svg)Keep in mind that the resources of the new version are all of your application's resources, not just those that are modified by this upgrade installation.

3\. Generate a new Product Code by clicking “Generate new”

![Generate New Product Code](https://cdn.advancedinstaller.com/img/wix-child-images/generate-new-product-code.png "Generate New Product Code")  

<!-- affiliate ads begin -->
<a href="https://review-au.sjv.io/c/5597632/2135316/14409" target="_top" id="2135316">
  <img src="//a.impactradius-go.com/display-ad/14409-2135316" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://review-au.sjv.io/i/5597632/2135316/14409" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://aligracehair.sjv.io/c/5597632/2006946/19272" target="_top" id="2006946">
  <img src="//a.impactradius-go.com/display-ad/19272-2006946" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2006946/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://article-files.techidaily.com/new-2024-approved-how-to-enhance-networked-stream-quality-with-vlc/"><u>[New] 2024 Approved How to Enhance Networked Stream Quality with VLC</u></a></li>
<li><a href="https://extra-information.techidaily.com/new-becoming-a-savvy-user-of-google-photos/"><u>[New] Becoming a Savvy User of Google Photos</u></a></li>
<li><a href="https://extra-hints.techidaily.com/2024-approved-apex-fusion-hubs-all-in-one-4k-multi-touch-desktops/"><u>2024 Approved Apex Fusion Hubs All-in-One 4K Multi-Touch Desktops</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyy-integration-launches-at-electionzcom-for-enhanced-data-processing/"><u>ABBYY Integration Launches at Electionz.com for Enhanced Data Processing</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyy-maintains-top-spot-in-the-smart-automation-industry/"><u>ABBYY Maintains Top Spot in the Smart Automation Industry</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyys-technological-mastery-skyrocketing-profits-with-a-60-increase-endorsed-by-the-esteemed-idc-marketscape-analysis/"><u>ABBYY's Technological Mastery: Skyrocketing Profits with a 60% Increase, Endorsed by the Esteemed IDC MarketScape Analysis</u></a></li>
<li><a href="https://some-tips.techidaily.com/automated-traffic-management-with-cookiebot-technology/"><u>Automated Traffic Management with Cookiebot Technology</u></a></li>
<li><a href="https://some-tips.techidaily.com/automated-with-cookiebot-streamlining-your-websites-data-collection/"><u>Automated with Cookiebot: Streamlining Your Website's Data Collection</u></a></li>
<li><a href="https://some-tips.techidaily.com/boosting-website-personalization-using-advanced-cookiebot-solutions/"><u>Boosting Website Personalization Using Advanced Cookiebot Solutions</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/how-to-mirror-apple-iphone-15-pro-max-to-windows-10-drfone-by-drfone-ios/"><u>How to Mirror Apple iPhone 15 Pro Max to Windows 10? | Dr.fone</u></a></li>
<li><a href="https://unlock-android.techidaily.com/in-2024-unlocking-made-easy-the-best-10-apps-for-unlocking-your-xiaomi-mix-fold-3-device-by-drfone-android/"><u>In 2024, Unlocking Made Easy The Best 10 Apps for Unlocking Your Xiaomi Mix Fold 3 Device</u></a></li>
<li><a href="https://extra-guidance.techidaily.com/seamlessly-blend-music-with-visuals-in-premiere-pro-for-2024/"><u>Seamlessly Blend Music with Visuals in Premiere Pro for 2024</u></a></li>
<li><a href="https://some-approaches.techidaily.com/the-essential-uav-upgrade-kit-must-haves-for-the-modern-pilot-for-2024/"><u>The Essential UAV Upgrade Kit - Must-Haves for the Modern Pilot for 2024</u></a></li>
</ul></div>

