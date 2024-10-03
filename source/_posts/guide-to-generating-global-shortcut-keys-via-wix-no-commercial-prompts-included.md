---
title: "Guide to Generating Global Shortcut Keys via WiX: No Commercial Prompts Included"
date: 2024-09-26T16:12:29.180Z
updated: 2024-10-03T18:51:11.310Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Guide to Generating Global Shortcut Keys via WiX: No Commercial Prompts Included"
thumbnail: https://thmb.techidaily.com/5a94426a32501655e657a3254c012c85eb00e68b90f4fb83cdfc375f3ce534ef.jpg
---

## Guide to Generating Global Shortcut Keys via WiX: No Commercial Prompts Included

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

## How to create non-advertised shortcuts for all users / per machine with WiX Toolset

When you define shortcuts in WiX Toolset, their default installation is **non-advertised (Standard Shortcuts)**. 

Even though this characteristic shouldn’t be a serious issue, it can be a source of ICE errors in some instances (for example, when you define components that have both per-user and per-machine data, with a per-machine keypath).

This article will show you how to fix ICE errors when creating non-advertised shortcuts using the WiX Toolset.

### Advertised vs. Non-advertised shortcuts

### What is an advertised shortcut?

Advertised shortcuts are helpful for developers when making sure a software is installed and running as intended, without any missing pieces. 

When an advertised shortcut is launched, Windows Installer checks to see if all the components included in the same feature as the shortcut are installed on the device. If that’s not the case, the shortcut will automatically launch the MSI from which the program was installed and reinstall the .msi file missing resources.

### What is a non-advertised shortcut (Standard Shortcut)?

We call a non-advertised shortcut (Standard Shortcuts) a standard Windows shortcut. In this case, you can see the target field points to the executable that will be launched if you right-click on it. If this executable is missing for any reason, the application will immediately crash.

### How to create non-advertised shortcuts?

