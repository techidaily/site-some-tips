---
title: "Boost Your Builds: Enhancing Visual Studio with WiX Extensions"
date: 2024-09-23T01:12:56.793Z
updated: 2024-09-28T07:11:06.646Z
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

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135366/19272" target="_top" id="2135366">
  <img src="//a.impactradius-go.com/display-ad/19272-2135366" border="0" alt="https://techidaily.com" width="160" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135366/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<a href="https://appsumo.8odi.net/c/5597632/2049370/7443" target="_top" id="2049370">
  <img src="//a.impactradius-go.com/display-ad/7443-2049370" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2049370/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to add the Setup project to your application?

Once the environment setup is complete, let’s create the setup package for our application. Suppose you already have the Windows Forms application. Follow the next steps to create the setup project:

1\. Right-click on the project solution → Add → New project.

2\. From the project list, choose _Setup Project for WiX_. 

![Setup Project for WiX](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/setup-project-for-wix.png "Setup Project for WiX")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1997630/19272" target="_top" id="1997630">
  <img src="//a.impactradius-go.com/display-ad/19272-1997630" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1997630/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

After creating the setup project, you should see it in the _Solution Explore_r. 

![Solution Explorer](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/solution-explorer.png "Solution Explorer")  

The _Product.wxs_ file contains the setup project logic.

![Product.wxs](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/product-wxs.png "Product.wxs")  

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2137224/26400" target="_top" id="2137224">
  <img src="//a.impactradius-go.com/display-ad/26400-2137224" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2137224/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<a href="https://dhgate.sjv.io/c/5597632/2106658/12108" target="_top" id="2106658">
  <img src="//a.impactradius-go.com/display-ad/12108-2106658" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://dhgate.sjv.io/i/5597632/2106658/12108" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

If the files have the _unmapped_ state like in the image below, make sure you change the state to _resolved_ by pressing the _plus_ button under the warning sign.

![files mapping](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/files-mapping.png "files mapping")  

Now, you should see the files in the _Products.wxs_ file.

![Products.wxs file](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/products-wxs-file.png "Products.wxs file")

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2130874/7443" target="_top" id="2130874">
  <img src="//a.impactradius-go.com/display-ad/7443-2130874" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2130874/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to create Shortcuts for your application?

Creating a shortcut is a common requirement when installing an application, but not such an easy task when using WiX. It can't be done from the Setup Editor, so you have to edit the XML file. Follow the next steps to add a shortcut on the Desktop and in the Programs Menu also:

1\. Define the directory structures.

![Define the directory structures](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/define-the-directory-structures.png "Define the directory structures")  

2\. Add the shortcuts to the installer package.

![Add the shortcuts to the installer package](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/add-the-shortcuts-to-the-installer-package.png "Add the shortcuts to the installer package")  

3\. Tell Windows to install the shortcuts.

![Tell Windows to install the shortcuts](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/tell-windows-to-install-the-shortcuts.png "Tell Windows to install the shortcuts")

### How to add installation dialogues?

When using Wix to create an installer package, it will not have the UI included by default. To add a minimal UI, you can follow the next steps: 

1\. Right click in the setup project → Add → References. In the Add Reference dialog, look in the bin folder of the WiX Toolset and add _WinUiExtension.dll_.

![WiX Toolset add WinUiExtension.dll](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/wix-toolset-add-winuiextension-dll.png "WiX Toolset add WinUiExtension.dll")  

2\. Go to the _Product.wsx_ file and add the next line inside the <_Product>_ element to reference the UI:  

_<UIRef Id="WixUI\_Minimal" />_

<!-- affiliate ads begin -->
<span id="1424528">
					<video width="864" height="1536" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1424528.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/16446-1424528">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1424528.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:540px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Flaganoo.pxf.io%2Fc%2F5597632%2F1424528%2F16446'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1424528/16446" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to install your application?

Now, you can build the setup project. Then, go to the bin folder inside the setup project folder to find the MSI file. Run the file and install the application. After installation, you should find the shortcuts on the Program Menu and Desktop. 

![build the setup project](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/build-the-setup-project.png "build the setup project")  

<!-- affiliate ads begin -->
<a href="https://bluettius.sjv.io/c/5597632/2139120/17108" target="_top" id="2139120">
  <img src="//a.impactradius-go.com/display-ad/17108-2139120" border="0" alt="https://techidaily.com" width="250" height="90"/>
</a>
<img height="0" width="0" src="https://bluettius.sjv.io/i/5597632/2139120/17108" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Conclusion

WiX is a great tool for software packaging, but it can be tricky sometimes. It is clearly not the best option for beginners or if you want to save time. 

You can have the same functionalities using **Advanced Installer**, but with a **modern and powerful GUI.** Advanced Installer also provides an extension to help you create and manage installers directly from Visual Studio. It offers a Viewer to quickly edit basic information, and you can also open the project in AI to have access to all available features. 

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Check out [this tutorial](https://www.youtube.com/watch?v=xG3RpCOtv4c "this tutorial") to see how to create Advanced Installer projects from Visual Studio.  

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
<li><a href="https://screen-activity-recording.techidaily.com/new-2024-approved-premium-portable-switch-game-clones/"><u>[New] 2024 Approved Premium Portable Switch Game Clones</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-value-in-the-air-the-cheapest-yet-effective-drones/"><u>[New] Value in the Air The Cheapest Yet Effective Drones</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-complete-guide-to-audiovideo-settings-in-win11s-zoom-app/"><u>2024 Approved The Complete Guide to Audio/Video Settings in Win11's Zoom App</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unleash-the-full-spectrum-of-sound-best-apps-for-music-videos/"><u>2024 Approved Unleash the Full Spectrum of Sound Best Apps for Music Videos</u></a></li>
<li><a href="https://fake-location.techidaily.com/complete-tutorial-to-use-vpna-to-fake-gps-location-on-vivo-x-fold-2-drfone-by-drfone-virtual-android/"><u>Complete Tutorial to Use VPNa to Fake GPS Location On Vivo X Fold 2 | Dr.fone</u></a></li>
<li><a href="https://youtube-web.techidaily.com/24-integrating-youtube-effective-strategies-for-modern-teachers/"><u>In 2024, Integrating YouTube Effective Strategies for Modern Teachers</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/in-2024-seamless-steps-to-gather-thousands-of-videos-on-tiktok/"><u>In 2024, Seamless Steps to Gather Thousands of Videos on TikTok</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-time-lapse-titans-choosing-the-creme-de-la-camera/"><u>In 2024, Time-Lapse Titans Choosing the Crème De La Camera</u></a></li>
<li><a href="https://unlock-android.techidaily.com/in-2024-top-12-prominent-infinix-smart-7-fingerprint-not-working-solutions-by-drfone-android/"><u>In 2024, Top 12 Prominent Infinix Smart 7 Fingerprint Not Working Solutions</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-ultimate-action-plan-from-ttml-and-xml-to-srt-translation-for-2024/"><u>The Ultimate Action Plan From TTML & XML to SRT Translation for 2024</u></a></li>
<li><a href="https://tech-revival.techidaily.com/transform-your-ideas-into-pictures-an-ultimate-guide-to-ai-driven-image-generation-via-chatgpt/"><u>Transform Your Ideas Into Pictures: An Ultimate Guide to AI-Driven Image Generation via ChatGPT</u></a></li>
</ul></div>

