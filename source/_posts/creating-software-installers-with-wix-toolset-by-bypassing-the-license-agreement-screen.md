---
title: Creating Software Installers with WiX Toolset by Bypassing the License Agreement Screen
date: 2024-09-27T07:16:40.820Z
updated: 2024-09-28T01:11:26.259Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Creating Software Installers with WiX Toolset by Bypassing the License Agreement Screen
thumbnail: https://thmb.techidaily.com/cb7e01d77e11396989975642eff6b3a0f5621896796311364cd34b031c122e69.jpg
---

## Creating Software Installers with WiX Toolset by Bypassing the License Agreement Screen

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

## How to build an installer without a license page using WiX Toolset

Although it is not required, almost every WiX UI configuration has a License Agreement Dialog. In this article, we will go through how to use WiX Toolset to build an installer without a license page.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2118315/7443" target="_top" id="2118315">
  <img src="//a.impactradius-go.com/display-ad/7443-2118315" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2118315/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to Build an Installer Without a License Page in WiX Toolset

The WiX UI Minimal dialog set will serve as a starting point for our project.

To get started, let's add the WiX UI minimal dialog set.

1\. Add a new reference for the **WixUIExtension.dll** file, that you can find in the bin directory of the WiX Toolset installation folder.

![Add a new reference for the WixUIExtension.dll file](https://cdn.advancedinstaller.com/img/build-installer-without-license-page-using-wix/add-new-reference-for-wix-ui-extension-dll-file.png "Add a new reference for the WixUIExtension.dll file")  

<!-- affiliate ads begin -->
<a href="https://25home.pxf.io/c/5597632/2148645/16836" target="_top" id="2148645">
  <img src="//a.impactradius-go.com/display-ad/16836-2148645" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://25home.pxf.io/i/5597632/2148645/16836" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. Now that the WiX UI Extension is referenced, add this code to your project under the Product Tag:

<UI Id="WixUI_Minimal">
      <TextStyle Id="WixUI_Font_Normal" FaceName="Tahoma" Size="8" />
      <TextStyle Id="WixUI_Font_Bigger" FaceName="Tahoma" Size="12" />
      <TextStyle Id="WixUI_Font_Title" FaceName="Tahoma" Size="9" Bold="yes" />
      <Property Id="DefaultUIFont" Value="WixUI_Font_Normal" />
      <Property Id="WixUI_Mode" Value="Minimal" />
      <DialogRef Id="ErrorDlg" />
      <DialogRef Id="FatalError" />
      <DialogRef Id="FilesInUse" />
      <DialogRef Id="MsiRMFilesInUse" />
      <DialogRef Id="PrepareDlg" />
      <DialogRef Id="ProgressDlg" />
      <DialogRef Id="ResumeDlg" />
      <DialogRef Id="UserExit" />
      <DialogRef Id="WelcomeDlg" />
      <Publish Dialog="WelcomeDlg" Control="Next" Event="NewDialog" Value="PrepareDlg">1</Publish>
     <Publish Dialog="ExitDialog" Control="Finish" Event="EndDialog" Value="Return" Order="999">1</Publish>
     <Publish Dialog="VerifyReadyDlg" Control="Back" Event="NewDialog" Value="MaintenanceTypeDlg">1</Publish>
     <Publish Dialog="MaintenanceWelcomeDlg" Control="Next" Event="NewDialog" Value="MaintenanceTypeDlg">1</Publish>
     <Publish Dialog="MaintenanceTypeDlg" Control="RepairButton" Event="NewDialog" Value="VerifyReadyDlg">1</Publish>
     <Publish Dialog="MaintenanceTypeDlg" Control="RemoveButton" Event="NewDialog" Value="VerifyReadyDlg">1</Publish>
     <Publish Dialog="MaintenanceTypeDlg" Control="Back" Event="NewDialog" Value="MaintenanceWelcomeDlg">1</Publish>
     <Property Id="ARPNOMODIFY" Value="1" />
</UI>
<UIRef Id="WixUI_Common" />

Copy

As you can see, this code implements the [WixUI\_Minimal](https://github.com/wixtoolset/wix3/blob/develop/src/ext/UIExtension/wixlib/WixUI%5FMinimal.wxs "WixUI_Minimal") dialog set – we slightly modified it to remove the license agreement dialog. The major difference is that it uses **WelcomeDlg** instead of **WelcomeEulaDlg**. 

From this point on, all we have to do is wire up the dialogs. 

Coming up, let's see how you can use Advanced Installer to build your installer without a license page – you won't need any code!

Are you new to Advanced Installer? Get familiar with it through our [30-day full-feature trial](https://tools.techidaily.com/advancedinstaller/products/).

### How to Use Advanced Installer to Build Your Installer without a license page

Yes, there's an even simpler way to build your installer without a license page. Here's how you can achieve that with the Advanced Installer GUI:

Advanced Installer doesn’t use the **WelcomeEulaDlg** by default**,** giving you the freedom to choose if your installer will include a License Agreement Dialog – you just need to add a **LicenseAgreementDlg**.

How can you add a **License Agreement Dialog** in Advanced Installer?

1\. Go to the Dialogs page and press the **Add Dialog** button. A window will pop up containing a list of predefined dialogs that you can use without any extra fine-tuning.

![Add Dialog](https://cdn.advancedinstaller.com/img/build-installer-without-license-page-using-wix/add-dialog.png "Add Dialog")  

2\. From that list choose the **LicenseAgreementDlg**.

![Choose Predefined Dialog LicenseAgreementDlg](https://cdn.advancedinstaller.com/img/build-installer-without-license-page-using-wix/choose-predefined-dialog.png "Choose Predefined Dialog LicenseAgreementDlg")  

<!-- affiliate ads begin -->
<a href="https://ursime.pxf.io/c/5597632/2136548/16384" target="_top" id="2136548">
  <img src="//a.impactradius-go.com/display-ad/16384-2136548" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ursime.pxf.io/i/5597632/2136548/16384" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

3\. A new window will pop up where you will need to specify the path of the license file, which has to be an RTF file.

![Specify Path of License File](https://cdn.advancedinstaller.com/img/build-installer-without-license-page-using-wix/specify-path-of-license-file.png "Specify Path of License File")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2002019/7443" target="_top" id="2002019">
  <img src="//a.impactradius-go.com/display-ad/7443-2002019" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2002019/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Conclusion

Now you know how to build an installer without a license page both with WiX Toolset and with Advanced Installer. It’s up to you which one you want to use.

While WiX enables you to code a friendly UI that is OK to begin with, Advanced Installer has its own dedicated GUI that you can use to quickly bring in any type of dialog.

What are your thoughts about WiX? Do you have any questions? Share them in the comments! 

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
<li><a href="https://fox-links.techidaily.com/new-2024-approved-how-to-record-with-flair-on-windows-10/"><u>[New] 2024 Approved How to Record with Flair on Windows 10</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-pro-mkv-reader-for-personal-computers/"><u>[New] Pro MKV Reader for Personal Computers</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-top-techniques-succeeding-in-spotify-advertising/"><u>[Updated] Top Techniques Succeeding in Spotify Advertising</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-essential-guide-for-avi-to-gif-editing-a-quick-filmora-workflow-on-windows-and-macos/"><u>2024 Approved The Essential Guide for AVI-to-GIF Editing A Quick Filmora Workflow on Windows & macOS</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-experts-handbook-for-srt-file-conversions/"><u>2024 Approved The Expert's Handbook for SRT File Conversions</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-tips-to-trim-down-lag-during-xbox-zoom-sessions/"><u>2024 Approved Tips to Trim Down Lag During Xbox-Zoom Sessions</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/complete-manual-integrating-srt-into-mp4-files-for-2024/"><u>Complete Manual Integrating SRT Into MP4 Files for 2024</u></a></li>
<li><a href="https://instagram-clips.techidaily.com/crafting-captivating-ig-stories-with-youtube-content-for-2024/"><u>Crafting Captivating IG Stories With YouTube Content for 2024</u></a></li>
<li><a href="https://instagram-clips.techidaily.com/in-2024-digital-footprints-on-instagram-effective-photo-watermarking/"><u>In 2024, Digital Footprints on Instagram Effective Photo Watermarking</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/in-2024-how-to-screen-mirroring-vivo-v29e-drfone-by-drfone-android/"><u>In 2024, How to Screen Mirroring Vivo V29e? | Dr.fone</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/in-2024-navigating-away-from-igs-suggestion-engine/"><u>In 2024, Navigating Away From IG's Suggestion Engine</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-essential-guide-to-apple-podcasts-transferring/"><u>In 2024, The Essential Guide to Apple Podcasts Transferring</u></a></li>
<li><a href="https://win11.techidaily.com/microsofts-pioneering-artificial-intelligence-hub/"><u>Microsoft’s Pioneering Artificial Intelligence Hub</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/settling-into-a-virtual-firepit-a-comprehensive-evaluation-of-the-minecraft-campfire-tales-edition/"><u>Settling Into a Virtual Firepit: A Comprehensive Evaluation of the Minecraft Campfire Tales Edition</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-complete-itunes-radio-downloading-blueprint-for-2024/"><u>The Complete iTunes Radio Downloading Blueprint for 2024</u></a></li>
</ul></div>

