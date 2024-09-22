---
title: "Unveiling Red Hat's Enhanced Enterprise Linux: Innovative Tools for Simplifying Hybrid Cloud Management | ZDNet"
date: 2024-09-17 10:11:56
updated: 2024-09-20 11:41:17
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/c375ce1878aec11dc45365bef1d03270965b9669f431a9e083c40be8add6302b.jpg
---

## Unveiling Red Hat's Enhanced Enterprise Linux: Innovative Tools for Simplifying Hybrid Cloud Management | ZDNet

![cloud-mazegettyimages-1171421825](https://www.zdnet.com/a/img/resize/cb36fb09c4e7e534856866a1a557e6c69faadb84/2024/05/01/6776e7a2-4c2b-4500-9420-1f76751ce165/cloud-mazegettyimages-1171421825.jpg?auto=webp&width=1280)

gremlin/Getty Images

Some people update to the latest version of an operating system as soon as it's available. Others hang on to their old operating system until it's covered in cobwebs and dust. [Red Hat](https://www.redhat.com/en) lets you do both. The Linux and hyper-cloud leader today released its newest flagship Linux distro, [Red Hat Enterprise Linux (RHEL) 9.4](https://developers.redhat.com/articles/2024/05/01/whats-new-red-hat-enterprise-linux-94), after last week announcing [four more years of support for the popular, decade-old RHEL 7.9](https://www.redhat.com/en/blog/announcing-4-years-extended-life-cycle-support-els-red-hat-enterprise-linux-7).

**Also: [Ubuntu 24.04: This great new Linux distro isn't just fast - it's a fortress](https://www.zdnet.com/article/ubuntu-24-04-this-great-new-linux-distro-isnt-just-fast-its-a-fortress/)**

Don't expect to see this kind of extended life for other RHEL versions. Unlike [Canonical](https://canonical.com/), which has given 12 years of support to all [long-term support (LTS) versions of Ubuntu](https://opensourcewatch.beehiiv.com/p/canonical-unveils-12-years-support-ubuntu-lts), Red Hat is giving RHEL 7 [Extended Life Cycle Support (ELS)](https://www.redhat.com/en/resources/els-datasheet) \-- a one-time, additional four years of support. This means that instead of RHEL 7.9 leaving support on June 30, 2024, you can now get maintenance support with security patches and bug fixes for RHEL 7.9 until June 30, 2028.

Of course, what Red Hat _really_ wants you to do is upgrade to a newer version of RHEL -- say, RHEL 9.4\. This latest version of the leading enterprise Linux distro introduces a host of new features designed to simplify the management of hybrid cloud environments.

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

As RHEL VP and general manager Gunnar Hellekson says, "Linux is no longer just about the kernel or the command line. It's about making the platform more accessible, manageable, and responsive, especially as technology organizations scale across the hybrid cloud. Whether exploring the potential of AI workloads or simply trying to optimize existing resources, the latest release of RHEL helps limit complexity and improve efficiency while making the most of existing skills and tools."

Specifically, RHEL 9.4 enhances capabilities in management and automation and provides proactive support for the construction of standard operating environments (SOEs) for distributed systems.

**Also: [If all kernel bugs are security bugs, how do you keep your Linux safe?](https://www.zdnet.com/article/if-all-kernel-bugs-are-security-bugs-how-do-you-keep-your-linux-safe/)**

In part, SOEs are driven by deployment-ready [Ansible](https://www.ansible.com/) [DevOps](https://www.zdnet.com/article/what-is-devops-an-executive-guide-to-agile-development-and-it-operations/) content collections that help configure and launch common administrative tasks. These roles-related capabilities include:

* System roles at the edge through [rpm-ostree](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree/) enable users to automate operating system-level tasks at the edge, such as [Podman](https://podman.io/), for deploying product-ready container workloads.
* A [fapolicyd](https://access.redhat.com/documentation/en-us/red%5Fhat%5Fenterprise%5Flinux/8/html/security%5Fhardening/assembly%5Fblocking-and-allowing-applications-using-fapolicyd%5Fsecurity-hardening) system role automates allowing or denying application executions at scale. This reduces the potential for human error when things go wrong.
* A snapshot system role for administrators to create and manage point-in-time snapshots of logical volume manager (LVM) storage volumes. This helps speed up backup and recovery solutions in a more repeatable and predictable manner at scale.
* A bootloader system role helps configure the kernel command line itself. This improves the consistency and management of Linux systems at scale.

If you manage clouds for a living, you may wonder what plans Red Hat has for combining Ansible DevOps with [Infrastructure as Code (IaC)](https://thenewstack.io/infrastructure-as-code-the-ultimate-guide/) [Terraform](https://www.terraform.io/) after [IBM finished acquiring its parent company, HashiCorp](https://devops.com/ibm-confirms-its-buying-hashicorp/). Red Hat isn't answering yet. (Yes, I asked.) The potential is certainly there for a powerful one-two DevOps/IaC punch.

In the meantime, [Red Hat Insights](https://www.redhat.com/en/technologies/management/insights) updates, including the [Insights image builder](https://access.redhat.com/documentation/en-us/red%5Fhat%5Fenterprise%5Flinux/8/html-single/creating%5Fcustomized%5Fimages%5Fby%5Fusing%5Finsights%5Fimage%5Fbuilder/index), will make it easier to create ready-to-run RHEL SOEs. The tool will soon offer proactive guidance, recommend additional relevant packages, and highlight crucial lifecycle information to aid system administrators and operations teams in managing upgrades and system longevity.

**Also: [This could be the best Linux distro of the year (and it's not even close)](https://www.zdnet.com/article/this-could-be-the-best-linux-distro-of-the-year-and-its-not-even-close/)**

The Red Hat Hybrid Cloud Console's virtual assistant now aids you in creating custom images for specific cloud platforms. Additionally, automation integration continues to deepen, with new RHEL system roles that streamline tasks such as application execution policies, snapshot management, and system boot configurations. These tools are designed to reduce human error and enhance operational efficiency at scale.

RHEL 9.4 has also improved its security stance. With its [zero trust architecture (ZTA)](https://www.redhat.com/en/topics/security/what-is-zero-trust) security model, RHEL passkey authentication enables passwordless and multifactor authentication (MFA) with [FIDO2 (Fast IDentity Online 2)](https://fidoalliance.org/fido2/) compliant passkeys for centrally managed users. You can also configure [WireGuard](https://access.redhat.com/documentation/en-us/red%5Fhat%5Fenterprise%5Flinux/9/html/configuring%5Fand%5Fmanaging%5Fnetworking/assembly%5Fsetting-up-a-wireguard-vpn%5Fconfiguring-and-managing-networking) \-- the high-performance, Linux kernel VPN -- via the RHEL web console to further improve system security.

Developers will be happy to see new [Application Streams](https://www.redhat.com/en/blog/introduction-appstreams-and-modules-red-hat-enterprise-linux) with Python 3.12 PostgreSQL 16, Ruby 3.3, MariaDB 10, LLVM 17, Rust 1.75, and Go 1.21\. In short, today's latest language and DBMS releases will be at your fingertips. 

**Also: [5 reasons why desktop Linux is finally growing in popularity](https://www.zdnet.com/article/5-reasons-why-desktop-linux-is-finally-growing-in-popularity/)**

With RHEL 9.4's general availability, Red Hat is also expanding its support for diverse hardware architectures, including full support for ARM. This move ensures that Red Hat's solutions are as flexible as the hybrid environments they are intended to support, accommodating a wide variety of server platforms.

Are you ready to move to something new? RHEL 9.4 is now available to existing customers through the Red Hat Customer Portal. Give it a look. I certainly will.

#### Linux

[The best Linux laptops for consumers and developers](https://www.zdnet.com/article/best-linux-laptop/ "The best Linux laptops for consumers and developers")

[Want to save your aging computer? Try these 5 Linux distributions](https://www.zdnet.com/article/want-to-save-your-old-computer-try-these-5-linux-distributions/ "Want to save your aging computer? Try these 5 Linux distributions")

[The best distros for beginners](https://www.zdnet.com/article/best-linux-desktops-for-beginners/ "The best distros for beginners")

[How to enable Linux on your Chromebook (and why you should)](https://www.zdnet.com/article/how-to-enable-linux-on-your-chromebook-and-why-you-should/ "How to enable Linux on your Chromebook (and why you should)")

* [The best Linux laptops for consumers and developers](https://www.zdnet.com/article/best-linux-laptop/ "The best Linux laptops for consumers and developers")
* [Want to save your aging computer? Try these 5 Linux distributions](https://www.zdnet.com/article/want-to-save-your-old-computer-try-these-5-linux-distributions/ "Want to save your aging computer? Try these 5 Linux distributions")
* [The best distros for beginners](https://www.zdnet.com/article/best-linux-desktops-for-beginners/ "The best distros for beginners")
* [How to enable Linux on your Chromebook (and why you should)](https://www.zdnet.com/article/how-to-enable-linux-on-your-chromebook-and-why-you-should/ "How to enable Linux on your Chromebook (and why you should)")

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
