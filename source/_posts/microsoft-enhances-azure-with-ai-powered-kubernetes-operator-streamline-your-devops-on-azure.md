---
title: Microsoft Enhances Azure with AI-Powered Kubernetes Operator - Streamline Your DevOps on Azure
date: 2024-12-16T20:50:43.414Z
updated: 2024-12-20T22:13:47.505Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/cloud/    https://www.zdnet.com/a/img/resize/b9d7177e858bfd9e7c81af39358e35b97f29cb01/2023/11/15/70107afd-5319-4539-b65e-0174033c25cd/abstract3dgettyimages-1404344027.jpg?width=170&height=96&fit=crop&auto=webp
---

## Microsoft Enhances Azure with AI-Powered Kubernetes Operator - Streamline Your DevOps on Azure

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
<li><a href="https://instagram-videos.techidaily.com/new-in-2024-quick-guide-to-infusing-new-flair-in-old-content-using-instagram-features/"><u>[New] In 2024, Quick Guide to Infusing New Flair in Old Content Using Instagram Features</u></a></li>
<li><a href="https://fox-blue.techidaily.com/updated-disable-snippet-view-in-youtube-for-full-content/"><u>[Updated] Disable Snippet View in YouTube for Full Content</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-art-of-transcribing-dreams-into-movies/"><u>[Updated] The Art of Transcribing Dreams Into Movies</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unleash-photo-dynamics-mastering-adobe-illustrator-blurs/"><u>[Updated] Unleash Photo Dynamics Mastering Adobe Illustrator Blurs</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/2024-approved-high-speed-windows-photo-explorer-tool/"><u>2024 Approved High-Speed Window's Photo Explorer Tool</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-first-step-in-vlogging-tools-you-need/"><u>2024 Approved The First Step in Vlogging Tools You Need</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/how-to-mirror-your-realme-gt-5-screen-to-pc-with-chromecast-drfone-by-drfone-android/"><u>How to Mirror Your Realme GT 5 Screen to PC with Chromecast | Dr.fone</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-repair-corrupt-mp4-and-avi-files-of-samsung-galaxy-m34-5g-with-video-repair-utility-on-windows-by-stellar-video-repair-mobile-video-repair/"><u>How to Repair corrupt MP4 and AVI files of Samsung Galaxy M34 5G with Video Repair Utility on Windows?</u></a></li>
<li><a href="https://fox-tls.techidaily.com/identifying-and-resolving-hardware-compatibility-problems-with-yl-solutions/"><u>Identifying & Resolving Hardware Compatibility Problems with YL Solutions</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-snicker-spinner-picture-editor/"><u>In 2024, Snicker Spinner Picture Editor</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-path-to-success-starts-on-screen-10-must-see-films/"><u>In 2024, The Path to Success Starts on Screen 10 Must-See Films</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-transfer-tactics-efficiently-getting-data-on-your-computer/"><u>In 2024, Transfer Tactics Efficiently Getting Data On Your Computer</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unveiling-simple-techniques-for-amazing-slow-motion-footage-in-android/"><u>In 2024, Unveiling Simple Techniques for Amazing Slow-Motion Footage in Android</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-ultimate-guide-to-professional-iphoneipad-podcast-production-for-2024/"><u>The Ultimate Guide to Professional iPhone/iPad Podcast Production for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-ultimate-pp-playbook-for-silent-scene-transitions-for-2024/"><u>The Ultimate PP Playbook for Silent Scene Transitions for 2024</u></a></li>
<li><a href="https://unlock-android.techidaily.com/top-15-apps-to-hack-wifi-password-on-xiaomi-13-ultra-by-drfone-android/"><u>Top 15 Apps To Hack WiFi Password On Xiaomi 13 Ultra</u></a></li>
<li><a href="https://win-luxury.techidaily.com/top-essential-factors-to-assess-when-selecting-your-crypto-exchange-platform-insights-from-yl-computing-and-yl-software/"><u>Top Essential Factors to Assess When Selecting Your Crypto Exchange Platform - Insights From YL Computing & YL Software</u></a></li>
<li><a href="https://fox-that.techidaily.com/ultimate-guide-solving-hey-siri-issues-on-your-iphone-17-tips-and-tricks/"><u>Ultimate Guide: Solving 'Hey Siri' Issues On Your iPhone – 17 Tips & Tricks</u></a></li>
<li><a href="https://location-social.techidaily.com/why-your-whatsapp-location-is-not-updating-and-how-to-fix-on-htc-u23-pro-drfone-by-drfone-virtual-android/"><u>Why Your WhatsApp Location is Not Updating and How to Fix On HTC U23 Pro | Dr.fone</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/E3yY7lZ-FKA?si=g8VEuExP8GH59B69" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

