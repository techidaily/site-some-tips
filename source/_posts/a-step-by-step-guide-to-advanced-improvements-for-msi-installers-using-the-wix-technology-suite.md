---
title: A Step-by-Step Guide to Advanced Improvements for MSI Installers Using the WiX Technology Suite
date: 2024-10-01T16:45:09.628Z
updated: 2024-10-03T17:32:19.331Z
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

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2012429/19272" target="_top" id="2012429">
  <img src="//a.impactradius-go.com/display-ad/19272-2012429" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2012429/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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

### Using Advanced Installer Approach to Handle Major Upgrades

WiX toolset approach to perform a major upgrade to an MSI package requires adding new code to your XML file.

But, if you want to make this process smoother, Advanced Installer enables you to do that directly from its GUI without writing any code. Here's how you can achieve it:

Before getting started, make sure you have a **backup copy of the project file** before beginning to edit the.AIP project. This is known as the "old.AIP Project." 

1\. Increment the "Version" from the "Product Details" section by going to the "Product Details" page:

![Increment Version](https://cdn.advancedinstaller.com/img/wix-child-images/increment-version.png "Increment Version")  

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2145009/26400" target="_top" id="2145009">
  <img src="//a.impactradius-go.com/display-ad/26400-2145009" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2145009/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. Customize the new version of your software by making the necessary changes to the Installer Project.

![Important](https://cdn.advancedinstaller.com/svg/common/IconMessageInfo.svg)Keep in mind that the resources of the new version are all of your application's resources, not just those that are modified by this upgrade installation.

3\. Generate a new Product Code by clicking “Generate new”

![Generate New Product Code](https://cdn.advancedinstaller.com/img/wix-child-images/generate-new-product-code.png "Generate New Product Code")  

<!-- affiliate ads begin -->
<a href="https://sentrypc.7eer.net/c/5597632/398449/3022" target="_top" id="398449">
  <img src="//a.impactradius-go.com/display-ad/3022-398449" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://sentrypc.7eer.net/i/5597632/398449/3022" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://ephamedtechinc.pxf.io/c/5597632/2136613/26400" target="_top" id="2136613">
  <img src="//a.impactradius-go.com/display-ad/26400-2136613" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2136613/26400" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://youtube-zero.techidaily.com/nlock-youtubes-potential-essential-tips-and-techniques-for-optimal-titles-for-2024/"><u>[New] Unlock YouTube's Potential Essential Tips & Techniques for Optimal Titles for 2024</u></a></li>
<li><a href="https://some-approaches.techidaily.com/new-unveil-images-clearly-10-online-editors-guide/"><u>[New] Unveil Images Clearly 10 Online Editors' Guide</u></a></li>
<li><a href="https://fox-blue.techidaily.com/updated-in-2024-samsung-photo-editor-review-2023-pros-con-features-and-guide/"><u>[Updated] In 2024, Samsung Photo Editor Review 2023 - Pros, Con, Features, and Guide</u></a></li>
<li><a href="https://extra-guidance.techidaily.com/updated-perfecting-tiktok-media-with-zoom-techniques/"><u>[Updated] Perfecting TikTok Media with Zoom Techniques</u></a></li>
<li><a href="https://fox-direct.techidaily.com/updated-the-blueprint-of-an-engaging-podcast-blurb/"><u>[Updated] The Blueprint of an Engaging Podcast Blurb</u></a></li>
<li><a href="https://video-screen-grab.techidaily.com/2024-approved-screen-shot-entire-page-view/"><u>2024 Approved Screen Shot Entire Page View</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhance-user-engagement-with-our-cookiebot-integration-services/"><u>Enhance User Engagement with Our Cookiebot Integration Services</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhance-user-experience-and-conversions-through-cookiebot-driven-optimization/"><u>Enhance User Experience & Conversions Through Cookiebot-Driven Optimization</u></a></li>
<li><a href="https://tech-savvy.techidaily.com/enhanced-audience-engagement-through-intelligent-conversational-agents/"><u>Enhanced Audience Engagement Through Intelligent Conversational Agents</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhanced-conversion-rates-via-cutting-edge-cookiebot-analytics-tools/"><u>Enhanced Conversion Rates via Cutting-Edge Cookiebot Analytics Tools</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhanced-user-experience-with-advanced-cookiebot-technology/"><u>Enhanced User Experience with Advanced Cookiebot Technology</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhancing-driver-safety-and-productivity-learn-about-mobile-gps-tools-in-car-task-management-and-avoiding-distractions-on-the-road-tips-from-abbyy-experts.m13/"><u>Enhancing Driver Safety & Productivity: Learn About Mobile GPS Tools, In-Car Task Management, and Avoiding Distractions on the Road | Tips From ABBYY Experts</u></a></li>
<li><a href="https://tech-renaissance.techidaily.com/student-exclusive-deals-how-to-score-big-savings-on-your-next-dell-purchase/"><u>Student-Exclusive Deals: How to Score Big Savings on Your Next Dell Purchase</u></a></li>
</ul></div>

