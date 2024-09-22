---
title: Resolving the Issue of Excessive CPU Consumption by Windows Module Installer
date: 2024-09-15T16:43:17.520Z
updated: 2024-09-22T18:12:02.028Z
tags:
  - deals
categories:
  - tech
thumbnail: https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/10/52781818963_ddd89fcf7e_o-1.jpg
---

## Resolving the Issue of Excessive CPU Consumption by Windows Module Installer

### Key Takeaways

* Let the Windows Modules Installer Worker process finish running even if it's using a lot of CPU. It will stop working once the update or maintenance task is complete.
* To stop the process as you want to do something on your PC, open Task Manager, access the "Processes" tab, right-click the process, and choose "End Task."
* Other troubleshooting methods include running Windows Update troubleshooter, clearing Windows Update cache and pausing the updates, and running the PC's maintenance tasks at your chosen time.

 Windows Modules Installer Worker (TiWorker.exe) is a normal Windows process related to your PC’s updates and maintenance. However, if it uses up a lot of CPU for an extended period it may be due to an error. Here are some things you can do to fix it.

##  Wait for It to Finish Running

 Windows launches the Windows Modules Installer Worker when there’s an update to install or a PC maintenance task to run. You should generally let the process finish running, even if it’s using up a lot of CPU.

 When the update or maintenance task has finished, the process will stop running.

 If it continues to run for an extended period or you want to perform other tasks, use the troubleshooting tips below.

