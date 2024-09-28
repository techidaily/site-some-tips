---
title: Silent Deployment & Removal with Wix MSI for Your Web Application
date: 2024-09-24T12:06:32.352Z
updated: 2024-09-28T10:25:26.766Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Silent Deployment & Removal with Wix MSI for Your Web Application
thumbnail: https://thmb.techidaily.com/34ef4ca08c3dfcb784929375e3e95bcc8f2ba621080c440e931274a3c95d80cc.jpg
---

## Silent Deployment & Removal with Wix MSI for Your Web Application

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

## How to use WIX MSI to do a silent install or uninstall of a web app

Written by [Renato Ivanescu](https://tools.techidaily.com/advancedinstaller/products/) · June 20th, 2023

When it comes to **installing or uninstalling an application package**, the level of user interaction can vary based on your specific needs. In cases where you prefer to minimize user involvement, a convenient solution is to opt for a **silent install or uninstall**. With a silent installation, users are spared the hassle of navigating through an installation wizard and repeatedly clicking the "Next" button.

This approach proves particularly beneficial in scenarios where you need to perform multiple installations or uninstallations, such as in enterprise settings or when deploying software across numerous devices.

If you're using WiX and you want to learn **how to create an MSI package for a silent installation or uninstallation** of an application, this article is exactly what you're searching for.

<!-- affiliate ads begin -->
<span id="1982485">
					<video width="576" height="240" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1982485.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1982485">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1982485.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1982485%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1982485/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to silently install and uninstall the MSI package

When you are creating an MSI installation package with WiX, you have two options for performing a silent install and uninstall:

**1\. Do not add any UI/UIRef elements to the installer package.** 

If you use WiX to create an MSI package, it will not have a built-in user interface by default (except for a simple progress dialog). 

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)To add an user interface to an MSI created with WiX, you have to use the **WiXUI library**. This is the standard user interface that WiX Toolset comes with. When creating a setup project, this library is not referenced by default. So, you will have a silent install if you do not add a reference for this library.  

**2\. Use command line arguments.** 

This option is available regardless of the software used to create MSI packages; therefore, it is available for MSI packages created with WiX. MSIs use msiexec.exe to install and uninstall the setup and accept the following silent install standard parameters: 

* **/quiet**: quiet mode → no user interaction required
* **/passive**: unattended mode → the installation only shows a progress bar
* **/qn** → specifies there is no UI during the installation process

A regular command line used to install an MSI silently should look like this:

msiexec /i <AppName.msi> /qn /l*v install.log

Copy

