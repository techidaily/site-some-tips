---
title: Visual Studio Integration with WiX Software Development Kit
date: 2024-09-27T06:33:39.069Z
updated: 2024-09-28T07:13:29.620Z
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
<a href="https://aligracehair.sjv.io/c/5597632/1896560/19272" target="_top" id="1896560">
  <img src="//a.impactradius-go.com/display-ad/19272-1896560" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1896560/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://appsumo.8odi.net/c/5597632/2137411/7443" target="_top" id="2137411">
  <img src="//a.impactradius-go.com/display-ad/7443-2137411" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2137411/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to add the Setup project to your application?

Once the environment setup is complete, let’s create the setup package for our application. Suppose you already have the Windows Forms application. Follow the next steps to create the setup project:

1\. Right-click on the project solution → Add → New project.

2\. From the project list, choose _Setup Project for WiX_. 

![Setup Project for WiX](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/setup-project-for-wix.png "Setup Project for WiX")  

<!-- affiliate ads begin -->
<a href="https://laganoo.pxf.io/c/5597632/1528703/16446" target="_top" id="1528703">
  <img src="//a.impactradius-go.com/display-ad/16446-1528703" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://laganoo.pxf.io/i/5597632/1528703/16446" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

After creating the setup project, you should see it in the _Solution Explore_r. 

![Solution Explorer](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/solution-explorer.png "Solution Explorer")  

The _Product.wxs_ file contains the setup project logic.

![Product.wxs](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/product-wxs.png "Product.wxs")  

### How to edit product details?

To edit the product details, open the _Product.wxs_ file and edit the corresponding fields. For example, we set the version to 1.1 and the manufacturer to Caphyon.

![edit product details](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/edit-product-details.png "edit product details")  

<!-- affiliate ads begin -->
<a href="https://laganoo.pxf.io/c/5597632/1657395/16446" target="_top" id="1657395">
  <img src="//a.impactradius-go.com/display-ad/16446-1657395" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://laganoo.pxf.io/i/5597632/1657395/16446" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://appsumo.8odi.net/c/5597632/2068425/7443" target="_top" id="2068425">
  <img src="//a.impactradius-go.com/display-ad/7443-2068425" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2068425/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to create Shortcuts for your application?

Creating a shortcut is a common requirement when installing an application, but not such an easy task when using WiX. It can't be done from the Setup Editor, so you have to edit the XML file. Follow the next steps to add a shortcut on the Desktop and in the Programs Menu also:

1\. Define the directory structures.

![Define the directory structures](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/define-the-directory-structures.png "Define the directory structures")  

<!-- affiliate ads begin -->
<a href="https://malaysia-healthcare-travel-council.pxf.io/c/5597632/1576474/17382" target="_top" id="1576474">
  <img src="//a.impactradius-go.com/display-ad/17382-1576474" border="0" alt="https://techidaily.com" width="160" height="90"/>
</a>
<img height="0" width="0" src="https://malaysia-healthcare-travel-council.pxf.io/i/5597632/1576474/17382" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. Add the shortcuts to the installer package.

![Add the shortcuts to the installer package](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/add-the-shortcuts-to-the-installer-package.png "Add the shortcuts to the installer package")  

3\. Tell Windows to install the shortcuts.

![Tell Windows to install the shortcuts](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/tell-windows-to-install-the-shortcuts.png "Tell Windows to install the shortcuts")

### How to add installation dialogues?

When using Wix to create an installer package, it will not have the UI included by default. To add a minimal UI, you can follow the next steps: 

1\. Right click in the setup project → Add → References. In the Add Reference dialog, look in the bin folder of the WiX Toolset and add _WinUiExtension.dll_.

![WiX Toolset add WinUiExtension.dll](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/wix-toolset-add-winuiextension-dll.png "WiX Toolset add WinUiExtension.dll")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2100527/7443" target="_top" id="2100527">
  <img src="//a.impactradius-go.com/display-ad/7443-2100527" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2100527/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. Go to the _Product.wsx_ file and add the next line inside the <_Product>_ element to reference the UI:  

_<UIRef Id="WixUI\_Minimal" />_

### How to install your application?

