---
title: "Configuring WiX Toolset Custom Actions: Ensuring Execution During System Uninstall Only"
date: 2024-09-26T17:28:21.896Z
updated: 2024-09-27T19:12:35.933Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Configuring WiX Toolset Custom Actions: Ensuring Execution During System Uninstall Only"
thumbnail: https://thmb.techidaily.com/c25817db2649211b5ab691c05f8445f856dd9c30835b0dd15640eaddc52cca01.jpg
---

## Configuring WiX Toolset Custom Actions: Ensuring Execution During System Uninstall Only

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

## How to set a WiX Toolset custom action to run only on uninstall

When you create an installer using the WiX Toolset, there are instances where you may want to set a custom action to run under specific conditions, such as uninstalling an application, installing an application, or running a custom script.

In this article, we’ll see how you can set a custom action to run when uninstalling an application using WiX Toolset.

### Understanding Custom Action conditions

Every event defined in the install sequences runs under **more or less** specific conditions.

These conditions can target more than one installer property. For this specific example, you may need to understand how the values of the “Installed”, and “REMOVE” properties are perceived by the installer's runs.

You can have a look at the table below:

| Property Name        | Install | Uninstall | Change | Repair | Upgrade |
| -------------------- | ------- | --------- | ------ | ------ | ------- |
| Installed            | False   | True      | True   | True   | True    |
| REINSTALL            | False   | False     | False  | True   | False   |
| UPGRADINGPRODUCTCODE | False   | False     | False  | False  | True    |
| REMOVE               | False   | True      | False  | False  | True    |

Remember that property names are case sensitive.

### How to Create a Custom Action and Link it to WiX Setup Project