![WIX MSI to do a silent install or uninstall of a web app](https://cdn.advancedinstaller.com/img/msi-package-silent-install-uninstall-wix/wix-msi-to-do-a-silent-install-or-uninstall-of-a-web-app.png "WIX MSI to do a silent install or uninstall of a web app")  

You can use the **/l\*v** install parameter to create an installation log. As the GUI is hidden, the installation log helps you identify the errors that can occur during the installation process.

If your installation package uses an EXE bootstrapper, you have to use a specific command line to launch the MSI. This command line can use the same parameters as when the MSI is launched with msiexec. The parameters will be passed to the MSI package.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Keep in mind that you must **use an elevated command prompt** to silently install an MSI package. Otherwise, the installation will fail as you do not have the privileges to complete the installation. To achieve this, use the Run as administrator context menu option.

### How to make the MSI installer package silent using Advanced Installer?

When using Advanced Installer to create an MSI package, you have the opportunity to enhance the user interface (UI) with attractive and robust themes. However, if you intend to execute a silent installation, you can effortlessly achieve this by enabling the "**Limit to basic user interface**" option. By selecting this option, the MSI will perform a silent install, displaying only a simple progress indicator and error handling functionality.

You can find this option on the _Install Parameters_ page, under the _Install Options_ section. Once enabled, a progress bar will be displayed throughout the installation process, ensuring a seamless experience for the user. With this setting in place, users won't need to perform any actions during the installation, as it will proceed automatically in the background.

![make the MSI installer package silent using Advanced Installer](https://cdn.advancedinstaller.com/img/msi-package-silent-install-uninstall-wix/make-the-msi-installer-package-silent-using-advanced-installer.png "make the MSI installer package silent using Advanced Installer")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2100538/7443" target="_top" id="2100538">
  <img src="//a.impactradius-go.com/display-ad/7443-2100538" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2100538/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

<!-- affiliate ads begin -->
<span id="1531882">
					<video width="864" height="1536" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1531882.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/16446-1531882">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1531882.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:540px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Flaganoo.pxf.io%2Fc%2F5597632%2F1531882%2F16446'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1531882/16446" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Conclusion

To perform a silent install using WiX without command-line arguments, you can omit or avoid adding a reference to the WiXUI library. However, with Advanced Installer, you can simply check the option available through the GUI to limit the MSI installation to a basic user interface. 

Discover the Advanced Installer UI level settings by watching the below video:

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
<a href="https://appsumo.8odi.net/c/5597632/1062447/7443" target="_top" id="1062447">
  <img src="//a.impactradius-go.com/display-ad/7443-1062447" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/1062447/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://desktop-recording.techidaily.com/new-audiovisual-elevation-leading-high-definition-hdmi-21-displays/"><u>[New] Audiovisual Elevation Leading High-Definition (HDMI 2.1) Displays</u></a></li>
<li><a href="https://fox-http.techidaily.com/new-in-2024-dimension-dilemma-solved-why-does-imovie-crop/"><u>[New] In 2024, Dimension Dilemma Solved Why Does iMovie Crop?</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-elevation-of-professional-display-an-in-depth-examination-of-the-bl2711u/"><u>[New] The Elevation of Professional Display An In-Depth Examination of the BL2711U</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-ultimate-selection-of-top-5-best-android-photo-apps/"><u>[New] The Ultimate Selection of Top 5 Best Android Photo Apps</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unlocking-social-media-stardom-essential-strategies-for-instagram-fame/"><u>[New] Unlocking Social Media Stardom Essential Strategies for Instagram Fame</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/updated-2024-approved-optimize-your-online-presence-with-linked-fb-stories/"><u>[Updated] 2024 Approved Optimize Your Online Presence with Linked FB Stories</u></a></li>
<li><a href="https://some-skills.techidaily.com/updated-ultimate-list-of-leading-real-time-tv-streamers-compared/"><u>[Updated] Ultimate List of Leading Real-Time TV Streamers Compared</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-quickest-way-to-entertain-kapwing-memes/"><u>2024 Approved The Quickest Way to Entertain - Kapwing Memes</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-ultimate-guide-to-fisheye-camera-capabilities/"><u>2024 Approved The Ultimate Guide to Fisheye Camera Capabilities</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-ultimate-tutorial-for-downloading-wm6/"><u>2024 Approved Ultimate Tutorial for Downloading WM6</u></a></li>
<li><a href="https://techno-recovery.techidaily.com/how-to-combine-two-columns-in-excel/"><u>How to Combine Two Columns in Excel</u></a></li>
<li><a href="https://tech-savvy.techidaily.com/optimize-your-speeches-top-7-ai-assistants/"><u>Optimize Your Speeches: Top 7 AI Assistants</u></a></li>
<li><a href="https://vp-tips.techidaily.com/powerful-manycam-substitutes-discover-superior-live-broadcast-tools-and-remote-camera-features/"><u>Powerful ManyCam Substitutes - Discover Superior Live Broadcast Tools and Remote Camera Features</u></a></li>
<li><a href="https://ai-topics.techidaily.com/updated-what-is-an-ai-video-generator-in-2024/"><u>Updated What Is an AI Video Generator, In 2024</u></a></li>
</ul></div>

