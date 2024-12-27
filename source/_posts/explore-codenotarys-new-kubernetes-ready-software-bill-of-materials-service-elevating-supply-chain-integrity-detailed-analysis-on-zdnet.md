---
title: Explore Codenotary's New Kubernetes-Ready Software Bill of Materials Service, Elevating Supply Chain Integrity - Detailed Analysis on ZDNet
date: 2024-12-24T17:14:46.336Z
updated: 2024-12-27T16:34:21.928Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/df9613a0c2aaec5985230e010833ea4d58145c5a/2017/07/12/0e12b766-4bc9-4d43-b610-e80b107ac54e/kubernetes-class.jpg?width=278&height=156&fit=crop&auto=webp
---

## Explore Codenotary's New Kubernetes-Ready Software Bill of Materials Service, Elevating Supply Chain Integrity - Detailed Analysis on ZDNet

Software Bill of Materials (SBOM)s aren't optional anymore. If we really want the applications we're running in containers to be secure, we must know what's what within them. To make that easier, [Codenotary](https://codenotary.com/), a leading software supply chain security company, is launching its new [SBOM Operator](https://github.com/ckotzbauer/sbom-operator) for Kubernetes in both its open-source [Community Attestation Service](https://cas.codenotary.com/) and its flagship service, Codenotary's [Trustcenter](https://codenotary.com/products/ci-cd/).

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/h5uImbOWmTg?si=z4kP-R0QbXbBAJTa" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<li><a href="https://some-tips.techidaily.com/new-stand-out-from-the-noise-logo-design-for-podcast-success/"><u>[New] Stand Out From the Noise Logo Design for Podcast Success</u></a></li>
<li><a href="https://on-screen-recording.techidaily.com/new-unraveling-sharex-professional-perspectives-and-picks-for-2024/"><u>[New] Unraveling ShareX Professional Perspectives & Picks for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-ultimate-guide-to-removing-photo-borders/"><u>[Updated] The Ultimate Guide to Removing Photo Borders</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-transforming-images-the-art-of-applying-luts-in-pro/"><u>[Updated] Transforming Images The Art of Applying LUTs in Pro</u></a></li>
<li><a href="https://youtube-docs.techidaily.com/approved-sky-high-engagement-optimizing-for-virality-and-visibility/"><u>2024 Approved Sky High Engagement Optimizing for Virality and Visibility</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-ultimate-cinemagraph-guide-top-5-must-know-tactics/"><u>2024 Approved The Ultimate Cinemagraph Guide - Top 5 Must-Know Tactics</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unlock-the-secrets-to-creating-instagram-hits-with-engaging-unboxing-videos/"><u>2024 Approved Unlock the Secrets to Creating Instagram Hits with Engaging Unboxing Videos</u></a></li>
<li><a href="https://discover-data.techidaily.com/how-to-harmonize-your-tunes-on-every-device-fixing-song-synchronization-error-202/"><u>How To Harmonize Your Tunes on Every Device – Fixing Song Synchronization Error 202([</u></a></li>
<li><a href="https://win-solutions.techidaily.com/latest-techniques-for-troubleshooting-and-preventing-arma-3-from-crashing/"><u>Latest Techniques for Troubleshooting and Preventing ArmA 3 From Crashing</u></a></li>
<li><a href="https://mondly-stories.techidaily.com/the-european-linguistic-odyssey-celebrated-on-this-day/"><u>The European Linguistic Odyssey Celebrated on This Day</u></a></li>
<li><a href="https://blue-screen-error.techidaily.com/troubleshooting-tips-for-resolving-critical-process-died-and-preventing-bsod-on-windows-10-systems/"><u>Troubleshooting Tips for Resolving Critical Process Died and Preventing BSOD on Windows 10 Systems</u></a></li>
</ul></div>

