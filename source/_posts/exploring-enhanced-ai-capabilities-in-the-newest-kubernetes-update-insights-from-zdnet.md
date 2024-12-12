---
title: Exploring Enhanced AI Capabilities in the Newest Kubernetes Update – Insights From ZDNet
date: 2024-12-09T16:13:20.281Z
updated: 2024-12-12T17:06:18.672Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/056b5dc5bf38553fc5e62980ac558058cdfef6fae043dca04e140a16eeec969f.jpg
---

## Exploring Enhanced AI Capabilities in the Newest Kubernetes Update – Insights From ZDNet

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
<li><a href="https://article-helps.techidaily.com/new-online-meme-maker-for-2024/"><u>[New] Online MEME Maker for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-top-13-easy-to-master-revenue-strategies-on-reddit/"><u>[New] Top 13 Easy-to-Master Revenue Strategies on Reddit</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unlock-potential-androidandioss-top-free-overlay-tools-guide/"><u>[New] Unlock Potential Android&iOS's Top Free Overlay Tools Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unveiling-windows-11s-hidden-secrets-for-media-upload/"><u>[New] Unveiling Windows 11'S Hidden Secrets for Media Upload</u></a></li>
<li><a href="https://screen-capture.techidaily.com/updated-master-the-art-of-pc-game-memories-with-these-6-steps/"><u>[Updated] Master the Art of PC Game Memories with These 6 Steps</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-streamlining-your-editing-workflow-with-final-cut-pro-tips/"><u>[Updated] Streamlining Your Editing Workflow with Final Cut Pro Tips</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-ultimate-guide-of-hdr-photo-on-iphone-camera/"><u>[Updated] The Ultimate Guide of HDR Photo on iPhone Camera</u></a></li>
<li><a href="https://fox-helps.techidaily.com/2024-approved-elite-imagery-the-finest-8k-camera-selections/"><u>2024 Approved Elite Imagery The Finest 8K Camera Selections</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unlock-the-full-potential-of-media-player-through-subtitles/"><u>2024 Approved Unlock the Full Potential of Media Player Through Subtitles</u></a></li>
<li><a href="https://games-able.techidaily.com/debunking-high-res-pixel-myths-in-consoles/"><u>Debunking High-Res Pixel Myths in Consoles</u></a></li>
<li><a href="https://youtube-sure.techidaily.com/oad-youtube-videos-on-android-9-powerful-apps-compared-for-2024/"><u>Download YouTube Videos on Android 9 Powerful Apps Compared for 2024</u></a></li>
<li><a href="https://hardware-updates.techidaily.com/improve-your-pcs-performance-with-free-gigabyte-ethernet-card-driver-downloads/"><u>Improve Your PC's Performance with Free Gigabyte Ethernet Card Driver Downloads!</u></a></li>
<li><a href="https://visual-screen-recording.techidaily.com/in-2024-capturing-every-detail-tactics-for-streamlined-meet-recordings/"><u>In 2024, Capturing Every Detail Tactics for Streamlined Meet Recordings</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-striking-14-text-animation-illustrations/"><u>In 2024, Striking 14 Text Animation Illustrations</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-top-5-cloud-voice-editors-for-chrome-os-transforming-your-tone-and-pitch/"><u>In 2024, Top 5 Cloud Voice Editors for Chrome OS Transforming Your Tone and Pitch</u></a></li>
<li><a href="https://win-forum.techidaily.com/overcoming-installation-woes-effective-strategies-for-forced-uninstalls/"><u>Overcoming Installation Woes: Effective Strategies for Forced Uninstalls</u></a></li>
<li><a href="https://extra-support.techidaily.com/photo-deformation-masterclass-essentials-for-2024/"><u>Photo Deformation Masterclass Essentials for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/tips-for-removing-spotifys-auto-suggesting-podcasts-for-2024/"><u>Tips for Removing Spotify's Auto-Suggesting Podcasts for 2024</u></a></li>
<li><a href="https://buynow-info.techidaily.com/ultimate-guide-leading-gaming-systems-in-2eplust-2024/"><u>Ultimate Guide: Leading Gaming Systems in 2E+t 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/9ECz3oZ8NrQ?si=86vkwkDJo9HQXpzt" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

