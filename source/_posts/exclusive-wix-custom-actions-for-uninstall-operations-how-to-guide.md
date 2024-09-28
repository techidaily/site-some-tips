---
title: "Exclusive WiX Custom Actions for Uninstall Operations: How-To Guide"
date: 2024-09-26T03:28:07.906Z
updated: 2024-09-28T05:24:12.510Z
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
<a href="https://dhgate.sjv.io/c/5597632/1186864/12108" target="_top" id="1186864">
  <img src="//a.impactradius-go.com/display-ad/12108-1186864" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://dhgate.sjv.io/i/5597632/1186864/12108" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://appsumo.8odi.net/c/5597632/2137394/7443" target="_top" id="2137394">
  <img src="//a.impactradius-go.com/display-ad/7443-2137394" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2137394/7443" style="position:absolute;visibility:hidden;" border="0" />
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

### How to set a custom action to run only on uninstall using Advanced Installer?

Using Advanced Installer, you can automatically set custom actions to run only on uninstall directly from its GUI - NO need to write any code.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Custom Actions are available for Professional, Enterprise and Architect project types in Advanced Installer. Have a look at how custom actions work in Advanced Installer through our [30-day full featured trial](https://tools.techidaily.com/advancedinstaller/products/)**.** (No credit card required)

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2151889/7443" target="_top" id="2151889">
  <img src="//a.impactradius-go.com/display-ad/7443-2151889" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2151889/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

1\. To add a new custom action, go to the **Custom Actions** page and add a new custom action to your project.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)You can use the same custom action DLL as before by adding a “**Call function from attached native DLL**” custom action.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2082536/7443" target="_top" id="2082536">
  <img src="//a.impactradius-go.com/display-ad/7443-2082536" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2082536/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

![Call Function from Attached Native DLL Custom Action](https://cdn.advancedinstaller.com/img/wix-child-images/call-function-from-attached-native-dll-custom-action.png "Call Function from Attached Native DLL Custom Action")  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2044586/7443" target="_top" id="2044586">
  <img src="//a.impactradius-go.com/display-ad/7443-2044586" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2044586/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<li><a href="https://extra-tips.techidaily.com/new-aeropixel-remastering-toolkit-windowsmac/"><u>[New] AeroPixel Remastering Toolkit (Windows/Mac)</u></a></li>
<li><a href="https://youtube-videos.techidaily.com/new-boost-your-visibility-with-a-cutting-edge-set-of-banners/"><u>[New] Boost Your Visibility with a Cutting-Edge Set of Banners</u></a></li>
<li><a href="https://facebook-video-share.techidaily.com/new-in-2024-a-global-perspective-your-favorite-travel-youtubers/"><u>[New] In 2024, A Global Perspective Your Favorite Travel Youtubers</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-art-of-preservation-digitizing-and-safeguarding-faded-family-memories/"><u>[New] The Art of Preservation Digitizing & Safeguarding Faded Family Memories</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-art-of-visual-storytelling-with-iphone-xs-new-lens/"><u>[New] The Art of Visual Storytelling with iPhone X's New Lens</u></a></li>
<li><a href="https://fox-hovers.techidaily.com/updated-high-end-psd-lighting-tweaks-for-2024/"><u>[Updated] High-End PSD Lighting Tweaks for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-techniques-to-zoom-into-online-engagements-intelligently/"><u>[Updated] Techniques to Zoom Into Online Engagements Intelligently</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/updated-the-ultimate-list-of-powerful-pc-screencasters-for-2024/"><u>[Updated] The Ultimate List of Powerful PC Screencasters for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unlock-creative-potential-with-10-best-backdrop-modification-software/"><u>2024 Approved Unlock Creative Potential with 10 Best Backdrop Modification Software</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/android-unlock-code-sim-unlock-your-samsung-galaxy-f14-5g-phone-and-remove-locked-screen-by-drfone-android/"><u>Android Unlock Code Sim Unlock Your Samsung Galaxy F14 5G Phone and Remove Locked Screen</u></a></li>
<li><a href="https://youtube-sure.techidaily.com/e-gaps-in-generations-of-viewers-6-interactive-tests-to-find-your-youtube-match-for-2024/"><u>Bridge Gaps in Generations of Viewers 6 Interactive Tests to Find Your YouTube Match for 2024</u></a></li>
<li><a href="https://bypass-frp.techidaily.com/hassle-free-ways-to-remove-frp-lock-from-realme-12-5g-phones-withwithout-a-pc-by-drfone-android/"><u>Hassle-Free Ways to Remove FRP Lock from Realme 12 5G Phones with/without a PC</u></a></li>
<li><a href="https://video-screen-grab.techidaily.com/in-2024-the-ultimate-guide-to-screen-capture-via-screencastify/"><u>In 2024, The Ultimate Guide to Screen Capture via Screencastify</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-ultrawide-vs-uhd-4k-monitors-the-experts-advice/"><u>In 2024, UltraWide VS UHD 4K Monitors The Expert's Advice</u></a></li>
<li><a href="https://some-tips.techidaily.com/strategy-cradle-nurturing-market-gains-for-2024/"><u>Strategy Cradle Nurturing Market Gains for 2024</u></a></li>
<li><a href="https://extra-resources.techidaily.com/the-ultimate-zoom-and-gmail-collaboration-methods/"><u>The Ultimate Zoom and Gmail Collaboration Methods</u></a></li>
<li><a href="https://some-tips.techidaily.com/ultra-quick-photo-inspector-app-for-2024/"><u>Ultra-Quick Photo Inspector App for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlock-your-potential-with-expert-picked-video-stabilization-tools-for-2024/"><u>Unlock Your Potential with Expert-Picked Video Stabilization Tools for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveiling-filmoras-most-attractive-edits-for-2024/"><u>Unveiling Filmora's Most Attractive Edits for 2024</u></a></li>
</ul></div>

