---
title: Silent Deployment & Removal with Wix MSI for Your Web Application
date: 2024-09-28T19:34:17.959Z
updated: 2024-10-03T16:47:55.778Z
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

<!-- affiliate ads begin -->
<span id="1374820">
					<video width="200" height="200" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1374820.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/15852-1374820">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1374820.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:125px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fthefitville.pxf.io%2Fc%2F5597632%2F1374820%2F15852'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1374820/15852" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

You can use the **/l\*v** install parameter to create an installation log. As the GUI is hidden, the installation log helps you identify the errors that can occur during the installation process.

If your installation package uses an EXE bootstrapper, you have to use a specific command line to launch the MSI. This command line can use the same parameters as when the MSI is launched with msiexec. The parameters will be passed to the MSI package.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Keep in mind that you must **use an elevated command prompt** to silently install an MSI package. Otherwise, the installation will fail as you do not have the privileges to complete the installation. To achieve this, use the Run as administrator context menu option.

<!-- affiliate ads begin -->
<a href="https://25home.pxf.io/c/5597632/2148646/16836" target="_top" id="2148646">
  <img src="//a.impactradius-go.com/display-ad/16836-2148646" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://25home.pxf.io/i/5597632/2148646/16836" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to make the MSI installer package silent using Advanced Installer?

When using Advanced Installer to create an MSI package, you have the opportunity to enhance the user interface (UI) with attractive and robust themes. However, if you intend to execute a silent installation, you can effortlessly achieve this by enabling the "**Limit to basic user interface**" option. By selecting this option, the MSI will perform a silent install, displaying only a simple progress indicator and error handling functionality.

You can find this option on the _Install Parameters_ page, under the _Install Options_ section. Once enabled, a progress bar will be displayed throughout the installation process, ensuring a seamless experience for the user. With this setting in place, users won't need to perform any actions during the installation, as it will proceed automatically in the background.

![make the MSI installer package silent using Advanced Installer](https://cdn.advancedinstaller.com/img/msi-package-silent-install-uninstall-wix/make-the-msi-installer-package-silent-using-advanced-installer.png "make the MSI installer package silent using Advanced Installer")  

<!-- affiliate ads begin -->
<a href="https://smilemakers.pxf.io/c/5597632/2123899/26106" target="_top" id="2123899">
  <img src="//a.impactradius-go.com/display-ad/26106-2123899" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://smilemakers.pxf.io/i/5597632/2123899/26106" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1896527/19272" target="_top" id="1896527">
  <img src="//a.impactradius-go.com/display-ad/19272-1896527" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1896527/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://facebook-video-content.techidaily.com/new-in-2024-escape-from-ennui-with-humor-top-20-funny-faces-in-social-media-jail/"><u>[New] In 2024, Escape From Ennui with Humor Top 20 Funny Faces in Social Media Jail</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/2024-approved-extended-motion-systems-appraisal/"><u>2024 Approved Extended Motion Systems Appraisal</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/2024-approved-innovative-photography-vertical-vistas-via-mobile/"><u>2024 Approved Innovative Photography Vertical Vistas via Mobile</u></a></li>
<li><a href="https://some-approaches.techidaily.com/2024-approved-the-aurora-hdr-experience-is-it-transformative/"><u>2024 Approved The Aurora HDR Experience Is It Transformative?</u></a></li>
<li><a href="https://win11.techidaily.com/changing-file-dates-in-windows-a-practical-overview/"><u>Changing File Dates in Windows: A Practical Overview</u></a></li>
<li><a href="https://windows11.techidaily.com/how-to-snapping-windows-uac-alerts/"><u>How-To: Snapping Windows UAC Alerts</u></a></li>
<li><a href="https://ai-driven-video-production.techidaily.com/new-in-2024-upgrading-your-edit-why-final-cut-pro-outshines-final-cut-express/"><u>New In 2024, Upgrading Your Edit Why Final Cut Pro Outshines Final Cut Express</u></a></li>
<li><a href="https://some-tips.techidaily.com/tech-news-recap-what-to-expect-from-the-latest-phone-launches-by-google-and-samsung-this-week/"><u>Tech News Recap: What to Expect From the Latest Phone Launches by Google and Samsung This Week</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-advantages-of-choosing-a-smartphone-with-e-ink-technology-a-personal-perspective/"><u>The Advantages of Choosing a Smartphone with E-Ink Technology: A Personal Perspective</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-concept-of-ai-singularity-explained-reality-check/"><u>The Concept of AI Singularity Explained: Reality Check.</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-hidden-costs-of-mining-bitcoin-on-your-personal-computer/"><u>The Hidden Costs of Mining Bitcoin on Your Personal Computer</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-ultimate-top-10-reading-list-chosen-by-our-community/"><u>The Ultimate Top 10 Reading List, Chosen by Our Community</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-5-reasons-artificial-intelligence-assistants-havent-won-me-over-insights-and-perspectives/"><u>Top 5 Reasons Artificial Intelligence Assistants Haven't Won Me Over: Insights and Perspectives</u></a></li>
<li><a href="https://some-tips.techidaily.com/transforming-ai-art-with-simple-tweaks-unlock-potential-using-these-essential-8-midjourney-commands/"><u>Transforming AI Art with Simple Tweaks: Unlock Potential Using These Essential 8 Midjourney Commands</u></a></li>
<li><a href="https://some-tips.techidaily.com/transition-time-embracing-perplexity-the-innovative-ai-driven-search-platform/"><u>Transition Time: Embracing Perplexity, the Innovative AI-Driven Search Platform</u></a></li>
<li><a href="https://ai-video-apps.techidaily.com/updated-2024-approved-vintage-video-magic-a-step-by-step-guide-to-vhs-effects-in-final-cut-pro/"><u>Updated 2024 Approved Vintage Video Magic A Step-by-Step Guide to VHS Effects in Final Cut Pro</u></a></li>
<li><a href="https://win11.techidaily.com/windows-users-explore-these-8-great-video-editors/"><u>Windows Users, Explore These 8 Great Video Editors</u></a></li>
</ul></div>

