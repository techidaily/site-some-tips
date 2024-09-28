---
title: Effortless Deletion of Files in Uninstall Processes via the WiX Toolset Methodology
date: 2024-09-21T13:41:37.414Z
updated: 2024-09-28T03:32:04.176Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Effortless Deletion of Files in Uninstall Processes via the WiX Toolset Methodology
thumbnail: https://thmb.techidaily.com/773b13fe6e17412a9b5b64d4e711163f73a0c0700089624569da26ef89b36362.jpg
---

## Effortless Deletion of Files in Uninstall Processes via the WiX Toolset Methodology

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

## How to Remove Files on Uninstall Using WiX Toolset

When uninstalling an application, Windows Installer removes by default only the files that were created during the installation process. But, how about the files that are created after the installation? 

In this article, we will see how to remove the files created after the installation using WiX Toolset.

### How to remove files by adding a new component to an existing Component Group in WiX Toolset?

First, you need to add a new Component in an existing Component Group or create a new Component Group altogether – which will need to be referenced in one of the installer’s features.

Let’s imagine that you want to delete a file (sample.txt) that was created by the application in the Install Folder. To delete it, you have to add a new Component to the component group that manages the **Install Folder**. 

<Component Id="DeleteSample" Guid="*">
	<RemoveFile Id="Sample File" On="uninstall" Name="sample.txt"/>
</Component>

Copy

For this code to work, you have to replace the wildcard from the Guid property with a brand new Guid.

Alternatively, you can replace both the name and the extension of the file, in the Name property, with wildcards, making the installer delete the following:

* only the files having a certain name, by replacing the extension with a wildcard
* only the files having a certain extension, by replacing the name with a wildcard
* all the files, by replacing both the name and the extension with wildcards

The **RemoveFile** element removes a file if the parent component is selected for removal.

<!-- affiliate ads begin -->
<a href="https://laganoo.pxf.io/c/5597632/1484951/16446" target="_top" id="1484951">
  <img src="//a.impactradius-go.com/display-ad/16446-1484951" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://laganoo.pxf.io/i/5597632/1484951/16446" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to remove files on uninstall using Advanced Installer?

Here is how you can remove the files created after the installation with Advanced Installer.

1\. Go to the **Files and Folders page**, and add a new File Removal.

![Add New File Removal](https://cdn.advancedinstaller.com/img/wix-child-images/add-new-file-removal.png "Add New File Removal")  

<!-- affiliate ads begin -->
<span id="1982485">
					<video width="576" height="240" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1982485.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1982485">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1982485.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1982485%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1982485/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)To use the [**File Operations**](https://tools.techidaily.com/advancedinstaller/products/) feature in Advanced Installer, you need to have a Professional license or higher. Start with our [30-day full feature trial](https://tools.techidaily.com/advancedinstaller/products/).

<!-- affiliate ads begin -->
<span id="1983582">
					<video width="576" height="240" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1983582.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1983582">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1983582.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1983582%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1983582/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. In the New File Removal Dialog, fill in the **Name** field with the name of the file you want to be deleted. 

3\. For the **Component** field, you can choose any component you want.

4\. In the **Remove On** field, choose the Component uninstall option 

5\. And for the **Condition** field, use the REMOVE=”ALL” condition.

![Remove All Condition](https://cdn.advancedinstaller.com/img/wix-child-images/remove-all-condition.png "Remove All Condition")  

That’s it!

### Conclusion

As you see, you can choose between two different approaches when it comes to deleting files during the uninstall process. It is up to you to decide. 

If you prefer to configure your packages through the use of XML, you should go with the WiX Toolset. But if you want a fast and efficient solution, then the option of using the GUI that comes with Advanced Installer is for you.

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
<a href="https://aligracehair.sjv.io/c/5597632/2135353/19272" target="_top" id="2135353">
  <img src="//a.impactradius-go.com/display-ad/19272-2135353" border="0" alt="https://techidaily.com" width="180" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135353/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://youtube-lab.techidaily.com/n-2024-elegant-aesthetics-mastering-youtubes-beauty-landscape/"><u>[New] In 2024, Elegant Aesthetics Mastering YouTube's Beauty Landscape</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-premier-no-8-digital-composers-kit/"><u>[New] Premier No. 8 Digital Composer's Kit</u></a></li>
<li><a href="https://vp-tips.techidaily.com/updated-2024-approved-effortless-setup-of-streamlabs-for-mac-users-via-obs/"><u>[Updated] 2024 Approved Effortless Setup of Streamlabs for Mac Users via OBS</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-streamline-screen-capabilities-building-in-frame-video-experiences-on-sierra/"><u>[Updated] Streamline Screen Capabilities Building In-Frame Video Experiences on Sierra</u></a></li>
<li><a href="https://tiktok-clips.techidaily.com/2024-approved-key-to-generating-an-exclusive-tag-on-tiktok/"><u>2024 Approved Key to Generating an Exclusive Tag on TikTok</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-essential-guide-to-zooming-with-gmail-emails-professionally/"><u>2024 Approved The Essential Guide to Zooming with Gmail Emails Professionally</u></a></li>
<li><a href="https://fake-location.techidaily.com/apply-these-techniques-to-improve-how-to-detect-fake-gps-location-on-vivo-y28-5g-drfone-by-drfone-virtual-android/"><u>Apply These Techniques to Improve How to Detect Fake GPS Location On Vivo Y28 5G | Dr.fone</u></a></li>
<li><a href="https://win-forum.techidaily.com/free-converter-change-mpg-format-to-m4v-without-hitches/"><u>Free Converter: Change MPG Format to M4V Without Hitches</u></a></li>
<li><a href="https://techno-recovery.techidaily.com/how-to-send-recorded-phone-calls-on-apple-devices-effortlessly/"><u>How to Send Recorded Phone Calls on Apple Devices Effortlessly</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-top-10-high-quality-photography-lenses/"><u>In 2024, Top 10 High-Quality Photography Lenses</u></a></li>
<li><a href="https://extra-resources.techidaily.com/top-10-web-based-subtitle-editor-tools/"><u>Top 10 Web-Based Subtitle Editor Tools</u></a></li>
</ul></div>

