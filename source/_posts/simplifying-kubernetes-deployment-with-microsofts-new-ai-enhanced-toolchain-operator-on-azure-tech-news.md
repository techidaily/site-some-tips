---
title: Simplifying Kubernetes Deployment with Microsoft's New AI-Enhanced Toolchain Operator on Azure | Tech News
date: 2024-12-15T17:44:43.733Z
updated: 2024-12-21T01:31:16.516Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/cloud/    https://www.zdnet.com/a/img/resize/b9d7177e858bfd9e7c81af39358e35b97f29cb01/2023/11/15/70107afd-5319-4539-b65e-0174033c25cd/abstract3dgettyimages-1404344027.jpg?width=170&height=96&fit=crop&auto=webp
---

## Simplifying Kubernetes Deployment with Microsoft's New AI-Enhanced Toolchain Operator on Azure | Tech News

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
<li><a href="https://fox-http.techidaily.com/updated-2024-approved-the-ultimate-guide-to-facetune-photo-enhancement/"><u>[Updated] 2024 Approved The Ultimate Guide to Facetune Photo Enhancement</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/updated-in-2024-vid-recorders-vault-top-techniques-for-tv-streaming/"><u>[Updated] In 2024, Vid-Recorder's Vault Top Techniques for TV Streaming</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-transform-textual-treasures-ae-font-exploration/"><u>2024 Approved Transform Textual Treasures AE Font Exploration</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unlocking-the-secrets-of-memetic-success-through-gifs/"><u>2024 Approved Unlocking the Secrets of Memetic Success Through GIFs</u></a></li>
<li><a href="https://win-solutions.techidaily.com/advanced-solutions-for-fixing-call-of-dutys-modern-warfare-memory-issue-error-12707/"><u>Advanced Solutions for Fixing Call of Duty's Modern Warfare Memory Issue (Error 12707)</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-vector-journey-start-categories-tools-and-initial-steps/"><u>In 2024, Vector Journey Start Categories, Tools, & Initial Steps</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/raspberry-pi-hat-compilation-2024-choosing-the-right-add-on-for-your-innovative-creations/"><u>Raspberry Pi HAT Compilation 2024: Choosing the Right Add-On for Your Innovative Creations</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-ultimate-guide-watching-basketball-with-precision-for-2024/"><u>The Ultimate Guide Watching Basketball with Precision for 2024</u></a></li>
<li><a href="https://tech-hub.techidaily.com/top-10-desired-visionos-enhancements-what-we-hope-apple-unveils-at-the-upcoming-wwdc-event/"><u>Top 10 Desired VisionOS Enhancements: What We Hope Apple Unveils at the Upcoming WWDC Event</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-tier-free-memes-for-everyday-chuckles-for-2024/"><u>Top-Tier Free Memes for Everyday Chuckles for 2024</u></a></li>
<li><a href="https://driver-error.techidaily.com/unlock-hidden-hardware-on-win-1011-pcs/"><u>Unlock Hidden Hardware on WIN 10/11 PCs</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/620kcQ7Dw7w?si=a5ussGs5HV7sG3hF" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

