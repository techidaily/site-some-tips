---
title: Mastering Quiet Install and Uninstall on Wix Using MSI Technology
date: 2024-09-25T01:43:11.591Z
updated: 2024-09-27T21:23:57.287Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Mastering Quiet Install and Uninstall on Wix Using MSI Technology
thumbnail: https://thmb.techidaily.com/4e207de12ae2e23e3e120883c3d81a23ae2c9e5768e29dea060181f5e75a70e5.jpg
---

## Mastering Quiet Install and Uninstall on Wix Using MSI Technology

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
<a href="https://aligracehair.sjv.io/c/5597632/2135408/19272" target="_top" id="2135408">
  <img src="//a.impactradius-go.com/display-ad/19272-2135408" border="0" alt="https://techidaily.com" width="120" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135408/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to silently install and uninstall the MSI package

When you are creating an MSI installation package with WiX, you have two options for performing a silent install and uninstall:

**1\. Do not add any UI/UIRef elements to the installer package.** 

If you use WiX to create an MSI package, it will not have a built-in user interface by default (except for a simple progress dialog). 

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)To add an user interface to an MSI created with WiX, you have to use the **WiXUI library**. This is the standard user interface that WiX Toolset comes with. When creating a setup project, this library is not referenced by default. So, you will have a silent install if you do not add a reference for this library.  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2137411/7443" target="_top" id="2137411">
  <img src="//a.impactradius-go.com/display-ad/7443-2137411" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2137411/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

**2\. Use command line arguments.** 

This option is available regardless of the software used to create MSI packages; therefore, it is available for MSI packages created with WiX. MSIs use msiexec.exe to install and uninstall the setup and accept the following silent install standard parameters: 

* **/quiet**: quiet mode → no user interaction required
* **/passive**: unattended mode → the installation only shows a progress bar
* **/qn** → specifies there is no UI during the installation process

A regular command line used to install an MSI silently should look like this:

msiexec /i <AppName.msi> /qn /l*v install.log

Copy

![WIX MSI to do a silent install or uninstall of a web app](https://cdn.advancedinstaller.com/img/msi-package-silent-install-uninstall-wix/wix-msi-to-do-a-silent-install-or-uninstall-of-a-web-app.png "WIX MSI to do a silent install or uninstall of a web app")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2027195/19272" target="_top" id="2027195">
  <img src="//a.impactradius-go.com/display-ad/19272-2027195" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2027195/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

You can use the **/l\*v** install parameter to create an installation log. As the GUI is hidden, the installation log helps you identify the errors that can occur during the installation process.

If your installation package uses an EXE bootstrapper, you have to use a specific command line to launch the MSI. This command line can use the same parameters as when the MSI is launched with msiexec. The parameters will be passed to the MSI package.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Keep in mind that you must **use an elevated command prompt** to silently install an MSI package. Otherwise, the installation will fail as you do not have the privileges to complete the installation. To achieve this, use the Run as administrator context menu option.

### How to make the MSI installer package silent using Advanced Installer?

When using Advanced Installer to create an MSI package, you have the opportunity to enhance the user interface (UI) with attractive and robust themes. However, if you intend to execute a silent installation, you can effortlessly achieve this by enabling the "**Limit to basic user interface**" option. By selecting this option, the MSI will perform a silent install, displaying only a simple progress indicator and error handling functionality.

You can find this option on the _Install Parameters_ page, under the _Install Options_ section. Once enabled, a progress bar will be displayed throughout the installation process, ensuring a seamless experience for the user. With this setting in place, users won't need to perform any actions during the installation, as it will proceed automatically in the background.

![make the MSI installer package silent using Advanced Installer](https://cdn.advancedinstaller.com/img/msi-package-silent-install-uninstall-wix/make-the-msi-installer-package-silent-using-advanced-installer.png "make the MSI installer package silent using Advanced Installer")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2037475/7443" target="_top" id="2037475">
  <img src="//a.impactradius-go.com/display-ad/7443-2037475" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2037475/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://youtube-stream.techidaily.com/new-rapid-share-tactics-for-youtube-lists/"><u>[New] Rapid Share Tactics for YouTube Lists</u></a></li>
<li><a href="https://screen-recording.techidaily.com/updated-2024-approved-how-to-record-twitch-live-stream/"><u>[Updated] 2024 Approved How to Record Twitch Live Stream</u></a></li>
<li><a href="https://facebook-video-share.techidaily.com/updated-flashflicker-artist/"><u>[Updated] FlashFlicker Artist</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-evolution-and-alternatives-to-googles-ar-stickers/"><u>[Updated] The Evolution and Alternatives to Google's AR Stickers</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-straightforward-approach-to-editing-age-on-tiktok/"><u>2024 Approved The Straightforward Approach to Editing Age on TikTok</u></a></li>
<li><a href="https://buynow-info.techidaily.com/broadening-gaming-horizons-by-sharing-your-xbox-one-titles-with-friends/"><u>Broadening Gaming Horizons by Sharing Your Xbox One Titles With Friends</u></a></li>
<li><a href="https://tech-hub.techidaily.com/empower-your-data-management-with-ai-using-chatgpt-in-google-sheets/"><u>Empower Your Data Management with AI: Using ChatGPT in Google Sheets</u></a></li>
<li><a href="https://visual-screen-recording.techidaily.com/simple-steps-for-iphone-screen-capture/"><u>Simple Steps for iPhone Screen Capture</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/turntable-innovation-meets-classic-vinyl-playback/"><u>Turntable Innovation Meets Classic Vinyl Playback</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-network-transmission-power-with-vlc-for-2024/"><u>Unlocking Network Transmission Power with VLC for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-the-potential-of-slug-line-formats-in-screenplays-for-2024/"><u>Unlocking the Potential of Slug Line Formats in Screenplays for 2024</u></a></li>
</ul></div>

