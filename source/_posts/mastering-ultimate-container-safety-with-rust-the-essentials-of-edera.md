---
title: Mastering Ultimate Container Safety with Rust - The Essentials of Edera
date: 2024-12-21T17:14:49.835Z
updated: 2024-12-27T16:08:38.712Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/65d523e3125219b2a2af94b6b89e81c6287ca6e9/2024/04/11/98da400c-8f12-4bcd-89a5-9b99d6fcef01/gettyimages-94985760.jpg?width=278&height=156&fit=crop&auto=webp
---

## Mastering Ultimate Container Safety with Rust - The Essentials of Edera

![containers](https://www.zdnet.com/a/img/resize/adf862e9818fa209479e4692e51d04e2bbb755bc/2024/04/11/98da400c-8f12-4bcd-89a5-9b99d6fcef01/gettyimages-94985760.jpg?auto=webp&width=1280)

Paul Taylor/Getty Images

One of the ultimate cloud security nightmares is when someone breaks through your container runtime into its underlying operating system. With attacks such as [Leaky Vessels](https://snyk.io/blog/cve-2024-21626-runc-process-cwd-container-breakout/), a hacker can wreak havoc on your programs, smash other containerized applications, and grant the attacker root user-level privileges. In short, it's all over for your security. To prevent such attacks, Edera is taking an old program into a new language to provide a memory-safe container runtime. 

Written in Rust, [Edera](https://github.com/edera-dev/) is built on the foundation of the classic open-source [type-1, bare-metal Virtual Machine hypervisor](https://www.networkworld.com/article/944300/why-you-want-a-bare-metal-hypervisor-and-how-to-choose.html), [Xen](https://xenproject.org/). This hypervisor was selected, as Edera Chief Innovation Officer and [Alpine Linux](https://www.alpinelinux.org/) maintainer Ariadne Conill, explained, because, unlike [KVM](https://linux-kvm.org/page/Main%5FPage), which runs inside the Linux kernel, it's a dedicated type-1 hypervisor. These are inherently more secure than the popular type-2 hypervisors. 

**Also: [The best VPN services: Expert tested and reviewed](https://www.zdnet.com/article/best-vpn/)**

If you're a techie, you may think that's true, but aren't hypervisors of both types all about virtual machines (VM), not containers? That's correct, but the Edera team has taken the hypervisor design and shifted it over to containers. As Emily Long, Edera's CEO, said, "Hypervisors haven't been reimagined for nearly two decades and just don't work in the cloud-native world." The Edera developers are building a true 21st-century hypervisor. 

The foundation of the new program is [Krata](https://github.com/edera-dev/krata). This is a Xen-based, single-host hypervisor built for [Open Container Initiative (OCI)](https://opencontainers.org/)\-compliant containers. It isolates containers with a fully memory-safe Rust control plane to bring Xen tooling into a new, secure era. In addition, Edera uses Lukko, an open-source memory safety runtime library. This library detects memory safety violations at runtime and cleanly terminates programs before they can be exploited.

Edera is secure by design. It's the only independent solution that offers isolation at the container level, making container escapes impossible, no matter where you run your infrastructure: a hyper cloud, a local cloud, or your own servers. 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/GPk8_xpN_rA?si=YbAdgsjAKsCn_UsB" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<li><a href="https://screen-mirroring-recording.techidaily.com/new-alternatives-spotlighted-by-az-screen-recorder/"><u>[New] Alternatives Spotlighted by AZ Screen Recorder</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unleash-the-potential-of-your-notes-use-mematic/"><u>[New] Unleash the Potential of Your Notes - Use Mematic</u></a></li>
<li><a href="https://facebook-video-share.techidaily.com/updated-tailoring-content-to-thrive-on-youtube-select-the-best-formats/"><u>[Updated] Tailoring Content to Thrive on YouTube – Select the Best Formats</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-transform-valorant-gameplay-top-ranked-costless-voice-alterer-revealed/"><u>[Updated] Transform Valorant Gameplay Top-Ranked, Costless Voice Alterer Revealed</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unlock-animoji-secrets-on-iphone-x-a-step-by-step-guide/"><u>[Updated] Unlock Animoji Secrets on iPhone X - A Step-by-Step Guide</u></a></li>
<li><a href="https://youtube-data.techidaily.com/ed-yt-portals-for-trend-tracking-and-analysis/"><u>[Updated] YT Portals for Trend-Tracking and Analysis</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unleashing-creativity-with-mobile-melodies-on-iphone/"><u>2024 Approved Unleashing Creativity with Mobile Melodies on iPhone</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unlock-full-potential-best-trio-for-zoom-conversion/"><u>2024 Approved Unlock Full Potential Best Trio for Zoom Conversion</u></a></li>
<li><a href="https://tech-revival.techidaily.com/convert-iso-to-high-quality-mp4-in-6-steps-expert-free-techniques-and-tools-for-2n4/"><u>Convert ISO to High-Quality MP4 in 6 Steps - Expert Free Techniques and Tools for 2N4!</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/how-do-i-sign-a-xlsm-files-document-electronically-by-ldigisigner-sign-a-excel-sign-a-excel/"><u>How do i sign a .xlsm files document electronically</u></a></li>
<li><a href="https://iphone-unlock.techidaily.com/in-2024-disabled-apple-iphone-15-pro-how-to-unlock-a-disabled-apple-iphone-15-pro-drfone-by-drfone-ios/"><u>In 2024, Disabled Apple iPhone 15 Pro How to Unlock a Disabled Apple iPhone 15 Pro? | Dr.fone</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/in-2024-how-to-change-your-sim-pin-code-on-your-samsung-galaxy-a15-5g-phone-by-drfone-android/"><u>In 2024, How To Change Your SIM PIN Code on Your Samsung Galaxy A15 5G Phone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-key-elements-for-effective-spotify-ad-execution/"><u>In 2024, The Key Elements for Effective Spotify Ad Execution</u></a></li>
</ul></div>