Now, you can build the setup project. Then, go to the bin folder inside the setup project folder to find the MSI file. Run the file and install the application. After installation, you should find the shortcuts on the Program Menu and Desktop. 

![build the setup project](https://cdn.advancedinstaller.com/img/wix-toolset-vs-extension/build-the-setup-project.png "build the setup project")  

<!-- affiliate ads begin -->
<a href="https://review-au.sjv.io/c/5597632/2098702/14409" target="_top" id="2098702">
  <img src="//a.impactradius-go.com/display-ad/14409-2098702" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://review-au.sjv.io/i/5597632/2098702/14409" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://some-tips.techidaily.com/new-subtly-lowering-volume-alives-guide/"><u>[New] Subtly Lowering Volume Alive’s Guide</u></a></li>
<li><a href="https://some-guidance.techidaily.com/new-the-ultimate-tv-show-prep-which-software-winsvirusmix-or-wirecast/"><u>[New] The Ultimate TV Show Prep Which Software Wins—VirusMix or WireCast?</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-ultimate-assortment-of-gopro-modifications/"><u>[New] Ultimate Assortment of Gopro Modifications</u></a></li>
<li><a href="https://on-screen-recording.techidaily.com/updated-prime-desktopmobile-communication-alternatives-to-zoom/"><u>[Updated] Prime Desktop/Mobile Communication Alternatives to Zoom</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unravel-the-mysteries-of-morphvox-the-ultimate-guide-to-voice-modification/"><u>[Updated] Unravel the Mysteries of MorphVOX The Ultimate Guide to Voice Modification</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-essential-manual-on-motion-detection-techniques/"><u>2024 Approved The Essential Manual on Motion Detection Techniques</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-understanding-drones-their-functionality-explored/"><u>2024 Approved Understanding Drones Their Functionality Explored</u></a></li>
<li><a href="https://tech-hub.techidaily.com/charting-the-boundaries-of-chatgpts-token-count/"><u>Charting the Boundaries of ChatGPT's Token Count</u></a></li>
<li><a href="https://some-techniques.techidaily.com/fundamentals-of-crafting-engaging-stories-for-2024/"><u>Fundamentals of Crafting Engaging Stories for 2024</u></a></li>
<li><a href="https://fox-blue.techidaily.com/in-2024-freeze-action-with-iphone-mastery-of-motion-blur-techniques/"><u>In 2024, Freeze Action with iPhone Mastery of Motion-Blur Techniques</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-how-to-use-zoom-on-xbox-one/"><u>In 2024, How to Use Zoom on Xbox One</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-transform-your-zoom-presentations-with-stunning-visuals/"><u>In 2024, Transform Your Zoom Presentations with Stunning Visuals</u></a></li>
<li><a href="https://desktop-recording.techidaily.com/is-itops-feature-set-enough-to-justify-usage/"><u>Is ITop's Feature Set Enough to Justify Usage?</u></a></li>
<li><a href="https://win-fantastic.techidaily.com/optimizing-your-flipbook-creation-for-seamless-mobile-experience-tips-and-tricks/"><u>Optimizing Your FlipBook Creation for Seamless Mobile Experience: Tips & Tricks</u></a></li>
<li><a href="https://extra-resources.techidaily.com/premium-animated-design-kits/"><u>Premium Animated Design Kits</u></a></li>
<li><a href="https://some-tips.techidaily.com/testing-the-capabilities-of-magix-image-viewer-for-2024/"><u>Testing the Capabilities of MAGIX Image Viewer for 2024</u></a></li>
<li><a href="https://change-location.techidaily.com/the-best-ispoofer-alternative-to-try-on-vivo-s18e-drfone-by-drfone-virtual-android/"><u>The Best iSpoofer Alternative to Try On Vivo S18e | Dr.fone</u></a></li>
<li><a href="https://extra-resources.techidaily.com/the-dji-x20-drone-vision-wear-review/"><u>The DJI X20 Drone Vision Wear Review</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-the-potential-of-bulk-tiktok-media-extraction-for-2024/"><u>Unlocking the Potential of Bulk TikTok Media Extraction for 2024</u></a></li>
</ul></div>

