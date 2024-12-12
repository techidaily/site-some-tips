---
title: "Get Your Home Cloud Operational in Just 60 Minutes: Expert Advice & Steps From ZDNet's Latest Article"
date: 2024-12-10T16:11:11.964Z
updated: 2024-12-12T16:34:18.181Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/15c27a9dd37e7d971ec6b1dda7daf6d5203783d6fa46bb3c8b563de8f86481fa.jpg
---

## Get Your Home Cloud Operational in Just 60 Minutes: Expert Advice & Steps From ZDNet's Latest Article

![Woman working on laptop](https://www.zdnet.com/a/img/resize/72bfc9ab1096af889f2d93ddb449d62ed41f4aa9/2023/02/15/f0d278b5-9c54-49ba-b81e-4e008276bbf7/gettyimages-975816152.jpg?auto=webp&width=1280)

Maskot/Getty Images

If you're worried your documents might at some point be used by the likes of Google, Apple, or Microsoft to train their [artificial intelligence](https://www.zdnet.com/article/what-is-ai-heres-everything-you-need-to-know-about-artificial-intelligence/) (AI) models, know that you are not alone. In fact, some people have considered migrating to another cloud provider to deal with this worry. 

If you've grown concerned about the privacy of your content, there's an alternative that's free and brings the power of the cloud to your home network. That option is called [Nextcloud](https://www.nextcloud.com) and it's a powerful solution that can be used in place of Google Drive, iCloud, or OneCloud. And the best news is that you can deploy this cloud service such that it is only accessible from your home network.

**Also:** [**The best Linux laptops for everyone**](https://www.zdnet.com/article/best-linux-laptop/)

To successfully install Nextcloud, you will need an instance of Ubuntu Server -- which is a Linux server -- up and running on your home network. For those who haven't heard of Linux, it's a free operating system you can install on computers (or as [virtual machines](https://www.zdnet.com/article/how-to-create-linux-virtual-machine-with-virtualbox/)) that is more powerful, flexible, reliable, and secure than either [Windows or MacOS](https://www.zdnet.com/article/cool-things-you-can-do-with-the-linux-desktop-that-you-cant-do-with-macos-or-windows/). 

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

You might either not know about Linux or believe it to be too challenging for your skills. But installing and running Linux involves much less effort than you might think. And as I recently wrote in an opinion piece, there's some important reasons why you should be [using Linux at home](https://www.zdnet.com/article/the-most-important-reason-you-should-be-using-linux-at-home/). 

**Also:** [**Ubuntu Cinnamon makes switching from Windows to Linux as painless as possible**](https://www.zdnet.com/article/ubuntu-cinnamon-is-for-users-who-prefer-the-familiarity-of-the-windows-desktop-but-with-the-freedom-of-open-source/)

In the end, the use of Linux at home is all about keeping your data safe from third-party services and having the ability to expand the applications, services, and tools available to you -- without having to break the bank or get a degree in computer science.

What's more, [Linux is everywhere](https://www.zdnet.com/article/8-things-you-can-do-with-linux-that-you-cant-do-with-macos-or-windows/). Not only does it run on computers, but also on IoT devices, smart devices, appliances, automobiles, and more.

In this series on making use of Linux at home, I now want to show you how to install the [Nextcloud](https://nextcloud.com/) on-premises cloud host. Think of it as your own Google Workspace, complete with documents, storage, calendar, email, and more. 

**Also:** [**How to replace Windows with Linux Mint on your PC**](https://www.zdnet.com/article/how-to-replace-windows-with-linux-mint-on-your-pc/)

It should come as no surprise given the title of this piece that there's a very easy way to install this cloud platform -- and I'm going to show you how it's done.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/LaGNHfAT92w?si=bvHo1iYK2JBIPtRo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## How to install a cloud service at home: It's easy

**What you'll need:** As mentioned above, you'll need an instance of Ubuntu Server up and running on your home network to successfully install Nextcloud. Fear not, as I've already explained [how you can install this system in under 30 minutes](https://www.zdnet.com/article/how-to-install-ubuntu-server-in-less-than-30-minutes/). With that server running, you'll need a user with sudo privileges (which you create during the operating system installation).

That's it. Let's do this.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/2En1CHbiYwA?si=jZKzTr9EIT2ShjGK" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## 1\. Log in to Ubuntu Server

The first thing is to log in to your Ubuntu Server instance, which will land you at the terminal window.

## 2\. Install Nextcloud with snap

To install Nextcloud, issue the command:

sudo snap install nextcloud

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/FLlUft1ZxI0?si=pBd5QdHEE27qsNlN" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## 3\. Find the IP address of your server

The Nextcloud command line installation should go off without a hitch and finish in less than a minute. 

**Also:** [**How to change your IP address with a VPN (and why you should)**](https://www.zdnet.com/article/how-to-change-your-ip-address-why-youd-want-to-and-when-you-shouldnt/) 

When that finishes, you'll need to first know the IP address of your server with the command:

ip a

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/1dR4tF3VgyU?si=AJipgqZsNNxsRsBW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## 4\. Access the web installer

Open a web browser and point it to http://SERVER (where SERVER is the IP address of your Ubuntu server).

## 5\. Create an admin user

In the resulting window of your web browser, type a new username and password to be used as an admin user.

Creating an admin user is the first step in the web GUI.

Screenshot by Jack Wallen/ZDNET

## 6\. Install recommended apps

In the resulting window, click Install Recommended Apps to add the Calendar, Contacts, Mail, Nextcloud Office, and Talk apps (you can add more later). This installation will take a bit more time (less than five minutes). 

**Also:** [**This official Ubuntu Spin might just be the perfect intro to Linux**](https://www.zdnet.com/article/this-official-ubuntu-spin-might-be-just-be-the-perfect-intro-to-linux/)

Allow the installation to complete and you'll be presented with the Nextcloud Hub, where you can access all of the pre-installed apps and start using your in-house cloud service.

I would go with the recommendations.

Screenshot by Jack Wallen/ZDNET

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/5FWCFI3f_cs?si=Kt2Onr_E4c616tbH" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## Next steps with Nextcloud

After the installation is complete, you can start using Nextcloud. 

However, I would suggest you at least [configure the email server settings](https://www.zdnet.com/home-and-office/work-life/how-to-add-an-email-account-to-your-onlyoffice-deployment/), so you'll be able to share and collaborate on files. To configure the email server, you'll first need to have an SMTP server. You can always use the Google SMTP server; the settings you'll need are:

* SMTP server: smtp.gmail.com
* Port: 465
* From email address: Your Gmail address
* Password: Your Gmail password (or app password, if you use two-factor Authentication with Gmail)

To configure the SMTP server, click your Nextcloud profile icon at the top right of the window and, from the dropdown, click Administration Settings. From the left sidebar, click Basic Settings, and then in the resulting window, scroll down until you see the Email Server section. Fill in the options as outlined above and click Save. With that process complete, click Send Email to make sure everything is working. 

Adding an SMTP server to Nextcloud.

Screenshot by Jack Wallen/ZDNET

Once you've taken care of the SMTP server settings, click the Mail icon at the top of the window. When prompted, fill out the necessary information for your email account, and click Connect.

Adding an email account in Nextcloud.

Screenshot by Jack Wallen/ZDNET

With this stage complete, your Nextcloud instance can do just about anything your other cloud services can offer… all while remaining within your home network. 

Even with the installation of Ubuntu Server, you should be able to complete this process in well under an hour. Believe me when I tell you, the time invested will be worth it.

#### See also

[How to replace Windows with Linux Mint on your PC](https://www.zdnet.com/article/how-to-replace-windows-with-linux-mint-on-your-pc/ "How to replace Windows with Linux Mint on your PC")

[5 best Linux commands for troubleshooting problems (and how I use them)](https://www.zdnet.com/article/5-best-linux-commands-for-troubleshooting-problems-and-how-i-use-them/ "5 best Linux commands for troubleshooting problems (and how I use them)")

[5 reasons why Pop!\_OS is this Linux pro's favorite distro](https://www.zdnet.com/article/5-reasons-why-pop-os-is-this-linux-pros-favorite-distro/ "5 reasons why Pop!_OS is this Linux pro's favorite distro")

[5 best open-source email clients for Linux (and why Geary is my go-to)](https://www.zdnet.com/article/5-best-open-source-email-clients-for-linux-and-why-geary-is-my-go-to/ "5 best open-source email clients for Linux (and why Geary is my go-to)")

* [How to replace Windows with Linux Mint on your PC](https://www.zdnet.com/article/how-to-replace-windows-with-linux-mint-on-your-pc/ "How to replace Windows with Linux Mint on your PC")
* [5 best Linux commands for troubleshooting problems (and how I use them)](https://www.zdnet.com/article/5-best-linux-commands-for-troubleshooting-problems-and-how-i-use-them/ "5 best Linux commands for troubleshooting problems (and how I use them)")
* [5 reasons why Pop!\_OS is this Linux pro's favorite distro](https://www.zdnet.com/article/5-reasons-why-pop-os-is-this-linux-pros-favorite-distro/ "5 reasons why Pop!_OS is this Linux pro's favorite distro")
* [5 best open-source email clients for Linux (and why Geary is my go-to)](https://www.zdnet.com/article/5-best-open-source-email-clients-for-linux-and-why-geary-is-my-go-to/ "5 best open-source email clients for Linux (and why Geary is my go-to)")

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
<li><a href="https://fox-glue.techidaily.com/new-2024-approved-secrets-unveiled-successful-podcast-on-apple-store/"><u>[New] 2024 Approved Secrets Unveiled Successful Podcast on Apple Store</u></a></li>
<li><a href="https://facebook-videos.techidaily.com/new-2024-approved-unleash-power-in-social-media-10-advanced-tactics-for-fb-optimization/"><u>[New] 2024 Approved Unleash Power in Social Media 10 Advanced Tactics for FB Optimization</u></a></li>
<li><a href="https://article-helps.techidaily.com/new-2024-approved-unravel-your-pcs-potential-with-windows-10s-latest-games/"><u>[New] 2024 Approved Unravel Your PC's Potential with Windows 10'S Latest Games</u></a></li>
<li><a href="https://youtube-webster.techidaily.com/n-2024-strategies-for-deleting-watch-later-items-on-youtube/"><u>[New] In 2024, Strategies for Deleting Watch Later Items on YouTube</u></a></li>
<li><a href="https://youtube-data.techidaily.com/ed-overcome-artificial-watches-for-natural-views-for-2024/"><u>[Updated] Overcome Artificial Watches for Natural Views for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/mp4ogvmovavi/"><u>無料で使えるMP4に簡単変換!動画形式OGVをMovaviでオンライン変更する方法</u></a></li>
<li><a href="https://novels-ebooks.techidaily.com/210174967-9781646546282-archangel-michael-breathes/"><u>Archangel Michael Breathes | Free Book</u></a></li>
<li><a href="https://some-tips.techidaily.com/convertir-videos-3gp-a-formatos-avanzados-online-sin-coste-soluciones-de-movavi/"><u>Convertir Videos 3GP a Formatos Avanzados Online Sin Coste: Soluciones De Movavi</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/crafting-engaging-podcasts-step-by-step-guide-with-free-examples/"><u>Crafting Engaging Podcasts Step-by-Step Guide with Free Examples</u></a></li>
<li><a href="https://android-location.techidaily.com/easy-ways-to-manage-your-poco-x5-location-settings-drfone-by-drfone-virtual/"><u>Easy Ways to Manage Your Poco X5 Location Settings | Dr.fone</u></a></li>
<li><a href="https://fake-location.techidaily.com/how-can-i-use-a-fake-gps-without-mock-location-on-xiaomi-redmi-note-12-pro-4g-drfone-by-drfone-virtual-android/"><u>How Can I Use a Fake GPS Without Mock Location On Xiaomi Redmi Note 12 Pro 4G? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/misez-vous-sur-loption-de-conversion-wma-a-ogg-en-ligne-gratuit-chez-movavi-une-solution-simple-et-rapide/"><u>Misez-Vous Sur L'option De Conversion WMA À Ogg en Ligne Gratuit Chez Movavi : Une Solution Simple Et Rapide</u></a></li>
<li><a href="https://some-tips.techidaily.com/movavi-video-editeur-dachat-transactions-protegees-en-gros-et-soldes-inedits/"><u>Movavi Vidéo Éditeur D'Achat - Transactions Protegées en Gros Et Soldes Inédits</u></a></li>
<li><a href="https://some-tips.techidaily.com/os-14-melhores-tradutores-de-audiomensagem-livres-que-voce-precisa-conhecer-hoje/"><u>Os 14 Melhores Tradutores De Audiomensagem Livres Que Você Precisa Conhecer Hoje</u></a></li>
<li><a href="https://some-tips.techidaily.com/quick-and-easy-guide-to-crafting-beautiful-iphone-collages-discover-the-most-effective-methods/"><u>Quick & Easy Guide to Crafting Beautiful iPhone Collages: Discover the Most Effective Methods!</u></a></li>
<li><a href="https://some-tips.techidaily.com/switch-your-videos-from-mp4-to-asf-seamlessly-get-started-now-no-cost-involved/"><u>Switch Your Videos From MP4 to ASF Seamlessly - Get Started Now, No Cost Involved!</u></a></li>
<li><a href="https://some-tips.techidaily.com/wav-wma-movavi/"><u>온라인 제공: WAV-WMA 변환은 세금 지불 없이 가능하며, Movavi로!</u></a></li>
</ul></div>

