---
title: Step-by-Step Guide to Building Windows Desktop Icons with the WiX Toolset
date: 2024-10-01T16:54:57.585Z
updated: 2024-10-03T16:59:09.295Z
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
<a href="https://aligracehair.sjv.io/c/5597632/2135408/19272" target="_top" id="2135408">
  <img src="//a.impactradius-go.com/display-ad/19272-2135408" border="0" alt="https://techidaily.com" width="120" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135408/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to add the WiX setup project

Once you have the WiX Toolset extension added to Visual Studio and your Windows Forms application is up and running, you need to create a setup project.Follow these steps to **create a setup project for your application**:

1\. Right-click on the project solution → _Add_ → _New Project._

2\. Choose _Setup Project for Wix_ from the project list. 

![Setup Project for Wix](https://cdn.advancedinstaller.com/img/create-desktop-shortcut-using-wix/setup-project-for-wix.png "Setup Project for Wix")  

<!-- affiliate ads begin -->
<a href="https://sentrypc.7eer.net/c/5597632/398449/3022" target="_top" id="398449">
  <img src="//a.impactradius-go.com/display-ad/3022-398449" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://sentrypc.7eer.net/i/5597632/398449/3022" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

3\. Once you add the setup project, you should find it in the _Solution Explorer_.

![Visual Studio Solution Explorer](https://cdn.advancedinstaller.com/img/create-desktop-shortcut-using-wix/viusal-studio-solution-explorer.png "Visual Studio Solution Explorer")  

4\. To add the desktop shortcut, we have to edit the _Product.wxs_ file.

### How to edit the Product.wxs file to add your desktop shortcut

### 1\. Define the directory structure

To include a desktop shortcut in your package, it is necessary to **declare the desktop directory**. You can achieve this by modifying the <Directory> structure to include the desktop directory declaration by using the TARGETDIR ID.

<Directory Id="TARGETDIR" Name="SourceDir">
  …
  <Directory Id="DesktopFolder" Name="Desktop" />
</Directory>

Copy

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
<a href="https://appsumo.8odi.net/c/5597632/2144297/7443" target="_top" id="2144297">
  <img src="//a.impactradius-go.com/display-ad/7443-2144297" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2144297/7443" style="position:absolute;visibility:hidden;" border="0" />
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

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2052060/7443" target="_top" id="2052060">
  <img src="//a.impactradius-go.com/display-ad/7443-2052060" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2052060/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://facebook-videos.techidaily.com/updated-2024-approved-facebooks-real-time-media-watch-guide-2023/"><u>[Updated] 2024 Approved Facebook's Real-Time Media Watch Guide, 2023</u></a></li>
<li><a href="https://youtube-blog.techidaily.com/ed-2024-approved-journey-around-the-world-on-youtube-including-you/"><u>[Updated] 2024 Approved Journey Around the World on YouTube, Including You</u></a></li>
<li><a href="https://youtube-help.techidaily.com/2024-approved-from-capture-to-share-proven-methods-for-live-360-video-on-youtube/"><u>2024 Approved From Capture to Share Proven Methods for Live 360° Video on Youtube</u></a></li>
<li><a href="https://fox-http.techidaily.com/2024-approved-top-online-sources-for-3d-glitter-text-designs/"><u>2024 Approved Top Online Sources for 3D Glitter Text Designs</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhance-your-visuals-with-our-cutting-edge-fork-of-stable-diffusion-perfect-for-creating-large-format-images-effortlessly/"><u>Enhance Your Visuals with Our Cutting-Edge Fork of Stable Diffusion, Perfect for Creating Large Format Images Effortlessly</u></a></li>
<li><a href="https://some-tips.techidaily.com/expanding-ai-assistance-bringing-chatgpt-features-into-diverse-applications/"><u>Expanding AI Assistance: Bringing ChatGPT Features Into Diverse Applications</u></a></li>
<li><a href="https://some-tips.techidaily.com/experience-the-future-with-taco-bells-ai-powered-drive-thru-system/"><u>Experience the Future with Taco Bell's AI-Powered Drive-Thru System</u></a></li>
<li><a href="https://some-tips.techidaily.com/experience-unmatched-travel-planning-with-bings-innovative-ai-concierge/"><u>Experience Unmatched Travel Planning with Bing's Innovative AI Concierge</u></a></li>
<li><a href="https://some-tips.techidaily.com/exploring-the-creality-k1-max-how-this-3d-printer-is-changing-the-game-for-hobbyists-and-professionals-alike/"><u>Exploring the Creality K1 Max: How This 3D Printer Is Changing the Game for Hobbyists and Professionals Alike</u></a></li>
<li><a href="https://some-tips.techidaily.com/exploring-the-innovative-strategy-behind-duckduckgos-latest-ai-powered-search-technology/"><u>Exploring the Innovative Strategy Behind DuckDuckGo's Latest AI-Powered Search Technology</u></a></li>
<li><a href="https://some-tips.techidaily.com/free-access-chatgpt-now-offers-customized-gpt-models-to-everyone/"><u>Free Access: ChatGPT Now Offers Customized GPT Models to Everyone</u></a></li>
<li><a href="https://some-tips.techidaily.com/how-to-effectively-recharge-oculus-quest-vr-controllers-a-comprehensive-tutorial/"><u>How To Effectively Recharge Oculus Quest VR Controllers - A Comprehensive Tutorial</u></a></li>
<li><a href="https://some-tips.techidaily.com/identifying-genuine-interactions-distinguishing-authentic-chatgpt-communications-from-fake-ones/"><u>Identifying Genuine Interactions: Distinguishing Authentic ChatGPT Communications From Fake Ones</u></a></li>
<li><a href="https://instagram-video-recordings.techidaily.com/in-2024-unveiling-clearer-imagery-instagrams-video-cropping-secrets/"><u>In 2024, Unveiling Clearer Imagery Instagram's Video Cropping Secrets</u></a></li>
<li><a href="https://android-location-track.techidaily.com/in-2024-ways-to-stop-parent-tracking-your-vivo-y17s-drfone-by-drfone-virtual-android/"><u>In 2024, Ways to stop parent tracking your Vivo Y17s | Dr.fone</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/in-2024-what-are-location-permissions-life360-on-infinix-zero-5g-2023-turbo-drfone-by-drfone-virtual-android/"><u>In 2024, What are Location Permissions Life360 On Infinix Zero 5G 2023 Turbo? | Dr.fone</u></a></li>
<li><a href="https://review-topics.techidaily.com/recover-lost-data-from-xiaomi-13-ultra-by-fonelab-android-recover-data/"><u>Recover lost data from Xiaomi 13 Ultra</u></a></li>
<li><a href="https://vp-tips.techidaily.com/step-by-step-guide-adding-and-viewing-subtitles-on-your-dvds/"><u>Step-by-Step Guide: Adding and Viewing Subtitles on Your DVDs</u></a></li>
<li><a href="https://ios-pokemon-go.techidaily.com/ways-to-trade-pokemon-go-from-far-away-on-apple-iphone-15-drfone-by-drfone-virtual-ios/"><u>Ways to trade pokemon go from far away On Apple iPhone 15? | Dr.fone</u></a></li>
</ul></div>

