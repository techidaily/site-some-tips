---
title: "Simplifying Kubernetes Deployments: Discover the New AI Toolchain Feature for Microsoft's Azure Services"
date: 2025-01-06T20:24:31.155Z
updated: 2025-01-12T17:48:29.336Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/3bbc4ff17b35bac37e3335e5a66057aab2f13c2b088afea3c5a850da277e1159.jpg
---

## Simplifying Kubernetes Deployments: Discover the New AI Toolchain Feature for Microsoft's Azure Services

![abstract3dgettyimages-1404344027](https://www.zdnet.com/a/img/resize/85bc9f88ac3ef6fa6aab012219d710edb517f31f/2023/11/15/70107afd-5319-4539-b65e-0174033c25cd/abstract3dgettyimages-1404344027.jpg?auto=webp&width=1280)

Xuanyu Han/Getty Images

If you want to run [artificial intelligence](https://www.zdnet.com/article/what-is-ai-heres-everything-you-need-to-know-about-artificial-intelligence/) (AI) and machine learning applications such as large language models (LLMs) at scale, you must run them on [Kubernetes](https://www.zdnet.com/article/what-is-kubernetes-everything-your-business-needs-to-know/). However, mastering Kubernetes -- everyone's favorite container orchestrator -- isn't easy. That's where [Kubernetes Al toolchain operator](https://learn.microsoft.com/en-us/azure/aks/ai-toolchain-operator) \-- the latest addition to Microsoft's [Azure Kubernetes Service (AKS)](https://azure.microsoft.com/en-us/products/kubernetes-service) \-- comes in. 

**Also: [Microsoft Azure introduces Radius open-source development platform](https://www.zdnet.com/article/microsoft-azure-introduces-radius-an-open-source-development-platform-for-multi-cloud-computing/)**

AKS already makes Kubernetes on Azure easier. Instead of working it out by hand, AKS's built-in code-to-cloud pipelines and guardrails give you a faster way to start developing and deploying cloud-native apps in Azure. With its unified management and governance for on-premises, edge, and multi-cloud Kubernetes clusters, AKS also makes it simpler (there's no such thing as "simple" when it comes to Kubernetes) to integrate with Azure security, identity, cost management, and migration services.

What Kubernetes AI toolchain operator brings to the table are automated ways to run open-source software AI/ML workloads cost-effectively and with less manual configuration. It also automates LLM model deployment on AKS across available CPU and GPU resources by selecting the optimally sized infrastructure for your LLM or other project.

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

AI toolchain operator does this by automatically provisioning the necessary GPU nodes and setting up the associated [inference server](https://www.gigabyte.com/Enterprise/Server?fid=2364) as an endpoint server to your AI models. An inference server, such as [Hugging Face's 7B](https://huggingface.co/tiiuae/falcon-7b) or [NVIDIA Triton Inference Server](https://developer.nvidia.com/triton-inference-server), applies trained AI models to incoming data to make real-time decisions. Inference is the process of running live data through a trained AI model to make a prediction or solve a task. Using this add-on reduces your onboarding time and enables you to focus on AI model usage and development rather than infrastructure setup.

It also makes it possible to easily split inferencing across multiple lower-GPU-count virtual machines (VMs). This means you can run your LLMs on more Azure regions, thus eliminating wait times for Azure regions with higher GPU-count VMs and lowering overall cost. In other words, you can automatically run your LLMs on lower-power, less-expensive regions. Yes, you may lose processing power, but not all jobs require higher horsepower. 

**Also: [I went hands-on with Microsoft's new AI features, and these 5 are the most useful](https://www.zdnet.com/article/i-went-hands-on-with-microsofts-new-ai-features-and-these-5-are-the-most-useful/)**

Making it easier to set up, you can also choose from preset models with AKS-hosted images. This significantly reduces your overall service setup time. Once it's been up and running for a while, you can then adjust your Azure model to better fit your workload. 

Additionally, [Azure Kubernetes Fleet Manager](https://azure.microsoft.com/en-us/products/kubernetes-fleet-manager) enables multi-cluster and at-scale scenarios for AKS clusters. Platform admins who are managing Kubernetes fleets with many clusters often face challenges staging their updates in a safe and predictable way. This allows admins to orchestrate updates across multiple clusters by using update runs, stages, and groups. Since AI/ML workloads tend to be very demanding, this makes managing them much easier.

In short, if you want to do serious work with AI/ML on Azure, the Kubernetes Al toolchain operator demands your attention.

#### More Microsoft

[The best Windows laptop models: Comparing Dell, Samsung, Lenovo, and more](https://www.zdnet.com/article/best-windows-laptop/ "The best Windows laptop models: Comparing Dell, Samsung, Lenovo, and more")

[5 Microsoft Edge settings to change for more secure browsing than Chrome offers](https://www.zdnet.com/article/5-microsoft-edge-settings-to-change-for-more-secure-browsing-than-chrome-offers/ "5 Microsoft Edge settings to change for more secure browsing than Chrome offers")

[The best VPN for Windows: Expert tested](https://www.zdnet.com/article/best-vpn-for-windows-pc/ "The best VPN for Windows: Expert tested")

[How to recover deleted files in Windows 10 or 11](https://www.zdnet.com/article/how-to-recover-deleted-files-in-windows-10-or-11/ "How to recover deleted files in Windows 10 or 11")

* [The best Windows laptop models: Comparing Dell, Samsung, Lenovo, and more](https://www.zdnet.com/article/best-windows-laptop/ "The best Windows laptop models: Comparing Dell, Samsung, Lenovo, and more")
* [5 Microsoft Edge settings to change for more secure browsing than Chrome offers](https://www.zdnet.com/article/5-microsoft-edge-settings-to-change-for-more-secure-browsing-than-chrome-offers/ "5 Microsoft Edge settings to change for more secure browsing than Chrome offers")
* [The best VPN for Windows: Expert tested](https://www.zdnet.com/article/best-vpn-for-windows-pc/ "The best VPN for Windows: Expert tested")
* [How to recover deleted files in Windows 10 or 11](https://www.zdnet.com/article/how-to-recover-deleted-files-in-windows-10-or-11/ "How to recover deleted files in Windows 10 or 11")

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
<li><a href="https://screen-sharing-recording.techidaily.com/new-dissecting-the-full-package-logitechs-4k-webcam-experience/"><u>[New] Dissecting the Full Package Logitech’s 4K Webcam Experience</u></a></li>
<li><a href="https://vp-tips.techidaily.com/new-techniques-to-realize-time-bending-scenes/"><u>[New] Techniques to Realize Time-Bending Scenes</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/updated-2024-approved-mastering-the-art-of-motion-creating-engaging-profitable-fb-ads/"><u>[Updated] 2024 Approved Mastering the Art of Motion Creating Engaging, Profitable FB Ads</u></a></li>
<li><a href="https://network-issues.techidaily.com/address-slow-response-roblox-windows-edition/"><u>Address Slow Response: Roblox Windows Edition</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/beyond-the-hype-an-objective-look-at-bose-quiet-control-30/"><u>Beyond the Hype: An Objective Look at Bose Quiet Control 30</u></a></li>
<li><a href="https://some-tips.techidaily.com/discover-the-ultimate-bbq-toolkit-of-2022-expert-picks-from-zdnet/"><u>Discover the Ultimate BBQ Toolkit of 2022 - Expert Picks From ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/ecoflow-river-3-an-unparalleled-choice-in-top-tier-portable-power-solutions-insights-from-an-expert-test/"><u>EcoFlow River ^3: An Unparalleled Choice in Top-Tier Portable Power Solutions - Insights From an Expert Test</u></a></li>
<li><a href="https://some-tips.techidaily.com/essential-strategies-for-growing-a-lush-garden-insights-from-zdnet/"><u>Essential Strategies for Growing a Lush Garden - Insights From ZDNET</u></a></li>
<li><a href="https://some-tips.techidaily.com/experience-brighter-nights-sooner-top-quality-govee-permanent-outdoor-lights-are-here-set-them-up-this-weekend-for-an-illuminated-transformation-zdnet/"><u>Experience Brighter Nights Sooner: Top-Quality Govee Permanent Outdoor Lights Are Here | Set Them Up This Weekend for an Illuminated Transformation [ZDNet]</u></a></li>
<li><a href="https://some-tips.techidaily.com/experience-unparalleled-joy-with-a-remote-controlled-lawnmower-your-ultimate-guide-to-stress-free-yard-work/"><u>Experience Unparalleled Joy with a Remote-Controlled Lawnmower: Your Ultimate Guide to Stress-Free Yard Work</u></a></li>
<li><a href="https://some-tips.techidaily.com/expert-picks-ultimate-guide-to-the-most-efficient-electric-grills-for-2eby2023-insights-from-zdnet/"><u>Expert Picks: Ultimate Guide to the Most Efficient Electric Grills for 2Eby2023 – Insights From ZDNET</u></a></li>
<li><a href="https://some-tips.techidaily.com/exploring-the-future-of-lawn-care-my-impressive-encounter-with-robot-mower-tesla-cybertruck-tech-insights-by-zdnet/"><u>Exploring the Future of Lawn Care: My Impressive Encounter with Robot Mower Tesla Cybertruck | Tech Insights by ZDNet</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/step-by-step-tutorial-utilizing-googles-magic-eraser-feature-across-mobile-devices-androidiphone/"><u>Step-by-Step Tutorial: Utilizing Google's Magic Eraser Feature Across Mobile Devices (Android/iPhone)</u></a></li>
<li><a href="https://novels-ebooks.techidaily.com/210593751-9798218018191-the-betrayal-how-i-continue-to-overcome-its-not-personal-its-facts-revised/"><u>The Betrayal & HOW I CONTINUE TO OVERCOME IT'S NOT PERSONAL - IT'S FACTS (REVISED) | Free Book</u></a></li>
<li><a href="https://fake-location.techidaily.com/thinking-about-changing-your-netflix-region-without-a-vpn-on-vivo-y100i-drfone-by-drfone-virtual-android/"><u>Thinking About Changing Your Netflix Region Without a VPN On Vivo Y100i? | Dr.fone</u></a></li>
<li><a href="https://howto.techidaily.com/vivo-y17s-screen-unresponsive-heres-how-to-fix-it-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Vivo Y17s Screen Unresponsive? Heres How to Fix It | Dr.fone</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/pejPLJBLmXw?si=WD97jA3doqbMCkCX" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

