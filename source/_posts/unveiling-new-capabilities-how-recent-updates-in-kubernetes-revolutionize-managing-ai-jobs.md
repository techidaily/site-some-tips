---
title: "Unveiling New Capabilities: How Recent Updates in Kubernetes Revolutionize Managing AI Jobs"
date: 2024-12-19T18:17:15.724Z
updated: 2024-12-22T00:39:10.863Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/9ea24c6282003fe5eaf1336598f1ab6b49832d478e258a2b3fdb222135f271e5.jpg
---

## Unveiling New Capabilities: How Recent Updates in Kubernetes Revolutionize Managing AI Jobs

![cloudcontaingettyimages-1350321232](https://www.zdnet.com/a/img/resize/53c77a881c2c43320c363e8707dd45bf2e7ead53/2024/08/16/c788b0c4-9389-46fe-9c93-a5fe95fca04f/cloudcontaingettyimages-1350321232.jpg?auto=webp&width=1280)

SerrNovik/Getty Images

[Kubernetes](https://kubernetes.io/), the [container-management orchestration system](https://www.zdnet.com/article/what-is-kubernetes-and-why-is-it-so-important/), has proven vital for modern computing, except for one area: [artificial intelligence](https://www.zdnet.com/article/what-is-ai-heres-everything-you-need-to-know-about-artificial-intelligence/) (AI) and machine learning (ML). The problem: AI/ML demands substantial CPU, memory, and GPU resources, which are [not easy to manage on Kubernetes](https://www.kubermatic.com/blog/ai-and-machine-learning-integration-into-kubernetes/).

Now, with the latest Kubernetes release -- [Kubernetes 1.31, Elli](https://kubernetes.io/blog/2024/08/13/kubernetes-v1-31-release/) \-- the [Cloud Native Computing Foundation (CNCF)](https://www.cncf.io/) is addressing these issues.

**Also: [5 ways CIOs can manage the business demand for generative AI](https://www.zdnet.com/article/5-ways-cios-can-manage-the-business-demand-for-generative-ai/)**

Elli's improved AI features start with alpha support for [Open Container Initiative (OCI)](https://opencontainers.org/) images and artifacts as a native volume source. This may not sound like much, but it enables developers to switch out large language models (LLM) as easily as they do ordinary container images. 

Elli also brings an updated dynamic resource allocation API and design to Kubernetes. This feature will help standardize accessing and managing hardware accelerators, such as GPUs, which are essential for AI and ML. It also simplifies the implementation of features such as cluster autoscaling, which -- in turn -- will make it easier to run AI and ML jobs on Kubernetes. 

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

In the past, Kubernetes had multiple ways to access a host's underlying hardware. The updated dynamic resource allocation (DRA) provides a more straightforward way to access system resources. The old style, which uses a DRA driver controller, is still supported via "classic DRA."

Leaving AI behind, Kubernetes also now fully supports [AppArmor](https://apparmor.net/), a Linux kernel security module that allows system administrators to restrict programs' capabilities with per-program profiles. This feature has reached general availability, enabling users to set AppArmor profiles for containers directly through the Kubernetes API. Implemented properly, AppArmour support will help make Kubernetes clusters and workloads more secure. 

Elsewhere on the security front, a new optional feature enables administrators to configure the endpoints so anonymous requests for access can be blocked. This will help protect clusters from Role Based Access Control (RBAC) misconfigurations that could otherwise give anonymous users broad access to the cluster.

**Also: [OIN expands Linux patent protection yet again (but not to AI)](https://www.zdnet.com/article/oin-expands-linux-patent-protection-yet-again-but-not-to-ai/)**

As an ever-evolving open-source program, Kubernetes 1.31 also continues to streamline and modernize its codebase by dropping out-of-date features. This includes: 

* **Removal of in-tree cloud provider integrations:** Completing a process that began with version 1.26, Kubernetes 1.31 removes all in-tree cloud provider integrations. This move is part of an ongoing effort to ensure Kubernetes remains a vendor-neutral platform. You can still integrate your Kubernetes clusters with a specific cloud provider. However, you won't be able to do so from inside Kubernetes. You'll have to use the recommended approach via external integration.
* **Deprecation of non-CSI volume limit plugins:** The release deprecates all non-CSI volume limit scheduler plugins, aligning with Kubernetes' strategy to transition to the Container Storage Interface (CSI) for all storage-related functionalities.
* **Deprecation of** [**Cgroups**](https://man7.org/linux/man-pages/man7/cgroups.7.html) **v1:** Cgroups is a Linux kernel feature that enables you to allocate, prioritize, and manage system resources among processes. From here on out, [cgroups v2](https://kubernetes.io/docs/concepts/architecture/cgroups/) is what you should be using.

Put it all together and this release is about much more than making Kubernetes AI-friendly. Angelos Kolaitis, a [Canonical](https://canonical.com/) senior software engineer and team leader for the Kubernetes 1.31 release, said this new release is about "taking the [complexity and the implementation-specific details out of the code of Kubernetes](https://kubernetespodcast.com/episode/233-kubernetes-1.31/), have Kubernetes focus on the desired state and leave all of the implementations, all of the extra source outside of it."

**Also: [What is Kubernetes, and why is it so important?](https://www.zdnet.com/article/what-is-kubernetes-and-why-is-it-so-important/)**

Beyond the new features, Kolaitis said, "You don't have to do anything, but Kubernetes will be taking extra steps to make sure that your workloads are running, and are reliable, and can be counted on to have your production services not breaking." 

New features are nice, but stability is golden. For that reason alone, I recommend exploring an update to Kubernetes 1.31 sooner rather than later. 

#### Open Source

[5 Linux commands you must know to keep your device running smoothly](https://www.zdnet.com/article/5-linux-commands-you-must-know-to-keep-your-device-running-smoothly/ "5 Linux commands you must know to keep your device running smoothly")

[The best Linux laptops you can buy: Expert tested](https://www.zdnet.com/article/best-linux-laptop/ "The best Linux laptops you can buy: Expert tested")

[The best Linux distros for beginners](https://www.zdnet.com/article/best-linux-desktops-for-beginners/ "The best Linux distros for beginners")

[My 5 favorite Linux text editors (and why you should be using one)](https://www.zdnet.com/article/my-favorite-linux-text-editors-and-why-you-should-be-using-one/ "My 5 favorite Linux text editors (and why you should be using one)")

* [5 Linux commands you must know to keep your device running smoothly](https://www.zdnet.com/article/5-linux-commands-you-must-know-to-keep-your-device-running-smoothly/ "5 Linux commands you must know to keep your device running smoothly")
* [The best Linux laptops you can buy: Expert tested](https://www.zdnet.com/article/best-linux-laptop/ "The best Linux laptops you can buy: Expert tested")
* [The best Linux distros for beginners](https://www.zdnet.com/article/best-linux-desktops-for-beginners/ "The best Linux distros for beginners")
* [My 5 favorite Linux text editors (and why you should be using one)](https://www.zdnet.com/article/my-favorite-linux-text-editors-and-why-you-should-be-using-one/ "My 5 favorite Linux text editors (and why you should be using one)")

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
<li><a href="https://some-tips.techidaily.com/new-the-editors-edge-adding-sleek-fades-to-your-work/"><u>[New] The Editor's Edge Adding Sleek Fades to Your Work</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-top-8-free-online-havens-for-3d-text-psdfiles/"><u>[New] Top 8 FREE Online Havens for 3D Text PSDFiles</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unlock-creative-potential-image-curve-magic-in-ps/"><u>[New] Unlock Creative Potential Image Curve Magic in PS</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unmatched-clarity-in-filming-top-rated-camera-stabilizers-guide/"><u>[New] Unmatched Clarity in Filming Top-Rated Camera Stabilizers Guide</u></a></li>
<li><a href="https://youtube-blog.techidaily.com/ed-in-2024-unveiling-the-shadows-a-systematic-guide-to-hidden-youtube-content/"><u>[Updated] In 2024, Unveiling the Shadows A Systematic Guide to Hidden YouTube Content</u></a></li>
<li><a href="https://extra-skills.techidaily.com/updated-sonic-kickstarts-curated-playlist-powerhouses/"><u>[Updated] Sonic Kickstarts Curated Playlist Powerhouses</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-techniques-for-maximizing-gopro-battery-life/"><u>[Updated] Techniques for Maximizing GoPro Battery Life</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-top-10-budget-friendly-apps-revolutionizing-smartphone-imagery/"><u>[Updated] Top 10 Budget-Friendly Apps Revolutionizing Smartphone Imagery</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unlock-the-full-potential-of-your-iphone-photos/"><u>[Updated] Unlock the Full Potential of Your iPhone Photos</u></a></li>
<li><a href="https://android-location-track.techidaily.com/9-best-phone-monitoring-apps-for-oppo-reno-10-pro-5g-drfone-by-drfone-virtual-android/"><u>9 Best Phone Monitoring Apps for Oppo Reno 10 Pro 5G | Dr.fone</u></a></li>
<li><a href="https://fox-ssl.techidaily.com/1728486393786-excel/"><u>Excelファイルの安全バックアップ計画:自動的に複製して保管方法</u></a></li>
<li><a href="https://tech-hub.techidaily.com/find-everything-you-need-for-your-apple-gadgets-detailed-manuals-specs-listed-and-expert-repair-tips-in-a-single-hub/"><u>Find Everything You Need for Your Apple Gadgets : Detailed Manuals, Specs Listed, and Expert Repair Tips in a Single Hub</u></a></li>
<li><a href="https://driver-download.techidaily.com/get-the-best-quality-video-with-logitech-c525-driver-update-for-windows-easy-download-options/"><u>Get the Best Quality Video with Logitech C525 Driver Update for Windows - Easy Download Options</u></a></li>
<li><a href="https://extra-hints.techidaily.com/in-2024-best-10-free-jpg-to-gif-conversion-tools/"><u>In 2024, Best 10 Free JPG to GIF Conversion Tools</u></a></li>
<li><a href="https://fox-direct.techidaily.com/in-2024-envisioned-worlds-await-equip-yourself-with-these-7-devices/"><u>In 2024, Envisioned Worlds Await Equip Yourself with These 7 Devices</u></a></li>
<li><a href="https://discover-best.techidaily.com/top-mp4-video-converter-tools-of-2023-comprehensive-guide/"><u>Top MP4 Video Converter Tools of 2023 - Comprehensive Guide</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/aRMCbJxLuwE?si=E5sfJvoqkv1qCMWz" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

