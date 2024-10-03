---
title: "Discovering Your Contacts' GPG Keys with Mozilla Thunderbird: A Step-by-Step Guide"
date: 2024-10-02T16:34:51.023Z
updated: 2024-10-03T16:21:31.749Z
tags:
  - work-life
categories:
  - tech
thumbnail: https://thmb.techidaily.com/18d989e548104708bf52f53d39fea00818139641241145ab7026454dd288c9b9.jpg
---

## Discovering Your Contacts' GPG Keys with Mozilla Thunderbird: A Step-by-Step Guide

![Smiling woman using laptop](https://www.zdnet.com/a/img/resize/427fd66cbb89652915ab2b69ecd99f6680359bf3/2020/04/07/e12cf506-15c6-430e-aab3-e957e9d50e53/lighting1.jpg?auto=webp&width=1280)

iStockphoto/Getty Images

Back in October, I wrote a piece about [using encrypted email in Thunderbird](https://www.zdnet.com/article/how-to-encrypt-email-in-thunderbird-and-why-you-should/). If you ever have to send sensitive information via email, you should be using encryption. If you're not encrypting those missives, the information they contain can be read by a third party. 

### More how-tos

* [How to download YouTube videos for free, plus two other methods](https://www.zdnet.com/article/how-to-download-youtube-videos-for-free-plus-two-other-methods/)
* [Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how](https://www.zdnet.com/article/wi-fi-problems-how-to-add-a-wired-network-to-your-home-without-ethernet-cable/)
* [Wiping a Windows laptop? Here's the safest free way to erase your personal data](https://www.zdnet.com/article/wiping-a-windows-laptop-heres-the-safest-free-way-to-erase-your-personal-data/)
* [How to connect a PS4 controller to a smartphone](https://www.zdnet.com/article/how-to-connect-a-ps4-controller-to-a-smartphone/)

You don't want that… especially when it comes to personal or professional [information that you don't want falling into the wrong hands](https://www.zdnet.com/article/online-security-101-how-to-protect-your-privacy-from-hackers-spies-and-the-government/). 

One of the complexities of using encryption in Thunderbird (or most email clients) is that you have to track down the recipient's public GPG key and add it to the client. Without that key, you can't send encrypted emails to the owner of the key, thereby rendering GPG useless. 

There are ways you can get the recipient's public key. You can have them send it to you, and you will then have to manually add it to your keyring. You can download it from a public GPG key server through the software that manages your keyring. 

**Also:** [**How to add 'Do Not Track' to Thunderbird (and why you should)**](https://www.zdnet.com/home-and-office/work-life/how-to-add-do-not-track-to-thunderbird-and-why-you-should/)

Fortunately, there's another way that's sort of hidden from sight. This less-than-obvious method is much easier than the other two options, so I highly recommend you try these simple steps first. 

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1918703/19272" target="_top" id="1918703">
  <img src="//a.impactradius-go.com/display-ad/19272-1918703" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1918703/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  How to locate a user's GPG key in Thunderbird 

Let me show you the way. 

##  Requirements 

The only thing you'll need is a running instance of [Thunderbird](https://www.thunderbird.net/) and an email from the recipient in question. I'll demonstrate with Thunderbird version 102.5.0 on [Pop!\_OS Linux](https://www.zdnet.com/article/pop-os-might-have-a-complicated-name-but-it-makes-using-linux-so-easy/) but the process is the same, no matter the operating system you are using. 

**Also:**[**You're definitely not making the post of your password manager**](https://www.zdnet.com/article/youre-definitely-not-making-the-most-of-your-password-manager/) 

 If you're using an older version of Thunderbird, I suggest you upgrade to the latest version, so you gain the advantage of new features and (more important) all the security patches that have been applied. 

That's all you need. Let's make this happen. 

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2087234/19272" target="_top" id="2087234">
  <img src="//a.impactradius-go.com/display-ad/19272-2087234" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2087234/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## 1\. Open Thunderbird and choose an email

The first thing you must do is open Thunderbird and locate an email from the recipient whose public GPG key you wish to add so you can send them encrypted emails.

<!-- affiliate ads begin -->
<span id="1155462">
					<video width="1024" height="576" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1155462.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/14559-1155462">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1155462.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:640px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fpropmoneyinc.pxf.io%2Fc%2F5597632%2F1155462%2F14559'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1155462/14559" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

## 2\. Open the email from the recipient

Open the email from the recipient by clicking on the entry in Thunderbird's top right pane.

## 3\. Access the context menu

In the reading pane (bottom right), right-click the email address in the From field, and then click Discover OpenPGP Key.

Downloading a recipient GPG key is actually much easier than you might think.

Jack Wallen/ZDNET

## 4\. Accept the key

In the resulting window, click Accepted and then click Import. A second pop-up will appear, including the details of the key that was successfully imported. 

**Also:** [**How to create message filters in Thunderbird to keep your inbox organized**](https://www.zdnet.com/article/how-to-create-message-filters-in-thunderbird-to-keep-your-inbox-organized/)

Close out that pop-up by clicking OK and you're done. 

Accepting a GPG from a recipient's email address.

Jack Wallen/ZDNET

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135352/19272" target="_top" id="2135352">
  <img src="//a.impactradius-go.com/display-ad/19272-2135352" border="0" alt="https://techidaily.com" width="160" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135352/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  Encryption enabled 

Now that you've imported the recipient's GPG key, you can encrypt any emails you send them. You can refer back to the post I cited earlier to find out exactly [how to encrypt those emails](https://www.zdnet.com/article/how-to-encrypt-email-in-thunderbird-and-why-you-should/), but it's essentially a matter of composing an email to the recipient that belongs to the key you just imported and then clicking the Encrypt button in the composer window. Email encryption has never been so easy. 

#### Open Source

[5 Linux commands you must know to keep your device running smoothly](https://www.zdnet.com/article/5-linux-commands-you-must-know-to-keep-your-device-running-smoothly/ "5 Linux commands you must know to keep your device running smoothly")

[The best Linux laptops you can buy: Expert tested](https://www.zdnet.com/article/best-linux-laptop/ "The best Linux laptops you can buy: Expert tested")

[The best Linux distros for beginners](https://www.zdnet.com/article/best-linux-desktops-for-beginners/ "The best Linux distros for beginners")

[My 5 favorite Linux text editors (and why you should be using one)](https://www.zdnet.com/article/my-favorite-linux-text-editors-and-why-you-should-be-using-one/ "My 5 favorite Linux text editors (and why you should be using one)")

* [5 Linux commands you must know to keep your device running smoothly](https://www.zdnet.com/article/5-linux-commands-you-must-know-to-keep-your-device-running-smoothly/ "5 Linux commands you must know to keep your device running smoothly")
* [The best Linux laptops you can buy: Expert tested](https://www.zdnet.com/article/best-linux-laptop/ "The best Linux laptops you can buy: Expert tested")
* [The best Linux distros for beginners](https://www.zdnet.com/article/best-linux-desktops-for-beginners/ "The best Linux distros for beginners")
* [My 5 favorite Linux text editors (and why you should be using one)](https://www.zdnet.com/article/my-favorite-linux-text-editors-and-why-you-should-be-using-one/ "My 5 favorite Linux text editors (and why you should be using one)")

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
<li><a href="https://youtube-sure.techidaily.com/024-approved-tips-to-perfectly-integrate-jump-cuts-into-videos/"><u>[New] 2024 Approved Tips to Perfectly Integrate Jump Cuts Into Videos</u></a></li>
<li><a href="https://vimeo-videos.techidaily.com/new-in-2024-optimizing-livestream-videos-on-twitch/"><u>[New] In 2024, Optimizing Livestream Videos on Twitch</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-best-value-in-cloud-pricing-a-comprehensive-list/"><u>[New] The Best Value in Cloud Pricing A Comprehensive List</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-professionals-blueprint-for-investing-in-high-definition-viewing/"><u>[New] The Professional's Blueprint for Investing in High-Definition Viewing</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-ultimate-guide-from-tweet-vids-to-mp3-audio-files/"><u>[New] The Ultimate Guide From Tweet Vids to MP3 Audio Files</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-top-windows-10-tips-for-maximum-productivity/"><u>[New] Top Windows 10 Tips For Maximum Productivity</u></a></li>
<li><a href="https://facebook-video-share.techidaily.com/updated-in-2024-audiovisual-harmony-merging-audio-and-visual-elements-on-youtube/"><u>[Updated] In 2024, Audiovisual Harmony Merging Audio and Visual Elements on YouTube</u></a></li>
<li><a href="https://extra-resources.techidaily.com/updated-top-best-background-erase-software/"><u>[Updated] Top Best Background Erase Software</u></a></li>
<li><a href="https://some-techniques.techidaily.com/find-the-perfect-phone-shot-blur-for-2024/"><u>Find the Perfect Phone Shot Blur for 2024</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/in-2024-how-to-mirror-nokia-g310-to-mac-drfone-by-drfone-android/"><u>In 2024, How to Mirror Nokia G310 to Mac? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unlocking-full-potential-in-depth-review-of-lgs-monitor-tech/"><u>In 2024, Unlocking Full Potential In-Depth Review of LG's Monitor Tech</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unveiling-prospects-and-limitations-within-samsungs-2023-image-editor/"><u>In 2024, Unveiling Prospects and Limitations Within Samsung's 2023 Image Editor</u></a></li>
<li><a href="https://tech-haven.techidaily.com/leveraging-chatgpt-for-enhanced-cognitive-behavioral-therapy-practices/"><u>Leveraging ChatGPT for Enhanced Cognitive Behavioral Therapy Practices</u></a></li>
<li><a href="https://some-tips.techidaily.com/utilizing-zoom-services-directly-from-your-inbox-gmail-edition-for-2024/"><u>Utilizing Zoom Services Directly From Your Inbox - Gmail Edition for 2024</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/what-is-a-sim-network-unlock-pin-get-your-lava-blaze-2-5g-phone-network-ready-by-drfone-android/"><u>What Is a SIM Network Unlock PIN? Get Your Lava Blaze 2 5G Phone Network-Ready</u></a></li>
</ul></div>

