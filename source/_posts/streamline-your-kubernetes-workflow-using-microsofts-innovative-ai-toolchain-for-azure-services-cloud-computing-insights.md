---
title: Streamline Your Kubernetes Workflow Using Microsoft's Innovative AI Toolchain for Azure Services | Cloud Computing Insights
date: 2025-01-05T03:09:17.932Z
updated: 2025-01-06T00:10:36.146Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/cloud/    https://www.zdnet.com/a/img/resize/b9d7177e858bfd9e7c81af39358e35b97f29cb01/2023/11/15/70107afd-5319-4539-b65e-0174033c25cd/abstract3dgettyimages-1404344027.jpg?width=170&height=96&fit=crop&auto=webp
---

## Streamline Your Kubernetes Workflow Using Microsoft's Innovative AI Toolchain for Azure Services | Cloud Computing Insights

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
<li><a href="https://fox-direct.techidaily.com/new-2024-approved-gopro-hero-5-vs-nikon-km-170-for-adventurers/"><u>[New] 2024 Approved GoPro HERO 5 vs Nikon KM-170 for Adventurers</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/new-2024-approved-mastering-ig-videos-building-a-powerful-focused-marketing-plan/"><u>[New] 2024 Approved Mastering IG Videos Building a Powerful, Focused Marketing Plan</u></a></li>
<li><a href="https://facebook-video-share.techidaily.com/new-in-2024-elevate-your-youtube-presentations-with-imovie-editing-skills/"><u>[New] In 2024, Elevate Your YouTube Presentations with iMovie Editing Skills</u></a></li>
<li><a href="https://facebook-videos.techidaily.com/new-in-2024-linking-your-favorite-tiktoks-seamlessly-to-facebook/"><u>[New] In 2024, Linking Your Favorite TikToks Seamlessly to Facebook</u></a></li>
<li><a href="https://some-tips.techidaily.com/adapting-cyber-defense-tactics-amidst-the-challenges-of-legacy-infrastructure/"><u>Adapting Cyber Defense Tactics Amidst the Challenges of Legacy Infrastructure</u></a></li>
<li><a href="https://some-tips.techidaily.com/atandt-and-ibm-unveil-new-collaborative-innovation-hub-aimed-at-government-services-zdnet/"><u>AT&T and IBM Unveil New Collaborative Innovation Hub Aimed at Government Services - ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/avoid-top-10-cloud-computing-blunders-insights-from-zdnet/"><u>Avoid Top 10 Cloud Computing Blunders - Insights From ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/best-cryptocurrency-exchanges-of-2022-a-comprehensive-guide-to-top-platforms-you-shouldnt-miss/"><u>Best Cryptocurrency Exchanges of 2022: A Comprehensive Guide to Top Platforms You Shouldn't Miss</u></a></li>
<li><a href="https://some-tips.techidaily.com/enhancing-cybersecurity-with-single-sign-on-and-multi-factor-authentication-strategies-by-global-organizations-zdnet/"><u>Enhancing Cybersecurity with Single Sign-On & Multi-Factor Authentication Strategies by Global Organizations | ZDNet</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/excellent-streamers-guide-to-360-degree-live-footage-for-2024/"><u>Excellent Streamers' Guide to 360-Degree Live Footage for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/explore-aws-newest-innovation-ai-powered-enterprise-chatbot-now-available-at-zero-cost-discover-the-easy-steps-on-zdnet/"><u>Explore AWS Newest Innovation: AI-Powered Enterprise Chatbot Now Available at Zero Cost – Discover the Easy Steps on ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/exploring-the-impact-of-international-alliances-on-cyber-defense-insights-from-government-leaders-zdnet/"><u>Exploring the Impact of International Alliances on Cyber Defense: Insights From Government Leaders - ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/future-proofing-asia-how-singapore-unveils-its-master-blueprint-for-generative-ai-and-self-governing-tech-systems-zdnet/"><u>Future-Proofing Asia: How Singapore Unveils Its Master Blueprint for Generative AI and Self-Governing Tech Systems | ZDNet</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/optimiza-la-calidad-de-tus-videos-con-inteligencia-artificial-como-usar-winxvideo-para-el-mejor-rendimiento/"><u>Optimiza La Calidad De Tus Videos Con Inteligencia Artificial: Cómo Usar Winxvideo Para El Mejor Rendimiento</u></a></li>
<li><a href="https://some-skills.techidaily.com/syncing-sonata-to-still-images-in-the-cyberrealm-for-2024/"><u>Syncing Sonata to Still Images in the Cyberrealm for 2024</u></a></li>
<li><a href="https://driver-install.techidaily.com/the-essential-guide-to-connecting-gear-with-drivers/"><u>The Essential Guide to Connecting Gear with Drivers</u></a></li>
<li><a href="https://mondly-stories.techidaily.com/vocal-acrobatics-mastering-intricate-language-forms/"><u>Vocal Acrobatics: Mastering Intricate Language Forms</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/kTHQrw8e1gk?si=gTPIa7KjhSZ0Vz97" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

