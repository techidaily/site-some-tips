---
title: Red Hat's Innovation Leap - Launching a Virtualized RHEL Desktop Experience on AWS Platform, as Reported by ZDNet
date: 2024-09-19 18:51:25
updated: 2024-09-20 10:53:28
tags:
  - amazon
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/03566a3f87b111629b9a28e337ee47a251185e4a/2022/10/20/467866e2-61cc-4113-ade9-50a21db41279/rhel-8-6.jpg?width=278&height=156&fit=crop&auto=webp
---

## Red Hat's Innovation Leap - Launching a Virtualized RHEL Desktop Experience on AWS Platform, as Reported by ZDNet

![Red Hat Enterprise Linux 8.6](https://www.zdnet.com/a/img/resize/fb12456a5d670426ec55d43a99276f92de38fae1/2022/10/20/467866e2-61cc-4113-ade9-50a21db41279/rhel-8-6.jpg?auto=webp&width=1280)

Red Hat

Once upon a time, and it wasn't that long ago, "desktops" were terminals to mainframes or midrange computers running Unix. Then along came the PC, and everything changed. That is, until now. Today, Desktop-as-a-Service (DaaS) is making a comeback. And [Red Hat](https://www.redhat.com/en) is joining this trend with the general availability of [Red Hat Enterprise Linux for Workstations](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux/workstations) (RHEL WS) on [Amazon Web Services](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2F%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7Ce11bebd9-9815-4990-8ce3-cf401238218e%7Cdtp&dtb=1), announced Tuesday.

### Cloud

* [​What is digital transformation? Everything you need to know](https://www.zdnet.com/article/what-is-digital-transformation-everything-you-need-to-know-about-how-technology-is-reshaping/)
* [The best cloud providers compared: AWS, Azure, Google Cloud, and more](https://www.zdnet.com/article/the-top-cloud-providers-of-2021-aws-microsoft-azure-google-cloud-hybrid-saas/)
* [The top 6 cheap web hosting services: Find an affordable option](https://www.zdnet.com/article/best-cheap-web-hosting/)
* [What is cloud computing? Here's everything you need to know](https://www.zdnet.com/article/what-is-cloud-computing-everything-you-need-to-know-about-the-cloud/)

It's not the only one. [Canonical](https://canonical.com/), [Ubuntu Linux](https://ubuntu.com/)'s parent company, is now offering its [Ubuntu desktop on AWS](https://www.zdnet.com/article/linux-aws-now-offers-ubuntu-virtual-desktops-for-developers-and-engineers/) as well. And, if you've been watching closely, Microsoft has the same plan. 

Forget about Windows on your PC, Microsoft's plan going forward is to have you subscribe to [Windows 365 Cloud PC](https://www.microsoft.com/en-us/windows-365) or the [Azure Virtual Desktop](https://click.linksynergy.com/deeplink?id=IokOf8qagZo&mid=24542&u1=zd-%5F%5FCOM%5FCLICK%5FID%5F%5F-dtp&murl=https%3A%2F%2Fazure.microsoft.com%2Fen-us%2Fproducts%2Fvirtual-desktop%2F). Microsoft doesn't care if you run "Windows" on a Windows PC, Mac, or old-school Linux desktop such as [Linux Mint](https://www.zdnet.com/article/linux-mint-21-arrives-heres-whats-new/).

The same's true with [Red Hat](https://www.redhat.com/en). The traditional desktop hasn't been a big part of Red Hat's business plans since it made the [switch from Red Hat Linux to RHEL](https://www.eweek.com/servers/why-linux-users-hate-red-hat/) in 2004\. Today, Red Hat will be happy for you to run RHEL WS via either an Amazon-provided [NICE DCV](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2Fhpc%2Fdcv%2F%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7Ce11bebd9-9815-4990-8ce3-cf401238218e%7Cdtp&dtb=1), AWS's high-performance remote display protocol client, or your web browser of choice. 

NICE DCV supports both Windows and Linux remote environments. It's available with native clients for Windows, Linux, and MacOS. These native clients support up to 4K resolution, multiple monitors, and features such as stylus/touch support, USB devices, multichannel audio, smart cards, and file redirection. It can also work, albeit not as well, with any modern web browser. 

So, if you really wanted to run an RHEL WS from, say, your iPad Pro, you could. Whatever platform you use, you'll get a high-end RHEL WS desktop for running power-hungry workloads such as animation rendering or data visualization.

**Also:** [**Want to ditch Windows? Windowsfx may be the ideal Linux distribution for you**](https://www.zdnet.com/article/want-to-ditch-windows-windowsfx-may-be-the-ideal-linux-distribution-for-you/)

This is a long way from when I used to write with vi on a VT-102 terminal attached to an AT&T 3B2 minicomputer. These AWS RHEL WS instances use GPU-accelerated hardware instances to handle graphics-intensive processes. It does this with powerful Amazon EC2 instances, including [G-family accelerated instances](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Fdocs.aws.amazon.com%2FAWSEC2%2Flatest%2FUserGuide%2Finstance-types.html%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7Ce11bebd9-9815-4990-8ce3-cf401238218e%7Cdtp&dtb=1) with [Graviton processors](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2Fec2%2Fgraviton%2F%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7Ce11bebd9-9815-4990-8ce3-cf401238218e%7Cdtp&dtb=1). 

This is far more powerful than traditional DaaS you may have used in the past, such as the Linux-based Chromebooks or Windows-enabled Critix. Red Hat and AWS can pull this off because of NICE DCV, AWS's high-end processors, and the growth of last-mile high-speed Internet. This service is not for anyone still using DSL!

No, this new Red Hat desktop take is meant for remote workers at animation studios, visual effects companies, and industrial design firms, who need workstation power at users' homes. This is a work-from-home offering for 21st-century high-end users. On this new platform, you'll have the same access to the full RHEL software suite and independent software vendor (ISV) applications. 

Want to give it a try? It's available today via the AWS Marketplace with support for both RHEL WS 8.6 [GRID](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2Fmarketplace%2Fpp%2Fprodview-lacci2zzxcd7e%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7Ce11bebd9-9815-4990-8ce3-cf401238218e%7Cdtp&dtb=1) and [Tesla](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2Fmarketplace%2Fpp%2Fprodview-npe75yf66owc4%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7Ce11bebd9-9815-4990-8ce3-cf401238218e%7Cdtp&dtb=1) drivers. With either instance, you're looking at an average price of 56.4 cents per hour. 

**Related stories:**

* [Red Hat Enterprise Linux 8.6: Better security, more options](https://www.zdnet.com/article/red-hat-enterprise-linux-8-6-better-security-more-options/)
* [Here come the new Red Hat Enterprise Linux distros](https://www.zdnet.com/article/here-come-the-new-red-hat-enterprise-linux-distros/)
* [Linux: AWS now offers Ubuntu virtual desktops for developers and engineers](https://www.zdnet.com/article/linux-aws-now-offers-ubuntu-virtual-desktops-for-developers-and-engineers/)

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
