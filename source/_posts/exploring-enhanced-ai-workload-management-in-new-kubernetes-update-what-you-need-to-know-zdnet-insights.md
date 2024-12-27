---
title: "Exploring Enhanced AI Workload Management in New Kubernetes Update: What You Need to Know | ZDNet Insights"
date: 2024-12-20T17:07:14.696Z
updated: 2024-12-27T16:32:27.174Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/1f78d2fb13516bc942d880b1ed451501538b368f9a6b178eea0c04126c8f2280.jpg
---

## Exploring Enhanced AI Workload Management in New Kubernetes Update: What You Need to Know | ZDNet Insights

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
<li><a href="https://instagram-clips.techidaily.com/new-2024-approved-how-to-get-more-followers-on-igtv-5-ways/"><u>[New] 2024 Approved How to Get More Followers on IGTV [5 Ways]</u></a></li>
<li><a href="https://fox-links.techidaily.com/new-elite-selection-top-ranked-free-ae-templates-for-2024/"><u>[New] Elite Selection Top-Ranked FREE AE Templates for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-superb-alter-ego-voice-tools-for-aspiring-vtubers/"><u>[New] Superb Alter-Ego Voice Tools For Aspiring VTubers</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-transform-your-images-on-android-our-picks-for-the-5-best-editors/"><u>[Updated] Transform Your Images on Android Our Picks for the 5 Best Editors</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unlocking-success-in-live-streaming-of-cricket-matches/"><u>2024 Approved Unlocking Success in Live Streaming of Cricket Matches</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unveiling-top-8-collaborative-video-collage-android-apps-freepremium/"><u>2024 Approved Unveiling Top 8 Collaborative Video Collage Android Apps (Free/Premium)</u></a></li>
<li><a href="https://tech-hub.techidaily.com/a-step-by-step-approach-to-boosting-productivity-through-chatgpt-integration/"><u>A Step-by-Step Approach to Boosting Productivity Through ChatGPT Integration</u></a></li>
<li><a href="https://fox-links.techidaily.com/echo-of-the-land-downloading-and-personalizing-tamil-ringtones/"><u>Echo of the Land Downloading & Personalizing Tamil Ringtones</u></a></li>
<li><a href="https://win11-tips.techidaily.com/how-to-resurrect-your-pcs-bluetooth-on-windows-11/"><u>How to Resurrect Your PC's Bluetooth on Windows 11</u></a></li>
<li><a href="https://easy-unlock-android.techidaily.com/how-to-unlock-nokia-xr21-pin-codepattern-lockpassword-by-drfone-android/"><u>How to Unlock Nokia XR21 PIN Code/Pattern Lock/Password</u></a></li>
<li><a href="https://fake-location.techidaily.com/how-to-use-special-features-virtual-location-on-zte-axon-40-lite-drfone-by-drfone-virtual-android/"><u>How To Use Special Features - Virtual Location On ZTE Axon 40 Lite? | Dr.fone</u></a></li>
<li><a href="https://iphone-unlock.techidaily.com/in-2024-everything-you-need-to-know-about-unlocked-apple-iphone-xs-drfone-by-drfone-ios/"><u>In 2024, Everything You Need To Know About Unlocked Apple iPhone XS | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-path-to-perfect-presentation-cutting-out-image-backdrops-on-canva/"><u>In 2024, The Path to Perfect Presentation Cutting Out Image Backdrops on Canva</u></a></li>
<li><a href="https://twitter-videos.techidaily.com/mastering-twitter-videos-adhere-to-aspect-ratio-rules-for-2024/"><u>Mastering Twitter Videos Adhere to Aspect Ratio Rules for 2024</u></a></li>
<li><a href="https://snapchat-videos.techidaily.com/top-15-creative-ways-to-use-filters-on-snapchat-for-2024/"><u>Top 15 Creative Ways to Use Filters on Snapchat for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-srt-enhancements-maximizing-performance-on-both-platforms-for-2024/"><u>Top SRT Enhancements Maximizing Performance on Both Platforms for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/ultimate-png-alterations-guide-for-2024/"><u>Ultimate PNG Alterations Guide for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-4k-potential-an-in-depth-look-at-dell-p2715q-for-2024/"><u>Unlocking 4K Potential An In-Depth Look at Dell P2715Q for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveiling-virtual-horizons-a-deep-dive-into-6-metaverse-cases-for-2024/"><u>Unveiling Virtual Horizons A Deep Dive Into 6 Metaverse Cases for 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/zAzTErKy6h8?si=vi5z3M9_7fW6qiAJ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

