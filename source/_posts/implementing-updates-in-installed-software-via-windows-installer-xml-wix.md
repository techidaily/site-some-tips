---
title: Implementing Updates in Installed Software via Windows Installer XML (WiX)
date: 2024-09-23T23:13:23.736Z
updated: 2024-09-28T10:55:57.193Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Implementing Updates in Installed Software via Windows Installer XML (WiX)
thumbnail: https://thmb.techidaily.com/d1c93d03f28bcd5dba090eaa199ea22428e61a4a76d990245599509aeb0bc8f2.jpg
---

## Implementing Updates in Installed Software via Windows Installer XML (WiX)

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

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2087239/19272" target="_top" id="2087239">
  <img src="//a.impactradius-go.com/display-ad/19272-2087239" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2087239/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to Create a Windows Forms Application in Visual Studio

For this tutorial, we'll use Visual Studio to create a simple Windows Forms application that will be installed and then updated. To create the application, follow the next steps:

1\. Go to _File → New → Project_.

![Visual Studio to create a simple Windows Forms](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/visual-studio-to-create-a-simple-windows-forms.png "Visual Studio to create a simple Windows Forms")  

2\. From the templates list, select _Windows Forms App_.

![select Windows Forms App](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/select-windows-forms-app.png "select Windows Forms App")  

3\. Configure your project in the configuration dialog and then press the _Create_ button.

![Configure your project in the configuration dialog](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/configure-your-project-in-the-configuration-dialog.png "Configure your project in the configuration dialog")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135361/19272" target="_top" id="2135361">
  <img src="//a.impactradius-go.com/display-ad/19272-2135361" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135361/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to Add the Setup Project for WiX in Visual Studio

Now, let’s create the installer package for our application. We need to add a setup project to our solution, and for this we'll use the WiX extension for Visual Studio. 

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Make sure you have the WiX extension added to Visual Studio. You’ll also need the Wax extension which provides a setup editor to help you create, verify and maintain the list of deployed files.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2100530/7443" target="_top" id="2100530">
  <img src="//a.impactradius-go.com/display-ad/7443-2100530" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2100530/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

Follow the next steps to add the setup project:

1\. Right-click on the Project Solution → Add → New project.

![Add the Setup Project for WiX in Visual Studio](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/add-the-setup-project-for-wix-in-visual-studio.png "Add the Setup Project for WiX in Visual Studio")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2151893/7443" target="_top" id="2151893">
  <img src="//a.impactradius-go.com/display-ad/7443-2151893" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2151893/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. From Templates, select _Setup Project for WiX_.

![Setup Project for WiX](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/setup-project-for-wix.png "Setup Project for WiX")  

3\. Configure the project and press the _Create_ button.

![Configure the project](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/configure-the-project.png "Configure the project")  

Once the setup project is added, you should see it in the Solution Explorer.

![Solution Explorer](https://cdn.advancedinstaller.com/img/update-application-using-wix-installer/solution-explorer.png "Solution Explorer")  

### How to add the project output using the WiX Setup Editor

Next, we’ll use the WiX Setup Editor to add the deployable files to our setup project. To open the editor, go to _Tools → WiX Setup Editor_. Then, make the following configurations:

1. Select the _Setup Project_ added to your application.
2. In the _Root_ directory, select _INSTALLFOLDER_.
3. Then, in the _Projects_ to install section, select the application you’re creating the installer for.

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

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2037474/7443" target="_top" id="2037474">
  <img src="//a.impactradius-go.com/display-ad/7443-2037474" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2037474/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<li><a href="https://youtube-tips.techidaily.com/n-2024-mastering-youtube-screens-final-touches/"><u>[New] In 2024, Mastering YouTube Screens' Final Touches</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-streamlined-editing-best-apps-compatible-with-macos-big-sur/"><u>[New] Streamlined Editing Best Apps Compatible with macOS Big Sur</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-quintessential-collection-of-anime-intros/"><u>[New] The Quintessential Collection of Anime Intros</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unveiling-the-typical-podcasters-income/"><u>[New] Unveiling the Typical Podcaster's Income</u></a></li>
<li><a href="https://vp-tips.techidaily.com/updated-in-2024-ultimate-shooting-top-10-high-definition-dslr-stands/"><u>[Updated] In 2024, Ultimate Shooting Top 10 High-Definition DSLR Stands</u></a></li>
<li><a href="https://instagram-video-recordings.techidaily.com/updated-the-ultimate-guidebook-to-making-wealth-on-instagram-for-2024/"><u>[Updated] The Ultimate Guidebook to Making Wealth on Instagram for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-ultimate-simplified-journey-for-metaverse-personas/"><u>2024 Approved The Ultimate Simplified Journey for Metaverse Personas</u></a></li>
<li><a href="https://extra-tips.techidaily.com/bring-life-and-movement-to-stills-with-illustrator-techniques/"><u>Bring Life & Movement to Stills with Illustrator Techniques</u></a></li>
<li><a href="https://techtrends.techidaily.com/decoding-the-mystery-fixing-windows-troubling-code-31-problems-with-ease/"><u>Decoding the Mystery: Fixing Windows' Troubling Code 31 Problems with Ease</u></a></li>
<li><a href="https://howto.techidaily.com/how-to-quickly-fix-bluetooth-not-working-on-oppo-k11x-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How to Quickly Fix Bluetooth Not Working on Oppo K11x | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unparalleled-hands-on-gear-in-the-vr-world/"><u>In 2024, Unparalleled Hands-On Gear in the VR World</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/recommended-best-applications-for-mirroring-your-oneplus-11-5g-screen-drfone-by-drfone-android/"><u>Recommended Best Applications for Mirroring Your OnePlus 11 5G Screen | Dr.fone</u></a></li>
<li><a href="https://fox-direct.techidaily.com/smart-image-management-on-ios-devices/"><u>Smart Image Management on iOS Devices</u></a></li>
</ul></div>

