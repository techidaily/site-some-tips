---
title: "Step-by-Step Guide: Setting Your Install Directory Right on Wix"
date: 2024-10-02T17:52:31.660Z
updated: 2024-10-03T18:15:38.542Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Step-by-Step Guide: Setting Your Install Directory Right on Wix"
thumbnail: https://thmb.techidaily.com/7e8f336fc2079d7aea2b749496409ce99e4eee3883904481ad00375958028d28.jpg
---

## Step-by-Step Guide: Setting Your Install Directory Right on Wix

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
<a href="https://appsumo.8odi.net/c/5597632/2049387/7443" target="_top" id="2049387">
  <img src="//a.impactradius-go.com/display-ad/7443-2049387" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2049387/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

You have to use the Directory element to define the directories and describe the hierarchy of folders on the target machine. We used the following elements in our example:

* **TARGETDIR** \- which is the root of all directory structures and it is present in every Wix project.
* **ProgramFilesFolder** \- a predefined property that references the _Program Files_ folder on the user’s machine and resolves to _C:\\Program Files._ On a 64-bit machine, it resolves to _C:\\Program Files (86)_.
* **MYAPPDIR** \- which creates the application’s folder under _Program Files_.

The default path after adding the above elements will be _C:\\Program Files\\DemoApp_. As you can see, the install folder ID must be all in uppercase characters to make it a public property. Thus, it will be passed from the UI to the execute sequence when the user modifies the default install path.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2043638/7443" target="_top" id="2043638">
  <img src="//a.impactradius-go.com/display-ad/7443-2043638" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2043638/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to add the WixUIExtension?

Now, let’s add the option that allows the user to change the default install location from the user interface.

Since Wix does not provide a built-in user interface (UI) by default, we need to add a reference to the _**WixUIExtension**_ library. This library stores some built-in dialog sequences including the _**WixUI\_InstallDir**_ dialogue set. 

This set has a dialogue, namely _**InstallDirDlg**_, that allows users to choose the directory where the product will be installed. To add the extension, follow the next steps:

1\. Go to the setup project (_DemoAppSetup_ in our case) → right-click on the setup project → Add reference.

