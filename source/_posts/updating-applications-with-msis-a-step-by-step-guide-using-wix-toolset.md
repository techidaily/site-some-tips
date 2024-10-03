---
title: "Updating Applications with MSIs: A Step-by-Step Guide Using WiX Toolset"
date: 2024-09-27T18:19:19.973Z
updated: 2024-10-03T17:31:58.684Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Updating Applications with MSIs: A Step-by-Step Guide Using WiX Toolset"
thumbnail: https://thmb.techidaily.com/e0d972d2fcbdfdcba3e132e48f8036c4f80fa7e20c32444994977f3585d2732d.jpeg
---

## Updating Applications with MSIs: A Step-by-Step Guide Using WiX Toolset

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

## How to Use WiX MSI to Update an Installed Application

Written by [Renato Ivanescu](https://tools.techidaily.com/advancedinstaller/products/) · April 27th, 2023

The process of developing software should always include a solid mechanism for application upgrades.

In this article, we will see how we can use WiX to create an installation package that will install a new version of an MSI application after removing the previous one.

### How to Create a Windows Forms Application in Visual Studio

For this tutorial, we'll use Visual Studio to create a simple Windows Forms application that will be installed and then updated. To create the application, follow the next steps:

1\. Go to _File → New → Project_.

![Visual Studio to create a simple Windows Forms](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/visual-studio-to-create-a-simple-windows-forms.png "Visual Studio to create a simple Windows Forms")  

2\. From the templates list, select _Windows Forms App_.

![select Windows Forms App](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/select-windows-forms-app.png "select Windows Forms App")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2105869/7443" target="_top" id="2105869">
  <img src="//a.impactradius-go.com/display-ad/7443-2105869" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2105869/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

3\. Configure your project in the configuration dialog and then press the _Create_ button.

![Configure your project in the configuration dialog](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/configure-your-project-in-the-configuration-dialog.png "Configure your project in the configuration dialog")  

### How to Add the Setup Project for WiX in Visual Studio

Now, let’s create the installer package for our application. We need to add a setup project to our solution, and for this we'll use the WiX extension for Visual Studio. 

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Make sure you have the WiX extension added to Visual Studio. You’ll also need the Wax extension which provides a setup editor to help you create, verify and maintain the list of deployed files.

Follow the next steps to add the setup project:

1\. Right-click on the Project Solution → Add → New project.

![Add the Setup Project for WiX in Visual Studio](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/add-the-setup-project-for-wix-in-visual-studio.png "Add the Setup Project for WiX in Visual Studio")  

2\. From Templates, select _Setup Project for WiX_.

![Setup Project for WiX](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/setup-project-for-wix.png "Setup Project for WiX")  

3\. Configure the project and press the _Create_ button.

![Configure the project](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/configure-the-project.png "Configure the project")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1975816/19272" target="_top" id="1975816">
  <img src="//a.impactradius-go.com/display-ad/19272-1975816" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1975816/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

Once the setup project is added, you should see it in the Solution Explorer.

![Solution Explorer](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/solution-explorer.png "Solution Explorer")  

<!-- affiliate ads begin -->
<a href="https://bluettius.sjv.io/c/5597632/2139108/17108" target="_top" id="2139108">
  <img src="//a.impactradius-go.com/display-ad/17108-2139108" border="0" alt="https://techidaily.com" width="250" height="90"/>
</a>
<img height="0" width="0" src="https://bluettius.sjv.io/i/5597632/2139108/17108" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to add the project output using the WiX Setup Editor

Next, we’ll use the WiX Setup Editor to add the deployable files to our setup project. To open the editor, go to _Tools → WiX Setup Editor_. Then, make the following configurations:

1. Select the _Setup Project_ added to your application.
2. In the _Root_ directory, select _INSTALLFOLDER_.
3. Then, in the _Projects_ to install section, select the application you’re creating the installer for.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2132162/7443" target="_top" id="2132162">
  <img src="//a.impactradius-go.com/display-ad/7443-2132162" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2132162/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to set the WiX Installer Version of Your Application

Before we create the MSI and install the application, let’s set a version number for our application. 

Edit the **Product.wxs** file in the setup project and set the product version to 1.0.1 as seen below:

<Product Id = "*" 
		    Name = "DemoApp" 
	                  Language = "1033" 
	                  Version = "1.0.1" 
	                  Manufacturer = "Caphyon" 
	                  UpgradeCode = "3c9e2988-90a2-4319-b261-674543c2dc16">

Copy

Now you can build the project and install your application by running the MSI file. You can find it in the setup project → bin → Debug. When the application is installed, you should find it in the programs list in **version 1.0.1**.

<!-- affiliate ads begin -->
<a href="https://zebaoaffiliateprogram.pxf.io/c/5597632/2137973/21526" target="_top" id="2137973">
  <img src="//a.impactradius-go.com/display-ad/21526-2137973" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://zebaoaffiliateprogram.pxf.io/i/5597632/2137973/21526" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to update the application

Let’s suppose we made some changes to our application. We’ll generate a new MSI that will uninstall the previous version and install the new one. For that, you must follow these steps:

1\. Make sure you change the _Product ID_. This is a unique GUID used to identify your application. To avoid setting it manually, you can replace it with the “\*” symbol. Thus, it changes every time you build the project. 

2\. Let’s also increase the version number from 1.0.1 to 1.0.2.

<Product Id = "*" 
		    Name = "DemoApp" 
	                  Language = "1033" 
	                  Version = "1.0.2" 
	                  Manufacturer = "Caphyon" 
	                  UpgradeCode = "3c9e2988-90a2-4319-b261-674543c2dc16">

Copy

3\. Keep your _UpgradeCode_ constant. As you can see, the _UpgradeCode_ remains the same for the updated version.

4\. Use the _MajorUpgrade_ element. This element includes the most common options for updates. If you increase the version number at the first step, you only have to add the _MajorUpgrade_ element with no other attribute, like in the example below:

<MajorUpgrade 
             DowngradeErrorMessage = "A newer version of [ProductName] is already installed."
 />

Copy

5\. In addition, if you want the new application version to keep the previous version number (in our example 1.0.1), you have to set the attribute _AllowSameVersionUpgrade_ to yes.

<MajorUpgrade 
             DowngradeErrorMessage = "A newer version of [ProductName] is already installed."
   	AllowSameVersionUpgrades = "yes"
 />

Copy

Once you complete the steps above, you can build and run the MSI. The previous version of your application will be uninstalled, and the new one will be installed.

### Conclusion

WiX allows you to upgrade an application's installed version by modifying the XML-based definition file. Alternatively, you can use Advanced Installer's GUI, which enables you to upgrade your application instantly.

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
<li><a href="https://facebook-video-share.techidaily.com/new-channel-milestone-hurdle-cross-the-10k-view-threshold-fast-for-2024/"><u>[New] Channel Milestone Hurdle – Cross the 10K View Threshold Fast for 2024</u></a></li>
<li><a href="https://discord-videos.techidaily.com/new-premium-font-fabrication-tools-for-discord-users/"><u>[New] Premium Font Fabrication Tools for Discord Users</u></a></li>
<li><a href="https://article-tips.techidaily.com/new-the-innovators-playbook-for-premiere-pro-fullscreen-edits/"><u>[New] The Innovator's Playbook for Premiere Pro Fullscreen Edits</u></a></li>
<li><a href="https://remote-screen-capture.techidaily.com/updated-5-best-snipping-tools-for-pc-for-2024/"><u>[Updated] 5 Best Snipping Tools for Pc for 2024</u></a></li>
<li><a href="https://fox-direct.techidaily.com/2024-approved-the-essential-guide-to-podcast-title-selection-strategies-and-examples/"><u>2024 Approved The Essential Guide to Podcast Title Selection Strategies & Examples</u></a></li>
<li><a href="https://apple-account.techidaily.com/a-step-by-step-guide-to-finding-your-apple-id-from-your-iphone-8-plus-by-drfone-ios/"><u>A Step-by-Step Guide to Finding Your Apple ID From Your iPhone 8 Plus</u></a></li>
<li><a href="https://techidaily.com/how-to-transfer-whatsapp-from-apple-iphone-14-pro-max-to-other-iphone-13-pro-devices-drfone-by-drfone-transfer-whatsapp-from-ios-transfer-whatsapp-from-ios/"><u>How To Transfer WhatsApp From Apple iPhone 14 Pro Max to other iPhone 13 Pro devices? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/revitalizing-microsoft-top-5-strategies-to-enhance-windows-experience/"><u>Revitalizing Microsoft: Top 5 Strategies to Enhance Windows Experience</u></a></li>
<li><a href="https://some-tips.techidaily.com/rotating-your-pictures-with-ease-a-step-by-step-guide-for-windows-11-users/"><u>Rotating Your Pictures with Ease: A Step-by-Step Guide for Windows 11 Users</u></a></li>
<li><a href="https://some-tips.techidaily.com/solving-the-problem-unsuccessful-booting-in-windows-systems/"><u>Solving the Problem: Unsuccessful Booting in Windows Systems</u></a></li>
<li><a href="https://some-tips.techidaily.com/step-by-step-guide-restoring-headphone-functionality-on-windows-11-systems/"><u>Step-by-Step Guide: Restoring Headphone Functionality on Windows 11 Systems</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-reasons-behind-my-choice-avoiding-iphone-and-ipad-applications-on-my-mac/"><u>The Reasons Behind My Choice: Avoiding iPhone and iPad Applications on My Mac</u></a></li>
<li><a href="https://technical-tips.techidaily.com/turn-those-funny-gif-animations-into-professional-mp4-footage-with-movavis-simple-conversion-solution/"><u>Turn Those Funny GIF Animations Into Professional MP4 Footage with Movavi's Simple Conversion Solution</u></a></li>
</ul></div>

