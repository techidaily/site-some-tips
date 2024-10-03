---
title: Effective Strategies for Deleting Files & Directories During WiX Software Uninstallation
date: 2024-10-01T16:31:41.420Z
updated: 2024-10-03T16:43:34.446Z
tags:
  - versus
categories:
  - advancedinstaller
description: This Article Describes Effective Strategies for Deleting Files & Directories During WiX Software Uninstallation
thumbnail: https://thmb.techidaily.com/c614df743851cde902b9dc7b624e356646f565efb6b83602d7f5ffd347873428.jpg
---

## Effective Strategies for Deleting Files & Directories During WiX Software Uninstallation

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

## How To Remove Files and Folders when Uninstalling with WiX

Written by [Alex Marin](https://tools.techidaily.com/advancedinstaller/products/) · May 27th, 2022

In some instances, when uninstalling an MSI, you may notice that some files and folders stay in the system and are not removed.

This can be seen in the example we portrayed in our article[How To Embed CAB Files in MSI](https://tools.techidaily.com/advancedinstaller/products/). There, we saw how to embed CAB files in an MSI with WiX Toolset and we created a simple MSI by using a basic WXS file.

If you tried that example and installed the MSI and then uninstalled it - you saw that the files still remained on the system. 

In this article, we're going to show you how to sort that out. Coming up, we will have a look at some options that you have with WiX to remove files and folders during uninstallation, and also how you can do the same with Advanced Installer.

### How to Remove Files with WiX?

WiX offers the possibility to remove files with the [RemoveFile](https://wixtoolset.org/docs/v3/xsd/wix/removefile/ "RemoveFile") element inside a component declaration.

For example, if we have a look at our original WXS, it should look something like this:

<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
<Product Id="*" UpgradeCode="12345678-1111-2222-3333-666666666666"
Name="My First Installer" Version="1.0.0.0" Manufacturer="Caphyon" Language="1033">
<Package InstallerVersion="200" Compressed="yes" Comments="Hello, this is my test installer"/>
<MediaTemplate EmbedCab="yes" />
<Directory Id="TARGETDIR" Name="SourceDir">
<Directory Id="ProgramFilesFolder">
<Directory Id="INSTALLDIR" Name="MyFirstInstaller">
<Component Id="Files" Guid="11111111-2222-3333-4444-555555555555">
<File Id="File1" Source="Trace32.exe"/>
</Component>
</Directory>
</Directory>
</Directory>
<Feature Id="Feature1" Level="1" Title="First feature" Description="This is the one and only feature in this installation">
<ComponentRef Id="Files"/>
</Feature>
</Product>
</Wix>

Copy

As mentioned, the **RemoveFile** element must be added under a component parent, like this:

<Directory Id="TARGETDIR" Name="SourceDir">
<Directory Id="ProgramFilesFolder">
<Directory Id="INSTALLDIR" Name="MyFirstInstaller">
<Component Id="Files" Guid="11111111-2222-3333-4444-555555555555">
<File Id="File1" Source="Trace32.exe"/>
<RemoveFile Id="PurgeAppFolder" Name="*.*" On="uninstall" />
</Component>
</Directory>
</Directory>
</Directory>

Copy

This is configured so that all the files (“\*.\*”) inside our INSTALLDIR are deleted during uninstallation. You can specify only one file (“myfile.extension”) or a certain type of files by extension, using the wildcard character (“\*.txt”).

The final WXS code will be:

<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
<Product Id="*" UpgradeCode="12345678-1111-2222-3333-666666666666"
Name="My First Installer" Version="1.0.0.0" Manufacturer="Caphyon" Language="1033">
<Package InstallerVersion="200" Compressed="yes" Comments="Hello, this is my test installer"/>
<MediaTemplate EmbedCab="yes" />
<Directory Id="TARGETDIR" Name="SourceDir">
<Directory Id="ProgramFilesFolder">
<Directory Id="INSTALLDIR" Name="MyFirstInstaller">
<Component Id="Files" Guid="11111111-2222-3333-4444-555555555555">
<File Id="File1" Source="Trace32.exe"/>
<RemoveFile Id="PurgeAppFolder" Name="*.*" On="uninstall" />
</Component>
</Directory>
</Directory>
</Directory>
<Feature Id="Feature1" Level="1" Title="First feature" Description="This is the one and only feature in this installation">
<ComponentRef Id="Files"/>
</Feature>
</Product>
</Wix>

Copy

Once we have the WXS created, let’s create the batch file to build the MSI:

"C:\Program Files (x86)\WiX Toolset v3.11\bin\candle.exe" test.wxs
"C:\Program Files (x86)\WiX Toolset v3.11\bin\light.exe" test.wixobj
@pause

Copy

Once you double-click the batch file, the MSI should be created.

![Remove MSI file with WiX](https://cdn.advancedinstaller.com/img/wix-child-images/wixremovefilemsi.png "Remove MSI file with WiX")  

<!-- affiliate ads begin -->
<a href="https://versadesk.pxf.io/c/5597632/1828647/21290" target="_top" id="1828647">
  <img src="//a.impactradius-go.com/display-ad/21290-1828647" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://versadesk.pxf.io/i/5597632/1828647/21290" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

If we install and uninstall the MSI, all the files should be removed during uninstallation and no files will remain in the system.

### How to Remove Folders with WiX

To remove folders during the installation or uninstallation of an MSI, you have the option of using the [RemoveFolder](https://wixtoolset.org/docs/v3/xsd/wix/removefolder/ "RemoveFolder") element. It works and behaves the same way as the RemoveFile element that we previously presented. 

The steps are the same as when adding it to your WXS file.

But, the RemoveFolders element only works for directories created with the MSI database and with empty folders. This means that you must use the RemoveFile element to empty the folders first, and then the RemoveFolder element to delete the actual folder.

You may wonder - what about the folders that are created by the application after it is executed?

WiX has the option to add a [RemoveFolderEX](https://wixtoolset.org/docs/v3/xsd/util/removefolderex/ "RemoveFolderEX") util extension element in your WXS. But adding this element is kind of tricky. 

The RemoveFolderEX is a Custom Action that adds temporary rows to the RemoveFile table for each subfolder of the root specified in the WXS. 

It has the characteristic that temporary rows must be written before the CostInitialize standard action, and MSI databases do not create properties for the directory hierarchy in your package until later, in the CostFinalize action. So, we need to get creative on how to add the RemoveFolderEx element in the WXS.

The easiest way to achieve this is to remember the directory we want to delete in the registry. Then, during the uninstallation - read the path from the registry and pass it to the RemoveFolderEx element. You can find a full step-by-step guide here: [The WiX toolset's Remember Property pattern](https://robmensching.com/blog/posts/2010/5/2/the-wix-toolsets-remember-property-pattern/ "The WiX toolset's Remember Property pattern").

### How to remove directories using VBScript Custom Action?

An alternative would be to create a Custom Action with a simple VBScript code to delete the unwanted remaining directories. This way, you don’t have to worry about empty directories.

1\. Let’s create a simple VBScript that will delete the folder, in our case _“C:\\Program Files (x86)\\MyFirstInstaller”_ (you can [pass properties](https://wixtoolset.org/docs/v3/xsd/wix/customaction/ "pass properties") to VBScript if you don’t want to hardcode your custom actions).

Dim FSO, Folder
set FSO=CreateObject("Scripting.FileSystemObject")
Folder="C:\Program Files (x86)\MyFirstInstaller"
FSO.DeleteFolder(Folder)

Copy

In our case, the VBScript is called_Sample.vbs_ and it’s placed near the WXS and batch file we previously created. 

2\. Adjust the WXS file to include the custom action. The code to add our Custom Action is:

<Binary Id='Sample.vbs' SourceFile='Sample.vbs' />
<CustomAction Id='Sample.vbs' VBScriptCall='' BinaryKey='Sample.vbs' Execute='deferred' Return='ignore'/>
<InstallExecuteSequence>
	<Custom Action='Sample.vbs' Before='InstallFinalize'>REMOVE~="ALL"</Custom>
	<ScheduleReboot Suppress="yes"/>
</InstallExecuteSequence>

Copy

Before moving forward, let’s see what the above configuration does:

2.1 We declare our binary for the custom action as_Sample.vbs_

2.2 We create a Custom Action called_Sample.vbs_

2.3 We declare the execution to be deferred and ignore the return code

2.4 We place it before the _**InstallFinalize**_sequence (because we are running a deferred custom action)

2.5 We tell the MSI to run the custom action only during the remove operation by adding the following [property](https://www.firegiant.com/docs/wix/v3/tutorial/events-and-actions/extra-actions/ "property"):

REMOVE~=”ALL”

Copy

2.6 We suppress the [Reboot](https://wixtoolset.org/docs/v3/xsd/wix/schedulereboot/ "Reboot")

3\. Now, it’s time to build the MSI by running the make\_msi.bat file that we previously created and test the scenario. 

4\. We can see that the folder is now deleted after the uninstallation of the package.

![Remove folder with WiX](https://cdn.advancedinstaller.com/img/wix-child-images/wixremovefolder.png "Remove folder with WiX")  

As previously mentioned, you need to be aware of what you are trying to achieve in terms of files and folders removal in your MSI. For demo purposes, we used a hardcoded VBScript, which is not a best practice.

An ideal script would have the ability to get the MSI directory variables to be able to correctly remove the directories during uninstallation – if the user selects to install the application in a different directory.

Another important aspect is when and how you declare your custom action to run. In our example, we are deleting folders in “Program Files”, meaning that we need to declare the custom as [action to run as deferred](https://tools.techidaily.com/advancedinstaller/products/).

### How to Remove files and folders with Advanced Installer?

Advanced Installer makes it easy to delete all the files you are adding to your project automatically during uninstallation. You don’t need to worry about declaring anything inside the project.

However, if the application is creating additional files that you want to remove during the uninstallation, use the [File Removal Operations](https://tools.techidaily.com/advancedinstaller/products/) that is included in Advanced Installer’s GUI.

If you are curious about how removing files and folders works in Advanced Installer, try it through our [30-day full featured trial](https://tools.techidaily.com/advancedinstaller/products/).

To achieve this, follow these steps:

1\. Navigate to the folder that contains the file you want to remove, right-click on it and select **New File Operation** \-**File Removal**.

![Advanced Installer File Removal](https://cdn.advancedinstaller.com/img/wix-child-images/aifileremoval.png "Advanced Installer File Removal")  

2\. A new dialog will appear where you can specify a file name, select a certain file type that you want to be deleted, and also choose if the operation happens during the installation or uninstallation of the MSI. 

You also have two more options: to **Remove Empty Folders** or **Remove Non Empty Folders**.

3\. Make sure to save your changes by clicking “OK”.

![Advanced Installer File Removal Dialog](https://cdn.advancedinstaller.com/img/wix-child-images/aifileremovaldialog.png "Advanced Installer File Removal Dialog")  

4\. If you want to delete an entire folder or clean up additional folders left by your application, you can right-click on the folder and choose **Properties.**

5\. A new dialog will appear which will have the**Operations** tab. Click on it.

![Advanced Installer Folder Operations](https://cdn.advancedinstaller.com/img/wix-child-images/aifolderoperations.png "Advanced Installer Folder Operations")  

<!-- affiliate ads begin -->
<a href="https://united.elfm.net/c/5597632/2139563/4704" target="_top" id="2139563">
  <img src="//a.impactradius-go.com/display-ad/4704-2139563" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://united.elfm.net/i/5597632/2139563/4704" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

You can choose to delete the folder whether it’s empty or not and select when the removing action should occur, as well as additional conditions and the overwrite behaviour.

As you can see, Advanced Installer's GUI makes removal operations for files and folders a more seamless process.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1975836/19272" target="_top" id="1975836">
  <img src="//a.impactradius-go.com/display-ad/19272-1975836" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1975836/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Conclusion

And there you have it! Now you know how to remove files and folders when uninstalling with WiX, and have a few options to do so. 

For direct access to the latest news, videos, and fresh HowTos and guides, join our mailing list to stay informed about the packaging industry: [https://www.advancedinstaller.com/newsletter-subscribe.html](https://tools.techidaily.com/advancedinstaller/products/)  

Let us know if there are any topics you'd like us to cover.

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
<a href="https://bluettius.sjv.io/c/5597632/2139122/17108" target="_top" id="2139122">
  <img src="//a.impactradius-go.com/display-ad/17108-2139122" border="0" alt="https://techidaily.com" width="468" height="60"/>
</a>
<img height="0" width="0" src="https://bluettius.sjv.io/i/5597632/2139122/17108" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://extra-hints.techidaily.com/new-accelerate-or-slow-down-on-the-screen-netflix/"><u>[New] Accelerate or Slow Down on the Screen (Netflix)</u></a></li>
<li><a href="https://instagram-video-recordings.techidaily.com/new-instamixer-uniting-android-and-ios-photo-sessions/"><u>[New] InstaMixer Uniting Android & iOS Photo Sessions</u></a></li>
<li><a href="https://some-guidance.techidaily.com/new-unrivaled-sonic-union-for-speakers/"><u>[New] Unrivaled Sonic Union for Speakers</u></a></li>
<li><a href="https://fox-blue.techidaily.com/updated-action-cam-showdown-2022-hero5-black-vs-ultra-30-streaming-for-2024/"><u>[Updated] Action Cam Showdown 2022 Hero5 Black Vs. Ultra 30 Streaming for 2024</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/updated-screen-recording-simplified-review-insights-for-2024/"><u>[Updated] Screen Recording Simplified Review Insights for 2024</u></a></li>
<li><a href="https://screen-recording.techidaily.com/2024-approved-seamless-communication-the-best-5-webcams-with-inbuilt-microphones/"><u>2024 Approved Seamless Communication The Best 5 Webcams with Inbuilt Microphones</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/best-3-nokia-c12-plus-emulator-for-mac-to-run-your-wanted-android-apps-drfone-by-drfone-android/"><u>Best 3 Nokia C12 Plus Emulator for Mac to Run Your Wanted Android Apps | Dr.fone</u></a></li>
<li><a href="https://buynow-info.techidaily.com/best-in-class-the-top-wireless-travel-routers-for-nomads/"><u>Best in Class: The Top Wireless Travel Routers for Nomads</u></a></li>
<li><a href="https://some-tips.techidaily.com/essential-8-tips-for-dust-free-spotless-macbook-care-that-guarantees-no-damage-to-your-device/"><u>Essential 8 Tips for Dust-Free, Spotless MacBook Care That Guarantees No Damage to Your Device</u></a></li>
<li><a href="https://some-tips.techidaily.com/exciting-new-enhancements-coming-soon-microsoft-improves-snipping-tool-and-paint-on-windows-11/"><u>Exciting New Enhancements Coming Soon: Microsoft Improves Snipping Tool & Paint on Windows 11</u></a></li>
<li><a href="https://some-tips.techidaily.com/guide-to-turning-off-windows-11s-built-in-security-microsoft-defender-explained/"><u>Guide to Turning Off Windows 11'S Built-In Security: Microsoft Defender Explained</u></a></li>
<li><a href="https://easy-unlock-android.techidaily.com/in-2024-mastering-android-device-manager-the-ultimate-guide-to-unlocking-your-oppo-a58-4g-device-by-drfone-android/"><u>In 2024, Mastering Android Device Manager The Ultimate Guide to Unlocking Your Oppo A58 4G Device</u></a></li>
<li><a href="https://some-tips.techidaily.com/is-the-new-run0-feature-phasing-out-sudo-in-the-linux-world/"><u>Is the New Run0 Feature Phasing Out Sudo in the Linux World?</u></a></li>
<li><a href="https://some-tips.techidaily.com/latest-news-roundup-changes-to-netflix-subscription-options-and-improved-solutions-for-iphone-repairs/"><u>Latest News Roundup: Changes to Netflix Subscription Options & Improved Solutions for iPhone Repairs</u></a></li>
</ul></div>