![add the WixUIExtension](https://cdn.advancedinstaller.com/img/set-install-folder-wix/add-the-wixuiextension.png "add the WixUIExtension")  

2\. In the opened dialogue, navigate to the Wix Toolse_t_ folder → Bin folder.

![Wix Toolset folder Bin folder](https://cdn.advancedinstaller.com/img/set-install-folder-wix/wix-toolset-folder-bin-folder.png "Wix Toolset folder Bin folder")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1997722/19272" target="_top" id="1997722">
  <img src="//a.impactradius-go.com/display-ad/19272-1997722" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1997722/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

3\. Select **WixUIExtension.dll** → click Add → click OK.

After completing the steps, you should find the extension in the **References** folder. 

![find the extension in the References folder](https://cdn.advancedinstaller.com/img/set-install-folder-wix/find-the-extension-in-the-references-folder.png "find the extension in the References folder")  

<!-- affiliate ads begin -->
<span id="1975658">
					<video width="128" height="480" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1975658.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1975658">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1975658.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:80px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1975658%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1975658/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<a href="https://laganoo.pxf.io/c/5597632/1528685/16446" target="_top" id="1528685">
  <img src="//a.impactradius-go.com/display-ad/16446-1528685" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://laganoo.pxf.io/i/5597632/1528685/16446" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to set the install folder in Advanced Installer?

When working with Advanced Installer, it is essential to understand how the default installation folder, also known as the Application folder, is configured. This folder location is initially defined in the _Install Parameters view (Product Files\\Manufacturer\\Product Name)_.

However, if you need to make any modifications, Advanced Installer offers a user-friendly graphical interface that allows you to easily change the default installation folder as required.

![set the install folder in Advanced Installer](https://cdn.advancedinstaller.com/img/set-install-folder-wix/set-the-install-folder-in-advanced-installer.png "set the install folder in Advanced Installer")  

The **Application folder** is usually the main installation folder. You can add the files and folders under this folder. 

![Advanced Installer Application folder](https://cdn.advancedinstaller.com/img/set-install-folder-wix/advanced-installer-application-folder.png "Advanced Installer Application folder")  

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
<li><a href="https://screen-video-capture.techidaily.com/new-screen-recording-simplified-unlocking-five-key-techniques-for-minecraft-on-a-mac/"><u>[New] Screen Recording Simplified Unlocking Five Key Techniques for Minecraft on a Mac</u></a></li>
<li><a href="https://article-files.techidaily.com/updated-2024-approved-sound-brilliance-for-podcasters-top-10-microphones/"><u>[Updated] 2024 Approved Sound Brilliance for Podcasters Top 10 Microphones</u></a></li>
<li><a href="https://extra-resources.techidaily.com/2024-approved-complete-evaluation-hero4-black-interface/"><u>2024 Approved Complete Evaluation Hero4 Black Interface</u></a></li>
<li><a href="https://screen-recording.techidaily.com/2024-approved-optimized-zoom-audio-settings-for-exceptional-listening/"><u>2024 Approved Optimized Zoom Audio Settings for Exceptional Listening</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhanced-user-engagement-with-advanced-cookiebot-technology/"><u>Enhanced User Engagement with Advanced Cookiebot Technology</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhancing-intelligence-in-automation-the-synergy-of-abbyy-and-uipath/"><u>Enhancing Intelligence in Automation: The Synergy of ABBYY and UiPath</u></a></li>
<li><a href="https://some-tips.techidaily.com/environmental-commitment-by-abbyy-over-2000-new-trees-set-for-yearly-planting-press-disclosure/"><u>Environmental Commitment by ABBYY: Over 2,000 New Trees Set for Yearly Planting - Press Disclosure</u></a></li>
<li><a href="https://some-tips.techidaily.com/federal-tech-innovations-automating-government-with-intelligence-official-podcast/"><u>Federal Tech Innovations: Automating Government with Intelligence - Official Podcast</u></a></li>
<li><a href="https://some-tips.techidaily.com/going-digital-with-abbyys-advanced-data-capture-tech-revolutionizing-healthcare-management/"><u>Going Digital with ABBYY's Advanced Data Capture Tech: Revolutionizing Healthcare Management</u></a></li>
<li><a href="https://some-tips.techidaily.com/how-artificial-intelligence-is-revolutionizing-the-landscape-of-banking-and-insurance/"><u>How Artificial Intelligence Is Revolutionizing the Landscape of Banking & Insurance</u></a></li>
<li><a href="https://android-unlock.techidaily.com/how-to-reset-gmail-password-on-samsung-galaxy-a23-5g-devices-by-drfone-android/"><u>How to Reset Gmail Password on Samsung Galaxy A23 5G Devices</u></a></li>
<li><a href="https://ios-unlock.techidaily.com/in-2024-can-you-unlock-iphone-12-pro-max-after-forgetting-the-passcode-by-drfone-ios/"><u>In 2024, Can You Unlock iPhone 12 Pro Max After Forgetting the Passcode?</u></a></li>
<li><a href="https://twitter-videos.techidaily.com/in-2024-restore-lost-sounds-to-twitter-vids/"><u>In 2024, Restore Lost Sounds to Twitter Vids</u></a></li>
<li><a href="https://some-tips.techidaily.com/optimize-with-cookiebot-smart-seo-tools-tailored-for-success/"><u>Optimize with Cookiebot: Smart SEO Tools Tailored for Success</u></a></li>
<li><a href="https://some-tips.techidaily.com/revolutionize-your-websites-user-experience-using-advanced-cookieless-tracking-technology/"><u>Revolutionize Your Website's User Experience Using Advanced Cookieless Tracking Technology</u></a></li>
<li><a href="https://tech-hub.techidaily.com/transform-your-gaming-world-with-these-6-tips-on-utilizing-chatgpt-in-script-writing/"><u>Transform Your Gaming World with These 6 Tips on Utilizing ChatGPT in Script Writing</u></a></li>
<li><a href="https://facebook-videos.techidaily.com/yearly-recording-runners-fb-live-sessions/"><u>Yearly Recording Runners FB Live Sessions</u></a></li>
</ul></div>

