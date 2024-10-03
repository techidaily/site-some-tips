---
title: "Crafting Personalized UI Prompts with WiX: A Guide to Tailoring User Input Dialogues"
date: 2024-09-26T19:57:02.495Z
updated: 2024-10-03T17:27:35.141Z
tags:
  - versus
categories:
  - advancedinstaller
description: "This Article Describes Crafting Personalized UI Prompts with WiX: A Guide to Tailoring User Input Dialogues"
thumbnail: https://thmb.techidaily.com/cb833d2c06ebc2c32cdbed9ef9e234accd8f5206773825bdc531095627fac7c4.jpg
---

## Crafting Personalized UI Prompts with WiX: A Guide to Tailoring User Input Dialogues

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

## How to create a custom dialog in WiX for user input

Written by [Renato Ivanescu](https://tools.techidaily.com/advancedinstaller/products/) · June 15th, 2023

During the installation process, **user input dialogs** play a crucial role by prompting users to provide necessary input. This feature is widely utilized in setup packages as it allows users to provide feedback, and it ensures proper installation and configuration of the software. Additionally, it allows you to store valuable information on the local machine for future use.

Let's say you have an application, and you want to create an installer package that collects information from the user.

In this tutorial, we’ll show you **how to create a custom dialog** to let the user provide input. We'll set it up so that it gets saved in a txt file on the local machine after installing the application. 

To achieve this, let's now directly follow the steps outlined in the upcoming sections.

### How to add the setup project?

To add the setup project for your application, go to _File_ → _New_ → _Project_. From the templates list, choose _Setup Project for Wix_. 

![Setup Project for Wix](https://cdn.advancedinstaller.com/img/create-wix-custom-dialog-user-input/setup-project-for-wix.png "Setup Project for Wix")  

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Keep in mind that you need to have the WiX extension added to Visual Studio to find the template. Check [this](https://tools.techidaily.com/advancedinstaller/products/) tutorial to see how to add it. There, you’ll also find how to **add the deployable files** once the Setup Project is created.  

Once you add the WiX extension and the deployable files, you have to edit the Product.wxs file and add the next line to reference the UI element we will use in this tutorial. 

<Product Id = “*” … >
   <UIRef Id="CustomSetupUI" />
</Product>

Copy

### How to create the installer dialogs?

Now, we are ready to create the dialogs for our installer package. A dialog is a Windows Installer XML file. We will create two dialogs for our installer package: 

* A welcome dialog → _SetupDlg.wxs_
* A dialog for the user input → _InputDlg.wxs_

To create a dialog, follow the next steps:

1. Right-click on the _Setup Project_ → _Add_ → _New Item._
2. Go to the _WiX_ section and choose _Installer File_.
3. Name it and click the _Add_ button.

![create the installer dialogs](https://cdn.advancedinstaller.com/img/create-wix-custom-dialog-user-input/create-the-installer-dialogs.png "create the installer dialogs")  

After you create the two dialogs, you should find them in the _Solution Explorer_ under the _Setup Project_.

![Solution Explorer](https://cdn.advancedinstaller.com/img/create-wix-custom-dialog-user-input/solution-explorer.png "Solution Explorer")  

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2123512/26400" target="_top" id="2123512">
  <img src="//a.impactradius-go.com/display-ad/26400-2123512" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2123512/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

<!-- affiliate ads begin -->
<a href="https://25home.pxf.io/c/5597632/2148634/16836" target="_top" id="2148634">
  <img src="//a.impactradius-go.com/display-ad/16836-2148634" border="0" alt="https://techidaily.com" width="80" height="31"/>
</a>
<img height="0" width="0" src="https://25home.pxf.io/i/5597632/2148634/16836" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to customize the installer dialogs?

Once the installer dialogs are created, you have to add the controls. 

1\. The welcome dialog from our example includes: 

\- Static texts

\- Two buttons: _Cancel_ (cancel the setup) and _Next_ (proceed to the next dialog)

![customize the installer dialogs](https://cdn.advancedinstaller.com/img/create-wix-custom-dialog-user-input/customize-the-installer-dialogs.png "customize the installer dialogs")  

For this dialog, you can use the following code.

<?xml version="1.0" encoding="UTF-8"?>
<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
<Fragment>
	<UI Id="CustomSetupUI">
	<TextStyle Id="RobotoBold" FaceName="RobotoBold" Size="10" />
	<Property Id="DefaultUIFont" Value="RobotoBold" />
	<DialogRef Id="InputDlg"/>
	<TextStyle Id="TahomaWelcome" FaceName="Tahoma" Size="14" Bold="yes" />
	<TextStyle Id="TahomaInput" FaceName="Tahoma" Size="10" />
	<Dialog Id="SetupDlg" Width="300" Height="200" Title="My Custom App">
	<Control Id="WelcomeMsg" Type="Text" X="45" Y="40" Width="250" Height="80" Transparent="yes" Text="{\TahomaWelcome}Welcome to the Setup Wizard"/>
	<Control Id="Info" Type="Text" X="27" Y="80" Width="300" Height="80" Transparent="yes" Text="{\TahomaInfo}Click 'Next' to continue or 'Cancel' to exit the Setup Wizard"/>
	<Control Id="InstallBtn" Type="PushButton" Text="Next" Height ="25" Width="60" X="165" Y="130">
	<Publish Event="EndDialog" Value="Return" />
	</Control>
	<Control Id="CancelBtn" Type="PushButton" Text="Cancel" Height ="25" Width="60" X="80"  Y="130" Cancel ="yes">
	<Publish Event="EndDialog" Value="Exit" />
	</Control> 
	</Dialog>
	</UI>
	<InstallUISequence>
	<Show Dialog ="SetupDlg" Before="ExecuteAction"/>
	</InstallUISequence>
	</Fragment>
</Wix>

Copy

2\. The input dialog includes:

\- Static texts

\- Two edit boxes for the user input

\- Two buttons: _Cancel_ (cancel the installer) and _Install_ (will start installing the application)

![input dialog](https://cdn.advancedinstaller.com/img/create-wix-custom-dialog-user-input/input-dialog.png "input dialog")  

For this dialog, add the code below. 

<?xml version="1.0" encoding="UTF-8"?>
<Wix xmlns="http://schemas.microsoft.com/wix/2006/wi">
	<Fragment>
	<UI Id="InputDlgUI">
	<Dialog Id="InputDlg" Height="200" Width="300" Title="Registration form">
	<Control Id="headerText" Type="Text" Height="50" Width="400" X="0" Y="0" TabSkip="no" />
	<Control Id="RegistMsg" Type="Text" X="20" Y="25" Width="250" Height="80" Transparent="yes" Text="{\TahomaInfo} Add an email and a password"/>
	<Control Id="nameLabel" Type="Text" X="20" Y="65" Height="17" Width="65" Transparent="yes" Text="E-mail:" />
	<Control Id="emailTextbox" Type="Edit" X="80" Y="65"  Height="17" Width="140" Property="EMAIL"  />
	<Control Id="emailLabel" Type="Text" X="20" Y="85" Height="17" Width="65" Transparent="yes" Text="Password:" />
	<Control Id="passwordTextbox" Type="Edit" X="80" Y="85"  Height="17" Width="140" Property="PASSWORD"  />
	<Control Id="InstallBtn" Type="PushButton" Text="Install" Height ="25" Width="60" X="160" Y="130">
	<Publish Event="DoAction" Value="UserInputCA">1</Publish>
	<Publish Event="EndDialog" Value="Return">1</Publish>
	</Control>
	<Control Id="CancelBtn" Type="PushButton" Text="Cancel" Height ="25" Width="60" X="80"  Y="130" Cancel ="yes">
	<Publish Event="EndDialog" Value="Exit" />
	</Control>
	</Dialog>
	</UI>
	<InstallUISequence>
	<Show Dialog="InputDlg" After="SetupDlg" />
	</InstallUISequence>
	</Fragment>
	<Fragment>
	<Binary Id="CustomActionBinary" SourceFile="$(var.UserInputCA.TargetDir)$(var.UserInputCA.TargetName).CA.dll"/>
	<CustomAction Id="UserInputCA" BinaryKey="CustomActionBinary" DllEntry="SaveUserInput"  />
	</Fragment>
</Wix>

Copy

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2151884/7443" target="_top" id="2151884">
  <img src="//a.impactradius-go.com/display-ad/7443-2151884" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2151884/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### How to save the user input in a txt file?

Now, we have to take the information from the input dialog and save it in the txt file. For this, we will use a custom action. To create it, follow the steps:

1\. Go to _Files_ → _New_ → _Project_ and search for _C# Custom Action Project for WiX_.

![save the user input in a txt file](https://cdn.advancedinstaller.com/img/create-wix-custom-dialog-user-input/save-the-user-input-in-a-txt-file.png "save the user input in a txt file")  

2\. Next, add the following code to **create the custom action**: 

public class CustomActions

        [CustomAction]
        public static ActionResult SaveUserInput(Session session)

            string email = session["EMAIL"];
            string password = session["PASSWORD"];
            string appdataPath = "C:\\Users\\Caphyon";
            if (!Directory.Exists(appdataPath + "\\UserData"))
                Directory.CreateDirectory(appdataPath + "\\UserData");
            File.WriteAllText(appdataPath + "\\UserData\\InputInfo.txt", email + "," + password);
            return ActionResult.Success;

Copy

As you can see, in order to store the user information, the custom action uses the Property attribute values of the _emailTextBox_ and _passwordTextBox_ control elements. The collected information will be written to a text file called _InputInfo.txt_ and saved in the directory _C:\\Users\\Caphyon\\UserData_.

3\. After creating the custom action, you need to **reference it in the Setup Project**. 

To do this, right-click on the _Setup Project_ → _Add_ → _Reference_. In the _Add Reference_ dialog, go to the _Projects_ tab and select the custom action that you created previously. Press the _Add_ button and then the _Ok_ button.

![reference it in the Setup Project](https://cdn.advancedinstaller.com/img/create-wix-custom-dialog-user-input/reference-it-in-the-setup-project.png "reference it in the Setup Project")  

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1886048/19272" target="_top" id="1886048">
  <img src="//a.impactradius-go.com/display-ad/19272-1886048" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1886048/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Build and install the project

After completing all the above steps, all you have to do is build the project and run the installer package. 

Enter the data into the text fields you added to the input dialog and click on the install button. After the installation is complete, you should be able to locate the text file that contains the information you entered in the text boxes.

### Conclusion

Designing user input dialogs in WiX can be challenging, particularly for complex scenarios like client-type applications. These cases often involve gathering and storing essential information, such as server address, port number, and firewall settings, in the registry. Editing the .wxs files to incorporate all the controls and create custom actions can be time-consuming.

A more streamlined and effective approach is to leverage a GUI-based tool. Advanced Installer provides an intuitive graphical user interface that simplifies the process of adding controls to dialogs. You can conveniently configure the controls directly from the user interface, saving you valuable time and effort.

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
<a href="https://aligracehair.sjv.io/c/5597632/1896560/19272" target="_top" id="1896560">
  <img src="//a.impactradius-go.com/display-ad/19272-1896560" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1896560/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://youtube-docs.techidaily.com/nveiling-secrets-sharing-restricted-youtube-content-via-email/"><u>[New] Unveiling Secrets Sharing Restricted YouTube Content via Email</u></a></li>
<li><a href="https://screen-capture.techidaily.com/updated-2024-approved-side-by-side-display-logging/"><u>[Updated] 2024 Approved Side-by-Side Display Logging</u></a></li>
<li><a href="https://some-skills.techidaily.com/updated-unlocking-superior-slow-motion-quality-through-fps-selection/"><u>[Updated] Unlocking Superior Slow Motion Quality Through FPS Selection</u></a></li>
<li><a href="https://video-screen-grab.techidaily.com/2024-approved-live-streaming-tools-head-to-head-obs-vs-fraps/"><u>2024 Approved Live Streaming Tools Head to Head OBS vs Fraps</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/2024-approved-new-users-on-the-road-to-zoom-room-mastery/"><u>2024 Approved New Users on the Road to Zoom Room Mastery</u></a></li>
<li><a href="https://some-tips.techidaily.com/cookiebot-enabled-enhancing-user-experience-through-personalized-engagement/"><u>Cookiebot-Enabled: Enhancing User Experience Through Personalized Engagement</u></a></li>
<li><a href="https://some-tips.techidaily.com/cookiebot-enhanced-marketing-solutions-drive-growth-through-advanced-analytics-and-personalization/"><u>Cookiebot-Enhanced Marketing Solutions: Drive Growth Through Advanced Analytics & Personalization</u></a></li>
<li><a href="https://some-tips.techidaily.com/cookiebot-enhanced-user-experience-tailored-and-tracked/"><u>Cookiebot-Enhanced User Experience: Tailored and Tracked</u></a></li>
<li><a href="https://some-tips.techidaily.com/cookiebot-the-backbone-of-your-sites-personalization-strategy/"><u>Cookiebot: The Backbone of Your Site's Personalization Strategy</u></a></li>
<li><a href="https://some-tips.techidaily.com/costains-abteilungsstrategie-fur-digitale-transformationen-die-rolle-von-abbyy-technologien-in-der-finanzverwaltung/"><u>Costain's Abteilungsstrategie Für Digitale Transformationen – Die Rolle Von ABBYY-Technologien in Der Finanzverwaltung</u></a></li>
<li><a href="https://some-tips.techidaily.com/digitale-transformation-zum-profitieren-vom-unternehmensarchiv-zur-effizienten-dokumentverwaltung/"><u>Digitale Transformation Zum Profitieren! Vom Unternehmensarchiv Zur Effizienten Dokumentverwaltung.</u></a></li>
<li><a href="https://some-tips.techidaily.com/e-book-techniques-pour-detruire-les-obstacles-a-la-registration-clientelle-mobile/"><u>E-Book: Techniques Pour Détruire Les Obstacles À La Régistration Clientelle Mobile</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhance-user-experience-through-advanced-tracking-technology-like-cookiebot/"><u>Enhance User Experience Through Advanced Tracking Technology Like Cookiebot</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhance-your-site-with-automated-visitor-tracking-the-secrets-in-the-bots/"><u>Enhance Your Site with Automated Visitor Tracking - The Secret's in the Bots!</u></a></li>
<li><a href="https://review-topics.techidaily.com/in-2024-can-life360-track-you-when-your-xiaomi-redmi-note-12r-is-off-drfone-by-drfone-virtual-android/"><u>In 2024, Can Life360 Track You When Your Xiaomi Redmi Note 12R is off? | Dr.fone</u></a></li>
<li><a href="https://ios-unlock.techidaily.com/in-2024-how-to-change-country-on-app-store-for-apple-iphone-se-2022-with-7-methods-by-drfone-ios/"><u>In 2024, How To Change Country on App Store for Apple iPhone SE (2022) With 7 Methods</u></a></li>
<li><a href="https://tech-revival.techidaily.com/showdown-between-tech-leaders-can-llama-3-outshine-gpt-4/"><u>Showdown Between Tech Leaders: Can Llama 3 Outshine GPT-4?</u></a></li>
<li><a href="https://program-issues.techidaily.com/success-story-how-to-play-dragon-age-origins-without-glitches-on-windows-11/"><u>Success Story: How to Play Dragon Age: Origins Without Glitches on Windows 11</u></a></li>
<li><a href="https://win11-tips.techidaily.com/unlocking-hidden-outlook-folders-on-pc-a-step-by-step-guide/"><u>Unlocking Hidden Outlook Folders on PC: A Step-by-Step Guide</u></a></li>
</ul></div>

