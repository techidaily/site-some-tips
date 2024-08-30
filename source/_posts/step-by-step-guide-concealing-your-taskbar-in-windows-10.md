---
title: "Step-by-Step Guide: Concealing Your Taskbar in Windows 10"
date: 2024-08-29T19:30:15.165Z
updated: 2024-08-30T19:30:15.165Z
tags:
  - deals
categories:
  - tech
thumbnail: https://thmb.techidaily.com/0ca2747bace885998e167d601fb15c3166c8be683eacac54f4c7c14302087724.jpg
---

## Step-by-Step Guide: Concealing Your Taskbar in Windows 10

### Quick Links

* [Automatically Hide the Taskbar in Settings](https://screen-video-capture.techidaily.com/new-2024-approved-capturing-every-moment-with-switch-hd-tech/)
* [Automatically Hide the Taskbar Using Command Prompt](https://instagram-videos.techidaily.com/updated-in-2024-achieve-flawless-video-for-instagram-perfection/)
* [Hide Taskbar with a PowerShell Command](https://some-techniques.techidaily.com/updated-excellence-in-video-selecting-peak-frame-rates-for-slow-motion-effects/)

### Key Takeaways

* You can save screen space by automatically hiding the taskbar on Windows 10.
* To hide the taskbar, right-click empty space on your desktop, then go to Personalization > Taskbar, and enable the toggle next to "Automatically Hide."
* Alternatively, you can use the Command Prompt or PowerShell to toggle the auto-hide option.

 The [Windows taskbar](https://remote-screen-capture.techidaily.com/updated-your-essential-guide-to-unmissable-gaming-adventures-for-2024/) is great for quickly accessing frequently used applications on your computer. However, some users prefer to hide it in order to save screen space. Here's how to hide the taskbar on Windows 10.

<!-- affiliate ads begin -->
<a href="https://secure.2checkout.com/order/checkout.php?PRODS=40085955&QTY=1&AFFILIATE=108875&CART=1"><img src="https://secure.avangate.com/images/merchant/f702defbc67edb455949f46babab0c18/products/2_logo9.png" border="0">FX PRO (Gold Robot + Silver Robot(Basic Package))</a>
<!-- affiliate ads end -->
##  Automatically Hide the Taskbar in Settings

 To automatically hide your taskbar, right-click anywhere on your PC's desktop and select "Personalize" from the pop-up menu.

![Right-click empty space on your desktop, then select 'Personalize.'](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/right-click-personalize.png) 

<!-- affiliate ads begin -->
<a href="https://shop.manycam.com/order/checkout.php?PRODS=17729331&QTY=1&AFFILIATE=108875&CART=1"><img src="https://secure.avangate.com/images/merchant/8230bea7d54bcdf99cdfe85cb07313d5/mcaffbanner600x500.png" border="0"></a>
<!-- affiliate ads end -->
 The "Settings" window will appear. In the left-hand pane, select "Taskbar." From here, toggle the slider to "On" under "Automatically Hide The Taskbar In Desktop Mode." If your PC is able to switch over to tablet mode, you can hide the taskbar by toggling that option to "On," as well.

![Select the 'Taskbar' tab, then enable 'Automatically hide the taskbar in desktop mode' and 'automatically hide the taskbar in tablet mode.'](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/taskbar-settings.png) 

 You can also right-click the taskbar and select "Taskbar Settings" to access the same Settings window, if you prefer that.

![Right-click the taskbar, then select 'Taskbar Settings.'](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/taskbar-settings-on-taskbar.png) 

<!-- affiliate ads begin -->
<a href="https://getlyla.pxf.io/c/5597632/1455723/15391" target="_top" id="1455723"><img src="//a.impactradius-go.com/display-ad/15391-1455723" border="0" alt="" width="336" height="280"/></a><img height="0" width="0" src="https://imp.pxf.io/i/5597632/1455723/15391" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->
 Your taskbar will now automatically hide. This means that, unless you get a notification from an app in the taskbar or you hover your mouse over where the taskbar should be, it won't show up.

**![GIF showing the taskbar auto hiding](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2020/06/GIF-showing-the-taskbar-auto-hiding.gif)** 

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2087394/7443" target="_top" id="2087394"><img src="//a.impactradius-go.com/display-ad/7443-2087394" border="0" alt="" width="1200" height="600"/></a><img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2087394/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->
 You can undo these settings by toggling the sliders back to the "Off" position.

##  Automatically Hide the Taskbar Using Command Prompt

 If you're feeling like a hacker, you can also toggle the auto-hide option between on and off by running [commands using the Command Prompt](https://some-knowledge.techidaily.com/how-to-leverage-slug-lines-in-articles-for-2024/).

 First, [open the Command Prompt](https://android-frp.techidaily.com/in-2024-step-by-step-tutorial-how-to-bypass-oppo-a78-frp-by-drfone-android/) by typing "command prompt" in the Windows Search bar and then select the "Command Prompt" app from the search results.

![Search 'command prompt' in the Start menu search, then open the result.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/run-command-prompt.png) 

<!-- affiliate ads begin -->
<a href="https://lightailing.sjv.io/c/5597632/1638364/17190" target="_top" id="1638364"><img src="//a.impactradius-go.com/display-ad/17190-1638364" border="0" alt="" width="1280" height="720"/></a><img height="0" width="0" src="https://imp.pxf.io/i/5597632/1638364/17190" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->
 In Command Prompt, run this command to toggle the taskbar automatically hide option to on:

powershell -command "&{$p='HKCU:SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\StuckRects3';$v=(Get-ItemProperty -Path $p).Settings;$v[8]=3;&Set-ItemProperty -Path $p -Name Settings -Value $v;&Stop-Process -f -ProcessName explorer}"

![toggle autohide option to on from command prompt](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2020/06/toggle-autohide-option-to-on-from-command-prompt.png) 

<!-- affiliate ads begin -->
<a href="https://unicoeye.pxf.io/c/5597632/2084399/18498" target="_top" id="2084399"><img src="//a.impactradius-go.com/display-ad/18498-2084399" border="0" alt="" width="1125" height="600"/></a><img height="0" width="0" src="https://imp.pxf.io/i/5597632/2084399/18498" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->
 And to toggle the taskbar auto-hide option to off, run this command:

powershell -command "&{$p='HKCU:SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\StuckRects3';$v=(Get-ItemProperty -Path $p).Settings;$v[8]=2;&Set-ItemProperty -Path $p -Name Settings -Value $v;&Stop-Process -f -ProcessName explorer}"

![toggle autohide option to off from command prompt](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2020/06/toggle-autohide-option-to-off-from-command-prompt.png) 

##  Hide Taskbar with a PowerShell Command

 You may have noticed that the command we used in Command Prompt actually invoked PowerShell first. You can skip the middleman and just run it with PowerShell directly, if you want.

 Search for "PowerShell" in the Start menu search, then launch it. It doesn't need to be run as administrator, but it won't hurt anything if you do.

![Search for 'powershell' in the Start menu search bar, then click "Open' or 'Run as Administrator.'](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/launch-powershell.png) 

 To auto-hide your taskbar, copy and paste the following command into PowerShell:

$p='HKCU:SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\StuckRects3';$v=(Get-ItemProperty -Path $p).Settings;$v[8]=3;&Set-ItemProperty -Path $p -Name Settings -Value $v;&Stop-Process -f -ProcessName explorer

![The command to auto-hide the taskbar in PowerShell.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/powershell-command.png) 

 If you want to re-enable your taskbar, you need to change "$v\[8\]=3" to "$v\[8\]=2" instead. Your complete command will look like this:

$p='HKCU:SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\StuckRects3';$v=(Get-ItemProperty -Path $p).Settings;$v[8]=2;&Set-ItemProperty -Path $p -Name Settings -Value $v;&Stop-Process -f -ProcessName explorer

![Re-enable the taskbar through PowerShell.](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/12/reenable.png) 

 If you just don't like how the taskbar looks, you may want to try [customizing the taskbar](https://remote-screen-capture.techidaily.com/updated-your-essential-guide-to-unmissable-gaming-adventures-for-2024/) instead of hiding it. There are even third-party apps, like [Start11](https://www.stardock.com/products/start11/), that give you even more granular control.

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
<li><a href="https://desktop-recording.techidaily.com/new-2024-approved-farmers-fantasy-top-10-game-simulations-unveiled/"><u>[New] 2024 Approved  Farmers' Fantasy  Top 10 Game Simulations Unveiled</u></a></li>
<li><a href="https://facebook-video-recording.techidaily.com/new-in-2024-digital-delights-8-most-watched-movies/"><u>[New] In 2024, Digital Delights  8 Most Watched Movies</u></a></li>
<li><a href="https://instagram-video-files.techidaily.com/new-in-2024-photoharmony-android-and-ios-instagram-collages/"><u>[New] In 2024, PhotoHarmony  Android & iOS Instagram Collages</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/new-in-2024-showcasing-iconic-ae-templates-for-social-media/"><u>[New] In 2024, Showcasing Iconic AE Templates for Social Media</u></a></li>
<li><a href="https://youtube-docs.techidaily.com/n-2024-the-backward-button-chronicles-youtubes-video-reversal/"><u>[New] In 2024, The Backward Button Chronicles  YouTube's Video Reversal</u></a></li>
<li><a href="https://digital-screen-recording.techidaily.com/new-sonic-and-the-hedgehog-switch-edition-top-10/"><u>[New] Sonic and the Hedgehog  Switch Edition (Top 10)</u></a></li>
<li><a href="https://some-guidance.techidaily.com/new-top-online-tips-creating-title-magic/"><u>[New] Top Online Tips  Creating Title Magic</u></a></li>
<li><a href="https://video-screen-grab.techidaily.com/updated-prime-racing-game-selection-top-five/"><u>[Updated] Prime Racing Game Selection  Top Five</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyy-erweitert-das-ipa-okosystem-durch-das-neue-globale-one-partner-programm-einbindung-und-zusammenarbeit-fur-verbesserte-prozessautomatisierung/"><u>ABBYY Erweitert Das IPA-Ökosystem Durch Das Neue, Globale One Partner Programm: Einbindung Und Zusammenarbeit Für Verbesserte Prozessautomatisierung</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyy-integration-launches-at-electionzcom-for-enhanced-data-processing/"><u>ABBYY Integration Launches at Electionz.com for Enhanced Data Processing</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyy-maintains-top-spot-in-the-smart-automation-industry/"><u>ABBYY Maintains Top Spot in the Smart Automation Industry</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyys-technological-mastery-skyrocketing-profits-with-a-60-increase-endorsed-by-the-esteemed-idc-marketscape-analysis/"><u>ABBYY's Technological Mastery: Skyrocketing Profits with a 60%% Increase, Endorsed by the Esteemed IDC MarketScape Analysis</u></a></li>
<li><a href="https://some-tips.techidaily.com/1724312832646-abbyy/"><u>ABBYYが清水智人氏を日本企業界の最前線指導者として紹介</u></a></li>
<li><a href="https://some-tips.techidaily.com/automated-traffic-management-with-cookiebot-technology/"><u>Automated Traffic Management with Cookiebot Technology</u></a></li>
<li><a href="https://some-tips.techidaily.com/automated-with-cookiebot-streamlining-your-websites-data-collection/"><u>Automated with Cookiebot: Streamlining Your Website's Data Collection</u></a></li>
<li><a href="https://tech-haven.techidaily.com/custom-ai-solutions-at-your-fingertips-introducing-openais-gpt-store-for-immediate-use/"><u>Custom AI Solutions at Your Fingertips – Introducing OpenAI’s GPT Store for Immediate Use</u></a></li>
<li><a href="https://android-location.techidaily.com/easy-ways-to-manage-your-oneplus-nord-ce-3-5g-location-settings-drfone-by-drfone-virtual/"><u>Easy Ways to Manage Your OnePlus Nord CE 3 5G Location Settings | Dr.fone</u></a></li>
<li><a href="https://change-location.techidaily.com/how-to-use-snapchat-location-spoofer-to-protect-your-privacy-on-apple-iphone-7-plus-drfone-by-drfone-virtual-ios/"><u>How to use Snapchat Location Spoofer to Protect Your Privacy On Apple iPhone 7 Plus? | Dr.fone</u></a></li>
<li><a href="https://android-location.techidaily.com/in-2024-for-people-wanting-to-mock-gps-on-tecno-camon-20-pro-5g-devices-drfone-by-drfone-virtual/"><u>In 2024, For People Wanting to Mock GPS on Tecno Camon 20 Pro 5G Devices | Dr.fone</u></a></li>
<li><a href="https://some-guidance.techidaily.com/in-2024-tech-triad-analysis-unraveling-the-vr-ar-mr-tapestry/"><u>In 2024, Tech Triad Analysis  Unraveling the VR-AR-MR Tapestry</u></a></li>
<li><a href="https://android-location-track.techidaily.com/in-2024-top-6-appsservices-to-trace-any-vivo-y100a-location-by-mobile-number-drfone-by-drfone-virtual-android/"><u>In 2024, Top 6 Apps/Services to Trace Any Vivo Y100A Location By Mobile Number | Dr.fone</u></a></li>
<li><a href="https://graphic-issues.techidaily.com/introducing-the-enhanced-windows-11-geforce-210-driver/"><u>Introducing the Enhanced Windows 11 GeForce 210 Driver</u></a></li>
<li><a href="https://some-tips.techidaily.com/leverage-advanced-traffic-insights-the-power-of-cookiebot-technology-on-websites/"><u>Leverage Advanced Traffic Insights: The Power of Cookiebot Technology on Websites</u></a></li>
<li><a href="https://some-tips.techidaily.com/leveraging-abbyys-text-recognition-vw-explores-enhanced-infotainment-tech/"><u>Leveraging ABBYY's Text Recognition: VW Explores Enhanced Infotainment Tech</u></a></li>
<li><a href="https://some-tips.techidaily.com/leveraging-cookiebot-technology-for-advanced-website-insights-and-customized-content/"><u>Leveraging Cookiebot Technology for Advanced Website Insights and Customized Content</u></a></li>
<li><a href="https://some-tips.techidaily.com/mastering-mental-clarity-tips-on-quieting-phones-organizing-thoughts-and-reflective-introspection-from-the-abbyy-experts/"><u>Mastering Mental Clarity: Tips on Quieting Phones, Organizing Thoughts, and Reflective Introspection From the ABBYY Experts</u></a></li>
<li><a href="https://tech-hub.techidaily.com/mastering-mindfulness-against-stress-using-chatgpt-tools/"><u>Mastering Mindfulness Against Stress Using ChatGPT Tools</u></a></li>
<li><a href="https://some-tips.techidaily.com/navigating-the-marketplace-strategies-from-the-abbyy-ai-hub/"><u>Navigating the Marketplace: Strategies From the ABBYY AI Hub</u></a></li>
<li><a href="https://some-tips.techidaily.com/navigating-through-artificial-intelligence-myths-key-takeaways-from-the-latest-abbyy-ai-summit/"><u>Navigating Through Artificial Intelligence Myths: Key Takeaways From the Latest ABBYY AI Summit</u></a></li>
<li><a href="https://some-tips.techidaily.com/optimize-with-cookiebot-technology-the-key-to-customized-user-experience-and-seo-success/"><u>Optimize with Cookiebot Technology: The Key to Customized User Experience and SEO Success</u></a></li>
<li><a href="https://some-tips.techidaily.com/professionelle-verbesserung-mit-hilfe-digitaler-zwillingsmodelle-fur-ihr-unternehmen/"><u>Professionelle Verbesserung Mit Hilfe Digitaler Zwillingsmodelle Für Ihr Unternehmen</u></a></li>
<li><a href="https://extra-tips.techidaily.com/ps5xbox-series-x-elite-console-companion-screens/"><u>PS5/Xbox Series X  Elite Console Companion Screens</u></a></li>
<li><a href="https://some-tips.techidaily.com/revamping-your-know-your-customer-approach-with-the-latest-techniques-insights-from-abbyy/"><u>Revamping Your Know-Your-Customer Approach with the Latest Techniques - Insights From ABBYY</u></a></li>
<li><a href="https://hardware-help.techidaily.com/revolutionary-maxsun-mini-itx-board-unique-rear-gpu-mounting-design/"><u>Revolutionary MaxSun Mini-ITX Board: Unique Rear GPU Mounting Design</u></a></li>
<li><a href="https://tech-recovery.techidaily.com/scholars-secret-navigating-how-to-secure-a-tidal-student-offer/"><u>Scholar's Secret: Navigating How to Secure a Tidal Student Offer</u></a></li>
<li><a href="https://some-tips.techidaily.com/strategies-to-enhance-page-ranking-and-web-traffic-through-seo-techniques/"><u>Strategies to Enhance Page Ranking and Web Traffic Through SEO Techniques</u></a></li>
<li><a href="https://some-tips.techidaily.com/streamline-legal-processes-using-abbyys-innovative-contract-analysis-platform/"><u>Streamline Legal Processes Using ABBYY's Innovative Contract Analysis Platform</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-evolution-of-trade-finance-adaptive-strategies-for-emerging-obstacles-and-opportunities/"><u>The Evolution of Trade Finance: Adaptive Strategies for Emerging Obstacles and Opportunities</u></a></li>
<li><a href="https://some-tips.techidaily.com/unleashing-the-power-of-ai-the-key-to-unlocking-iot-potential-insights-from-abbyy/"><u>Unleashing the Power of AI: The Key to Unlocking IoT Potential - Insights From ABBYY</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-significant-savings-with-abbyy-discover-the-story-of-a-6m-windfall-for-a-leading-finance-firm/"><u>Unlocking Significant Savings with ABBYY: Discover the Story of a $6M Windfall for a Leading Finance Firm</u></a></li>
<li><a href="https://win-able.techidaily.com/world-of-warcraft-performance-tweaks-and-fixes-expert-advice-for-eliminating-lag-and-improving-frame-rate/"><u>World of Warcraft Performance Tweaks & Fixes: Expert Advice for Eliminating Lag and Improving Frame Rate !</u></a></li>
</ul></div>
