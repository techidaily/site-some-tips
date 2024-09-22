---
title: New Breakthrough in StarlingX Edge Technology Announced – Discover the Power of the Upgrade | ZDNet Insights
date: 2024-09-18 10:32:54
updated: 2024-09-20 10:24:47
tags:
  - edge-computing
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/edge-computing/    https://www.zdnet.com/a/img/resize/72be91e981ff57b2ebad7a55c1762f5aa2a63c98/2021/11/19/f1c1e2cb-df25-4ef1-bf2e-76a7087ef5c1/edge-computing.png?width=170&height=128&fit=crop&format=pjpg&auto=webp
---

## New Breakthrough in StarlingX Edge Technology Announced – Discover the Power of the Upgrade | ZDNet Insights

![Bright arrows moving forward towards blue screens.](https://www.zdnet.com/a/img/resize/671d44eb10868c4e95d9d7fe8c95e82b32ef2df3/2021/11/19/f1c1e2cb-df25-4ef1-bf2e-76a7087ef5c1/edge-computing.png?auto=webp&width=1280)

metamorworks/Shutterstock

When [Gartner](https://www.gartner.com/en) recently looked into its crystal ball, [it saw](https://www.equinix.com/resources/analyst-reports/gartner-distributed-enterprise-predictions-2022?ls=Advertising%20-%20Web&lsd=22q1%5Fenterprise%5Fdigital-infrastructure--not-applicable%5F/resources/analyst-reports/gartner-distributed-enterprise-predictions-2022%5Fdm%5Fobility%5Fpaid-search%5Fgoogle%5Fus-en%5FAMER%5Fdigital-edge%5Fdemand-gen&utm%5Fcampaign=us-en%5Fgoogle%5Fpaid-search%5Fdigital-edge%5Fdm&utm%5Fsource=google&utm%5Fmedium=paid-search&utm%5Fcontent=digital-infrastructure--not-applicable%5Fgartner-distributed-enterprise-predictions-2022&gclid=CjwKCAjwyaWZBhBGEiwACslQo1AGTjhNzGVtdMvA2aB17%5FaXR24lcHFSGMewfbYLWpLwzsH6Mult0BoCfQ0QAvD%5FBwE), "By 2025, more than 50% of enterprise-managed data will be created and processed outside the data center or cloud." So where will it be then? It will be on [edge computing](https://www.zdnet.com/topic/edge-computing/), and chances are excellent that you'll be using the newest version of [StarlingX](https://www.starlingx.io/), [StarlingX 7.0](https://docs.starlingx.io/specs/specs/stx-7.0/index.html), the open-source edge computing and IoT cloud platform there.

**Also:** [Google is exiting the IoT business. Microsoft is doing the opposite](https://www.zdnet.com/article/google-is-exiting-the-iot-services-business-microsoft-is-doing-the-opposite/) 

### Cloud

* [​What is digital transformation? Everything you need to know](https://www.zdnet.com/article/what-is-digital-transformation-everything-you-need-to-know-about-how-technology-is-reshaping/)
* [The best cloud providers compared: AWS, Azure, Google Cloud, and more](https://www.zdnet.com/article/the-top-cloud-providers-of-2021-aws-microsoft-azure-google-cloud-hybrid-saas/)
* [The top 6 cheap web hosting services: Find an affordable option](https://www.zdnet.com/article/best-cheap-web-hosting/)
* [What is cloud computing? Here's everything you need to know](https://www.zdnet.com/article/what-is-cloud-computing-everything-you-need-to-know-about-the-cloud/)

Why? Because rather than trying to reinvent the wheel, the [OpenInfra Foundation's](https://openinfra.dev/) StarlingX uses best-of-breed open-source programs to deliver a complete edge computing stack. This starts with Ceph. This Red Hat-sponsored do-it-all, open-source software-defined storage platform can work with object-level, block-level, and file-level storage. For cloud management, it uses the tried and true OpenStack. And, for container orchestration, StarlingX uses, of course, Kubernetes.

It comes as no surprise then that StarlingX is used in industrial Internet of Things (IoT), telecom, video delivery, and so on. In short, if you need ultra-low latency and all the resources a full cloud stack can bring you, StarlingX is probably for you. Such Telecom companies as Docomo, NTT, Verizon, and Vodafone are already using it for their 5G deployments.

Ildikó Váncsa, OpenInfra's Senior Manager for Community & Ecosystem, added in a statement that more is to come. While what it brings to the table is great for 5G Open Radio Access Network (RAN), its characteristics also make "StarlingX the ideal platform for innovations like autonomous vehicles, smart cities, augmented reality, manufacturing, drone delivery, and remote healthcare to become reality."

The biggest single change is that StarlingX no longer uses [CentOS](https://www.centos.org/) for its base operating system. Instead, it now uses [Debian](https://www.debian.org/). Specifically, the latest [Debian Stable Release, Bullseye.](https://www.debian.org/releases/bullseye/) The [developers moved to Debian](https://docs.starlingx.io/specs/specs/stx-6.0/approved/starlingx%5F2008704%5Fdebian%5Ftransition.html) because they didn't want to rely on a commercial Linux distro. They felt burned by Red Hat's decision to turn CentOS into an upstream of [Red Hat Enterprise Linux (RHEL)](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux). Debian, on the other hand, appeared more stable and had a robust community that already supports core StarlingX open-source programs such as Kubernetes, Ceph, and OpenStack.

**Also:** [CentOS Linux lives on in the AlmaLinux 9](https://www.zdnet.com/article/old-style-centos-linux-lives-on-in-the-new-almalinux-9/)

That said, StarlingX 7,0 does come with prebuilt CentOS, Debian, and Docker images. It also now uses [Kubernetes 1.23](https://kubernetes.io/blog/2021/12/07/kubernetes-1-23-release-announcement/), the December 2021 release, by default.

To help StarlingX live up to its potential, the new StarlingX 7.0 key features include:

* **Improved scalability**: The more sub-clouds StarlingX's Distributed Cloud architecture can manage, the larger you can grow your edge infrastructure, StarlingX 7.0 can handle up to 1,000 sub-clouds.
* **Greater network speed**: StarlingX 7.0 now uses [Istio service mesh](https://istio.io/latest/about/service-mesh/) to speed up Kubernetes' observability, traffic management, security, and policy management functions.
* **Enhanced security**: It now enables you to log commands using the popular representational state transfer (REST) Application Programming Interface (API) to Kubernetes. This enables you to spot suspicious activity and block it before it can cause trouble.
* **Enhanced security II**: It has also replaced Kubernetes Pod Security Policies (PSP) with Pod Security Admission Controller. This is a more efficient and reliable way to enforce pod security standards.

Check out the [StarlingX 7.0 release notes](https://docs.starlingx.io/releasenotes/r7-0-release-notes-85446867da2a.html) for more details about these and other features.

If you see [Edge Computing](https://www.zdnet.com/article/edge-computing-is-coming-and-businesses-arent-ready/) in your company's future, you should look into StarlingX. When Arpit Joshipura, the Linux Foundation's general manager of networking, said in 2019 that [edge computing would overtake cloud computing by 2025](https://www.zdnet.com/article/linux-foundation-executive-believes-edge-computing-will-be-more-important-than-cloud-computing/), it looks like he was right. And, by using best-of-best-of-breed open-source software to create a complete stack, your developers will find it much easier to build solid, Edge Computing applications and services. 

#### Featured

[The fastest VPNs: Expert tested and reviewed](https://www.zdnet.com/article/fastest-vpn/ "The fastest VPNs: Expert tested and reviewed")

[Google Pixel 9 Pro XL vs. Samsung Galaxy S24 Ultra: I tested both and here are the key differences](https://www.zdnet.com/article/google-pixel-9-pro-xl-vs-samsung-galaxy-s24-ultra/ "Google Pixel 9 Pro XL vs. Samsung Galaxy S24 Ultra: I tested both and here are the key differences")

[How to upgrade your 'incompatible' Windows 10 PC to Windows 11](https://www.zdnet.com/article/how-to-upgrade-your-incompatible-windows-10-pc-to-windows-11/ "How to upgrade your 'incompatible' Windows 10 PC to Windows 11")

[Your Android phone is getting an anti-theft upgrade, thanks to AI. How it works](https://www.zdnet.com/article/your-android-phone-is-getting-an-anti-theft-upgrade-thanks-to-ai-how-it-works/ "Your Android phone is getting an anti-theft upgrade, thanks to AI. How it works")

* [The fastest VPNs: Expert tested and reviewed](https://www.zdnet.com/article/fastest-vpn/ "The fastest VPNs: Expert tested and reviewed")
* [Google Pixel 9 Pro XL vs. Samsung Galaxy S24 Ultra: I tested both and here are the key differences](https://www.zdnet.com/article/google-pixel-9-pro-xl-vs-samsung-galaxy-s24-ultra/ "Google Pixel 9 Pro XL vs. Samsung Galaxy S24 Ultra: I tested both and here are the key differences")
* [How to upgrade your 'incompatible' Windows 10 PC to Windows 11](https://www.zdnet.com/article/how-to-upgrade-your-incompatible-windows-10-pc-to-windows-11/ "How to upgrade your 'incompatible' Windows 10 PC to Windows 11")
* [Your Android phone is getting an anti-theft upgrade, thanks to AI. How it works](https://www.zdnet.com/article/your-android-phone-is-getting-an-anti-theft-upgrade-thanks-to-ai-how-it-works/ "Your Android phone is getting an anti-theft upgrade, thanks to AI. How it works")

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
