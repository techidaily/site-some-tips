---
title: "Unveiling Codenotary's New SBOM Offering: Enhanced Security for Kubernetes Clusters - Insights From ZDNet"
date: 2024-12-20T16:17:49.186Z
updated: 2024-12-27T16:59:56.260Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/802eeff691c55a6d5d09cbae446dc45a39ed24ae91160c0e7074f7929a9448f1.jpg
---

## Unveiling Codenotary's New SBOM Offering: Enhanced Security for Kubernetes Clusters - Insights From ZDNet

Software Bill of Materials (SBOM)s aren't optional anymore. If we really want the applications we're running in containers to be secure, we must know what's what within them. To make that easier, [Codenotary](https://codenotary.com/), a leading software supply chain security company, is launching its new [SBOM Operator](https://github.com/ckotzbauer/sbom-operator) for Kubernetes in both its open-source [Community Attestation Service](https://cas.codenotary.com/) and its flagship service, Codenotary's [Trustcenter](https://codenotary.com/products/ci-cd/).

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/bXmwwSmYqq4?si=Bb-eJfLnlpeeClyt" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<li><a href="https://vp-tips.techidaily.com/new-in-2024-auditory-interpretation-made-easy-priceless-access/"><u>[New] In 2024, Auditory Interpretation Made Easy, Priceless Access</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/new-in-2024-mac-enhancement-synchronized-screen-plus-audio-tracking/"><u>[New] In 2024, Mac Enhancement Synchronized Screen + Audio Tracking</u></a></li>
<li><a href="https://tiktok-video-recordings.techidaily.com/new-in-2024-mastering-pc-tiktok-live-streams-a-step-by-step-guide/"><u>[New] In 2024, Mastering PC TikTok Live Streams A Step-by-Step Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-transforming-the-metaverse-essential-gear-to-consider-top-7/"><u>[New] Transforming the Metaverse Essential Gear to Consider (Top 7)</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unleashing-the-power-of-edit-in-tiktok-video-creation/"><u>[New] Unleashing the Power of Edit in TikTok Video Creation</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-sculpted-sentences-turning-text-into-3d-art/"><u>[Updated] Sculpted Sentences Turning Text Into 3D Art</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-tailoring-your-whatsapp-ringtone-for-ios-and-android-devices/"><u>[Updated] Tailoring Your WhatsApp Ringtone for iOS and Android Devices</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-excellent-videocameras-of-the-year-2024/"><u>[Updated] The Excellent Videocameras of the Year 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-utilizing-luts-for-professional-color-grading/"><u>[Updated] Utilizing LUTs for Professional Color Grading</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-perfect-pairing-of-xbox-and-zooming-techniques-for-gaming/"><u>2024 Approved The Perfect Pairing of Xbox and Zooming Techniques for Gaming</u></a></li>
<li><a href="https://vp-tips.techidaily.com/best-ios-slideshow-software-from-x-to-ios13/"><u>Best iOS Slideshow Software From X to IOS13</u></a></li>
<li><a href="https://youtube-tips.techidaily.com/cing-your-youtube-profiles-a-guide-to-crafting-descriptions/"><u>Enhancing Your YouTube Profiles A Guide to Crafting Descriptions</u></a></li>
<li><a href="https://win-top.techidaily.com/gratuit-online-transformeren-van-tga-naar-bmp-met-movavi-begrijp-het-in-een-stuk/"><u>Gratuit Online Transformeren Van TGA Naar BMP Met Movavi - Begrijp Het in Een Stuk</u></a></li>
<li><a href="https://unlock-android.techidaily.com/in-2024-how-to-bypass-android-lock-screen-using-emergency-call-on-xiaomi-by-drfone-android/"><u>In 2024, How to Bypass Android Lock Screen Using Emergency Call On Xiaomi?</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/infinity-series-ultra-hd-single-touch-display-for-2024/"><u>Infinity Series – Ultra HD, Single Touch Display for 2024</u></a></li>
<li><a href="https://hardware-updates.techidaily.com/step-by-step-updating-your-lenovo-x1-carbon-on-windows-107-with-newest-drivers/"><u>Step-by-Step: Updating Your Lenovo X1 Carbon on Windows 10/7 with Newest Drivers!</u></a></li>
</ul></div>

