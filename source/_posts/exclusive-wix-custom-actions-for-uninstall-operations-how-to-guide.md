---
title: "Exclusive WiX Custom Actions for Uninstall Operations: How-To Guide"
date: 2024-09-27T19:27:34.929Z
updated: 2024-10-03T17:24:47.669Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Exclusive WiX Custom Actions for Uninstall Operations: How-To Guide"
thumbnail: https://thmb.techidaily.com/13a2ed7d3d473fc4b094f952faefa5141a38181bbb0354fc87e696c7a5f69650.png
---

## Exclusive WiX Custom Actions for Uninstall Operations: How-To Guide

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

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1948895/19272" target="_top" id="1948895">
  <img src="//a.impactradius-go.com/display-ad/19272-1948895" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1948895/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<a href="https://review-au.sjv.io/c/5597632/2098703/14409" target="_top" id="2098703">
  <img src="//a.impactradius-go.com/display-ad/14409-2098703" border="0" alt="https://techidaily.com" width="468" height="60"/>
</a>
<img height="0" width="0" src="https://review-au.sjv.io/i/5597632/2098703/14409" style="position:absolute;visibility:hidden;" border="0" />
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

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1948881/19272" target="_top" id="1948881">
  <img src="//a.impactradius-go.com/display-ad/19272-1948881" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1948881/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Adding the custom action to the Install Execute Sequence

In order for your custom action to be called when the installer is running, you need to add it to the install sequence. 

Insert the custom action into the Install Execute Sequence as follows:

<InstallExecuteSequence> 
     <Custom Action='CustomAction1' After='InstallInitialize'>Installed AND REMOVE=”ALL”</Custom> 
</InstallExecuteSequence>

Copy

![Tip](https://cdn.advancedinstaller.com/svg/common/IconMessageTip.svg)The **Installed AND REMOVE=”ALL”** condition will make sure that the custom action will run only when uninstalling the application.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2144278/7443" target="_top" id="2144278">
  <img src="//a.impactradius-go.com/display-ad/7443-2144278" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2144278/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to set a custom action to run only on uninstall using Advanced Installer?

Using Advanced Installer, you can automatically set custom actions to run only on uninstall directly from its GUI - NO need to write any code.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Custom Actions are available for Professional, Enterprise and Architect project types in Advanced Installer. Have a look at how custom actions work in Advanced Installer through our [30-day full featured trial](https://tools.techidaily.com/advancedinstaller/products/)**.** (No credit card required)

1\. To add a new custom action, go to the **Custom Actions** page and add a new custom action to your project.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)You can use the same custom action DLL as before by adding a “**Call function from attached native DLL**” custom action.

<!-- affiliate ads begin -->
<span id="1424528">
					<video width="864" height="1536" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1424528.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/16446-1424528">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1424528.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:540px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Flaganoo.pxf.io%2Fc%2F5597632%2F1424528%2F16446'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1424528/16446" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

![Call Function from Attached Native DLL Custom Action](https://cdn.advancedinstaller.com/img/wix-child-images/call-function-from-attached-native-dll-custom-action.png "Call Function from Attached Native DLL Custom Action")  

2\. In the Properties section, under the **Function** field, select the function you want your custom action to call.

![Custom Action Function](https://cdn.advancedinstaller.com/img/wix-child-images/custom-action-function.png "Custom Action Function")  

3\. Now, in the **Execution Stage Condition** section, uncheck the Install and Maintenance checkboxes. That will make sure that your custom action will run only when you uninstall the application.

![Execution Stage Condition](https://cdn.advancedinstaller.com/img/wix-child-images/execution-stage-condition.png "Execution Stage Condition")  

And that’s it! As you could see, setting a custom action through Advanced Installer intuitive GUI requires no code skills allowing you to be time efficient when configuring your application.

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
<li><a href="https://screen-activity-recording.techidaily.com/new-nurturing-nature-in-valheim-top-seed-selection-tips-for-2024/"><u>[New] Nurturing Nature in Valheim Top Seed Selection Tips for 2024</u></a></li>
<li><a href="https://extra-support.techidaily.com/new-portable-balance-enhancer-for-shooting-blurs/"><u>[New] Portable Balance Enhancer for Shooting Blurs</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/new-post-production-pro-tailoring-video-content-to-instagram-standards-with-x/"><u>[New] Post-Production Pro Tailoring Video Content to Instagram Standards with X</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/2024-approved-exclusive-listing-top-15-platforms-for-gopro-optimal-use/"><u>2024 Approved Exclusive Listing Top 15 Platforms for GoPro Optimal Use</u></a></li>
<li><a href="https://fox-http.techidaily.com/advanced-tips-for-3d-color-grading/"><u>Advanced Tips for 3D Color Grading</u></a></li>
<li><a href="https://some-skills.techidaily.com/exciting-news-googles-bard-is-rolling-out-immediately-with-additional-plugin-support/"><u>Exciting News! Google's Bard Is Rolling Out Immediately with Additional Plugin Support</u></a></li>
<li><a href="https://some-tips.techidaily.com/understanding-the-ping-tool-a-comprehensive-guide-on-testing-your-online-connectivity/"><u>Understanding the PING Tool: A Comprehensive Guide on Testing Your Online Connectivity</u></a></li>
<li><a href="https://techno-recovery.techidaily.com/understanding-your-internet-data-usage-tips-and-tricks/"><u>Understanding Your Internet Data Usage - Tips & Tricks</u></a></li>
<li><a href="https://some-tips.techidaily.com/windows-11-creators-update-troubleshooting-fixing-downloads-and-audio-problems/"><u>Windows 11 Creators Update Troubleshooting: Fixing Downloads and Audio Problems</u></a></li>
<li><a href="https://some-tips.techidaily.com/windows-11-creators-update-download-stuck-and-no-sound-issues-fixed/"><u>Windows 11 Creators Update: Download Stuck & No Sound Issues [Fixed]</u></a></li>
<li><a href="https://some-tips.techidaily.com/windows-11-essentials-executing-a-pristine-system-reboot/"><u>Windows 11 Essentials: Executing a Pristine System Reboot</u></a></li>
</ul></div>

