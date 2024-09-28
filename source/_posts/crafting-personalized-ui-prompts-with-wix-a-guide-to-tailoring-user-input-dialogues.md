---
title: "Crafting Personalized UI Prompts with WiX: A Guide to Tailoring User Input Dialogues"
date: 2024-09-22T05:00:04.670Z
updated: 2024-09-27T18:17:23.505Z
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

<!-- affiliate ads begin -->
<a href="https://25home.pxf.io/c/5597632/2148649/16836" target="_top" id="2148649">
  <img src="//a.impactradius-go.com/display-ad/16836-2148649" border="0" alt="https://techidaily.com" width="720" height="90"/>
</a>
<img height="0" width="0" src="https://25home.pxf.io/i/5597632/2148649/16836" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

![Note](https://cdn.advancedinstaller.com/svg/common/IconMessageNote.svg)Keep in mind that you need to have the WiX extension added to Visual Studio to find the template. Check [this](https://tools.techidaily.com/advancedinstaller/products/) tutorial to see how to add it. There, you’ll also find how to **add the deployable files** once the Setup Project is created.  

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2144275/7443" target="_top" id="2144275">
  <img src="//a.impactradius-go.com/display-ad/7443-2144275" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2144275/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

Once you add the WiX extension and the deployable files, you have to edit the Product.wxs file and add the next line to reference the UI element we will use in this tutorial. 

<Product Id = “*” … >
   <UIRef Id="CustomSetupUI" />
</Product>

Copy

<!-- affiliate ads begin -->
<a href="https://versadesk.pxf.io/c/5597632/1815678/21290" target="_top" id="1815678">
  <img src="//a.impactradius-go.com/display-ad/21290-1815678" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://versadesk.pxf.io/i/5597632/1815678/21290" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

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
<a href="https://aligracehair.sjv.io/c/5597632/2012415/19272" target="_top" id="2012415">
  <img src="//a.impactradius-go.com/display-ad/19272-2012415" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2012415/19272" style="position:absolute;visibility:hidden;" border="0" />
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
<a href="https://appsumo.8odi.net/c/5597632/2151882/7443" target="_top" id="2151882">
  <img src="//a.impactradius-go.com/display-ad/7443-2151882" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2151882/7443" style="position:absolute;visibility:hidden;" border="0" />
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
<li><a href="https://video-capture.techidaily.com/new-2024-approved-complete-evaluation-of-camstudio-screen-recorder/"><u>[New] 2024 Approved Complete Evaluation of CamStudio Screen Recorder</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-essential-blueprint-for-srt-file-adaptability/"><u>[New] The Essential Blueprint for SRT File Adaptability</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/updated-explore-largest-collection-of-free-vector-graphics-portals-for-2024/"><u>[Updated] Explore Largest Collection of Free Vector Graphics Portals for 2024</u></a></li>
<li><a href="https://twitter-videos.techidaily.com/updated-in-2024-simple-guide-sharing-tweets-with-imagesvideos-directly-to-twitter/"><u>[Updated] In 2024, Simple Guide Sharing Tweets with Images/Videos Directly to Twitter</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-transforming-movies-into-virtual-reality-realms/"><u>[Updated] Transforming Movies Into Virtual Reality Realms</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-understanding-and-utilizing-windows-11-auto-hdr-functionality/"><u>[Updated] Understanding and Utilizing Windows 11 Auto HDR Functionality</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-smart-guide-for-spawning-share-worthy-memes-in-9gag/"><u>2024 Approved The Smart Guide for Spawning Share-Worthy Memes in 9GAG</u></a></li>
<li><a href="https://android-unlock.techidaily.com/downloading-samfw-frp-tool-30-for-lava-storm-5g-by-drfone-android/"><u>Downloading SamFw FRP Tool 3.0 for Lava Storm 5G</u></a></li>
<li><a href="https://tech-haven.techidaily.com/exploring-the-capabilities-of-shapley-explanations-in-artifice-intelligence-systems/"><u>Exploring the Capabilities of Shapley Explanations in Artifice Intelligence Systems</u></a></li>
<li><a href="https://extra-hints.techidaily.com/in-2024-10-superior-video-text-enhancements/"><u>In 2024, 10 Superior Video Text Enhancements</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-easy-way-to-download-and-use-the-ifunny-meme-app/"><u>In 2024, The Easy Way to Download and Use the iFunny Meme App</u></a></li>
<li><a href="https://ai-vdieo-software.techidaily.com/new-digital-drawing-board-converting-videos-into-cartoons-with-ease/"><u>New Digital Drawing Board Converting Videos Into Cartoons with Ease</u></a></li>
<li><a href="https://some-tips.techidaily.com/tailoring-text-features-in-ae-compositions-for-2024/"><u>Tailoring Text Features in AE Compositions for 2024</u></a></li>
</ul></div>

