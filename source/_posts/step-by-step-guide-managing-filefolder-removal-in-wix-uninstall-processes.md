---
title: "Step-by-Step Guide: Managing File/Folder Removal in WiX Uninstall Processes"
date: 2024-09-22T18:40:56.810Z
updated: 2024-09-28T10:13:43.989Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Step-by-Step Guide: Managing File/Folder Removal in WiX Uninstall Processes"
thumbnail: https://thmb.techidaily.com/ef2d39454969b75baf5c215d0724710d89c3d8cc82ce806ec7a058e29ddc30fe.jpg
---

## Step-by-Step Guide: Managing File/Folder Removal in WiX Uninstall Processes

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
<a href="https://ephamedtechinc.pxf.io/c/5597632/2137204/26400" target="_top" id="2137204">
  <img src="//a.impactradius-go.com/display-ad/26400-2137204" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2137204/26400" style="position:absolute;visibility:hidden;" border="0" />
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

<!-- affiliate ads begin -->
<a href="https://aidotcom.pxf.io/c/5597632/2134502/19576" target="_top" id="2134502">
  <img src="//a.impactradius-go.com/display-ad/19576-2134502" border="0" alt="https://techidaily.com" width="672" height="90"/>
</a>
<img height="0" width="0" src="https://aidotcom.pxf.io/i/5597632/2134502/19576" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

2\. A new dialog will appear where you can specify a file name, select a certain file type that you want to be deleted, and also choose if the operation happens during the installation or uninstallation of the MSI. 

You also have two more options: to **Remove Empty Folders** or **Remove Non Empty Folders**.

3\. Make sure to save your changes by clicking “OK”.

![Advanced Installer File Removal Dialog](https://cdn.advancedinstaller.com/img/wix-child-images/aifileremovaldialog.png "Advanced Installer File Removal Dialog")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1896505/19272" target="_top" id="1896505">
  <img src="//a.impactradius-go.com/display-ad/19272-1896505" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1896505/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

4\. If you want to delete an entire folder or clean up additional folders left by your application, you can right-click on the folder and choose **Properties.**

5\. A new dialog will appear which will have the**Operations** tab. Click on it.

![Advanced Installer Folder Operations](https://cdn.advancedinstaller.com/img/wix-child-images/aifolderoperations.png "Advanced Installer Folder Operations")  

<!-- affiliate ads begin -->
<a href="https://bluettius.sjv.io/c/5597632/2139115/17108" target="_top" id="2139115">
  <img src="//a.impactradius-go.com/display-ad/17108-2139115" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://bluettius.sjv.io/i/5597632/2139115/17108" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

You can choose to delete the folder whether it’s empty or not and select when the removing action should occur, as well as additional conditions and the overwrite behaviour.

As you can see, Advanced Installer's GUI makes removal operations for files and folders a more seamless process.

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
<li><a href="https://screen-activity-recording.techidaily.com/new-2024-approved-savespace-pros-review-summary/"><u>[New] 2024 Approved SaveSpace Pros Review Summary</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-timing-translation-from-20mb-to-seconds-measurement/"><u>[New] Timing Translation From 20Mb to Seconds Measurement</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-ultimate-pc-edition-of-image-overlay-mastery/"><u>[Updated] Ultimate PC Edition of Image Overlay Mastery</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unlock-your-full-viewing-experience-with-these-3-strategies-to-download-youtube-srt/"><u>[Updated] Unlock Your Full Viewing Experience with These 3 Strategies to Download YouTube SRT</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-transform-your-snaps-with-smart-zoom-usage-in-snapchat/"><u>2024 Approved Transform Your Snaps with Smart Zoom Usage in Snapchat</u></a></li>
<li><a href="https://android-location.techidaily.com/3-effective-methods-to-fake-gps-location-on-android-for-your-oppo-a1x-5g-drfone-by-drfone-virtual/"><u>3 Effective Methods to Fake GPS location on Android For your Oppo A1x 5G | Dr.fone</u></a></li>
<li><a href="https://desktop-recording.techidaily.com/detailed-walkthrough-ipad-screen-recording/"><u>Detailed Walkthrough IPad Screen Recording</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/game-enthusiasts-rejoice-eblazter-presents-customizable-gaming-computers-in-one-compact-design/"><u>Game Enthusiasts Rejoice: EBlazter Presents Customizable Gaming Computers in One Compact Design</u></a></li>
<li><a href="https://techidaily.com/how-to-recover-lost-data-on-apple-iphone-13-pro-drfone-by-drfone-ios-data-recovery-ios-data-recovery/"><u>How To Recover Lost Data on Apple iPhone 13 Pro? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-15-smartest-ways-to-watch-nba-live-in-action/"><u>In 2024, The 15 Smartest Ways to Watch NBA Live in Action</u></a></li>
<li><a href="https://discover-cloud.techidaily.com/itunes-locked-down-heres-how-to-gain-full-access-in-macos/"><u>ITunes-Locked Down? Here's How to Gain Full Access in macOS!</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/pioneering-computer-solutions-by-toms-systems/"><u>Pioneering Computer Solutions by Tom's Systems</u></a></li>
<li><a href="https://tech-revival.techidaily.com/revolutionize-your-home-routine-leverage-these-6-chatgpt-tips-for-greater-productivity/"><u>Revolutionize Your Home Routine: Leverage These 6 ChatGPT Tips for Greater Productivity</u></a></li>
<li><a href="https://technical-tips.techidaily.com/simplify-purchases-a-step-by-step-tutorial-for-using-apple-pay-feature-on-the-apple-watch/"><u>Simplify Purchases: A Step-by-Step Tutorial for Using Apple Pay Feature on the Apple Watch</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-5-cloud-based-voice-customizers-for-chrome-os-vocal-transformation-tools-reviewed-for-2024/"><u>Top 5 Cloud-Based Voice Customizers for Chrome OS Vocal Transformation Tools Reviewed for 2024</u></a></li>
</ul></div>

