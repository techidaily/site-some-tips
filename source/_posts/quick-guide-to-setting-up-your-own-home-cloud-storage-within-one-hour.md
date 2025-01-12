---
title: Quick Guide to Setting Up Your Own Home Cloud Storage Within One Hour
date: 2025-01-09T18:02:48.373Z
updated: 2025-01-12T21:22:23.523Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/5e0529876851ece32f2686c17564f6aeaaddc32a/2023/02/15/f0d278b5-9c54-49ba-b81e-4e008276bbf7/gettyimages-975816152.jpg?width=278&height=156&fit=crop&auto=webp
---

## Quick Guide to Setting Up Your Own Home Cloud Storage Within One Hour

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
<iframe width="560" height="315" src="https://www.youtube.com/embed/mMYEK2gtY5c?si=ytxNz_JHZkTrwb4b" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## How to install a cloud service at home: It's easy

**What you'll need:** As mentioned above, you'll need an instance of Ubuntu Server up and running on your home network to successfully install Nextcloud. Fear not, as I've already explained [how you can install this system in under 30 minutes](https://www.zdnet.com/article/how-to-install-ubuntu-server-in-less-than-30-minutes/). With that server running, you'll need a user with sudo privileges (which you create during the operating system installation).

That's it. Let's do this.

## 1\. Log in to Ubuntu Server

The first thing is to log in to your Ubuntu Server instance, which will land you at the terminal window.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/fJlICvacgJY?si=jNeijBVj7ia4ammA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## 2\. Install Nextcloud with snap

To install Nextcloud, issue the command:

sudo snap install nextcloud

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/hXIq2G0nShk?si=5Z4Fwv7ZB6oKWsdd" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## 3\. Find the IP address of your server

The Nextcloud command line installation should go off without a hitch and finish in less than a minute. 

**Also:** [**How to change your IP address with a VPN (and why you should)**](https://www.zdnet.com/article/how-to-change-your-ip-address-why-youd-want-to-and-when-you-shouldnt/) 

When that finishes, you'll need to first know the IP address of your server with the command:

ip a

## 4\. Access the web installer

Open a web browser and point it to http://SERVER (where SERVER is the IP address of your Ubuntu server).

## 5\. Create an admin user

In the resulting window of your web browser, type a new username and password to be used as an admin user.

Creating an admin user is the first step in the web GUI.

Screenshot by Jack Wallen/ZDNET

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/6xGqSETroqA?si=4C1GPgXi-AksR_oO" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## 6\. Install recommended apps

In the resulting window, click Install Recommended Apps to add the Calendar, Contacts, Mail, Nextcloud Office, and Talk apps (you can add more later). This installation will take a bit more time (less than five minutes). 

**Also:** [**This official Ubuntu Spin might just be the perfect intro to Linux**](https://www.zdnet.com/article/this-official-ubuntu-spin-might-be-just-be-the-perfect-intro-to-linux/)

Allow the installation to complete and you'll be presented with the Nextcloud Hub, where you can access all of the pre-installed apps and start using your in-house cloud service.

I would go with the recommendations.

Screenshot by Jack Wallen/ZDNET

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/cC-HtDQVoG0?si=nQcoa7q8q2IL8U0m" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<li><a href="https://fox-access.techidaily.com/updated-the-eye-catching-4k-experience-dell-p2715q-in-focus/"><u>[Updated] The Eye Catching 4K Experience Dell P2715Q in Focus</u></a></li>
<li><a href="https://change-location.techidaily.com/9-mind-blowing-tricks-to-hatch-eggs-in-pokemon-go-without-walking-on-vivo-y36-drfone-by-drfone-virtual-android/"><u>9 Mind-Blowing Tricks to Hatch Eggs in Pokemon Go Without Walking On Vivo Y36 | Dr.fone</u></a></li>
<li><a href="https://win11.techidaily.com/accelerate-windows-tasks-with-top-5-car-drivers/"><u>Accelerate Windows Tasks with Top 5 Car Drivers</u></a></li>
<li><a href="https://change-location.techidaily.com/in-2024-a-detailed-guide-on-faking-your-location-in-mozilla-firefox-on-nokia-xr21-drfone-by-drfone-virtual-android/"><u>In 2024, A Detailed Guide on Faking Your Location in Mozilla Firefox On Nokia XR21 | Dr.fone</u></a></li>
<li><a href="https://unlock-android.techidaily.com/in-2024-how-to-bypass-android-lock-screen-using-emergency-call-on-honor-magic-5-lite-by-drfone-android/"><u>In 2024, How to Bypass Android Lock Screen Using Emergency Call On Honor Magic 5 Lite?</u></a></li>
<li><a href="https://unlock-android.techidaily.com/in-2024-unlocking-the-power-of-smart-lock-a-beginners-guide-for-infinix-note-30-5g-users-by-drfone-android/"><u>In 2024, Unlocking the Power of Smart Lock A Beginners Guide for Infinix Note 30 5G Users</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/the-new-directors-toolkit-15-basic-cinematography-movements/"><u>The New Director’s Toolkit 15 Basic Cinematography Movements</u></a></li>
<li><a href="https://some-approaches.techidaily.com/the-ultimate-marketing-playbook-for-digital-beginners-on-reddit-for-2024/"><u>The Ultimate Marketing Playbook for Digital Beginners on Reddit for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-6-to-do-apps-in-2eplustodo-a-comprehensive-guide/"><u>Top 6 To-Do Apps in 2E+TODO - A Comprehensive Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-strategies-sought-by-executives-securing-elite-technology-professionals-as-revealed-in-insights-from-industry-titans-zdnet/"><u>Top Strategies Sought by Executives: Securing Elite Technology Professionals as Revealed in Insights From Industry Titans - ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/transforming-your-data-management-master-the-art-of-utilizing-google-sheets-inbuilt-table-features-for-effortless-workflows-zdnet/"><u>Transforming Your Data Management: Master the Art of Utilizing Google Sheets' Inbuilt Table Features for Effortless Workflows | ZDNET</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlock-professional-success-how-to-find-and-follow-your-passion-with-five-expert-tips-by-zdnet/"><u>Unlock Professional Success: How to Find and Follow Your Passion with Five Expert Tips by ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-career-growth-top-strategies-from-industry-experts-to-break-boundaries-in-the-office/"><u>Unlocking Career Growth: Top Strategies From Industry Experts to Break Boundaries in the Office</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-employee-potential-key-lessons-from-industry-visionaries-powered-by-zdnet/"><u>Unlocking Employee Potential: Key Lessons From Industry Visionaries | Powered By ZDNet</u></a></li>
</ul></div>

