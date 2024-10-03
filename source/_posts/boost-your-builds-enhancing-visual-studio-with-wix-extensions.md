---
title: "Boost Your Builds: Enhancing Visual Studio with WiX Extensions"
date: 2024-10-02T18:11:45.644Z
updated: 2024-10-03T18:11:56.922Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Boost Your Builds: Enhancing Visual Studio with WiX Extensions"
thumbnail: https://thmb.techidaily.com/a284b8622794b8ba45f3866eaa63e737e0684e210dde0d1e1927202914413ca4.jpg
---

## Boost Your Builds: Enhancing Visual Studio with WiX Extensions

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

## WiX Toolset Visual Studio Extension

Written by [Renato Ivanescu](https://tools.techidaily.com/advancedinstaller/products/) · June 15th, 2023

As part of the software packaging industry, you're most likely familiar with Windows Installer XML, or WiX. The WiX Toolset is widely used to build Windows Installer packages. 

WiX is more like a programming tool; it uses XMLs and does not have a graphical interface like some other similar tools. So, it uses a different approach to define the elements inside an installation package. 

WiX Toolset has an extension that lets you use the Visual Studio IDE to create and compile setup projects. In this article, we will be guiding you through the creation of an installation package for a Windows Forms application using the **WiX Toolset Visual Studio Extension**. 

### How to add the WiX Toolset extension to Visual Studio?

We first need to add the WiX Toolset extension to the Visual Studio IDE before creating the installation package for the application. To do that, follow the next steps:

1\. Go to _Extensions_ → _Manage Extensions_.

2\. In the _Manage Extensions_ dialog, go to the _Online_ section.

3\. Search for _WiX Toolset Visual Studio Extension_.

![Search for WiX Toolset Visual Studio Extension](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/search-for-wix-toolset-visual-studio-extension.png "Search for WiX Toolset Visual Studio Extension")  

4\. Press the _Download_ button. Pay attention to the fact that the changes will be made after you close Visual Studio IDE. 

In addition to installing the WiX extension, you also need to install the WiX Toolset build tools if you haven’t already. That way, you’ll be able to build the setup project that will be added to your application.

When creating the setup project for an application, you need to add the deployable files and keep them up-to-date. This task can be difficult if you are using WiX, especially when you are a beginner, as it needs to be done programmatically.

So, we will install a second extension, namely the Wax extension. It provides an interactive GUI that helps you create, verify, and maintain the list of deployed files. To add this extension, follow the same steps as above, but this time search for the Wax extension.

![Wax extension](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/wax-extension.png "Wax extension")  

<!-- affiliate ads begin -->
<a href="https://unicoeye.pxf.io/c/5597632/2134489/18498" target="_top" id="2134489">
  <img src="//a.impactradius-go.com/display-ad/18498-2134489" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://unicoeye.pxf.io/i/5597632/2134489/18498" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to add the Setup project to your application?

Once the environment setup is complete, let’s create the setup package for our application. Suppose you already have the Windows Forms application. Follow the next steps to create the setup project:

1\. Right-click on the project solution → Add → New project.

2\. From the project list, choose _Setup Project for WiX_. 

![Setup Project for WiX](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/setup-project-for-wix.png "Setup Project for WiX")  

After creating the setup project, you should see it in the _Solution Explore_r. 

![Solution Explorer](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/solution-explorer.png "Solution Explorer")  

<!-- affiliate ads begin -->
<a href="https://laganoo.pxf.io/c/5597632/1657400/16446" target="_top" id="1657400">
  <img src="//a.impactradius-go.com/display-ad/16446-1657400" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://laganoo.pxf.io/i/5597632/1657400/16446" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

The _Product.wxs_ file contains the setup project logic.

![Product.wxs](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/product-wxs.png "Product.wxs")  

### How to edit product details?

To edit the product details, open the _Product.wxs_ file and edit the corresponding fields. For example, we set the version to 1.1 and the manufacturer to Caphyon.

![edit product details](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/edit-product-details.png "edit product details")  

### How to add project output to your setup project?

To add the deployable files to the setup project, use the _Wix Setup Editor_. To open the editor, go to _Tools_ → _WiX Setup Editor_. 

You have to make some configurations here:

\- select the setup project added to your application, in our case it is _AppSetup_.

\- in the Root directory, select _INSTALLFOLDER_. 

\- In the _Projects to install_ section, select the application you’re creating the installer for. In our case, we selected _MyApp_.

![add project output to your setup project](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/add-project-output-to-your-setup-project.png "add project output to your setup project")  

<!-- affiliate ads begin -->
<a href="https://bluettieu.pxf.io/c/5597632/2141680/17091" target="_top" id="2141680">
  <img src="//a.impactradius-go.com/display-ad/17091-2141680" border="0" alt="https://techidaily.com" width="120" height="90"/>
</a>
<img height="0" width="0" src="https://bluettieu.pxf.io/i/5597632/2141680/17091" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

If the files have the _unmapped_ state like in the image below, make sure you change the state to _resolved_ by pressing the _plus_ button under the warning sign.

![files mapping](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/files-mapping.png "files mapping")  

Now, you should see the files in the _Products.wxs_ file.

![Products.wxs file](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/products-wxs-file.png "Products.wxs file")

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2100529/7443" target="_top" id="2100529">
  <img src="//a.impactradius-go.com/display-ad/7443-2100529" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2100529/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to create Shortcuts for your application?

Creating a shortcut is a common requirement when installing an application, but not such an easy task when using WiX. It can't be done from the Setup Editor, so you have to edit the XML file. Follow the next steps to add a shortcut on the Desktop and in the Programs Menu also:

1\. Define the directory structures.

![Define the directory structures](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/define-the-directory-structures.png "Define the directory structures")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1997717/19272" target="_top" id="1997717">
  <img src="//a.impactradius-go.com/display-ad/19272-1997717" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1997717/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. Add the shortcuts to the installer package.

![Add the shortcuts to the installer package](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/add-the-shortcuts-to-the-installer-package.png "Add the shortcuts to the installer package")  

3\. Tell Windows to install the shortcuts.

![Tell Windows to install the shortcuts](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/tell-windows-to-install-the-shortcuts.png "Tell Windows to install the shortcuts")

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2006919/19272" target="_top" id="2006919">
  <img src="//a.impactradius-go.com/display-ad/19272-2006919" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2006919/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to add installation dialogues?

When using Wix to create an installer package, it will not have the UI included by default. To add a minimal UI, you can follow the next steps: 

1\. Right click in the setup project → Add → References. In the Add Reference dialog, look in the bin folder of the WiX Toolset and add _WinUiExtension.dll_.

![WiX Toolset add WinUiExtension.dll](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/wix-toolset-add-winuiextension-dll.png "WiX Toolset add WinUiExtension.dll")  

<!-- affiliate ads begin -->
<a href="https://25home.pxf.io/c/5597632/2148637/16836" target="_top" id="2148637">
  <img src="//a.impactradius-go.com/display-ad/16836-2148637" border="0" alt="https://techidaily.com" width="125" height="90"/>
</a>
<img height="0" width="0" src="https://25home.pxf.io/i/5597632/2148637/16836" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. Go to the _Product.wsx_ file and add the next line inside the <_Product>_ element to reference the UI:  

_<UIRef Id="WixUI\_Minimal" />_

### How to install your application?

Now, you can build the setup project. Then, go to the bin folder inside the setup project folder to find the MSI file. Run the file and install the application. After installation, you should find the shortcuts on the Program Menu and Desktop. 

![build the setup project](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/build-the-setup-project.png "build the setup project")  

### Conclusion

WiX is a great tool for software packaging, but it can be tricky sometimes. It is clearly not the best option for beginners or if you want to save time. 

You can have the same functionalities using **Advanced Installer**, but with a **modern and powerful GUI.** Advanced Installer also provides an extension to help you create and manage installers directly from Visual Studio. It offers a Viewer to quickly edit basic information, and you can also open the project in AI to have access to all available features. 

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Check out [this tutorial](https://www.youtube.com/watch?v=xG3RpCOtv4c "this tutorial") to see how to create Advanced Installer projects from Visual Studio.  

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2137214/26400" target="_top" id="2137214">
  <img src="//a.impactradius-go.com/display-ad/26400-2137214" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2137214/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<li><a href="https://fox-access.techidaily.com/new-2024-approved-unearthing-the-potential-in-magixs-image-sorter/"><u>[New] 2024 Approved Unearthing the Potential in MAGIX's Image Sorter</u></a></li>
<li><a href="https://video-capture.techidaily.com/new-first-time-filmmaker-guide-setting-up-logitech-cam-for-2024/"><u>[New] First-Time Filmmaker Guide Setting up Logitech Cam for 2024</u></a></li>
<li><a href="https://facebook-videos.techidaily.com/updated-effortless-strategies-to-detect-duplicate-and-phony-likes-for-2024/"><u>[Updated] Effortless Strategies to Detect Duplicate and Phony Likes for 2024</u></a></li>
<li><a href="https://facebook-video-recording.techidaily.com/updated-in-2024-enhancing-interactivity-tips-for-hosting-splitting-screen-events-on-facebook/"><u>[Updated] In 2024, Enhancing Interactivity Tips for Hosting Splitting-Screen Events on Facebook</u></a></li>
<li><a href="https://hardware-reviews.techidaily.com/1723964487791-get-the-pro-level-logitech-g502-hero-at-an-amazing-price-only-35-experience-ultra-high-definition-controls-and-25k-dpi-sensitivity/"><u>Get the Pro-Level Logitech G502 Hero at an Amazing Price - Only $35! Experience Ultra-High Definition Controls and 25K DPI Sensitivity.</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-i-transferred-messages-from-honor-magic-5-pro-to-iphone-12xs-max-in-seconds-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>How I Transferred Messages from Honor Magic 5 Pro to iPhone 12/XS (Max) in Seconds | Dr.fone</u></a></li>
<li><a href="https://youtube-webster.techidaily.com/24-funny-flicks-compilation-of-chuckle-inducing-short-youtube-videos/"><u>In 2024, Funny Flicks Compilation of Chuckle-Inducing Short YouTube Videos</u></a></li>
<li><a href="https://some-tips.techidaily.com/my-passion-for-starry-jewelry-denied-by-samsung-a-tale-of-cosmic-aspirations-and-tech-restrictions/"><u>My Passion for Starry Jewelry Denied by Samsung – A Tale of Cosmic Aspirations and Tech Restrictions</u></a></li>
<li><a href="https://some-tips.techidaily.com/pixel-8-pro-vs-oneplus-12-face-off-determining-the-undeniable-champion/"><u>Pixel 8 Pro Vs. OnePlus 12 Face-Off: Determining the Undeniable Champion</u></a></li>
<li><a href="https://some-tips.techidaily.com/revamped-contact-manager-unveiling-the-latest-updates-in-microsofts-outlook-mobile-application/"><u>Revamped Contact Manager: Unveiling the Latest Updates in Microsoft's Outlook Mobile Application</u></a></li>
<li><a href="https://some-tips.techidaily.com/revamped-version-of-apples-sports-platform-whats-new/"><u>Revamped Version of Apple's Sports Platform - What's New?</u></a></li>
<li><a href="https://some-tips.techidaily.com/revitalize-and-rejuvenate-your-aged-android-smartphone-with-these-8-key-strategies/"><u>Revitalize and Rejuvenate Your Aged Android Smartphone with These 8 Key Strategies!</u></a></li>
<li><a href="https://win-howtos.techidaily.com/step-by-step-guide-to-overcome-windows-11-installation-error-80240020/"><u>Step-by-Step Guide to Overcome Windows 11 Installation Error 80240020</u></a></li>
</ul></div>

