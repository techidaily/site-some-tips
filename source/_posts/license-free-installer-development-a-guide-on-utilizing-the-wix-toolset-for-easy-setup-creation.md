---
title: "License-Free Installer Development: A Guide on Utilizing the WiX Toolset for Easy Setup Creation"
date: 2024-09-28T20:19:28.128Z
updated: 2024-10-03T18:38:14.348Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes License-Free Installer Development: A Guide on Utilizing the WiX Toolset for Easy Setup Creation"
thumbnail: https://thmb.techidaily.com/fbcf05b0c32ba329cf6957ae3248e625c39ba58c1a53bbe9519d95b22a1c1295.jpg
---

## License-Free Installer Development: A Guide on Utilizing the WiX Toolset for Easy Setup Creation

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

### How to Build an Installer Without a License Page in WiX Toolset

The WiX UI Minimal dialog set will serve as a starting point for our project.

To get started, let's add the WiX UI minimal dialog set.

1\. Add a new reference for the **WixUIExtension.dll** file, that you can find in the bin directory of the WiX Toolset installation folder.

![Add a new reference for the WixUIExtension.dll file](https://cdn.advancedinstaller.com/img/build-installer-without-license-page-using-wix/add-new-reference-for-wix-ui-extension-dll-file.png "Add a new reference for the WixUIExtension.dll file")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135368/19272" target="_top" id="2135368">
  <img src="//a.impactradius-go.com/display-ad/19272-2135368" border="0" alt="https://techidaily.com" width="250" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135368/19272" style="position:absolute;visibility:hidden;" border="0" />
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

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1997675/19272" target="_top" id="1997675">
  <img src="//a.impactradius-go.com/display-ad/19272-1997675" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1997675/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to Use Advanced Installer to Build Your Installer without a license page

Yes, there's an even simpler way to build your installer without a license page. Here's how you can achieve that with the Advanced Installer GUI:

Advanced Installer doesn’t use the **WelcomeEulaDlg** by default**,** giving you the freedom to choose if your installer will include a License Agreement Dialog – you just need to add a **LicenseAgreementDlg**.

How can you add a **License Agreement Dialog** in Advanced Installer?

1\. Go to the Dialogs page and press the **Add Dialog** button. A window will pop up containing a list of predefined dialogs that you can use without any extra fine-tuning.

![Add Dialog](https://cdn.advancedinstaller.com/img/build-installer-without-license-page-using-wix/add-dialog.png "Add Dialog")  

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2136622/26400" target="_top" id="2136622">
  <img src="//a.impactradius-go.com/display-ad/26400-2136622" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2136622/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. From that list choose the **LicenseAgreementDlg**.

![Choose Predefined Dialog LicenseAgreementDlg](https://cdn.advancedinstaller.com/img/build-installer-without-license-page-using-wix/choose-predefined-dialog.png "Choose Predefined Dialog LicenseAgreementDlg")  

3\. A new window will pop up where you will need to specify the path of the license file, which has to be an RTF file.

![Specify Path of License File](https://cdn.advancedinstaller.com/img/build-installer-without-license-page-using-wix/specify-path-of-license-file.png "Specify Path of License File")  

<!-- affiliate ads begin -->
<a href="https://unicoeye.pxf.io/c/5597632/2148775/18498" target="_top" id="2148775">
  <img src="//a.impactradius-go.com/display-ad/18498-2148775" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://unicoeye.pxf.io/i/5597632/2148775/18498" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://screen-activity-recording.techidaily.com/new-2024-approved-how-to-record-mov-files-on-windows-10/"><u>[New] 2024 Approved How to Record MOV Files on Windows 10</u></a></li>
<li><a href="https://youtube-tips.techidaily.com/n-2024-youtube-shorts-earnings-guide-must-knows-and-future-potential/"><u>[New] In 2024, Youtube Shorts Earnings Guide Must-Knows & Future Potential</u></a></li>
<li><a href="https://fox-access.techidaily.com/updated-behind-the-scenes-with-intova-edge-x-for-2024/"><u>[Updated] Behind the Scenes with Intova Edge X for 2024</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/updated-mindful-meandering-leisurely-pc-games/"><u>[Updated] Mindful Meandering Leisurely PC Games</u></a></li>
<li><a href="https://some-tips.techidaily.com/1-abbyy-top-choice-for-everest-groups-idp-peak-matrix-evaluation/"><u>1. ABBYY: Top Choice for Everest Group's IDP Peak Matrix Evaluation</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/2024-approved-2023s-premier-action-cameras-for-ocean-thrills/"><u>2024 Approved 2023'S Premier Action Cameras for Ocean Thrills</u></a></li>
<li><a href="https://fox-info.techidaily.com/2024-approved-peak-of-puns-premium-meme-templates/"><u>2024 Approved Peak of Puns Premium Meme Templates</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbey-jahresumsatz-steigt-um-19-in-deutschland-fur-das-jahr-2018-seo-freundliche-ubersicht/"><u>ABBEY Jahresumsatz Steigt Um 19 % in Deutschland Für Das Jahr 2018 - SEO-Freundliche Übersicht</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyy-announces-scott-opitz-as-new-cmo-exciting-times-ahead/"><u>ABBYY Announces Scott Opitz as New CMO: Exciting Times Ahead</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyy-finereader-et-ideticiel-accelere-le-tri-du-courrier-dans-les-communes-avec-larchivage-numerique/"><u>ABBYY FineReader Et IDéticiel Accélère Le Tri Du Courrier Dans Les Communes Avec L'Archivage Numérique</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyy-finereader-fur-blinde-und-sehschwache-schulerinnen-uberwindet-lernbarrieren-mit-spracherkennungstechnologie/"><u>ABBYY FineReader Für Blinde Und Sehschwache SchülerInnen - Überwindet Lernbarrieren Mit Spracherkennungstechnologie</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyy-unveils-cutting-edge-digital-tools-to-streamline-legal-practices-during-the-2020-american-bar-association-technology-exhibition/"><u>ABBYY Unveils Cutting-Edge Digital Tools to Streamline Legal Practices During the 2020 American Bar Association Technology Exhibition</u></a></li>
<li><a href="https://some-tips.techidaily.com/1724313333809-cookiebot-enabled-enhance-your-websites-analytics-and-personalization/"><u>Cookiebot-Enabled: Enhance Your Website's Analytics & Personalization</u></a></li>
<li><a href="https://activate-lock.techidaily.com/in-2024-how-to-remove-activation-lock-from-the-apple-iphone-13-pro-without-previous-owner-by-drfone-ios/"><u>In 2024, How to Remove Activation Lock From the Apple iPhone 13 Pro Without Previous Owner?</u></a></li>
<li><a href="https://easy-unlock-android.techidaily.com/in-2024-top-10-fingerprint-lock-apps-to-lock-your-oneplus-nord-ce-3-lite-5g-phone-by-drfone-android/"><u>In 2024, Top 10 Fingerprint Lock Apps to Lock Your OnePlus Nord CE 3 Lite 5G Phone</u></a></li>
<li><a href="https://screen-capture.techidaily.com/pinnacle-programs-for-peak-webcam-video-quality/"><u>Pinnacle Programs for Peak Webcam Video Quality</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyy-timeline-connector-for-alteryx-abbyy/"><u>ビジネス分析を強化するABBYY Timeline Connector for Alteryx® - ABBYYブログでの完全ガイド</u></a></li>
</ul></div>

