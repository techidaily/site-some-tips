---
title: "Wix Made Simple: The Ultimate Tips for Perfecting Your Installation Path"
date: 2024-09-24T03:45:37.040Z
updated: 2024-09-28T09:00:46.667Z
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

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1925468/19272" target="_top" id="1925468">
  <img src="//a.impactradius-go.com/display-ad/19272-1925468" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1925468/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<a href="https://wigfever.sjv.io/c/5597632/2014851/22899" target="_top" id="2014851">
  <img src="//a.impactradius-go.com/display-ad/22899-2014851" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://wigfever.sjv.io/i/5597632/2014851/22899" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://imp.i357552.net/c/5597632/857865/11832" target="_top" id="857865">
  <img src="//a.impactradius-go.com/display-ad/11832-857865" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://imp.i357552.net/i/5597632/857865/11832" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to set the install folder in Advanced Installer?

When working with Advanced Installer, it is essential to understand how the default installation folder, also known as the Application folder, is configured. This folder location is initially defined in the _Install Parameters view (Product Files\\Manufacturer\\Product Name)_.

However, if you need to make any modifications, Advanced Installer offers a user-friendly graphical interface that allows you to easily change the default installation folder as required.

![set the install folder in Advanced Installer](https://cdn.advancedinstaller.com/img/set-install-folder-wix/set-the-install-folder-in-advanced-installer.png "set the install folder in Advanced Installer")  

The **Application folder** is usually the main installation folder. You can add the files and folders under this folder. 

![Advanced Installer Application folder](https://cdn.advancedinstaller.com/img/set-install-folder-wix/advanced-installer-application-folder.png "Advanced Installer Application folder")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1975821/19272" target="_top" id="1975821">
  <img src="//a.impactradius-go.com/display-ad/19272-1975821" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1975821/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

If you wish to allow users to customize the installation path, no additional configuration is necessary. By default, the installer includes the **FolderDlg** dialogue, which presents the current path of the Application Folder and enables users to modify it during the installation process.

![FolderDlg](https://cdn.advancedinstaller.com/img/set-install-folder-wix/folderdlg.png "FolderDlg")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1948932/19272" target="_top" id="1948932">
  <img src="//a.impactradius-go.com/display-ad/19272-1948932" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1948932/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<li><a href="https://desktop-recording.techidaily.com/new-best-in-class-ps3-virtual-games-for-pc/"><u>[New] Best-in-Class PS3 Virtual Games for PC</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-top-sites-for-fetching-got-ringtone-downloads/"><u>[New] Top Sites for Fetching GoT Ringtone Downloads</u></a></li>
<li><a href="https://screen-recording.techidaily.com/updated-a-thorough-insight-into-obs-recording-technology/"><u>[Updated] A Thorough Insight Into OBS Recording Technology</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-ultimate-tutorial-for-full-utilization-of-final-cut-pro/"><u>[Updated] Ultimate Tutorial for Full Utilization of Final Cut Pro</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-strategies-to-reinforce-stability-in-windows-10-photo-viewer/"><u>2024 Approved Strategies to Reinforce Stability in Windows 10 Photo Viewer</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-professionals-guide-to-innovative-360-cams-2023/"><u>2024 Approved The Professionals’ Guide to Innovative 360° Cams, 2023</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/decode-and-maximize-your-impact-on-instagram-with-these-insights/"><u>Decode & Maximize Your Impact on Instagram with These Insights</u></a></li>
<li><a href="https://techidaily.com/how-to-factory-reset-samsung-galaxy-s23-ultra-if-i-forgot-security-code-or-password-drfone-by-drfone-reset-android-reset-android/"><u>How to Factory Reset Samsung Galaxy S23 Ultra If I Forgot Security Code or Password? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unlocking-potential-an-in-depth-look-at-vivocut-editing/"><u>In 2024, Unlocking Potential An In-Depth Look at VivoCut Editing</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/mastering-mov-video-sharing-on-instagram-tips-and-tricks-for-perfect-posts-without-hitches/"><u>Mastering MOV Video Sharing on Instagram: Tips & Tricks for Perfect Posts Without Hitches!</u></a></li>
<li><a href="https://blog-min.techidaily.com/winxwinxai/"><u>WinX影片导出器和WinX视频AI软件的电商支持点拓展 - 立即获取专业解决方案</u></a></li>
</ul></div>

