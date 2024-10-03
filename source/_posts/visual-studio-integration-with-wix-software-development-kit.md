---
title: Visual Studio Integration with WiX Software Development Kit
date: 2024-09-26T18:17:01.942Z
updated: 2024-10-03T16:54:40.909Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Visual Studio Integration with WiX Software Development Kit
thumbnail: https://thmb.techidaily.com/d1a4704b31151e9550e9b3ab1b575cfa25b0e8f640c5b81b3310074251149c70.jpg
---

## Visual Studio Integration with WiX Software Development Kit

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
<span id="1982461">
					<video width="576" height="240" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1982461.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1982461">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1982461.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1982461%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1982461/22993" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://appsumo.8odi.net/c/5597632/2144283/7443" target="_top" id="2144283">
  <img src="//a.impactradius-go.com/display-ad/7443-2144283" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2144283/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to add the Setup project to your application?

Once the environment setup is complete, let’s create the setup package for our application. Suppose you already have the Windows Forms application. Follow the next steps to create the setup project:

1\. Right-click on the project solution → Add → New project.

2\. From the project list, choose _Setup Project for WiX_. 

![Setup Project for WiX](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/setup-project-for-wix.png "Setup Project for WiX")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135372/19272" target="_top" id="2135372">
  <img src="//a.impactradius-go.com/display-ad/19272-2135372" border="0" alt="https://techidaily.com" width="336" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135372/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

After creating the setup project, you should see it in the _Solution Explore_r. 

![Solution Explorer](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/solution-explorer.png "Solution Explorer")  

The _Product.wxs_ file contains the setup project logic.

![Product.wxs](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/product-wxs.png "Product.wxs")  

<!-- affiliate ads begin -->
<a href="https://malaysia-healthcare-travel-council.pxf.io/c/5597632/1557743/17382" target="_top" id="1557743">
  <img src="//a.impactradius-go.com/display-ad/17382-1557743" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://malaysia-healthcare-travel-council.pxf.io/i/5597632/1557743/17382" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2087267/19272" target="_top" id="2087267">
  <img src="//a.impactradius-go.com/display-ad/19272-2087267" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2087267/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to edit product details?

To edit the product details, open the _Product.wxs_ file and edit the corresponding fields. For example, we set the version to 1.1 and the manufacturer to Caphyon.

![edit product details](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/edit-product-details.png "edit product details")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2043661/7443" target="_top" id="2043661">
  <img src="//a.impactradius-go.com/display-ad/7443-2043661" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2043661/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to add project output to your setup project?

To add the deployable files to the setup project, use the _Wix Setup Editor_. To open the editor, go to _Tools_ → _WiX Setup Editor_. 

You have to make some configurations here:

\- select the setup project added to your application, in our case it is _AppSetup_.

\- in the Root directory, select _INSTALLFOLDER_. 

\- In the _Projects to install_ section, select the application you’re creating the installer for. In our case, we selected _MyApp_.

![add project output to your setup project](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/add-project-output-to-your-setup-project.png "add project output to your setup project")  

If the files have the _unmapped_ state like in the image below, make sure you change the state to _resolved_ by pressing the _plus_ button under the warning sign.

![files mapping](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/files-mapping.png "files mapping")  

Now, you should see the files in the _Products.wxs_ file.

![Products.wxs file](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/products-wxs-file.png "Products.wxs file")

<!-- affiliate ads begin -->
<a href="https://imp.i357552.net/c/5597632/999558/11832" target="_top" id="999558">
  <img src="//a.impactradius-go.com/display-ad/11832-999558" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://imp.i357552.net/i/5597632/999558/11832" style="position:absolute;visibility:hidden;" border="0" />
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

### How to install your application?

Now, you can build the setup project. Then, go to the bin folder inside the setup project folder to find the MSI file. Run the file and install the application. After installation, you should find the shortcuts on the Program Menu and Desktop. 

![build the setup project](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/build-the-setup-project.png "build the setup project")  

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

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2082535/7443" target="_top" id="2082535">
  <img src="//a.impactradius-go.com/display-ad/7443-2082535" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2082535/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://instagram-video-files.techidaily.com/new-2024-approved-who-skipped-my-story-unfollowers-scan/"><u>[New] 2024 Approved Who Skipped My Story? Unfollowers Scan</u></a></li>
