---
title: "1. Implementing CustomActions in WiX: Integrating CustomActionData Seamlessly"
date: 2024-09-27T17:26:10.300Z
updated: 2024-10-03T19:08:29.857Z
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
<a href="https://aligracehair.sjv.io/c/5597632/2135399/19272" target="_top" id="2135399">
  <img src="//a.impactradius-go.com/display-ad/19272-2135399" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135399/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to configure CustomActions with Advanced Installer?

If you use Advanced Installer to build and create your MSI, there is no need for an extra CustomAction to set the property of interest with the same name as the Deferred CustomAction.

All you need to do is specify the value of the CustomActionData property within the “ActionData” and Advanced Installer does the rest for you.

![Configure CustomActions](https://cdn.advancedinstaller.com/img/wix-pass-customactiondata-to-customaction/configure-custom-actions.png "Configure CustomActions")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2094476/7443" target="_top" id="2094476">
  <img src="//a.impactradius-go.com/display-ad/7443-2094476" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2094476/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Have a look at our [How to Use CustomActionData to Access Windows Installer Properties in Deferred CustomActions](https://tools.techidaily.com/advancedinstaller/products/) article to find out more about:- Why do you need CustomActionData- When can Deferred CustomActions go wrong- How you can pass CustomActionData to a CustomAction using Advanced Installer

<!-- affiliate ads begin -->
<a href="https://malaysia-healthcare-travel-council.pxf.io/c/5597632/1576474/17382" target="_top" id="1576474">
  <img src="//a.impactradius-go.com/display-ad/17382-1576474" border="0" alt="https://techidaily.com" width="160" height="90"/>
</a>
<img height="0" width="0" src="https://malaysia-healthcare-travel-council.pxf.io/i/5597632/1576474/17382" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://aligracehair.sjv.io/c/5597632/2135364/19272" target="_top" id="2135364">
  <img src="//a.impactradius-go.com/display-ad/19272-2135364" border="0" alt="https://techidaily.com" width="120" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135364/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://extra-skills.techidaily.com/new-step-by-step-guide-iphone-picture-perfection/"><u>[New] Step-by-Step Guide IPhone Picture Perfection</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/2024-approved-unleashing-creativity-in-instagram-photography-through-border-use/"><u>2024 Approved Unleashing Creativity in Instagram Photography Through Border Use</u></a></li>
<li><a href="https://hardware-help.techidaily.com/asrocks-stunning-32-oled-display-with-enhanced-color-at-480hz-a-visual-delight-and-network-companion/"><u>ASROCK's Stunning 32 OLED Display with Enhanced Color at 480Hz: A Visual Delight and Network Companion</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhanced-user-experience-with-dynamic-content-powered-by-cookiebot/"><u>Enhanced User Experience with Dynamic Content: Powered by Cookiebot</u></a></li>
<li><a href="https://some-tips.techidaily.com/establishing-trustworthiness-through-identification-verification-in-the-digital-era-of-banking/"><u>Establishing Trustworthiness Through Identification Verification in the Digital Era of Banking</u></a></li>
<li><a href="https://some-tips.techidaily.com/evolution-of-abbyy-embracing-a-new-identity-with-an-emphasis-on-organizational-growth-and-personnel-empowerment/"><u>Evolution of ABBYY: Embracing a New Identity with an Emphasis on Organizational Growth and Personnel Empowerment</u></a></li>
<li><a href="https://some-tips.techidaily.com/future-leaders-expect-more-process-clarity-and-innovative-tech-reveals-abbyy-research-on-wfh-adaptations/"><u>Future Leaders Expect More Process Clarity and Innovative Tech, Reveals ABBYY Research on WFH Adaptations</u></a></li>
<li><a href="https://fox-that.techidaily.com/get-siri-back-on-track-essential-tips-and-tricks-for-iphones-and-ipads/"><u>Get Siri Back On Track: Essential Tips and Tricks for iPhones & iPads</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-repair-broken-video-files-of-huawei-p60-pro-by-stellar-video-repair-mobile-video-repair/"><u>How to Repair Broken video files of Huawei P60 Pro?</u></a></li>
<li><a href="https://fox-helps.techidaily.com/in-depth-analysis-navigating-zoom-for-webinars-and-livestreams-for-2024/"><u>In-Depth Analysis Navigating Zoom for Webinars and Livestreams for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/is-genuine-consumer-centric-approach-now-at-the-forefront-of-insurance-claims/"><u>Is Genuine Consumer-Centric Approach Now at the Forefront of Insurance Claims?</u></a></li>
<li><a href="https://some-tips.techidaily.com/leverage-advanced-traffic-insights-the-power-of-cookiebot-technology-on-websites/"><u>Leverage Advanced Traffic Insights: The Power of Cookiebot Technology on Websites</u></a></li>
<li><a href="https://techtrends.techidaily.com/step-by-step-guide-why-your-pc-cant-exit-windows-11-properly-and-how-to-fix-it/"><u>Step-by-Step Guide: Why Your PC Can't Exit Windows 11 Properly and How to Fix It</u></a></li>
<li><a href="https://windows11.techidaily.com/win-11-tackle-icons-not-aligned/"><u>Win 11: Tackle Icons Not Aligned</u></a></li>
</ul></div>

