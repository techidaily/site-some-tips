---
title: "Wix Made Simple: The Ultimate Tips for Perfecting Your Installation Path"
date: 2024-10-01T16:37:11.983Z
updated: 2024-10-03T16:13:33.937Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Wix Made Simple: The Ultimate Tips for Perfecting Your Installation Path"
thumbnail: https://thmb.techidaily.com/7572b835422df4a46e1dde0ebf1594c94500d035cdbdf693fb3fdb8a7d6301cc.jpg
---

## Wix Made Simple: The Ultimate Tips for Perfecting Your Installation Path

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

## How to correctly set the install folder in Wix

Written by [Renato Ivanescu](https://tools.techidaily.com/advancedinstaller/products/) · June 8th, 2023

When creating an installer, it is crucial to **prioritize the setting of the installation directory**. This directory, often referred to as the "install path," represents the specific location on the user's computer where the application will be installed.

Typically, a package specifies a **default install path**. However, it is essential to provide users with the flexibility to browse and select a **custom install path** during the installation process. You can accomplish this by including a user-friendly interface that enables straightforward selection of the chosen installation directory.

If you are interested in how to correctly set the install path for an MSI created with WiX Toolset, this is the article you need.

In this tutorial, we’ll show you **how to define a default install path** and how to **let the user select a custom install path** from the user interface for a Windows Forms application.

![Important](https://cdn.advancedinstaller.com/svg/common/IconMessageInfo.svg)Keep in mind that for this tutorial, we used the WiX Visual Studio extension to create the setup project. So, it’s important to make sure you have it installed.  

### How to define the directory structure?

First, we have to add the directory definition for the setup project. This directory will serve as the default installation path specified in the user interface. To accomplish this, we must make modifications to the **Product.wxs** file, similar to the provided sample below.

![define the directory structure](https://cdn.advancedinstaller.com/img/set-install-folder-wix/define-the-directory-structure.png "define the directory structure")  

You have to use the Directory element to define the directories and describe the hierarchy of folders on the target machine. We used the following elements in our example:

* **TARGETDIR** \- which is the root of all directory structures and it is present in every Wix project.
* **ProgramFilesFolder** \- a predefined property that references the _Program Files_ folder on the user’s machine and resolves to _C:\\Program Files._ On a 64-bit machine, it resolves to _C:\\Program Files (86)_.
* **MYAPPDIR** \- which creates the application’s folder under _Program Files_.

The default path after adding the above elements will be _C:\\Program Files\\DemoApp_. As you can see, the install folder ID must be all in uppercase characters to make it a public property. Thus, it will be passed from the UI to the execute sequence when the user modifies the default install path.

### How to add the WixUIExtension?

Now, let’s add the option that allows the user to change the default install location from the user interface.

Since Wix does not provide a built-in user interface (UI) by default, we need to add a reference to the _**WixUIExtension**_ library. This library stores some built-in dialog sequences including the _**WixUI\_InstallDir**_ dialogue set. 

This set has a dialogue, namely _**InstallDirDlg**_, that allows users to choose the directory where the product will be installed. To add the extension, follow the next steps:

1\. Go to the setup project (_DemoAppSetup_ in our case) → right-click on the setup project → Add reference.

![add the WixUIExtension](https://cdn.advancedinstaller.com/img/set-install-folder-wix/add-the-wixuiextension.png "add the WixUIExtension")  

2\. In the opened dialogue, navigate to the Wix Toolse_t_ folder → Bin folder.

![Wix Toolset folder Bin folder](https://cdn.advancedinstaller.com/img/set-install-folder-wix/wix-toolset-folder-bin-folder.png "Wix Toolset folder Bin folder")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2123749/7443" target="_top" id="2123749">
  <img src="//a.impactradius-go.com/display-ad/7443-2123749" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2123749/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

3\. Select **WixUIExtension.dll** → click Add → click OK.

After completing the steps, you should find the extension in the **References** folder. 

![find the extension in the References folder](https://cdn.advancedinstaller.com/img/set-install-folder-wix/find-the-extension-in-the-references-folder.png "find the extension in the References folder")  

### How to use the WinUI\_InstallDir?

Once the _WixUIExtension_ is referenced, we can use the _WixUI\_InstallD_ir functionality. 

Follow the steps below to correctly configure the installation path:

1\. Set the value for the **WIXUI\_INSTALLDIR** property. This value should correspond to the ID assigned to the directory where the user will specify the installation location. In our case, the ID is MYAPPDIR.

<Property Id="WIXUI_INSTALLDIR" Value="MYAPPDIR" />

Copy

2\. Reference the WixUI\_InstalDir.

<UIRef Id="WixUI_InstallDir" />

Copy

When you run the MSI, a series of dialogs will appear, including the **InstallDirDlg**, which allows the user to choose a custom installation path.

![InstallDirDlg](https://cdn.advancedinstaller.com/img/set-install-folder-wix/installdirdlg.png "InstallDirDlg")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2123730/7443" target="_top" id="2123730">
  <img src="//a.impactradius-go.com/display-ad/7443-2123730" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2123730/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1896546/19272" target="_top" id="1896546">
  <img src="//a.impactradius-go.com/display-ad/19272-1896546" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1896546/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to set the install folder in Advanced Installer?

When working with Advanced Installer, it is essential to understand how the default installation folder, also known as the Application folder, is configured. This folder location is initially defined in the _Install Parameters view (Product Files\\Manufacturer\\Product Name)_.

However, if you need to make any modifications, Advanced Installer offers a user-friendly graphical interface that allows you to easily change the default installation folder as required.

![set the install folder in Advanced Installer](https://cdn.advancedinstaller.com/img/set-install-folder-wix/set-the-install-folder-in-advanced-installer.png "set the install folder in Advanced Installer")  

<!-- affiliate ads begin -->
<a href="https://unicoeye.pxf.io/c/5597632/2134246/18498" target="_top" id="2134246">
  <img src="//a.impactradius-go.com/display-ad/18498-2134246" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://unicoeye.pxf.io/i/5597632/2134246/18498" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

The **Application folder** is usually the main installation folder. You can add the files and folders under this folder. 

![Advanced Installer Application folder](https://cdn.advancedinstaller.com/img/set-install-folder-wix/advanced-installer-application-folder.png "Advanced Installer Application folder")  

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2137227/26400" target="_top" id="2137227">
  <img src="//a.impactradius-go.com/display-ad/26400-2137227" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2137227/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

If you wish to allow users to customize the installation path, no additional configuration is necessary. By default, the installer includes the **FolderDlg** dialogue, which presents the current path of the Application Folder and enables users to modify it during the installation process.

![FolderDlg](https://cdn.advancedinstaller.com/img/set-install-folder-wix/folderdlg.png "FolderDlg")  

### Conclusion

Setting the installation path correctly for an installer package created with **WiX** requires quite several steps. You have to edit the XML file and use an additional extension to let the user choose a different install path from the UI.

In contrast, when using **Advanced Installer**, the process is much simpler. The default installation path is automatically set, and you can effortlessly modify it through the intuitive user interface. Additionally, the installer includes the **FolderDlg** dialog by default, which allows users to modify the installation path if necessary. With Advanced Installer, you can streamline the installation path configuration without the need for extensive manual adjustments.

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
<li><a href="https://facebook-video-share.techidaily.com/new-bursting-laughter-crafting-engaging-reaction-videos-on-youtube-3-methods-for-2024/"><u>[New] Bursting Laughter Crafting Engaging Reaction Videos on YouTube (3 Methods) for 2024</u></a></li>
<li><a href="https://facebook-video-recording.techidaily.com/new-leveraging-visual-appeal-in-facebook-slideshows/"><u>[New] Leveraging Visual Appeal in Facebook Slideshows</u></a></li>
<li><a href="https://youtube-blog.techidaily.com/ed-2024-approved-8-premier-resources-download-free-high-quality-green-screen-footage/"><u>[Updated] 2024 Approved 8 Premier Resources Download Free, High-Quality Green Screen Footage</u></a></li>
<li><a href="https://fox-direct.techidaily.com/updated-2024-approved-dive-into-the-most-effective-online-tools-your-guide-to-perfect-captions/"><u>[Updated] 2024 Approved Dive Into the Most Effective Online Tools Your Guide to Perfect Captions</u></a></li>
<li><a href="https://some-tips.techidaily.com/1-enhancing-your-file-navigation-on-windows-a-step-by-step-guide/"><u>1. Enhancing Your File Navigation on Windows: A Step-by-Step Guide</u></a></li>
<li><a href="https://remote-screen-capture.techidaily.com/2024-approved-essential-videography-the-leading-screen-recorder-apps/"><u>2024 Approved Essential Videography The Leading Screen Recorder Apps</u></a></li>
<li><a href="https://some-techniques.techidaily.com/2024-approved-greatest-kid-friendly-flying-toys-summary/"><u>2024 Approved Greatest Kid-Friendly Flying Toys Summary</u></a></li>
<li><a href="https://some-tips.techidaily.com/guide-configuring-your-pc-with-windows-11-no-microsoft-account-required/"><u>Guide: Configuring Your PC with Windows 11 - No Microsoft Account Required</u></a></li>
<li><a href="https://some-tips.techidaily.com/how-microsofts-directx-raytracing-dxr-innovation-propels-next-gen-pc-gaming-performance/"><u>How Microsoft's DirectX Raytracing (DXR) Innovation Propels Next-Gen PC Gaming Performance</u></a></li>
<li><a href="https://some-skills.techidaily.com/in-2024-top-spots-for-classic-ringtone-downloads/"><u>In 2024, Top Spots for Classic Ringtone Downloads</u></a></li>
<li><a href="https://remote-screen-capture.techidaily.com/navigating-sharex-critical-thoughts-and-alternatives-for-2024/"><u>Navigating ShareX Critical Thoughts & Alternatives for 2024</u></a></li>
<li><a href="https://hardware-help.techidaily.com/quick-and-easy-procedure-updating-drivers-on-a-sata-ahci-controller-device/"><u>Quick & Easy Procedure: Updating Drivers on a SATA AHCI Controller Device</u></a></li>
<li><a href="https://some-tips.techidaily.com/setting-up-your-preferred-mic-and-cam-in-windows-11-step-by-step-guide/"><u>Setting Up Your Preferred Mic & Cam in Windows 11 – Step-by-Step Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/significant-upgrade-unveiled-icloud-now-fully-functional-with-windows-os/"><u>Significant Upgrade Unveiled: ICloud Now Fully Functional with Windows OS</u></a></li>
<li><a href="https://some-tips.techidaily.com/step-by-step-guide-concealing-your-taskbar-in-windows-10/"><u>Step-by-Step Guide: Concealing Your Taskbar in Windows 10</u></a></li>
<li><a href="https://some-approaches.techidaily.com/swiftly-delete-autoplayed-podcast-suggestions-on-spotify-for-2024/"><u>Swiftly Delete Autoplayed Podcast Suggestions on Spotify for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/ultimate-guide-to-optimal-key-binding-tools-on-windows-systems/"><u>Ultimate Guide to Optimal Key Binding Tools on Windows Systems</u></a></li>
<li><a href="https://some-tips.techidaily.com/upcoming-mandatory-windows-11-update-23h2-what-you-need-to-know/"><u>Upcoming Mandatory Windows 11 Update 23H2: What You Need to Know</u></a></li>
<li><a href="https://some-tips.techidaily.com/why-microsofts-recall-functionality-works-without-artificial-intelligence-in-computers/"><u>Why Microsoft's Recall Functionality Works Without Artificial Intelligence in Computers</u></a></li>
</ul></div>

