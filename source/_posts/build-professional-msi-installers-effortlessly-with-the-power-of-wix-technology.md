---
title: Build Professional MSI Installers Effortlessly with the Power of WiX Technology
date: 2024-10-02T19:02:15.513Z
updated: 2024-10-03T18:50:21.925Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Build Professional MSI Installers Effortlessly with the Power of WiX Technology
thumbnail: https://thmb.techidaily.com/96aa1b87d78d9da06b5a26c2f6109ba265782381d85277a374a3a1037690eb16.jpg
---

## Build Professional MSI Installers Effortlessly with the Power of WiX Technology

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

## How to create an MSI installer with WiX

Written by [Renato Ivanescu](https://tools.techidaily.com/advancedinstaller/products/) · June 20th, 2023

The **MSI format** is a widely recognized standard in the software industry for distributing software packages to Windows-based devices. MSI packages offer numerous advantages over alternative software installation methods, including enhanced reliability and improved performance. 

**WiX** is an open-source toolset to build MSI packages. It enables developers to create a software installation by writing XML that describes components, registry entries, and other resources.

In this article, I’ll show you **how to use WiX to create an MSI installer** for a Windows Forms application. Let’s dive in!

### Add the setup project to your application

Once you have created the Windows Forms application, the next step is to add the setup package to it.

1. _Right-click on the project solution_ → _Add_ → _New project._
2. From the project list, choose _Setup Project for WiX_. You will find this template only if you have the _Wix Toolset Visual Studio Extension_ installed. Need help installing it? We've got you – check out [this](https://tools.techidaily.com/advancedinstaller/products/) tutorial.

![Setup Project for WiX](https://cdn.advancedinstaller.com/img/create-msi-installer-with-wix/setup-project-for-wix.png "Setup Project for WiX")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2144271/7443" target="_top" id="2144271">
  <img src="//a.impactradius-go.com/display-ad/7443-2144271" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2144271/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

After creating the setup project, you should see it in _Solution Explore_r. The _Product.wxs_ file is the one containing the setup project logic.

![Solution Explorer - Product.wxs](https://cdn.advancedinstaller.com/img/create-msi-installer-with-wix/solution-explorer-product-wxs.png "Solution Explorer - Product.wxs")  

### Add project output to your setup project

Next, we need to include the deployable files in the setup project. To achieve this, we can use the Wix Setup Editor.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)**Wix Setup Editor** is an interactive GUI used to manage the setup files. It is available only if you have the Wax extension installed. If you want to see how to add the extension, you can also read [this](https://tools.techidaily.com/advancedinstaller/products/) article. 

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2036481/19272" target="_top" id="2036481">
  <img src="//a.impactradius-go.com/display-ad/19272-2036481" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2036481/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

To open the editor, go to _Tools_ → _WiX Setup Editor_. Here we have to make some configurations:

* Select the setup project in the ‘_Setup project to edit’_ section. In our case, it is _AppSetup_.
* For the ‘_Root directory’_, select _INSTALLFOLDER_.
* In the ‘_Projects to install_ section’, select your Window Forms application. We selected _MyApp,_ as this is our application.

![Wix Setup Editor](https://cdn.advancedinstaller.com/img/create-msi-installer-with-wix/wix-setup-editor.png "Wix Setup Editor")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2094482/7443" target="_top" id="2094482">
  <img src="//a.impactradius-go.com/display-ad/7443-2094482" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2094482/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

Make sure the files have the _resolved_ state like in the image above. If they have the _unmapped_ state as shown below, update it to _resolved_ by pressing the ‘+’ button under the warning sign.

![Add project output to your setup project](https://cdn.advancedinstaller.com/img/create-msi-installer-with-wix/add-project-output-to-your-setup-project.png "Add project output to your setup project")  

### How to edit product details

To modify the product details, navigate to the _Product.wxs_ file and make the necessary edits to the relevant fields. For example, we set the version to 1.2 and the manufacturer to Caphyon.

<Product Id="*" Name="My Application" Language="1033" Version="1.2" Manufacturer="Caphyon" UpgradeCode="be6d0f2f-6e81-4b75-a499-b5084d0e9a8f">
		<Package InstallerVersion="200" Compressed="yes" InstallScope="perMachine" />
		<MajorUpgrade DowngradeErrorMessage="A newer version of [ProductName] is already installed." />
		<MediaTemplate />
		<Feature Id="ProductFeature" Title="My Application" Level="1">
			<ComponentGroupRef Id="ProductComponents" />
		</Feature>
</Product>

Copy

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2137205/26400" target="_top" id="2137205">
  <img src="//a.impactradius-go.com/display-ad/26400-2137205" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2137205/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to create Shortcuts for your application?

In order to create a shortcut, we will need to make edits to the XML file since the Wix Setup Editor does not provide direct shortcut creation functionality.

Follow the next steps to add a shortcut on the Desktop and one in the Programs Menu:

1\. Define the directory structures.

<Directory Id="TARGETDIR" Name="SourceDir">
			<Directory Id="ProgramFilesFolder">
				<Directory Id="INSTALLFOLDER" Name="My Application" />
			</Directory>
			<Directory Id="ProgramMenuFolder">
				<Directory Id="MyAppFolder" Name="My Application"/>
			</Directory>
			<Directory Id="DesktopFolder" Name="Desktop" />
</Directory>

Copy

2\. Add the shortcuts to the installer package.

<DirectoryRef Id="MyAppFolder">
	<Component Id="ApplicationShortcut" Guid="e75a5c28-29d6-4d65-a5da-04363a176440">
		<Shortcut Id="ApplicationStartMenuShortcut"
						  Name="MyApp"
						  Description="MyApp"
						  Target="[INSTALLFOLDER]MyApp.exe"
						  WorkingDirectory="INSTALLFOLDER"/>
		<RemoveFolder Id="CleanUpShortCut" Directory="MyAppFolder" On="uninstall"/>
		<RegistryValue Root="HKCU" Key="Software\MyCompany\MyApp" Name="installed" Type="integer" Value="1" KeyPath="yes"/>
			</Component>
</DirectoryRef>
<DirectoryRef Id="DesktopFolder">
		<Component Id="ApplicationShortcutDesktop" Guid="cde1e030-eb64-49a5-b7b8-400b379c2d1a">
		<Shortcut Id="ApplicationDesktopShortcut" 
						  Name="MyApp" 
						  Description="MyApp" 
						  Target="[INSTALLFOLDER]MyApp.exe"
						  WorkingDirectory="INSTALLFOLDER" />
		<RegistryValue Root="HKCU" Key="Software\MyCompany\MyApp" Name="installed" Type="integer" Value="1" KeyPath="yes" />
		</Component>
</DirectoryRef>

Copy

3\. Tell Windows to install the shortcuts.

<Product Id="*" ….>
		<Feature Id="ProductFeature" Title="My Application" Level="1">
			….
			<ComponentRef Id="ApplicationShortcut" />
			<ComponentRef Id="ApplicationShortcutDesktop" />
		</Feature>
	</Product>

Copy

### How to add installation dialogues?

By default, when you create an installer package using WiX, it does not include a user interface (UI). However, if you wish to incorporate a minimal UI, you can follow the steps outlined below:

1\. _Right-click in the setup project_ → _Add_ → _Reference_s. In the _Add Reference_ dialog, look in the bin folder of the Wix toolset and add WinUiExtension.dll.

![add installation dialogues](https://cdn.advancedinstaller.com/img/create-msi-installer-with-wix/add-installation-dialogues.png "add installation dialogues")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1972670/19272" target="_top" id="1972670">
  <img src="//a.impactradius-go.com/display-ad/19272-1972670" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1972670/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. Go to the _Product.wsx_ file and add the next line inside the <_Product>_ element to reference the UI: 

<UIRef Id="WixUI_Minimal" />

Copy

### How to install your application?

Now, you can build the setup project. 

1. Go to the _bin_ folder inside the setup project folder to find the MSI file.
2. Run the file and install the application.
3. After the installation, you should find the shortcuts on the _Program Menu_ and _Desktop_.

![install your application](https://cdn.advancedinstaller.com/img/create-msi-installer-with-wix/install-your-application.png "install your application")  

### Conclusion

WiX toolset is a flexible tool for creating installer packages but when it comes to more complex packaging scenarios, it may require additional time and effort. The WiX Setup Editor offers limited functionalities, and you will often need to manually edit the XML file to configure most settings.

Alternatively, you can explore a GUI-based tool like Advanced Installer to create and manage installation packages. It has a user-friendly interface and is much easier to use. It provides a range of pre-built templates which simplify the process of creating MSIs. 

You can watch the tutorial below to see how easy it is to create an MSI with Advanced Installer.

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
<li><a href="https://screen-capture.techidaily.com/new-in-2024-incorporating-markers-a-step-by-step-videography-guide/"><u>[New] In 2024, Incorporating Markers A Step-By-Step Videography Guide</u></a></li>
<li><a href="https://screen-video-capture.techidaily.com/updated-top-3-voice-capturing-ipad-apps-reviewed/"><u>[Updated] TOP 3 Voice Capturing iPad Apps Reviewed</u></a></li>
<li><a href="https://extra-resources.techidaily.com/2024-approved-bridging-light-and-time-iphones-extended-exposure-techniques/"><u>2024 Approved Bridging Light and Time IPhone's Extended Exposure Techniques</u></a></li>
<li><a href="https://youtube-lab.techidaily.com/approved-pro-gamers-and-casters-to-subscribe-now/"><u>2024 Approved Pro Gamers & Casters to Subscribe Now</u></a></li>
<li><a href="https://blog-min.techidaily.com/4-ways-to-transfer-music-from-xiaomi-redmi-a2plus-to-iphone-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>4 Ways to Transfer Music from Xiaomi Redmi A2+ to iPhone | Dr.fone</u></a></li>
<li><a href="https://ai-vdieo-software.techidaily.com/free-vs-paid-the-best-3d-animation-software-for-creators/"><u>Free Vs. Paid The Best 3D Animation Software for Creators</u></a></li>
<li><a href="https://hardware-help.techidaily.com/how-to-secure-your-canon-d530s-optimal-functioning-with-latest-driver-downloads/"><u>How To Secure Your Canon D530's Optimal Functioning With Latest Driver Downloads</u></a></li>
<li><a href="https://some-tips.techidaily.com/introducing-apples-anticipated-vision-pro-glasses-a-comprehensive-review/"><u>Introducing Apple's Anticipated Vision Pro Glasses: A Comprehensive Review</u></a></li>
<li><a href="https://some-tips.techidaily.com/introducing-stable-diffusion-3-next-level-ai-innovation-unveiled/"><u>Introducing Stable Diffusion 3: Next-Level AI Innovation Unveiled</u></a></li>
<li><a href="https://some-tips.techidaily.com/is-investing-in-a-virtual-reality-vr-headset-worth-it/"><u>Is Investing in a Virtual Reality (VR) Headset Worth It?</u></a></li>
<li><a href="https://some-tips.techidaily.com/join-the-universal-zero-cost-meta-vr-community-a-new-era-of-virtual-interaction-begins/"><u>Join the Universal, Zero-Cost Meta VR Community - A New Era of Virtual Interaction Begins!</u></a></li>
<li><a href="https://some-tips.techidaily.com/mastering-personalized-text-generation-emulating-your-writing-style-with-chatgpt/"><u>Mastering Personalized Text Generation: Emulating Your Writing Style with ChatGPT</u></a></li>
<li><a href="https://some-tips.techidaily.com/maximizing-your-creative-outputs-mastering-the-synergy-of-chatgpt-dall-e-ter-and-midjourney/"><u>Maximizing Your Creative Outputs: Mastering the Synergy of ChatGPT, Dall-E Ter, and MidJourney</u></a></li>
<li><a href="https://some-tips.techidaily.com/my-disappointing-experience-with-online-car-shopping-at-carvana-vs-traditional-dealers/"><u>My Disappointing Experience with Online Car Shopping at Carvana Vs. Traditional Dealers</u></a></li>
<li><a href="https://some-tips.techidaily.com/next-level-smart-features-how-apples-cutting-edge-artificial-intelligence-transforms-siri-and-app-usage/"><u>Next-Level Smart Features: How Apple's Cutting-Edge Artificial Intelligence Transforms Siri and App Usage</u></a></li>
<li><a href="https://some-tips.techidaily.com/revolutionary-milestone-by-t-mobile-ultimate-speed-triumphs-as-new-record-for-sub-6-5g-uploads-established/"><u>Revolutionary Milestone by T-Mobile: Ultimate Speed Triumphs as New Record for Sub-6 5G Uploads Established</u></a></li>
<li><a href="https://facebook-video-files.techidaily.com/tailored-guide-to-following-and-watching-facebook-broadcasts/"><u>Tailored Guide to Following and Watching Facebook Broadcasts</u></a></li>
<li><a href="https://win11-tips.techidaily.com/troubleshooting-windows-11-resolving-webcam-error-code-a00f4289/"><u>Troubleshooting Windows 11: Resolving Webcam Error Code A00F4289</u></a></li>
<li><a href="https://hardware-help.techidaily.com/upgrade-now-why-switching-from-your-outdated-android-device-is-essential/"><u>Upgrade Now: Why Switching From Your Outdated Android Device Is Essential</u></a></li>
</ul></div>

