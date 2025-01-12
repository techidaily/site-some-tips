---
title: "Securing Containers Permanently: The Ultimate Guide Using Rust-Powered Edera - Insights From ZDNet"
date: 2025-01-09T19:12:11.789Z
updated: 2025-01-12T18:19:38.183Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/db339cfb71ad17e704275f446976657b74bdf593b2c3464a856c74dd3bbe549b.jpg
---

## Securing Containers Permanently: The Ultimate Guide Using Rust-Powered Edera - Insights From ZDNet

![containers](https://www.zdnet.com/a/img/resize/adf862e9818fa209479e4692e51d04e2bbb755bc/2024/04/11/98da400c-8f12-4bcd-89a5-9b99d6fcef01/gettyimages-94985760.jpg?auto=webp&width=1280)

Paul Taylor/Getty Images

One of the ultimate cloud security nightmares is when someone breaks through your container runtime into its underlying operating system. With attacks such as [Leaky Vessels](https://snyk.io/blog/cve-2024-21626-runc-process-cwd-container-breakout/), a hacker can wreak havoc on your programs, smash other containerized applications, and grant the attacker root user-level privileges. In short, it's all over for your security. To prevent such attacks, Edera is taking an old program into a new language to provide a memory-safe container runtime. 

Written in Rust, [Edera](https://github.com/edera-dev/) is built on the foundation of the classic open-source [type-1, bare-metal Virtual Machine hypervisor](https://www.networkworld.com/article/944300/why-you-want-a-bare-metal-hypervisor-and-how-to-choose.html), [Xen](https://xenproject.org/). This hypervisor was selected, as Edera Chief Innovation Officer and [Alpine Linux](https://www.alpinelinux.org/) maintainer Ariadne Conill, explained, because, unlike [KVM](https://linux-kvm.org/page/Main%5FPage), which runs inside the Linux kernel, it's a dedicated type-1 hypervisor. These are inherently more secure than the popular type-2 hypervisors. 

**Also: [The best VPN services: Expert tested and reviewed](https://www.zdnet.com/article/best-vpn/)**

If you're a techie, you may think that's true, but aren't hypervisors of both types all about virtual machines (VM), not containers? That's correct, but the Edera team has taken the hypervisor design and shifted it over to containers. As Emily Long, Edera's CEO, said, "Hypervisors haven't been reimagined for nearly two decades and just don't work in the cloud-native world." The Edera developers are building a true 21st-century hypervisor. 

The foundation of the new program is [Krata](https://github.com/edera-dev/krata). This is a Xen-based, single-host hypervisor built for [Open Container Initiative (OCI)](https://opencontainers.org/)\-compliant containers. It isolates containers with a fully memory-safe Rust control plane to bring Xen tooling into a new, secure era. In addition, Edera uses Lukko, an open-source memory safety runtime library. This library detects memory safety violations at runtime and cleanly terminates programs before they can be exploited.

Edera is secure by design. It's the only independent solution that offers isolation at the container level, making container escapes impossible, no matter where you run your infrastructure: a hyper cloud, a local cloud, or your own servers. 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/odDOPrPjRYY?si=7QHzdUkTPNkHJiVj" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## Edera's key features

**Isolation**

* Type 1 hypervisor runs on bare metal with no shared kernel state between containers.
* Hardened security guarantees with no container escapes.
* Trusted and untrusted workloads run in the same cluster with zero risk.

**Memory Safety**

* Coded in Rust, ensuring complete memory safety.
* The principle of least authority limits the attack surface.

**Secure Memory Encryption**

* Unilateral data transfer between confidential containers.
* Memory encryption between guests creating highly secure enclaves.

Additionally, the finished Edera Protect will include a suite of advanced features, such as an enterprise control plane, multi-cluster management, and guided memory safety violation remediation. These features will be complemented by out-of-the-box Kubernetes compatibility and premium support services.

Eventually, Edera will also enable customers to deploy a mix of workload types in their clusters instead of having different clusters for legacy virtualization and containers. It will also support distributing traditional VM images in the same way containers are distributed, providing a more consistent developer experience when working with both containers and traditional VMs. 

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

Edera's founding team, composed of Conill, Long, and Alex Zenla, CTO, is an all-women team. This is a departure from the usual tech bro technology development leadership norm. Their combined expertise spans engineering leadership, software security, product innovation, and executive management. They have a shared vision of building a more inclusive, empowering, and secure technological future.

The time is right for Edera. With companies needing more secure containers thanks to the increasing complexity of container orchestration and Kubernetes security vulnerabilities, Edera presents a secure-by-design approach that addresses these challenges. Indeed, the company's unique approach, leveraging Rust's memory safety capabilities and modern hypervisor technology, may render many existing security tools obsolete by providing robust isolation at the container level.

**Also: [Google survey: 63% of IT and security pros believe AI will improve corporate cybersecurity](https://www.zdnet.com/article/ai-should-improve-corporate-cybersecurity-google-and-csa-survey-finds/)**

Anyone can contribute to Krata today, and Lukko is set for an initial release on May 1, 2024\. The founders will shortly be starting their first fundraising round and are excited to start that process. 

I'm excited to see what they do going forward. This really is a new, innovative approach to container security, and it could well be a game changer for cloud-native computing.

#### Featured

[Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how](https://www.zdnet.com/article/wi-fi-problems-how-to-add-a-wired-network-to-your-home-without-ethernet-cable/ "Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how")

[The best smart rings you can buy: Expert tested](https://www.zdnet.com/article/best-smart-ring/ "The best smart rings you can buy: Expert tested")

[One of the best budget tablets I've tested replaced both my Kindle and iPad](https://www.zdnet.com/article/one-of-the-best-budget-tablets-ive-tested-replaced-bot-my-kindle-and-ipad/ "One of the best budget tablets I've tested replaced both my Kindle and iPad")

[Wiping a Windows laptop? Here's the safest free way to erase your personal data](https://www.zdnet.com/article/wiping-a-windows-laptop-heres-the-safest-free-way-to-erase-your-personal-data/ "Wiping a Windows laptop? Here's the safest free way to erase your personal data")

* [Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how](https://www.zdnet.com/article/wi-fi-problems-how-to-add-a-wired-network-to-your-home-without-ethernet-cable/ "Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how")
* [The best smart rings you can buy: Expert tested](https://www.zdnet.com/article/best-smart-ring/ "The best smart rings you can buy: Expert tested")
* [One of the best budget tablets I've tested replaced both my Kindle and iPad](https://www.zdnet.com/article/one-of-the-best-budget-tablets-ive-tested-replaced-bot-my-kindle-and-ipad/ "One of the best budget tablets I've tested replaced both my Kindle and iPad")
* [Wiping a Windows laptop? Here's the safest free way to erase your personal data](https://www.zdnet.com/article/wiping-a-windows-laptop-heres-the-safest-free-way-to-erase-your-personal-data/ "Wiping a Windows laptop? Here's the safest free way to erase your personal data")

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
<li><a href="https://eaxpv-info.techidaily.com/new-2024-approved-frame-by-frame-building-a-filmmaking-foundation-on-youtube/"><u>[New] 2024 Approved Frame by Frame Building a Filmmaking Foundation on YouTube</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/new-in-2024-best-tools-for-crafting-memorable-instagram-reels-top-6/"><u>[New] In 2024, Best Tools for Crafting Memorable Instagram Reels (Top 6)</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/new-windows-11-auto-hdr-how-to-turn-on-windows-11-auto-hdr-for-2024/"><u>[New] Windows 11 Auto HDR How to Turn on Windows 11 Auto HDR for 2024</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/updated-step-by-step-guide-turn-off-spotifys-recommended-listings/"><u>[Updated] Step-by-Step Guide Turn Off Spotify's Recommended Listings</u></a></li>
<li><a href="https://some-tips.techidaily.com/expert-analysis-protonvpn-unmatched-security-and-reliable-leak-shielding-as-featured-on-zdnet/"><u>Expert Analysis: ProtonVPN - Unmatched Security and Reliable Leak Shielding, as Featured on ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/expertly-selected-ultimate-vpn-solutions-for-windows-users-in-depth-comparisons-and-ratings-pcmag/"><u>Expertly Selected Ultimate VPN Solutions for Windows Users: In-Depth Comparisons & Ratings | PCMag</u></a></li>
<li><a href="https://some-tips.techidaily.com/experts-picks-elite-vpn-providers-for-ios-unbiased-ratings-and-detailed-analysis-pcmag/"><u>Experts' Picks: Elite VPN Providers for iOS - Unbiased Ratings & Detailed Analysis | PCMag</u></a></li>
<li><a href="https://some-tips.techidaily.com/find-your-perfect-mac-protection-the-ultimate-vpn-guide-and-comparisons-insights-from-industry-pros-techreviewzdnet/"><u>Find Your Perfect Mac Protection: The Ultimate VPN Guide & Comparisons - Insights From Industry Pros | TechReviewZDNET</u></a></li>
<li><a href="https://some-tips.techidaily.com/guide-setting-up-your-vpn-connection-on-windows-11-tips-and-tricks/"><u>Guide: Setting Up Your VPN Connection on Windows 11 - Tips & Tricks</u></a></li>
<li><a href="https://some-guidance.techidaily.com/in-2024-structuring-a-compelling-resume-cv-on-linkedin/"><u>In 2024, Structuring a Compelling Resume (CV) on LinkedIn</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-depth-surfshark-vpn-analysis-insights-from-zdnets-latest-review/"><u>In-Depth Surfshark VPN Analysis - Insights From ZDNet's Latest Review</u></a></li>
<li><a href="https://buynow-help.techidaily.com/top-rated-classic-gamepads-ultimate-pick-for-pc-and-raspberry-pi/"><u>Top-Rated Classic Gamepads: Ultimate Pick for PC and Raspberry Pi</u></a></li>
<li><a href="https://howto.techidaily.com/what-to-do-when-vivo-y100a-has-black-screen-of-death-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>What To Do When Vivo Y100A Has Black Screen of Death? | Dr.fone</u></a></li>
</ul></div>

