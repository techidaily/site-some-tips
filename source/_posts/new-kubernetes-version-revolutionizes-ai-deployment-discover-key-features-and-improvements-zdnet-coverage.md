---
title: "New Kubernetes Version Revolutionizes AI Deployment: Discover Key Features & Improvements - ZDNet Coverage"
date: 2024-12-20T01:45:34.980Z
updated: 2024-12-20T16:39:26.313Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/a9309627364580efd732c4c8f6349cf67c0dc25ea886bdb64936441ab4225274.png
---

## New Kubernetes Version Revolutionizes AI Deployment: Discover Key Features & Improvements - ZDNet Coverage

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
<li><a href="https://some-tips.techidaily.com/updated-the-hero5-users-blueprint-for-incredible-time-lapse-videos/"><u>[Updated] The Hero5 User's Blueprint for Incredible Time-Lapse Videos</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unmatched-timers-for-weddings-top-10-choices-on-phones/"><u>[Updated] Unmatched Timers for Weddings Top 10 Choices on Phones</u></a></li>
<li><a href="https://youtube-sure.techidaily.com/onic-beauty-personalities-to-follow-on-youtube-for-2024/"><u>10 Iconic Beauty Personalities to Follow on YouTube for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-thrifty-choices-for-virtual-reality-heads/"><u>2024 Approved Thrifty Choices for Virtual Reality Heads</u></a></li>
<li><a href="https://youtube-video-recordings.techidaily.com/go-backwards-a-step-by-step-for-reversing-youtube-videos/"><u>Go Backwards A Step-by-Step for Reversing YouTube Videos</u></a></li>
<li><a href="https://printer-issues.techidaily.com/how-to-react-when-your-printer-disconnects/"><u>How to React When Your Printer Disconnects</u></a></li>
<li><a href="https://some-guidance.techidaily.com/in-2024-streamline-your-media-experience-with-pip-in-safari/"><u>In 2024, Streamline Your Media Experience with PIP in Safari</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-streamline-your-video-projects-using-movie-maker-on-windows-8/"><u>In 2024, Streamline Your Video Projects Using Movie Maker on Windows 8</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-easy-path-to-observing-well-liked-comments-on-the-video-platform/"><u>In 2024, The Easy Path to Observing Well-Liked Comments on the Video Platform</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-metrics-of-mastery-assessing-luminances-hdr-capabilities/"><u>In 2024, The Metrics of Mastery Assessing Luminance's HDR Capabilities</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-top-tier-photographic-archives/"><u>In 2024, Top Tier Photographic Archives</u></a></li>
<li><a href="https://techno-recovery.techidaily.com/skyrocket-your-computer-efficiency-with-these-7-high-impact-techniques/"><u>Skyrocket Your Computer Efficiency with These 7 High-Impact Techniques</u></a></li>
<li><a href="https://win-answers.techidaily.com/solving-common-directdraw-graphics-glitches-easily/"><u>Solving Common DirectDraw Graphics Glitches Easily</u></a></li>
<li><a href="https://extra-resources.techidaily.com/the-encore-list-top-pick-for-digital-music-tones/"><u>The Encore List Top Pick for Digital Music Tones</u></a></li>
<li><a href="https://extra-resources.techidaily.com/top-10-titans-of-aerial-lifting-technology/"><u>Top 10 Titans of Aerial Lifting Technology</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-20-must-have-tools-and-effects-for-your-tiktok-edits-for-2024/"><u>Top 20 Must-Have Tools & Effects for Your TikTok Edits for 2024</u></a></li>
<li><a href="https://vimeo-videos.techidaily.com/unveiling-the-magic-of-end-screens-for-vimeo-content/"><u>Unveiling the Magic of End Screens for Vimeo Content</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/kiW7sLvL65k?si=IHSeRFsYCrfqpn2o" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

