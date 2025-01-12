---
title: Launching SBOM Capabilities with Codenotary for Enhanced Kubernetes Security - Insights on ZDNet
date: 2025-01-11T16:50:43.343Z
updated: 2025-01-12T17:17:07.905Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/df9613a0c2aaec5985230e010833ea4d58145c5a/2017/07/12/0e12b766-4bc9-4d43-b610-e80b107ac54e/kubernetes-class.jpg?width=278&height=156&fit=crop&auto=webp
---

## Launching SBOM Capabilities with Codenotary for Enhanced Kubernetes Security - Insights on ZDNet

Software Bill of Materials (SBOM)s aren't optional anymore. If we really want the applications we're running in containers to be secure, we must know what's what within them. To make that easier, [Codenotary](https://codenotary.com/), a leading software supply chain security company, is launching its new [SBOM Operator](https://github.com/ckotzbauer/sbom-operator) for Kubernetes in both its open-source [Community Attestation Service](https://cas.codenotary.com/) and its flagship service, Codenotary's [Trustcenter](https://codenotary.com/products/ci-cd/).

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/LaGNHfAT92w?si=bvHo1iYK2JBIPtRo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<li><a href="https://fox-direct.techidaily.com/new-2024-approved-insta-tips-for-enthusiasts-on-uploading-podcasts/"><u>[New] 2024 Approved Insta-Tips for Enthusiasts on Uploading Podcasts</u></a></li>
<li><a href="https://fox-helps.techidaily.com/new-elite-unmanned-aerial-vehicles-up-for-grabs/"><u>[New] Elite Unmanned Aerial Vehicles Up for Grabs</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/updated-how-to-make-macbook-pro-video-tutorials-easy-for-2024/"><u>[Updated] How to Make Macbook Pro Video Tutorials Easy for 2024</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/2024-approved-revolutionize-replies-enhancing-interaction-on-telegram-platforms/"><u>2024 Approved Revolutionize Replies Enhancing Interaction on Telegram Platforms</u></a></li>
<li><a href="https://youtube-tips.techidaily.com/approved-subscriber-threshold-raised-for-profits/"><u>2024 Approved Subscriber Threshold Raised for Profits</u></a></li>
<li><a href="https://some-tips.techidaily.com/dont-miss-out-get-your-hands-on-the-affordable-colsen-tabletop-fire-pit-for-just-50-today/"><u>Don't Miss Out! Get Your Hands on the Affordable Colsen Tabletop Fire Pit for Just $50 Today!</u></a></li>
<li><a href="https://some-tips.techidaily.com/ecoflow-river-3-a-leading-choice-for-beginners-in-portable-power-solutions/"><u>EcoFlow River 3 - A Leading Choice for Beginners in Portable Power Solutions</u></a></li>
<li><a href="https://fox-sure.techidaily.com/effective-solo-marketing-in-2008-boosting-ad-performance-through-massmail-solutions/"><u>Effective Solo Marketing in 2008: Boosting Ad Performance Through MassMail Solutions</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhance-your-green-thumb-with-our-plant-care-software-at-an-extra-discounted-price-this-labor-day-exclusive-deal-alert/"><u>Enhance Your Green Thumb with Our Plant Care Software at an Extra Discounted Price This Labor Day | Exclusive Deal Alert!</u></a></li>
<li><a href="https://some-tips.techidaily.com/experience-endless-entertainment-with-this-ultimate-remote-controlled-lawn-mowing-system-a-review-unleash-your-green-thumb-in-a-whole-new-way/"><u>Experience Endless Entertainment with This Ultimate Remote-Controlled Lawn Mowing System: A Review - Unleash Your Green Thumb in a Whole New Way!</u></a></li>
<li><a href="https://some-tips.techidaily.com/expert-tips-on-picking-your-ideal-lawn-mower-according-to-zdnet-standards/"><u>Expert Tips on Picking Your Ideal Lawn Mower According to ZDNet Standards</u></a></li>
<li><a href="https://some-tips.techidaily.com/exploring-the-elite-quad-of-2022-walkie-talkies-in-depth-review-zdnet/"><u>Exploring the Elite Quad of 2022 Walkie-Talkies - In Depth Review | ZDNET</u></a></li>
<li><a href="https://some-tips.techidaily.com/exploring-the-most-efficient-traveling-solar-panels-for-2-unveiling-our-picks-on-zdnet/"><u>Exploring the Most Efficient Traveling Solar Panels for 2#: Unveiling Our Picks on ZDNET</u></a></li>
<li><a href="https://some-tips.techidaily.com/first-look-at-the-dji-mini-3-pro-the-ultimate-tiny-drone-for-stealthy-aerial-photography-with-integrated-battery-charger-gadgethub-zdnet/"><u>First Look at the DJI Mini 3 Pro – The Ultimate Tiny Drone for Stealthy Aerial Photography with Integrated Battery Charger | GadgetHub ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/gear-up-for-adventure-with-the-ultimate-guide-to-best-outdoor-tvs-expert-ratings-zdnet/"><u>Gear Up for Adventure with the Ultimate Guide to Best Outdoor TVs - Expert Ratings | ZDNET</u></a></li>
<li><a href="https://on-screen-recording.techidaily.com/in-2024-enhance-your-experience-with-mi-11-screen-capture-guide/"><u>In 2024, Enhance Your Experience with Mi 11 Screen Capture Guide</u></a></li>
<li><a href="https://digital-screen-recording.techidaily.com/in-2024-mastering-voice-over-recording-for-videos/"><u>In 2024, Mastering Voice-Over Recording for Videos</u></a></li>
<li><a href="https://solve-helper.techidaily.com/top-5-high-definition-media-players-for-pc-and-mac-detailed-comparison-downloads-and-user-reviews-4k-edition/"><u>Top 5 High Definition Media Players for PC and Mac: Detailed Comparison, Downloads & User Reviews - 4K Edition</u></a></li>
<li><a href="https://data-recovery.techidaily.com/windows-stellar/"><u>Windows 用の失われたファイルを復元する Stellar データリカバリ -無料版でも利用可能</u></a></li>
</ul></div>