<li><a href="https://article-tips.techidaily.com/new-in-2024-elevating-photography-with-canons-time-lapse-methods/"><u>[New] In 2024, Elevating Photography with Canon's Time-Lapse Methods</u></a></li>
<li><a href="https://remote-screen-capture.techidaily.com/updated-instant-live-from-obs-to-instagram-app/"><u>[Updated] Instant Live From OBS to Instagram App</u></a></li>
<li><a href="https://location-social.techidaily.com/4-feasible-ways-to-fake-location-on-facebook-for-your-motorola-moto-g84-5g-drfone-by-drfone-virtual-android/"><u>4 Feasible Ways to Fake Location on Facebook For your Motorola Moto G84 5G | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/adjusting-your-ubuntu-desktop-relocating-the-dock-side-panel/"><u>Adjusting Your Ubuntu Desktop: Relocating the Dock Side Panel</u></a></li>
<li><a href="https://some-tips.techidaily.com/exploring-the-latest-features-of-the-16-gen-9-lenovo-legion-pro-7i-gaming-laptop-reviewed/"><u>Exploring the Latest Features of the 16 Gen 9 Lenovo Legion Pro 7I Gaming Laptop Reviewed!</u></a></li>
<li><a href="https://some-tips.techidaily.com/fixing-issues-with-your-windows-start-menu-a-comprehensive-guide/"><u>Fixing Issues with Your Windows Start Menu: A Comprehensive Guide</u></a></li>
<li><a href="https://location-social.techidaily.com/in-2024-how-to-activate-and-use-life360-ghost-mode-on-apple-iphone-6s-plus-drfone-by-drfone-virtual-ios/"><u>In 2024, How To Activate and Use Life360 Ghost Mode On Apple iPhone 6s Plus | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/making-the-most-of-onedrive-with-windows-11-why-microsoft-encourages-integration/"><u>Making the Most of OneDrive with Windows 11: Why Microsoft Encourages Integration</u></a></li>
<li><a href="https://some-tips.techidaily.com/resizing-icons-effortlessly-in-windows-10-a-step-by-step-guide/"><u>Resizing Icons Effortlessly in Windows 10: A Step-by-Step Guide</u></a></li>
<li><a href="https://screen-video-capture.techidaily.com/top-microphones-for-idevices-and-their-benefits-explained-for-2024/"><u>Top Microphones for iDevices & Their Benefits Explained for 2024</u></a></li>
<li><a href="https://program-issues.techidaily.com/troubleshooting-failed-skype-message-transmissions-expert-tips-and-solutions/"><u>Troubleshooting Failed Skype Message Transmissions: Expert Tips and Solutions</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-the-power-of-ai-with-windows-copilot-enable-and-harness-microsofts-intelligent-assistant-efficiently/"><u>Unlocking the Power of AI with Windows Copilot - Enable & Harness Microsoft’s Intelligent Assistant Efficiently</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveiling-natures-artistry-a-guide-to-apple-vision-pro-wonders-and-the-iconic-beauty-of-lake-vrangla/"><u>Unveiling Nature's Artistry: A Guide to Apple Vision Pro Wonders and the Iconic Beauty of Lake Vrangla</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveiling-perplexity-your-ultimate-investment-in-an-exclusive-ai-chatbot/"><u>Unveiling Perplexity: Your Ultimate Investment in an Exclusive AI Chatbot</u></a></li>
<li><a href="https://ai-video-tools.techidaily.com/updated-mov-file-editing-made-easy-top-10-free-video-editors-for-2024/"><u>Updated MOV File Editing Made Easy Top 10 Free Video Editors for 2024</u></a></li>
<li><a href="https://win-answers.techidaily.com/warzone-troubles-mastering-fps-increase-and-stutter-elimination-techniques-for-gamers/"><u>Warzone Troubles? Mastering FPS Increase and Stutter Elimination Techniques for Gamers</u></a></li>
</ul></div>