According to [ICE43](https://learn.microsoft.com/en-us/windows/win32/msi/ice43 "ICE43"), Microsoft recommends using separate registry keys in the HKCU (HKEY\_CURRENT\_USER) as keypaths of the non-advertised shortcuts.

To implement this method, you only need to create a new component where you will build the shortcut and the registry value that will serve as the shortcut’s keypath.

This method is actually very simple to implement. All you need to do is create a new component where you will build the shortcut and the registry value that will serve as the shortcut’s keypath.

<Component>
      <Shortcut Id="NonAdShortApp" Directory="DesktopFolder"     Name="NonAdShortApp.exe" WorkingDirectory="INSTALLFOLDER" Target="[#NonAdShortApp.exe]"/> 
      <RegistryValue Root="HKCU" Key="Software\[Manufacturer]\[ProductName]" Type="string" Value="" KeyPath="yes" />
</Component>

Copy

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Keep in mind that his method forces you to add registry entries in your setup package, which may not be as practical in a multi-user scenario. This means that if a user uninstalls the application, all the other users will have orphaned registry entries in their respective HKCU hives.

<!-- affiliate ads begin -->
<a href="https://wigfever.sjv.io/c/5597632/2005184/22899" target="_top" id="2005184">
  <img src="//a.impactradius-go.com/display-ad/22899-2005184" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://wigfever.sjv.io/i/5597632/2005184/22899" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

A major difference between advertised and non-advertised shortcuts is the use of files (that are already installed per machine) as keypaths – which is not possible for non-advertised shortcuts.

To overcome this situation, we will turn an advertised shortcut into a non-advertised one.

Let’s get started!

First, **declare the shortcut** using the following lines:

<Component Id="NonAdShortApp.exe" Guid="4f4d8d47-72a3-4e00-b959-ccae259837df">
	<File Id="NonAdShortApp.exe" Name="NonAdShortApp.exe" Source="$(var.NonAdShortApp_TargetDir)NonAdShortApp.exe" KeyPath="yes">
		<Shortcut Id="NonAdShortApp" Directory="DesktopFolder" Name="NonAdShortApp.exe" WorkingDirectory="INSTALLFOLDER" Advertise="yes"/>
	</File>
</Component>

Copy

We have created a new advertised shortcut in our component which uses a file as a KeyPath. 

Now, we will use the DISABLEADVTSHORTCUTS property to **turn our advertised shortcut** into a **non-advertised** one, bypassing the ICE43 condition.

<Property Id="DISABLEADVTSHORTCUTS" Value="1" />

Copy

That’s it! By adding this line of code into your WiX project, you can turn any advertised shortcut into a non-advertised one without declaring additional registry entries for each shortcut.

<!-- affiliate ads begin -->
<span id="1982457">
					<video width="576" height="240" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1982457.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1982457">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1982457.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1982457%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1982457/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to create a non-advertised shortcut with Advanced Installer

Through Advanced Installer’s GUI, you have a straightforward way to generate non-advertised shortcuts without using any code.

1\. Go to the **Shortcuts Page** and create a new shortcut for an installed file.

![Create New Shortcut](https://cdn.advancedinstaller.com/img/wix-child-images/create-new-shortcut.png "Create New Shortcut")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2123734/7443" target="_top" id="2123734">
  <img src="//a.impactradius-go.com/display-ad/7443-2123734" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2123734/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. In the shortcut’s properties, you can use the "_Advertised Shortcut"_ checkbox to make your shortcut an advertised one. (This option is unchecked by default, leave it as it is to create a **non-advertised shortcut**).

![Create Advertised Shorcut](https://cdn.advancedinstaller.com/img/wix-child-images/create-advertised-shortcut.png "Create Advertised Shorcut")  

3\. To place the shortcut on the Desktop go to the **Paths** section.

4\. Once in the Paths section, change the Shortcut folder option from **SHORTCUTDIR** to **DesktopFolder**.

![Change Shortcut Folder](https://cdn.advancedinstaller.com/img/wix-child-images/change-shortcut-folder.png "Change Shortcut Folder")  

5\. To make sure that your setup package is ICE valid, go to: File - Settings - Package Validation

6\. In the **Build Settings** section, check the "_Enable ICE validation for MSI packages_” checkbox.

![Enable ICE Validation for MSI Packages](https://cdn.advancedinstaller.com/img/wix-child-images/enable-ice-validation-for-msi-packages.png "Enable ICE Validation for MSI Packages")  

Done!

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Check out Advanced Installer’s friendly GUI through our [30-day full featured trial](https://tools.techidaily.com/advancedinstaller/products/)**.** (No credit card required)

<!-- affiliate ads begin -->
<a href="https://smilemakers.pxf.io/c/5597632/2123899/26106" target="_top" id="2123899">
  <img src="//a.impactradius-go.com/display-ad/26106-2123899" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://smilemakers.pxf.io/i/5597632/2123899/26106" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Conclusion

Now we know how to avoid ICE errors by creating non-advertised shortcuts with the WiX Toolset.

Of course, you can always choose a tool that doesn't require any code to create non-advertised shortcuts, such as Advanced Installer.

We hope you found this article useful.

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
<a href="https://aligracehair.sjv.io/c/5597632/2135368/19272" target="_top" id="2135368">
  <img src="//a.impactradius-go.com/display-ad/19272-2135368" border="0" alt="https://techidaily.com" width="250" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135368/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://youtube-lab.techidaily.com/ed-elevate-your-youtube-presence-with-these-8-free-courses-for-2024/"><u>[Updated] Elevate Your YouTube Presence with These 8 Free Courses for 2024</u></a></li>
<li><a href="https://extra-skills.techidaily.com/updated-insta-prowess-guide-the-9-secrets-behind-top-posters-success/"><u>[Updated] Insta Prowess Guide The 9 Secrets Behind Top Posters' Success</u></a></li>
<li><a href="https://techtrends.techidaily.com/anticipating-the-release-of-apples-new-sound-integrated-gadget-cost-projections-scheduled-launch-date-features-overview-and-secret-rumors/"><u>Anticipating the Release of Apple's New Sound-Integrated Gadget: Cost Projections, Scheduled Launch Date, Features Overview & Secret Rumors</u></a></li>
<li><a href="https://some-tips.techidaily.com/creating-and-activating-system-restore-points-on-windows-11-a-comprehensive-guide/"><u>Creating & Activating System Restore Points on Windows 11: A Comprehensive Guide</u></a></li>
<li><a href="https://android-location-track.techidaily.com/in-2024-how-to-track-vivo-y55s-5g-2023-location-by-number-drfone-by-drfone-virtual-android/"><u>In 2024, How to Track Vivo Y55s 5G (2023) Location by Number | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/rapidez-au-detriment-de-la-souplesse-comment-lacceleration-du-processus-douanier-a-la-frontiere-royaume-uniue-affecte-le-commerce/"><u>Rapidez Au Détriment De La Souplesse : Comment L'accélération Du Processus Douanier À La Frontière Royaume-Uni/UE Affecte Le Commerce</u></a></li>
<li><a href="https://youtube-videos.techidaily.com/soundscapes-synergy-ideal-dj-videos-to-download/"><u>Soundscapes Synergy Ideal DJ Videos to Download</u></a></li>
<li><a href="https://some-tips.techidaily.com/strategies-dadoption-des-technologies-dans-lindustrie-de-lassurance-un-plan-detaille/"><u>Stratégies D'Adoption Des Technologies Dans L'Industrie De L'Assurance : Un Plan Détaillé</u></a></li>
<li><a href="https://some-tips.techidaily.com/streamlining-success-your-ultimate-roadmap-for-synchronizing-human-resources-procedures-and-information-in-automation/"><u>Streamlining Success: Your Ultimate Roadmap for Synchronizing Human Resources, Procedures & Information in Automation</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/the-photo-keepers-companion-unlimited-free-options-and-elite-subscription-saviors/"><u>The Photo Keeper’s Companion Unlimited Free Options & Elite Subscription Saviors</u></a></li>
<li><a href="https://win11.techidaily.com/tricks-for-stealthy-login-silencing-security-prompts-in-windows-11/"><u>Tricks for Stealthy Login: Silencing Security Prompts in Windows 11</u></a></li>
<li><a href="https://some-tips.techidaily.com/valider-les-pieces-didentite-a-distance-grace-a-la-technologie-de-reconnaissance-optique-de-caracteres-ocr-de-abbyy-avec-le-systeme-trustid-en-nuage/"><u>Valider Les Pièces D'identité À Distance Grâce À La Technologie De Reconnaissance Optique De Caractères (OCR) De ABBYY Avec Le Système TrustID en Nuage</u></a></li>
</ul></div>

