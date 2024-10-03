---
title: "Tutorial: How to Include and Use .CAB Archives Within MSI Setup Files"
date: 2024-09-26T16:00:05.321Z
updated: 2024-10-03T19:30:59.766Z
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

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1886048/19272" target="_top" id="1886048">
  <img src="//a.impactradius-go.com/display-ad/19272-1886048" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1886048/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<a href="https://aligracehair.sjv.io/c/5597632/2012429/19272" target="_top" id="2012429">
  <img src="//a.impactradius-go.com/display-ad/19272-2012429" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2012429/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Using Advanced Installer's GUI to Manage CAB Files Within Your MSIs

 Advanced Installer offers multiple options to handle CAB files within your MSI. Watch our tutorial video to see how it works. 

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)If you want to see a comparison between WiX and Advanced Installer, check our article titled [Bundles-WiX vs. Advanced Installer](https://tools.techidaily.com/advancedinstaller/products/), where we discuss the basics of WiX - such as where to get it, how to install it, and how to create a bundle of two MSI applications with it.

<!-- affiliate ads begin -->
<a href="https://unicoeye.pxf.io/c/5597632/2134244/18498" target="_top" id="2134244">
  <img src="//a.impactradius-go.com/display-ad/18498-2134244" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://unicoeye.pxf.io/i/5597632/2134244/18498" style="position:absolute;visibility:hidden;" border="0" />
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
<span id="1977028">
					<video width="128" height="480" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1977028.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1977028">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1977028.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:80px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1977028%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1977028/22993" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://screen-activity-recording.techidaily.com/updated-2024-approved-quick-fire-methods-to-record-and-save-your-virtual-gatherings-windows-and-mac/"><u>[Updated] 2024 Approved Quick-Fire Methods to Record and Save Your Virtual Gatherings (Windows & Mac)</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/updated-plan-ahead-masterful-fb-timelines-using-free-resources/"><u>[Updated] Plan Ahead Masterful Fb Timelines Using Free Resources</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/updated-pro-gopro-filming-and-live-sharing-best-practices-for-facebookperiscope-for-2024/"><u>[Updated] Pro Gopro Filming and Live Sharing Best Practices for Facebook/Periscope for 2024</u></a></li>
<li><a href="https://location-fake.techidaily.com/6-ways-to-change-spotify-location-on-your-oppo-reno-10-proplus-5g-drfone-by-drfone-virtual-android/"><u>6 Ways to Change Spotify Location On Your Oppo Reno 10 Pro+ 5G | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/cookiebot-enhanced-the-ultimate-analytics-powerhouse/"><u>Cookiebot-Enhanced: The Ultimate Analytics Powerhouse</u></a></li>
<li><a href="https://some-tips.techidaily.com/customer-triumph-stories-effective-ai-adaptation-and-management-techniques/"><u>Customer Triumph Stories: Effective AI Adaptation and Management Techniques</u></a></li>
<li><a href="https://some-tips.techidaily.com/diving-deep-into-tech-jargon-understanding-ocr-and-idps-key-differences/"><u>Diving Deep Into Tech Jargon: Understanding OCR and IDP's Key Differences</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhance-site-personalization-with-advanced-cookiebot-technology/"><u>Enhance Site Personalization with Advanced Cookiebot Technology</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhance-your-marketing-strategy-using-cookiebot-solutions/"><u>Enhance Your Marketing Strategy Using Cookiebot Solutions</u></a></li>
<li><a href="https://tech-haven.techidaily.com/the-art-of-storytelling-enhanced-by-ais-intelligence/"><u>The Art of Storytelling Enhanced by AI's Intelligence</u></a></li>
<li><a href="https://some-guidance.techidaily.com/top-10-methods-for-seamlessly-moving-images-from-your-iphone-onto-a-mac/"><u>Top 10 Methods for Seamlessly Moving Images From Your iPhone Onto a Mac</u></a></li>
</ul></div>

