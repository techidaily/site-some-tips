---
title: Secure Your Kubernetes Deployments with Codenotary's New SBOM Service Feature | Cybersecurity News on ZDNet
date: 2025-01-07T19:30:00.664Z
updated: 2025-01-12T18:30:25.502Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/df9613a0c2aaec5985230e010833ea4d58145c5a/2017/07/12/0e12b766-4bc9-4d43-b610-e80b107ac54e/kubernetes-class.jpg?width=278&height=156&fit=crop&auto=webp
---

## Secure Your Kubernetes Deployments with Codenotary's New SBOM Service Feature | Cybersecurity News on ZDNet

Software Bill of Materials (SBOM)s aren't optional anymore. If we really want the applications we're running in containers to be secure, we must know what's what within them. To make that easier, [Codenotary](https://codenotary.com/), a leading software supply chain security company, is launching its new [SBOM Operator](https://github.com/ckotzbauer/sbom-operator) for Kubernetes in both its open-source [Community Attestation Service](https://cas.codenotary.com/) and its flagship service, Codenotary's [Trustcenter](https://codenotary.com/products/ci-cd/).

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/lxv4NM-89CU?si=Uj5rOkhrwZ_6QIuW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<li><a href="https://youtube-zero.techidaily.com/ccess-exclusive-video-artwork-free-flawless-and-fast-for-2024/"><u>[New] Access Exclusive Video Artwork – Free, Flawless, and Fast for 2024</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/new-in-2024-breaking-down-instagrams-timeframe-per-video/"><u>[New] In 2024, Breaking Down Instagram's Timeframe Per-Video</u></a></li>
<li><a href="https://fox-helps.techidaily.com/new-in-2024-mastering-the-craft-of-online-title-perfection/"><u>[New] In 2024, Mastering the Craft of Online Title Perfection</u></a></li>
<li><a href="https://article-tips.techidaily.com/new-in-2024-top-10-enterprise-cloud-options/"><u>[New] In 2024, Top 10 Enterprise Cloud Options</u></a></li>
<li><a href="https://some-tips.techidaily.com/ace-any-role-talk-strategies-for-conquering-the-who-am-i-job-interview-question-forbes/"><u>Ace Any Role Talk: Strategies for Conquering the Who Am I? Job Interview Question | Forbes</u></a></li>
<li><a href="https://some-tips.techidaily.com/becoming-a-chief-ai-officer-the-pathway-to-leadership-in-artificial-intelligence-roles/"><u>Becoming a Chief AI Officer - The Pathway to Leadership in Artificial Intelligence Roles</u></a></li>
<li><a href="https://tech-savvy.techidaily.com/can-gpt-assist-in-finalizing-writings/"><u>Can GPT Assist in Finalizing Writings?</u></a></li>
<li><a href="https://some-tips.techidaily.com/future-proof-your-career-embrace-being-an-ai-architect-and-user-at-work/"><u>Future-Proof Your Career: Embrace Being an AI Architect & User at Work!</u></a></li>
<li><a href="https://tech-revival.techidaily.com/guide-for-quick-and-simple-upgrade-to-windows-1011-for-desktops-and-laptops/"><u>Guide for Quick & Simple Upgrade to Windows 10/11 for Desktops and Laptops</u></a></li>
<li><a href="https://extra-tips.techidaily.com/in-2024-balancing-ambient-sound-on-windowsos-x-machines/"><u>In 2024, Balancing Ambient Sound on Windows/OS X Machines</u></a></li>
<li><a href="https://unlock-android.techidaily.com/in-2024-how-to-unlock-any-xiaomi-redmi-12-5g-phone-password-using-emergency-call-by-drfone-android/"><u>In 2024, How To Unlock Any Xiaomi Redmi 12 5G Phone Password Using Emergency Call</u></a></li>
<li><a href="https://change-location.techidaily.com/in-2024-the-most-useful-tips-for-pokemon-go-ultra-league-on-samsung-galaxy-a15-5g-drfone-by-drfone-virtual-android/"><u>In 2024, The Most Useful Tips for Pokemon Go Ultra League On Samsung Galaxy A15 5G | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/mastering-automation-in-it-save-16-and-boost-efficiency-using-windows-powershell-exclusive-offer-on-zdnet/"><u>Mastering Automation in IT: Save $16 & Boost Efficiency Using Windows PowerShell - Exclusive Offer on ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/nail-your-next-tech-interview-a-step-by-step-guide-to-masterful-applications-with-expert-tips-from-zdnet/"><u>Nail Your Next Tech Interview: A Step-by-Step Guide to Masterful Applications with Expert Tips From ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/securing-your-dream-job-in-technology-a-strategic-guide-to-joining-microsofts-talent-pool/"><u>Securing Your Dream Job in Technology: A Strategic Guide to Joining Microsoft's Talent Pool</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-future-of-work-exploring-unconventional-and-mysterious-new-ai-influenced-careers/"><u>The Future of Work: Exploring Unconventional & Mysterious New AI-Influenced Careers</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-the-core-of-success-insider-tips-on-launching-your-apple-job-journey-techinsight/"><u>Unlocking the Core of Success: Insider Tips on Launching Your Apple Job Journey | TechInsight</u></a></li>
</ul></div>

