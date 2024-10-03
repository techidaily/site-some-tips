---
title: "Step-by-Step Guide: File Removal During Uninstallation with WiX Toolset"
date: 2024-09-30T18:26:53.446Z
updated: 2024-10-03T17:17:32.538Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Step-by-Step Guide: File Removal During Uninstallation with WiX Toolset"
thumbnail: https://thmb.techidaily.com/acfc08d56b4206022979b3dc0ecd7952203549957dd5b874ab0b46f7e315b993.jpg
---

## Step-by-Step Guide: File Removal During Uninstallation with WiX Toolset

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

### How to remove files on uninstall using Advanced Installer?

Here is how you can remove the files created after the installation with Advanced Installer.

1\. Go to the **Files and Folders page**, and add a new File Removal.

![Add New File Removal](https://cdn.advancedinstaller.com/img/wix-child-images/add-new-file-removal.png "Add New File Removal")  

<!-- affiliate ads begin -->
<a href="https://bluettius.sjv.io/c/5597632/2139117/17108" target="_top" id="2139117">
  <img src="//a.impactradius-go.com/display-ad/17108-2139117" border="0" alt="https://techidaily.com" width="320" height="90"/>
</a>
<img height="0" width="0" src="https://bluettius.sjv.io/i/5597632/2139117/17108" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)To use the [**File Operations**](https://tools.techidaily.com/advancedinstaller/products/) feature in Advanced Installer, you need to have a Professional license or higher. Start with our [30-day full feature trial](https://tools.techidaily.com/advancedinstaller/products/).

<!-- affiliate ads begin -->
<a href="https://laganoo.pxf.io/c/5597632/1528693/16446" target="_top" id="1528693">
  <img src="//a.impactradius-go.com/display-ad/16446-1528693" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://laganoo.pxf.io/i/5597632/1528693/16446" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. In the New File Removal Dialog, fill in the **Name** field with the name of the file you want to be deleted. 

3\. For the **Component** field, you can choose any component you want.

4\. In the **Remove On** field, choose the Component uninstall option 

5\. And for the **Condition** field, use the REMOVE=”ALL” condition.

![Remove All Condition](https://cdn.advancedinstaller.com/img/wix-child-images/remove-all-condition.png "Remove All Condition")  

That’s it!

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135416/19272" target="_top" id="2135416">
  <img src="//a.impactradius-go.com/display-ad/19272-2135416" border="0" alt="https://techidaily.com" width="336" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135416/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<a href="https://appsumo.8odi.net/c/5597632/2043856/7443" target="_top" id="2043856">
  <img src="//a.impactradius-go.com/display-ad/7443-2043856" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2043856/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://facebook-video-footage.techidaily.com/updated-in-2024-dailymovement-vs-youtube-income-comparison/"><u>[Updated] In 2024, DailyMovement vs Youtube Income Comparison</u></a></li>
<li><a href="https://fox-glue.techidaily.com/updated-in-2024-perfect-guide-for-linking-instagram-to-tiktok/"><u>[Updated] In 2024, Perfect Guide for Linking Instagram to TikTok</u></a></li>
<li><a href="https://fox-info.techidaily.com/2024-approved-edit-away-bloat-organizing-your-overflow-of-tiktok-saves/"><u>2024 Approved Edit Away Bloat Organizing Your Overflow of TikTok Saves</u></a></li>
<li><a href="https://some-tips.techidaily.com/cookiebot-driven-data-collection-solutions/"><u>Cookiebot-Driven Data Collection Solutions</u></a></li>
<li><a href="https://some-tips.techidaily.com/cookiebot-driven-marketing-success-strategies/"><u>Cookiebot-Driven Marketing Success Strategies</u></a></li>
<li><a href="https://some-tips.techidaily.com/cookiebot-driven-unleashing-the-power-of-personalized-tracking/"><u>Cookiebot-Driven: Unleashing the Power of Personalized Tracking</u></a></li>
<li><a href="https://some-tips.techidaily.com/cookiebot-enabled-analytics-powering-your-digital-experience/"><u>Cookiebot-Enabled Analytics: Powering Your Digital Experience</u></a></li>
<li><a href="https://some-tips.techidaily.com/cookiebot-enabled-enhance-your-website-with-advanced-tracking-solutions/"><u>Cookiebot-Enabled: Enhance Your Website with Advanced Tracking Solutions</u></a></li>
<li><a href="https://some-tips.techidaily.com/cookiebot-enabled-enhance-your-websites-analytics-effortlessly/"><u>Cookiebot-Enabled: Enhance Your Website's Analytics Effortlessly</u></a></li>
<li><a href="https://activate-lock.techidaily.com/how-to-remove-icloud-on-apple-iphone-se-smoothly-by-drfone-ios/"><u>How To Remove iCloud On Apple iPhone SE Smoothly</u></a></li>
<li><a href="https://youtube-sure.techidaily.com/ng-selection-of-10-free-video-subtitle-extractors-for-2024/"><u>Leading Selection of 10 Free Video Subtitle Extractors for 2024</u></a></li>
<li><a href="https://youtube-stream.techidaily.com/maximizing-viewership-with-effective-game-streaming-for-2024/"><u>Maximizing Viewership with Effective Game Streaming for 2024</u></a></li>
<li><a href="https://easy-unlock-android.techidaily.com/pattern-locks-are-unsafe-secure-your-realme-narzo-60-5g-phone-now-with-these-tips-by-drfone-android/"><u>Pattern Locks Are Unsafe Secure Your Realme Narzo 60 5G Phone Now with These Tips</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/unleash-creative-potential-applying-effects-and-filters-on-zoom/"><u>Unleash Creative Potential Applying Effects and Filters on Zoom</u></a></li>
</ul></div>

