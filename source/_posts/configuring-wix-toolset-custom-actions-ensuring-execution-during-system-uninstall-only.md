---
title: "Configuring WiX Toolset Custom Actions: Ensuring Execution During System Uninstall Only"
date: 2024-09-30T17:06:28.344Z
updated: 2024-10-03T18:37:43.531Z
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

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2027190/19272" target="_top" id="2027190">
  <img src="//a.impactradius-go.com/display-ad/19272-2027190" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2027190/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://appsumo.8odi.net/c/5597632/2130890/7443" target="_top" id="2130890">
  <img src="//a.impactradius-go.com/display-ad/7443-2130890" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2130890/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://ephamedtechinc.pxf.io/c/5597632/2130530/26400" target="_top" id="2130530">
  <img src="//a.impactradius-go.com/display-ad/26400-2130530" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2130530/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to set a custom action to run only on uninstall using Advanced Installer?

Using Advanced Installer, you can automatically set custom actions to run only on uninstall directly from its GUI - NO need to write any code.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Custom Actions are available for Professional, Enterprise and Architect project types in Advanced Installer. Have a look at how custom actions work in Advanced Installer through our [30-day full featured trial](https://tools.techidaily.com/advancedinstaller/products/)**.** (No credit card required)

1\. To add a new custom action, go to the **Custom Actions** page and add a new custom action to your project.

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)You can use the same custom action DLL as before by adding a “**Call function from attached native DLL**” custom action.

<!-- affiliate ads begin -->
<span id="1834906">
					<video width="864" height="864" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1834906.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/16836-1834906">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1834906.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:540px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2F25home.pxf.io%2Fc%2F5597632%2F1834906%2F16836'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1834906/16836" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

![Call Function from Attached Native DLL Custom Action](https://cdn.advancedinstaller.com/img/wix-child-images/call-function-from-attached-native-dll-custom-action.png "Call Function from Attached Native DLL Custom Action")  

2\. In the Properties section, under the **Function** field, select the function you want your custom action to call.

![Custom Action Function](https://cdn.advancedinstaller.com/img/wix-child-images/custom-action-function.png "Custom Action Function")  

3\. Now, in the **Execution Stage Condition** section, uncheck the Install and Maintenance checkboxes. That will make sure that your custom action will run only when you uninstall the application.

![Execution Stage Condition](https://cdn.advancedinstaller.com/img/wix-child-images/execution-stage-condition.png "Execution Stage Condition")  

And that’s it! As you could see, setting a custom action through Advanced Installer intuitive GUI requires no code skills allowing you to be time efficient when configuring your application.

<!-- affiliate ads begin -->
<a href="https://laganoo.pxf.io/c/5597632/1657396/16446" target="_top" id="1657396">
  <img src="//a.impactradius-go.com/display-ad/16446-1657396" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://laganoo.pxf.io/i/5597632/1657396/16446" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://twitter-videos.techidaily.com/updated-2024-approved-filming-for-tweet-sharing-content-without-retweeting/"><u>[Updated] 2024 Approved Filming for Tweet Sharing Content without Retweeting</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyy-renouvele-son-image-visuelle-et-logo/"><u>ABBYY Renouvele Son Image Visuelle Et Logo</u></a></li>
<li><a href="https://some-tips.techidaily.com/automated-conversion-tracking-with-cookiebot-technology/"><u>Automated Conversion Tracking with Cookiebot Technology</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/bebop-2s-avian-spectacle-a-compreran-analysis/"><u>Bebop 2'S Avian Spectacle – A Compreran Analysis</u></a></li>
<li><a href="https://some-tips.techidaily.com/boost-your-online-presence-the-revolutionary-power-of-cookiebot-integration/"><u>Boost Your Online Presence: The Revolutionary Power of Cookiebot Integration</u></a></li>
<li><a href="https://blog-min.techidaily.com/connect-with-creativity-discover-the-artistry-of-digiarty/"><u>Connect with Creativity: Discover the Artistry of DigiArty</u></a></li>
<li><a href="https://facebook.techidaily.com/how-to-fix-facebook-notifications-not-loading/"><u>How to Fix Facebook Notifications Not Loading</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-rescue-lost-pictures-from-motorola-moto-g14-by-fonelab-android-recover-pictures/"><u>How to Rescue Lost Pictures from Motorola Moto G14?</u></a></li>
<li><a href="https://twitter-videos.techidaily.com/in-2024-boost-your-brand-twitter-ads-guide/"><u>In 2024, Boost Your Brand Twitter Ads Guide</u></a></li>
<li><a href="https://buynow-info.techidaily.com/meet-the-mobile-marvel-exclusive-insights-into-the-hp-zbook-firefly-15-g8-laptop/"><u>Meet the Mobile Marvel: Exclusive Insights Into the HP ZBook Firefly 15 G8 Laptop</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/1723964482600-nextorages-trailblazing-pcie-gen-4-m2-nvme-ssd-for-gaming-unmatched-speeds-of-up-to-7400-mbs/"><u>Nextorage's Trailblazing PCIe Gen 4 M.2 NVMe SSD for Gaming - Unmatched Speeds of Up to 7,400 MB/S!</u></a></li>
<li><a href="https://some-tips.techidaily.com/pionierarbeit-von-dsgf-fur-digitalisierung-der-finanzen-partnerschaft-mit-abbyy-macht-wirkung/"><u>Pionierarbeit Von DSGF Für Digitalisierung Der Finanzen: Partnerschaft Mit ABBYY Macht Wirkung</u></a></li>
<li><a href="https://graphic-issues.techidaily.com/remedied-geforce-shader-compatibility/"><u>Remedied GeForce Shader Compatibility</u></a></li>
<li><a href="https://some-tips.techidaily.com/revolutionize-your-marketing-analytics-with-our-cutting-edge-cookiebot-solutions/"><u>Revolutionize Your Marketing Analytics with Our Cutting-Edge Cookiebot Solutions</u></a></li>
<li><a href="https://some-tips.techidaily.com/seamless-integration-abbyy-connects-with-automation-anywhere/"><u>Seamless Integration: ABBYY Connects with Automation Anywhere</u></a></li>
<li><a href="https://some-tips.techidaily.com/unleashing-endless-possibilities-the-future-of-document-capture-solutions-insights-from-abbyy/"><u>Unleashing Endless Possibilities: The Future of Document Capture Solutions - Insights From ABBYY</u></a></li>
<li><a href="https://some-tips.techidaily.com/web-page-essentials-unlocking-effective-strategies-for-search-engines/"><u>Web Page Essentials: Unlocking Effective Strategies for Search Engines</u></a></li>
</ul></div>

