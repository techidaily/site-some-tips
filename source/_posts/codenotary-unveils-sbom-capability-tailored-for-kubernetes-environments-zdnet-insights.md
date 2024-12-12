---
title: Codenotary Unveils SBOM Capability Tailored for Kubernetes Environments | ZDNet Insights
date: 2024-12-10T16:13:15.468Z
updated: 2024-12-12T16:47:46.131Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/df9613a0c2aaec5985230e010833ea4d58145c5a/2017/07/12/0e12b766-4bc9-4d43-b610-e80b107ac54e/kubernetes-class.jpg?width=278&height=156&fit=crop&auto=webp
---

## Codenotary Unveils SBOM Capability Tailored for Kubernetes Environments | ZDNet Insights

Software Bill of Materials (SBOM)s aren't optional anymore. If we really want the applications we're running in containers to be secure, we must know what's what within them. To make that easier, [Codenotary](https://codenotary.com/), a leading software supply chain security company, is launching its new [SBOM Operator](https://github.com/ckotzbauer/sbom-operator) for Kubernetes in both its open-source [Community Attestation Service](https://cas.codenotary.com/) and its flagship service, Codenotary's [Trustcenter](https://codenotary.com/products/ci-cd/).

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/_7AYCS7zBU0?si=7R9oIpE4hyEbtk3x" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

### Open Source

* [5 Linux commands you must know to keep your device running smoothly](https://www.zdnet.com/article/5-linux-commands-you-must-know-to-keep-your-device-running-smoothly/)
* [The best Linux laptops you can buy: Expert tested](https://www.zdnet.com/article/best-linux-laptop/)
* [The best Linux distros for beginners](https://www.zdnet.com/article/best-linux-desktops-for-beginners/)
* [My 5 favorite Linux text editors (and why you should be using one)](https://www.zdnet.com/article/my-favorite-linux-text-editors-and-why-you-should-be-using-one/)

An SBOM (pronounced S-Bomb) is a record containing the details and supply chain relationships of the components used in building software. Since most programs today are made by assembling existing open-source and commercial software components, it's essential to know the name and specific versions of all these elements. For instance, a program using Apache Log4j2 versions 2.17.0 is vulnerable to [Log4Shell attacks](https://thenewstack.io/log4shell-we-are-in-so-much-trouble/). One using [Log4j2 2.17.1 or newer is as safe as houses](https://logging.apache.org/log4j/2.x/security.html). 

Now, you could check for that and thousands of other potential vulnerabilities by hand, or you could turn to a service like Codenotary's new offering. I know which one I'd pick. 

The SBOM Operator for Kubernetes mitigates the risk of software supply chain attacks by tracking all software and software dependencies running in Kubernetes. It does this by generating SBOMs of your running container images and maintaining up-to-date records of all builds, and dependencies. SBOM Operator builds its SBOMs using its own SBOM generator. When a new vulnerability shows up -- and trust me, one will -- this lets you know that it's time to make a fix when dangerous or vulnerable artifacts are detected.

To make this keep working properly, Codenotary continuously updates its SBOM records, This data is kept in its open-source speedy, immutable database, [Immudb](https://codenotary.com/technologies/immudb/). This is a zero-trust tamper-proof, auditable database. The container image files are kept in a Git repository.

Codenotary claims this information is instantly available for search. With it, you can locate the software artifacts in your code in seconds. The program also keeps a history of verified image content changes.

"By itself, the SBOM is not very useful without continuously being updated and maintained as the information is deprecated with every new deployment or update," said Dennis Zimmer, Codenotary's co-founder and CTO. "Now, users know exactly what is running in containers, with the most recent information, so they have the ability to immediately remediate something if necessary."

SBOM Operator's chief programmer, Christian Kotzbauer, said, "I am pleased to contribute to the wider adoption and use of SBOMs with the Codenotary integration in my Kubernetes operator, especially the additional security, timestamp, and search capabilities across the infrastructure were key to developing the extension. 

This is another step forward in Codenotary's efforts to provide comprehensive tools for cataloging and securing the software development lifecycle. Its programs and services, both free and paid, deserve Kubernetes developers' attention.

**Related Stories:**

* [The Alpha and Omega of software supply chain security](https://www.zdnet.com/article/the-alpha-and-omega-of-software-supply-chain-security/)
* [Securing the open-source ecosystem: SBOMs are no longer optional](https://www.zdnet.com/article/securing-the-open-source-ecosystem-sboms-are-no-longer-optional/)
* [Codenotary: Notarize and verify your software bill of materials](https://www.zdnet.com/article/codenotary-open-source-notarization-service-for-software-bill-of-material-arrives/)

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
<li><a href="https://fox-blue.techidaily.com/new-in-2024-reclaiming-one-headphone-harmony/"><u>[New] In 2024, Reclaiming One-Headphone Harmony</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-edge-of-gaming-technology-samsung-ue590-monitor/"><u>[New] The Edge of Gaming Technology Samsung UE590 Monitor</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-essence-of-color-in-photography-top-11-tutorials/"><u>[New] The Essence of Color in Photography (Top 11 Tutorials)</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-ultimate-guide-to-choosing-top-8-free-srt-services/"><u>[New] The Ultimate Guide to Choosing Top 8 Free SRT Services</u></a></li>
<li><a href="https://extra-information.techidaily.com/updated-a-step-by-step-journey-clearing-images-with-picsart/"><u>[Updated] A Step-By-Step Journey Clearing Images with Picsart</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/updated-optimizing-facebook-live-from-pcmaclaptop-through-obs-for-2024/"><u>[Updated] Optimizing Facebook Live From PC/Mac/Laptop Through OBS for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-art-of-pictorial-twists-and-turns/"><u>[Updated] The Art of Pictorial Twists and Turns</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unveiling-the-potential-of-todays-drones-for-tomorrow/"><u>2024 Approved Unveiling the Potential of Today's Drones for Tomorrow</u></a></li>
<li><a href="https://win-exclusive.techidaily.com/6-effective-solutions-for-fixing-windows-10-setup-stuck-at-1-34-64-or-99/"><u>6 Effective Solutions for Fixing Windows 10 Setup Stuck at 1%, 34%, 64%, or 99%</u></a></li>
<li><a href="https://on-screen-recording.techidaily.com/expert-tutorials-on-precision-digital-video-capture/"><u>Expert Tutorials on Precision Digital Video Capture</u></a></li>
<li><a href="https://mondly-stories.techidaily.com/1719581066868-hello-in-indonesian-a-quick-guide-to-indonesian-greetings/"><u>Hello In Indonesian: A Quick Guide To Indonesian Greetings</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/in-2024-leading-tech-in-snap-capture/"><u>In 2024, Leading Tech in Snap Capture</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-ultimate-6-digital-backdrop-eradicators-boosting-image-clarity/"><u>In 2024, Ultimate 6 Digital Backdrop Eradicators Boosting Image Clarity</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unveiling-the-basics-of-vlogging-gear-and-software/"><u>In 2024, Unveiling the Basics of Vlogging Gear & Software</u></a></li>
<li><a href="https://fix-guide.techidaily.com/oppo-reno-11-5g-screen-unresponsive-heres-how-to-fix-it-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Oppo Reno 11 5G Screen Unresponsive? Heres How to Fix It | Dr.fone</u></a></li>
<li><a href="https://data-wizards.techidaily.com/reclaiming-bygone-broadcast-materials/"><u>Reclaiming Bygone Broadcast Materials</u></a></li>
<li><a href="https://some-tips.techidaily.com/swiftly-restore-working-airdrop-between-apple-gadgets-and-macs-for-2024/"><u>Swiftly Restore Working AirDrop Between Apple Gadgets & Macs for 2024</u></a></li>
</ul></div>

