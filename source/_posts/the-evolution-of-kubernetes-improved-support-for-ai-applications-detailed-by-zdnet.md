---
title: "The Evolution of Kubernetes: Improved Support for AI Applications Detailed by ZDNet"
date: 2025-01-10T16:26:29.712Z
updated: 2025-01-12T17:16:07.937Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/609392eeb7e6d07659b5310d5497d83d3c111a4e7e0b8902513730d25dcd2f24.png
---

## The Evolution of Kubernetes: Improved Support for AI Applications Detailed by ZDNet

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
<li><a href="https://youtube-tips.techidaily.com/ed-accelerate-engagement-implementing-the-top-12-video-growth-strategies-for-2024/"><u>[Updated] Accelerate Engagement - Implementing the Top 12 Video Growth Strategies for 2024</u></a></li>
<li><a href="https://fox-links.techidaily.com/2024-approved-chucklechief-easy-meme-design-tool/"><u>2024 Approved ChuckleChief Easy Meme Design Tool</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/2024-approved-easy-guide-to-instagram-post-duplication/"><u>2024 Approved Easy Guide to Instagram Post Duplication</u></a></li>
<li><a href="https://screen-activity-recording.techidaily.com/2024-approved-secure-mp3-conversion-of-live-skype-talks/"><u>2024 Approved Secure MP3 Conversion of Live Skype Talks</u></a></li>
<li><a href="https://apple-account.techidaily.com/how-to-remove-an-airtag-from-your-apple-id-account-on-apple-iphone-8-by-drfone-ios/"><u>How to Remove an AirTag from Your Apple ID Account On Apple iPhone 8?</u></a></li>
<li><a href="https://some-tips.techidaily.com/how-to-use-google-wallet-for-securely-storing-and-accessing-your-electronic-us-passport-online/"><u>How To Use Google Wallet for Securely Storing & Accessing Your Electronic US Passport Online</u></a></li>
<li><a href="https://extra-guidance.techidaily.com/in-2024-professional-stabilization-tech-for-youtube-content-creators/"><u>In 2024, Professional Stabilization Tech for YouTube Content Creators</u></a></li>
<li><a href="https://some-tips.techidaily.com/speedy-mac-tricks-unveiled-a-comprehensive-tutorial-for-using-google-keyboard-shortcuts-with-macos-systems/"><u>Speedy Mac Tricks Unveiled: A Comprehensive Tutorial for Using Google Keyboard Shortcuts with macOS Systems</u></a></li>
<li><a href="https://some-tips.techidaily.com/unihertz-titan-slim-smartphone-overview-insights-from-zdnet/"><u>Unihertz Titan Slim Smartphone Overview - Insights From ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/unleash-creative-potential-with-google-pixel-ns-cutting-edge-ai-photo-editing-expert-analysis-by-zdnet/"><u>Unleash Creative Potential with Google Pixel N's Cutting-Edge AI Photo Editing | Expert Analysis by ZDNET</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveiling-the-hidden-gem-why-the-economical-pixel-4a-pro-claims-the-spotlight-as-this-years-ultimate-value-packed-phone-by-google-android-central/"><u>Unveiling the Hidden Gem: Why the Economical Pixel 4a Pro Claims the Spotlight as This Year's Ultimate Value-Packed Phone by Google | Android Central</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/fHWdQw1gRyI?si=ve9wZnPupiooLThG" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