##  Run Windows Update Troubleshooter

 Windows Modules Installer Worker often runs longer than expected when there is a problem with an update. In this case, run the Windows Update troubleshooter to [find and fix any update problems](https://extra-guidance.techidaily.com/2024-approved-smoothing-out-the-rough-edges-in-photo-booth-videos/).

 Microsoft is phasing out troubleshooters in favor of the Get Help app on Windows 11\. In the future, use that app to resolve issues with your PC.

 If you’re on Windows 11, navigate to Settings > System > Troubleshoot > Other Troubleshooters, then click the "Run" button next to Windows Update.

!['Run' highlighted for 'Windows Update' troubleshooter in Windows 11 Settings.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2024/01/1-launch-windows-update-troubleshooter-windows-11.jpg) 

 On Windows 10, head to Settings > Update & Security > Troubleshoot > Additional Troubleshooters. Select "Windows Update" and click "Run the Troubleshooter."

!['Run the Troubleshooter' highlighted for 'Windows Update' troubleshooter in Windows 10 Settings.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2024/01/2-open-windows-update-troubleshooter-windows-10.jpg) 

 Follow the on-screen instructions in the tool to resolve any update issues.

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1948949/19272" target="_top" id="1948949">
  <img src="//a.impactradius-go.com/display-ad/19272-1948949" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1948949/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  Temporarily End the Windows Modules Installer Process

 If you need to perform a task and the Windows Modules Installer Worker process is using up so much CPU that your PC has become unresponsive, you can [temporarily end the process](https://extra-guidance.techidaily.com/updated-professionally-enhancing-photos-with-effective-use-of-3d-lut-filters/). We don't recommend you do this unless you have a really need to. 

 To end the process, right-click the Start Menu icon and select "Task Manager." Open the "Processes" tab, right-click "Windows Modules Installer Worker," and select "End Task."

!['End Task' highlighted for 'Windows Modules Installer Worker' in Task Manager.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2024/01/3-end-windows-modules-installer-worker-process.jpg) 

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2123509/26400" target="_top" id="2123509">
  <img src="//a.impactradius-go.com/display-ad/26400-2123509" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2123509/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  Clear Windows Update Cache and Pause Updates

 If you want to prevent Windows Modules Installer Worker from running, clear your Windows Update cache and pause the updates. This way, the process won’t have updates to install and won’t be able to check for new updates. 

 We don’t recommend pausing updates as newer updates often bring bug fixes and security patches that improve and safeguard your system.

 To start, open a Run window by pressing Windows+R, then type the following in the box and press Enter:

services.msc

 Find the service named "Windows Update." Right-click it and select "Stop."

!['Stop' highlighted for 'Windows Update' on the 'Services' window.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2024/01/4-stop-windows-update-service.jpg) 

 Open Run again by pressing Windows+R, type the following path in the box, and press Enter:

C:\Windows\SoftwareDistribution\

 Select all files in the folder by pressing Ctrl+A, then right-click a selected file and choose "Delete" (a trash can icon on Windows 11). Make sure to [empty the Recycle Bin](https://some-guidance.techidaily.com/new-the-complete-powerdirector-2024-users-handbook/) as well.

!['Delete' highlighted for Windows Update cache.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2024/01/5-delete-windows-update-cache.jpg) 

 Now that your update cache is deleted, pause the updates. [On Windows 11](https://iphone-unlock.techidaily.com/complete-fixes-to-solve-apple-iphone-14-randomly-asking-for-apple-id-password-drfone-by-drfone-ios/), navigate to Settings > Windows Update. On the right pane, next to "Pause Updates," click the drop-down menu and choose how long to pause the updates.

!['Pause Updates' highlighted in Windows 11 Settings.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2024/01/6-pause-updates-windows-11.jpg) 

[On Windows 10](https://instagram-video-recordings.techidaily.com/climbing-the-social-ladder-6-precise-methods-for-gaining-instagram-verification/), go to Settings > Update & Security > Windows Update. On the right pane, click "Advanced Options." In the "Pause Updates" section, click the "Pause Until" drop-down menu and select a time duration.

!['Pause Until' highlighted in Windows 10 Settings.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2024/01/7-pause-updates-windows-10.jpg) 

<!-- affiliate ads begin -->
<a href="https://unicoeye.pxf.io/c/5597632/2134492/18498" target="_top" id="2134492">
  <img src="//a.impactradius-go.com/display-ad/18498-2134492" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://unicoeye.pxf.io/i/5597632/2134492/18498" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

<!-- affiliate ads begin -->
<a href="https://imp.i357552.net/c/5597632/977686/11832" target="_top" id="977686">
  <img src="//a.impactradius-go.com/display-ad/11832-977686" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://imp.i357552.net/i/5597632/977686/11832" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  Run Computer Maintenance at Your Specified Time

 Windows Modules Installer Worker runs when your PC is performing a maintenance task. Luckily, you can [change when the system runs those tasks](https://twitter-videos.techidaily.com/new-2024-approved-tweeting-with-videos-a-quick-tutorial/), allowing you to prevent the process from running when you’re working on important tasks.

 To make that change, open the Start Menu and find "Security and Maintenance". Click it to open it. Then, expand the "Maintenance" section and choose "Change Maintenance Settings."

!['Change Maintenance Settings' highlighted in Control Panel.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2024/01/8-change-windows-maintenance-settings.jpg) 

 Select the "Run Maintenance Tasks Daily at" drop-down menu and select when you want your PC to run the maintenance tasks. This should be when you aren’t working on important tasks on your PC. Then, select "OK."

!['Run Maintenance Tasks Daily at' and 'OK' highlighted on the 'Automatic Maintenance' screen.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2024/01/9-modify-windows-maintenance-time.jpg) 

 And that’s all there is to eliminating or reducing Windows Modules Installer Worker’s CPU usage on a Windows computer. It isn't the only process related to Windows Updates that can cause problems, though. There are other [troubleshooting steps you can try if Windows Update is stuck](https://extra-guidance.techidaily.com/2024-approved-smoothing-out-the-rough-edges-in-photo-booth-videos/).

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
<li><a href="https://youtube-data.techidaily.com/024-approved-ignite-engagement-how-to-employ-youtubes-featured-channel-spotlighting-strategies/"><u>[New] 2024 Approved Ignite Engagement How to Employ YouTube’s Featured Channel Spotlighting Strategies</u></a></li>
<li><a href="https://fox-info.techidaily.com/updated-in-2024-full-spectrum-visual-creativity-with-vsco/"><u>[Updated] In 2024, Full Spectrum Visual Creativity with VSCO</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/2024-approved-advanced-tips-for-sending-fb-videos-via-whatsapp/"><u>2024 Approved Advanced Tips for Sending FB Videos via WhatsApp</u></a></li>
<li><a href="https://common-error.techidaily.com/a-developers-handbook-on-fixing-opengl-glexttexturecompression-format-issue-error-1281-a-complete-solution/"><u>A Developer's Handbook on Fixing OpenGL GL_EXT_texture_compression Format Issue (Error 1281): A Complete Solution</u></a></li>
<li><a href="https://some-tips.techidaily.com/convert-swf-animations-to-gif-format-at-no-cost-using-an-online-tool-movavis-solution/"><u>Convert SWF Animations to GIF Format at No Cost Using an Online Tool: Movavi's Solution</u></a></li>
<li><a href="https://some-tips.techidaily.com/convertir-archivo-swf-a-formato-de-video-mpeg-online-sin-coste/"><u>Convertir Archivo SWF a Formato De Video MPEG Online Sin Coste</u></a></li>
<li><a href="https://some-tips.techidaily.com/facil-conversao-de-arquivos-raw-para-dng-gratuita-on-line-pela-inteira-com-suporte-tecnico-pelo-movavi/"><u>Fácil Conversão De Arquivos RAW Para DNG Gratuita On-Line Pela Inteira Com Suporte Técnico Pelo Movavi</u></a></li>
<li><a href="https://pokemon-go-android.techidaily.com/in-2024-catch-or-beat-sleeping-snorlax-on-pokemon-go-for-honor-v-purse-drfone-by-drfone-virtual-android/"><u>In 2024, Catch or Beat Sleeping Snorlax on Pokemon Go For Honor V Purse | Dr.fone</u></a></li>
<li><a href="https://android-transfer.techidaily.com/in-2024-how-to-transfer-videos-from-oppo-reno-8t-to-ipad-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>In 2024, How to Transfer Videos from Oppo Reno 8T to iPad | Dr.fone</u></a></li>
<li><a href="https://android-transfer.techidaily.com/in-2024-how-to-use-phone-clone-to-migrate-your-nokia-g310-data-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>In 2024, How to Use Phone Clone to Migrate Your Nokia G310 Data? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/movavi-product-distribution-and-returns-policy-comprehensive-guide/"><u>Movavi Product Distribution & Returns Policy - Comprehensive Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/movavis-fraktoppsett-og-tilbakevendende-vilje-mastering-your-pension-rights/"><u>Movavis Fraktoppsett Og Tilbakevendende Vilje - Mastering Your Pension Rights</u></a></li>
<li><a href="https://some-tips.techidaily.com/online-archiving-made-easy-and-free-convert-arw-images-to-png-with-movavis-conversion-tools/"><u>Online Archiving Made Easy & Free: Convert ARW Images to PNG with Movavi's Conversion Tools</u></a></li>
<li><a href="https://some-tips.techidaily.com/passaggio-rapido-e-gratuito-da-webm-a-mp4-il-processo-di-conversione-facile-con-onlineconvmp4/"><u>Passaggio Rapido E Gratuito Da WebM a MP4: Il Processo Di Conversione Facile Con OnlineConvMP4</u></a></li>
<li><a href="https://graphic-issues.techidaily.com/resolving-win11-dark-display-post-fall-update/"><u>Resolving Win11 Dark Display Post-Fall Update</u></a></li>
</ul></div>

