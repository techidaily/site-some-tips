---
title: Easily Find and Manage GPG Keys for Secure Email Communication in Thunderbird - Expert Tips & Tricks
date: 2024-09-17 15:39:13
updated: 2024-09-20 12:41:51
tags:
  - work-life
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/3e91ba41f0b1f5144af732b7aaa7aa673410b605/2020/04/07/e12cf506-15c6-430e-aab3-e957e9d50e53/lighting1.jpg?width=278&height=156&fit=crop&auto=webp
---

## Easily Find and Manage GPG Keys for Secure Email Communication in Thunderbird - Expert Tips & Tricks

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

##  How to locate a user's GPG key in Thunderbird 

Let me show you the way. 

##  Requirements 

The only thing you'll need is a running instance of [Thunderbird](https://www.thunderbird.net/) and an email from the recipient in question. I'll demonstrate with Thunderbird version 102.5.0 on [Pop!\_OS Linux](https://www.zdnet.com/article/pop-os-might-have-a-complicated-name-but-it-makes-using-linux-so-easy/) but the process is the same, no matter the operating system you are using. 

**Also:**[**You're definitely not making the post of your password manager**](https://www.zdnet.com/article/youre-definitely-not-making-the-most-of-your-password-manager/) 

 If you're using an older version of Thunderbird, I suggest you upgrade to the latest version, so you gain the advantage of new features and (more important) all the security patches that have been applied. 

That's all you need. Let's make this happen. 

## 1\. Open Thunderbird and choose an email

The first thing you must do is open Thunderbird and locate an email from the recipient whose public GPG key you wish to add so you can send them encrypted emails.

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
