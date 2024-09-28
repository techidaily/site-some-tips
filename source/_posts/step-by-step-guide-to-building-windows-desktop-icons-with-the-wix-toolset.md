---
title: Step-by-Step Guide to Building Windows Desktop Icons with the WiX Toolset
date: 2024-09-26T03:27:04.859Z
updated: 2024-09-27T17:53:44.359Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Step-by-Step Guide to Building Windows Desktop Icons with the WiX Toolset
thumbnail: https://thmb.techidaily.com/509fff23b0ac771700c9cc9f462572328b6f939b94b3444a0e657778351b7b6a.jpg
---

## Step-by-Step Guide to Building Windows Desktop Icons with the WiX Toolset

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

## How to Create a Desktop Shortcut using WiX Toolset

Written by [Renato Ivanescu](https://tools.techidaily.com/advancedinstaller/products/) · February 15th, 2023

In this article, we want to focus on desktop shortcut creation specifically for a **Windows Forms application using the WiX Toolset**.

**Shortcuts** serve as a valuable tool in the development of applications, allowing for an easier way to find and launch programs. It's a common practice to create shortcuts during application installation, especially for desktop access.

Before we get started, you need to make sure you have the WiX Toolset extension for Visual Studio. Check out this article: [WiX Toolset Visual Studio Extension](https://tools.techidaily.com/advancedinstaller/products/) to see how you can **add the extension to Visual Studio**.

<!-- affiliate ads begin -->
<a href="https://unicoeye.pxf.io/c/5597632/2134246/18498" target="_top" id="2134246">
  <img src="//a.impactradius-go.com/display-ad/18498-2134246" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://unicoeye.pxf.io/i/5597632/2134246/18498" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to add the WiX setup project

Once you have the WiX Toolset extension added to Visual Studio and your Windows Forms application is up and running, you need to create a setup project.Follow these steps to **create a setup project for your application**:

1\. Right-click on the project solution → _Add_ → _New Project._

2\. Choose _Setup Project for Wix_ from the project list. 

![Setup Project for Wix](https://cdn.advancedinstaller.com/img/create-desktop-shortcut-using-wix/setup-project-for-wix.png "Setup Project for Wix")  

3\. Once you add the setup project, you should find it in the _Solution Explorer_.

![Visual Studio Solution Explorer](https://cdn.advancedinstaller.com/img/create-desktop-shortcut-using-wix/viusal-studio-solution-explorer.png "Visual Studio Solution Explorer")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2037346/7443" target="_top" id="2037346">
  <img src="//a.impactradius-go.com/display-ad/7443-2037346" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2037346/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

4\. To add the desktop shortcut, we have to edit the _Product.wxs_ file.

### How to edit the Product.wxs file to add your desktop shortcut

### 1\. Define the directory structure

To include a desktop shortcut in your package, it is necessary to **declare the desktop directory**. You can achieve this by modifying the <Directory> structure to include the desktop directory declaration by using the TARGETDIR ID.

<Directory Id="TARGETDIR" Name="SourceDir">
  …
  <Directory Id="DesktopFolder" Name="Desktop" />
</Directory>

Copy

<!-- affiliate ads begin -->
<a href="https://bluettius.sjv.io/c/5597632/2139111/17108" target="_top" id="2139111">
  <img src="//a.impactradius-go.com/display-ad/17108-2139111" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://bluettius.sjv.io/i/5597632/2139111/17108" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### 2\. Add the shortcut to your package

Once the desktop directory is added to the directory structure, let’s **add the shortcut to the installer package**.

Follow these steps:

2.1\. Add a reference to the desktop directory structure created at the previous step using _<DirectoryRef>_ element.

<DirectoryRef Id="DesktopFolder">

Copy

2.2\. Define an atomic unit of installation using a _<Component>_ element.

<Component Id="ApplicationShortcutDesktop"                   
           Guid="305dc292-f9af-4961-9fd1-bf38f5ad08db">

Copy

2.3\. Specify the shortcut to be installed using a _<Shortcut>_ element. Here you have to set some attributes, including: ID (is unique), name, description (optional), target (points to the executable file), and the working directory for the shortcut.

<Shortcut Id="ApplicationDesktopShortcut" 
          Name="DSapp" 
          Description="My Application" 
          Target="[INSTALLFOLDER]DSapp.exe" 
          WorkingDirectory="INSTALLFOLDER" />

Copy

2.4\. Create a registry entry by using a _<RegistryValue>_ element.

<RegistryValue Root="HKCU"                Key="Software\MyCompany\DSapp"                Name="installed"                Type="integer"                Value="1"                KeyPath="yes" />

Copy

Here is how the final code should look:

<Fragment> <DirectoryRef Id="DesktopFolder">  <Component Id="ApplicationShortcutDesktop"                                 Guid="305dc292-f9af-4961-9fd1-bf38f5ad08db">      <Shortcut Id="ApplicationDesktopShortcut"                 Name="DSapp"                 Description="My Application"                 Target="[INSTALLFOLDER]DSapp.exe"                 WorkingDirectory="INSTALLFOLDER" />      <RegistryValue Root="HKCU"                      Key="Software\MyCompany\DSapp"                      Name="installed"                      Type="integer"                      Value="1"                      KeyPath="yes" />  </Component> </DirectoryRef></Fragment>

Copy

<!-- affiliate ads begin -->
<span id="1328683">
					<video width="200" height="200" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1328683.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/15852-1328683">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1328683.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:125px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fthefitville.pxf.io%2Fc%2F5597632%2F1328683%2F15852'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1328683/15852" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### 3\. Add an icon to your desktop shortcut

You can help your users find your application easier by adding an icon to your shortcut. By doing this, you not only establish familiarity with your application but also improve its recognition and accessibility. 

Follow these steps to include the icon in your setup project:

3.1\. Create a folder under the setup project (Icons), and copy the icon (Shortcuticon.ico) to that folder.

![Create folder under the setup project](https://cdn.advancedinstaller.com/img/create-desktop-shortcut-using-wix/create-folder-for-setup-project.png "Create folder under the setup project")  

3.2\. Then, you can add the icon to your installation package by declaring the _<Icon>_ element within the <Fragment/> element. Make sure to set an _Id_ for the icon and specify the _path_ to the icon file.

<Fragment>
	<Icon Id="MyIcon" SourceFile="Icons\ShortcutIcon.ico" />
</Fragment>

Copy

3.3\. Next, you have to add a reference to the icon on the shortcut element using the _Id_ you set for the icon.

          <Shortcut Id="ApplicationDesktopShortcut" 	
          Name="DSapp" 
          Description="My Application" 
          …
          Icon ="MyIcon"
          />
        
Copy

### 4\. Install the shortcut

In the final step, we need to instruct the installer to **install the shortcut**. We can achieve that by using a _<Feature>_ element and referencing the shortcut component with a _<ComponentRef>_ element, which includes the component ID as a reference.

<Feature Id="ProductFeature" Title="AppSetup" Level="1">
   …
   <ComponentRef Id="ApplicationShortcutDesktop" />
</Feature>

Copy

### Conclusion

While creating a shortcut with WiX can be a time-consuming process involving multiple modifications to the XML file, there is a more efficient solution available.

Using a tool with a powerful GUI, such as Advanced Installer, simplifies the process by offering a visual interface for creating shortcuts.

Additionally, if you already have a WiX project, Advanced Installer even allows you to import it, making the task faster and more straightforward to complete.

You can check out the following video to see how to create a desktop shortcut using Advanced Installer:

Transform your application packaging process with ease and efficiency by trying Advanced Installer's [30-day full-featured free trial now](https://tools.techidaily.com/advancedinstaller/products/)!

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
<li><a href="https://facebook-video-share.techidaily.com/new-2024-approved-expert-advice-for-embedding-youtube-playlists-with-ease/"><u>[New] 2024 Approved Expert Advice for Embedding YouTube Playlists with Ease</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/updated-dive-into-camtasias-ken-burns-feature-rich-tutorial/"><u>[Updated] Dive Into Camtasia’s Ken Burns Feature-Rich Tutorial</u></a></li>
<li><a href="https://fox-http.techidaily.com/updated-in-2024-quick-guide-applying-on-screen-captions-to-photos-videos/"><u>[Updated] In 2024, Quick Guide Applying On-Screen Captions to Photos Videos</u></a></li>
<li><a href="https://visual-screen-recording.techidaily.com/updated-masterclass-in-brief-lapses-top-5-for-2024/"><u>[Updated] Masterclass in Brief Lapses #Top 5 for 2024</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/updated-step-by-step-screen-recording-in-win10-gaming-for-2024/"><u>[Updated] Step-by-Step Screen Recording in Win10 Gaming for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-complete-guide-to-the-latest-in-lgs-ultra-clear-monitoring/"><u>[Updated] The Complete Guide to the Latest in LG’s Ultra-Clear Monitoring</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-thorough-breakdown-the-dji-inspire-1-features/"><u>[Updated] Thorough Breakdown The DJI Inspire 1 Features</u></a></li>
<li><a href="https://tech-savvy.techidaily.com/achieve-longer-bluetooth-connections-strategies-for-windows-11-systems/"><u>Achieve Longer Bluetooth Connections: Strategies for Windows 11 Systems</u></a></li>
<li><a href="https://win-forum.techidaily.com/boost-your-brand-across-top-platforms-twitter-instagram-facebook-and-youtubing/"><u>Boost Your Brand Across Top Platforms - Twitter, Instagram, Facebook & YouTubing</u></a></li>
<li><a href="https://youtube-videos.techidaily.com/easy-download-of-youtube-preview-pictures/"><u>Easy Download of YouTube Preview Pictures</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-streaming-success-easily-convert-srt-formats/"><u>In 2024, Streaming Success Easily Convert SRT Formats</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-streamlining-submission-a-podcasters-guide/"><u>In 2024, Streamlining Submission A Podcaster's Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-route-to-richer-tiktok-bios-a-guide-to-linktree-integration/"><u>In 2024, The Route to Richer TikTok Bios A Guide to Linktree Integration</u></a></li>
<li><a href="https://tiktok-videos.techidaily.com/in-2024-top-30-inspirational-ideas-fusing-animated-themes-and-social-media/"><u>In 2024, Top 30 Inspirational Ideas Fusing Animated Themes and Social Media</u></a></li>
<li><a href="https://hardware-updates.techidaily.com/include-stage-directions-that-metaphorically-represent-scientific-processes-eg-characters-absorbing-information-as-silica-gel-absorbs-water/"><u>Include Stage Directions that Metaphorically Represent Scientific Processes (E.g., Characters 'Absorbing' Information as Silica Gel Absorbs Water).</u></a></li>
<li><a href="https://some-tips.techidaily.com/syncing-b-roll-sequences-with-main-scenes-effortlessly-for-2024/"><u>Syncing B Roll Sequences with Main Scenes Effortlessly for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-professionals-playbook-refined-gopro-video-production-techniques-for-2024/"><u>The Professional's Playbook Refined GoPro Video Production Techniques for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/transformative-tactics-for-advanced-iphone-x-animoji-utilization-for-2024/"><u>Transformative Tactics for Advanced iPhone X Animoji Utilization for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveiling-image-quality-a-newbies-comprehensible-guide-for-2024/"><u>Unveiling Image Quality A Newbie's Comprehensible Guide for 2024</u></a></li>
</ul></div>