1\. Create a new “[C# Custom Action Project for WiX v3](https://tools.techidaily.com/advancedinstaller/products/)” in your Visual Studio solution.

Here is a basic custom action snippet which will write “Hello World!” in the installation log.

using System; 
using System.Collections.Generic; 
using System.Text; 
using Microsoft.Deployment.WindowsInstaller; 
namespace CustomAction

    public class CustomActions 

    [CustomAction] 
    public static ActionResult CustomAction(Session session) 

    session.Log("Hello World!"); 
    return ActionResult.Success; 

Copy

2\. You can change the name of the function to a name that suits your function.

3\. Then, you have to reference this custom action in your WiX setup project. 

To do that, right click the “References” folder on your WiX setup project and choose “**Add Reference…**” 

4\. Following up, click on the “**Projects**” tab and choose your custom action project.

![Choose Custom Action Project](https://cdn.advancedinstaller.com/img/wix-child-images/choose-custom-action-project.png "Choose Custom Action Project")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2130869/7443" target="_top" id="2130869">
  <img src="//a.impactradius-go.com/display-ad/7443-2130869" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2130869/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to declare the WiX custom action

Now, we need to actually declare the custom action in the “Product.wxs” file. For that, you need to add the following code under the Product Tag:

<Binary Id="CustomActionBinary" SourceFile="$(var.CUSTOMACTIONSNAME.TargetDir)$(var.CUSTOMACTIONSNAME.TargetName).CA.dll" /> <CustomAction Id="CUSTOMACTIONAME" Impersonate="no" BinaryKey="CustomActionBinary" DllEntry="CUSTOMACTIONFUNCTION" Return="check" />

Copy

In order for it to work, you have to change the following names:

| “CUSTOMACTIONSNAME”    | The name of the custom action that was added in the references folder |
| ---------------------- | --------------------------------------------------------------------- |
| “CUSTOMACTIONNAME”     | The name of your choice                                               |
| “CUSTOMACTIONFUNCTION” | Your custom action project's function name that you want to call      |

### Adding the custom action to the Install Execute Sequence

In order for your custom action to be called when the installer is running, you need to add it to the install sequence. 

Insert the custom action into the Install Execute Sequence as follows:

<InstallExecuteSequence> 
     <Custom Action='CustomAction1' After='InstallInitialize'>Installed AND REMOVE=”ALL”</Custom> 
</InstallExecuteSequence>

Copy

![Tip](https://cdn.advancedinstaller.com/svg/common/IconMessageTip.svg)The **Installed AND REMOVE=”ALL”** condition will make sure that the custom action will run only when uninstalling the application.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135367/19272" target="_top" id="2135367">
  <img src="//a.impactradius-go.com/display-ad/19272-2135367" border="0" alt="https://techidaily.com" width="180" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135367/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to set a custom action to run only on uninstall using Advanced Installer?

Using Advanced Installer, you can automatically set custom actions to run only on uninstall directly from its GUI - NO need to write any code.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Custom Actions are available for Professional, Enterprise and Architect project types in Advanced Installer. Have a look at how custom actions work in Advanced Installer through our [30-day full featured trial](https://tools.techidaily.com/advancedinstaller/products/)**.** (No credit card required)

<!-- affiliate ads begin -->
<span id="1983539">
					<video width="576" height="240" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1983539.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1983539">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1983539.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1983539%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1983539/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

1\. To add a new custom action, go to the **Custom Actions** page and add a new custom action to your project.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)You can use the same custom action DLL as before by adding a “**Call function from attached native DLL**” custom action.

![Call Function from Attached Native DLL Custom Action](https://cdn.advancedinstaller.com/img/wix-child-images/call-function-from-attached-native-dll-custom-action.png "Call Function from Attached Native DLL Custom Action")  

2\. In the Properties section, under the **Function** field, select the function you want your custom action to call.

![Custom Action Function](https://cdn.advancedinstaller.com/img/wix-child-images/custom-action-function.png "Custom Action Function")  

3\. Now, in the **Execution Stage Condition** section, uncheck the Install and Maintenance checkboxes. That will make sure that your custom action will run only when you uninstall the application.

![Execution Stage Condition](https://cdn.advancedinstaller.com/img/wix-child-images/execution-stage-condition.png "Execution Stage Condition")  

And that’s it! As you could see, setting a custom action through Advanced Installer intuitive GUI requires no code skills allowing you to be time efficient when configuring your application.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1948954/19272" target="_top" id="1948954">
  <img src="//a.impactradius-go.com/display-ad/19272-1948954" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1948954/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Conclusion

In this article, we presented two approaches for configuring a custom action to run on uninstall.As we’ve seen, WiX is not GUI-based and sometimes it can be challenging to achieve specific tasks, having to create custom scripts from scratch. On the other hand, the process of adding custom actions is much simpler and quicker using Advanced Installer which offers a dedicated GUI for adding and defining custom actions.

We hope you like it! For more topic suggestions, leave a comment below.

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
<a href="https://aligracehair.sjv.io/c/5597632/2080333/19272" target="_top" id="2080333">
  <img src="//a.impactradius-go.com/display-ad/19272-2080333" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2080333/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://screen-activity-recording.techidaily.com/new-in-2024-streaming-software-showdown-the-ultimate-guide-to-obs-vs-shadowplay/"><u>[New] In 2024, Streaming Software Showdown The Ultimate Guide to OBS Vs. ShadowPlay</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-top-3-techniques-converting-pin-videos-to-mp3s/"><u>[New] Top 3 Techniques Converting Pin Videos To MP3s</u></a></li>
<li><a href="https://visual-screen-recording.techidaily.com/updated-from-watchlist-to-documents-a-comprehensible-list-of-six-mac-techniques-for-screenshotting-netflix/"><u>[Updated] From Watchlist to Documents - A Comprehensible List of Six Mac Techniques for Screenshotting Netflix</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unlocking-the-secret-to-a-streamlined-tiktok-bio-with-linktree/"><u>[Updated] Unlocking the Secret to a Streamlined TikTok Bio with Linktree</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-vector-editing-revolution-post-acid-pro-era/"><u>[Updated] Vector Editing Revolution Post-ACID Pro Era</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-digital-revolution-todays-vr-landscape-and-tomorrows-trials/"><u>2024 Approved The Digital Revolution Today's VR Landscape & Tomorrow's Trials</u></a></li>
<li><a href="https://techidaily.com/expert-analysis-elevating-knowledge-with-the-everest-consortium-on-sophisticated-content-mastery/"><u>Expert Analysis: Elevating Knowledge with the Everest Consortium on Sophisticated Content Mastery</u></a></li>
<li><a href="https://iphone-location.techidaily.com/find-my-app-troubleshooting-no-location-found-vs-location-not-available-and-how-to-fix-them-on-apple-iphone-15-drfone-by-drfone-virtual-ios/"><u>Find My App Troubleshooting No Location Found vs. Location Not Available & How to Fix Them On Apple iPhone 15 | Dr.fone</u></a></li>
<li><a href="https://hardware-help.techidaily.com/get-the-newest-hp-printer-software-for-windows-11-installation-steps/"><u>Get the Newest HP Printer Software for Windows 11 - Installation Steps</u></a></li>
<li><a href="https://bypass-frp.techidaily.com/how-can-we-bypass-samsung-galaxy-f15-5g-frp-by-drfone-android/"><u>How Can We Bypass Samsung Galaxy F15 5G FRP?</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-journey-to-picture-perfection-iphone-tips-for-stunning-skylines/"><u>In 2024, Journey to Picture Perfection IPhone Tips for Stunning Skylines</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/in-2024-step-by-step-guide-to-slow-mo-techniques-on-instagram-reels/"><u>In 2024, Step-by-Step Guide to Slow Mo Techniques on Instagram Reels</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-experts-playbook-top-techniques-for-youtube-to-mpeg/"><u>In 2024, The Expert's Playbook Top Techniques for YouTube-to-MPEG</u></a></li>
<li><a href="https://eaxpv-info.techidaily.com/understanding-the-distinctions-a-comparative-analysis-of-mkv-vs-avi-formats/"><u>Understanding the Distinctions: A Comparative Analysis of MKV Vs. AVI Formats</u></a></li>
</ul></div>

