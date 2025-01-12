---
title: Microsoft Azure Introduces AI Models as a Service and Advanced RAG Solutions for Business-Scale Generative AI - ZDNet
date: 2025-01-05T20:40:00.712Z
updated: 2025-01-12T16:49:30.613Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/cloud/    https://www.zdnet.com/a/img/resize/9e3345b33081ac18b2f8a9c4262cd077e0467eb5/2024/05/21/74b4d81a-1ca6-4e36-9ee9-b470f1871b49/img-3188.jpg?width=170&height=96&fit=crop&auto=webp
---

## Microsoft Azure Introduces AI Models as a Service and Advanced RAG Solutions for Business-Scale Generative AI - ZDNet

![Microsoft sign at Build](https://www.zdnet.com/a/img/resize/14a22ec6cc9ef498000ff589414ea861bf0caea7/2024/05/21/74b4d81a-1ca6-4e36-9ee9-b470f1871b49/img-3188.jpg?auto=webp&width=1280)

Sabrina Ortiz/ZDNET

At its annual Build developer conference on Tuesday, Microsoft unveiled several new capabilities of its Azure AI Services within its Azure cloud computing business, with a focus on [generative artificial intelligence](https://www.zdnet.com/article/what-is-generative-ai-and-why-is-it-so-popular-heres-everything-you-need-to-know/). 

The new capabilities range from enabling greater database access to automatically dubbing videos into multiple languages to rapid training of large language models to understand complex document structures. Most of the innovations and enhancements are already in preview mode this week.

## **It starts with Studio** 

Perhaps most relevant to most developers, Microsoft has enhanced its integrated development environment for AI, [Azure AI Studio](https://ai.azure.com). 

To tie together all the pieces that go into making a cloud application on Azure, Microsoft has amplified what's called [Azure Developer CLI](https://learn.microsoft.com/en-us/azure/developer/azure-developer-cli/overview), a set of templated commands used to deploy applications to the cloud. A feature in preview lets a developer "create resources in copilot sample repositories and facilitate large language model operations (LLM Ops) as part of continuous integration/continuous delivery (CI/CD) solutions to accelerate code-to-cloud workflows."

**Also:** [**Microsoft Build is this week - here's what to expect, how to watch, and why I'm excited**](https://www.zdnet.com/article/microsoft-build-is-this-week-heres-what-to-expect-how-to-watch-and-why-im-excited/)

Another upcoming feature of Azure AI Studio is what Microsoft calls "Models as a Service," where a selection of large language models will be invokable by programmers as an API without having to manage the GPU infrastructure for the models, said Microsoft.

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/Nyp7-xVwqHA?si=XCuZbpKLFIdrGQQh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## **Rapidly understand complex documents**

Microsoft is also introducing a new type of AI model called "custom generative," a way to rapidly develop a language model to process complex documents by using templates to define the structure of a document. The approach reduces the number of "labels" a developer needs to craft, the metadata that teaches an AI model about the various fields in a document.

"The model will use large language models (LLMs) to extract the fields, and users will only need to correct the output when the model does not get a field right," said Microsoft. 

**Also: [Every Copilot+ PC Microsoft just announced to take on Apple's M3 MacBooks](https://www.zdnet.com/article/every-copilot-pc-microsoft-just-announced-to-take-on-apples-m3-macbooks/)**

Custom generative is going into preview "soon," said Microsoft. 

A slew of additional features are meant to facilitate the multiple parts of creating a generative AI app, from "prompt flow" to the tracing and debugging to the stats on Gen AI once put into production.

## **Expanded use of RAG**

For enterprises wanting to base large language models on their own data, both to particularize the results of queries and also to avoid hallucinations, the company has updated its Azure AI Search. The service is based on what's called retrieval-augmented generation, or, "RAG," a widespread practice of looking for the answers to a prompt in a database instead of just searching the most recent prompts. 

New capabilities for Azure AI Search include enhancements to the way the service scores results stored as "vectors," compressed representations of data that are suited to LLMs. The changes "give customers more options and flexibility to improve the accuracy of their responses," said Microsoft.

The service also adds the ability to turn images, not just text, into vectors, to make it easier for LLMs to retrieve images for a query response.

**Also: [3 AI features coming to Copilot+ PCs that I wish were on my MacBook](https://www.zdnet.com/article/3-ai-features-coming-to-copilot-pcs-that-i-wish-were-on-my-macbook/)**

It will also be easier to connect the Azure AI Search service to corporate data by using Fabric, the data analytics platform [unveiled at Build last year](https://www.zdnet.com/article/microsoft-unveils-fabric-analytics-program-onelake-data-lake-to-span-cloud-providers/), through a connector that routes data contained in the OneLake data lake, also unveiled last year. 

Microsoft emphasizes the ability to scale the RAG function with large vector sizes and expanded storage capability in Azure AI Search.

The functions are available in Azure AI Search in a preview form now.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/_SbYznUy_zY?si=ThBkP934r3mizi48" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## **Database enhancements**

While RAG is useful in and of itself, most companies will need to retrieve data with a combination of traditional database retrieval methods. In a blog post, Shireesh Thota, who is corporate vice president in charge of Azure Databases, writes in a blog post that: "As AI applications become more mainstream, seamless database management is paramount. Trusted solutions that can scale limitlessly and autonomously, respond fast, and offer unparalleled flexibility and reliability will shape the future of coding."

**Also: [6 ways AI can help launch your next business venture](https://www.zdnet.com/article/6-ways-ai-can-help-launch-your-next-business-venture/)**

For that reason, Microsoft has added to its database offerings features that are critical to large language model deployment: "vector search," which allows the compressed representation of content to be indexed and more easily retrieved; and "embeddings," a means to compress input data for a language model on the front end so it can be stored in a way familiar to the database. 

Azure Cosmos DB for NoSQL extends the Azure Cosmos database to perform vector search. Microsoft says it makes Cosmos the first cloud database with "lower latency vector search at cloud scale without the need to manage servers."

Azure Database for PostgreSQL in-database embedding updates the Azure implementation of the venerable PostgreSQL database so it can automatically compress input data into representations the LLM understands.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/e4Nt2xXXtmE?si=CtKwFry4b0AJXnaN" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## **On-ramp to app development** 

Several new offerings are meant to standardize the way generative AI apps are developed. They include "patterns and practices for private chatbots," a collection of reference implementations that Microsoft says enable enterprises to "create private chatbots that are reliable, cost-efficient and compliant."

The chatbot templates are available now. 

## **New multimodality**

No developer AI conference would be complete without some new models. Microsoft unveiled an addition to its "Phi" family of language models, [introduced a year ago](https://azure.microsoft.com/en-us/blog/introducing-phi-3-redefining-whats-possible-with-slms/). Phi are made to be small, meaning, having a not-very-large amount of parameters, or, neural "weights," so that they could be employed on "edge" devices such as a PC. A new version, Phi-3-Vision now supports performing queries on images. 

"Sized at 4.2 billion parameters, Phi-3-vision supports general visual reasoning tasks and chart/graph/table reasoning," said Microsoft. 

In addition to the Phi updates, Microsoft announced availability of OpenAI's newest large language model, GPT-4o, [introduced last week](https://www.zdnet.com/article/6-ways-openai-just-supercharged-chatgpt-for-free-users/), in Azure AI Studio in preview form. Studio also gains OpenAI's GPT-4 "Turbo with vision capabilities," which was [rolled out last month by OpenAI](https://www.zdnet.com/article/openai-makes-gpt-4-turbo-with-vision-available-for-developers/). GPT-4 with vision, said Microsoft, "introduces a new dimension to AI apps, enabling the creation of content that spans across text, images and more, for a richer user experience. 

"This, along with the new capabilities of Microsoft Azure AI Enterprise Chat (previously known as On Your Data) integrated with retrieval-augmented generation (RAG), marks the beginning of an era for multimodal AI apps, providing developers with the tools to build more intuitive and interactive solutions. This update is now generally available."

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/it8VkxDUdAc?si=ef6VZWR7kW4P9ikh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## **Customizing the guardrails**

Microsoft's rolling out tools to allow organizations to tweak what kinds of guardrails are imposed on generative AI. "Custom Categories" lets the developer create filters of their choosing to particularize content restrictions. "This new feature also includes a rapid option, enabling you to deploy new custom filters within an hour to protect against emerging threats and incidents," said Microsoft. 

Another feature, in preview, "prompt shields," is meant to block jailbreak attacks against large language models, which can often be achieved via simply crafting a prompt in a clever way.

Both capabilities are part of Microsoft's [Azure AI Content Safety offering](https://azure.microsoft.com/en-us/products/ai-services/ai-content-safety/?ef%5Fid=%5Fk%5FCj0KCQjwjLGyBhCYARIsAPqTz18NpuoRrMlLnci02eTazSJqIEOh2gzy0dXSZ9DbQL6tB87CU-w6VEsaAqMbEALw%5FwcB%5Fk%5F&OCID=AIDcmm5edswduu%5FSEM%5F%5Fk%5FCj0KCQjwjLGyBhCYARIsAPqTz18NpuoRrMlLnci02eTazSJqIEOh2gzy0dXSZ9DbQL6tB87CU-w6VEsaAqMbEALw%5FwcB%5Fk%5F&gad%5Fsource=1&gclid=Cj0KCQjwjLGyBhCYARIsAPqTz18NpuoRrMlLnci02eTazSJqIEOh2gzy0dXSZ9DbQL6tB87CU-w6VEsaAqMbEALw%5FwcB). 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/tkpBmccvJ_Q?si=J7ellPL1G1l8Axi_" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## **Speak the speech**

Following the path of models such as [Google's Gemini](https://www.zdnet.com/article/what-is-google-gemini/) and [OpenAI's GPT-4o](https://www.zdnet.com/article/i-put-gpt-4o-through-my-coding-tests-and-it-aced-them-except-for-one-weird-result/), Microsoft is placing greater emphasis on giving voice to programs. Two capabilities in preview include analytical tools to survey audio and video data for things such as sentiment analysis, and a video dubbing service that can automatically translate a video into multiple languages. 

#### Featured

[Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how](https://www.zdnet.com/article/wi-fi-problems-how-to-add-a-wired-network-to-your-home-without-ethernet-cable/ "Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how")

[The best smart rings you can buy: Expert tested](https://www.zdnet.com/article/best-smart-ring/ "The best smart rings you can buy: Expert tested")

[One of the best budget tablets I've tested replaced both my Kindle and iPad](https://www.zdnet.com/article/one-of-the-best-budget-tablets-ive-tested-replaced-bot-my-kindle-and-ipad/ "One of the best budget tablets I've tested replaced both my Kindle and iPad")

[Wiping a Windows laptop? Here's the safest free way to erase your personal data](https://www.zdnet.com/article/wiping-a-windows-laptop-heres-the-safest-free-way-to-erase-your-personal-data/ "Wiping a Windows laptop? Here's the safest free way to erase your personal data")

* [Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how](https://www.zdnet.com/article/wi-fi-problems-how-to-add-a-wired-network-to-your-home-without-ethernet-cable/ "Wi-Fi problems? Add a wired network to your home without Ethernet cable - here's how")
* [The best smart rings you can buy: Expert tested](https://www.zdnet.com/article/best-smart-ring/ "The best smart rings you can buy: Expert tested")
* [One of the best budget tablets I've tested replaced both my Kindle and iPad](https://www.zdnet.com/article/one-of-the-best-budget-tablets-ive-tested-replaced-bot-my-kindle-and-ipad/ "One of the best budget tablets I've tested replaced both my Kindle and iPad")
* [Wiping a Windows laptop? Here's the safest free way to erase your personal data](https://www.zdnet.com/article/wiping-a-windows-laptop-heres-the-safest-free-way-to-erase-your-personal-data/ "Wiping a Windows laptop? Here's the safest free way to erase your personal data")

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
<li><a href="https://fox-http.techidaily.com/new-speedy-shutterbugs-iphones-quick-time-lapse-guide-for-2024/"><u>[New] Speedy Shutterbugs IPhone's Quick Time-Lapse Guide for 2024</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/updated-disentangle-focus-from-webcams-surroundings/"><u>[Updated] Disentangle Focus From Webcam's Surroundings</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/2024-approved-pros-choice-of-top-slo-mo-mobile-photography-apps-on-ios-and-android/"><u>2024 Approved Pro's Choice of Top Slo-Mo Mobile Photography Apps on iOS & Android</u></a></li>
<li><a href="https://some-tips.techidaily.com/boost-your-android-phones-endurance-top-10-settings-adjustments-to-maximize-battery-life-featured-on-zdnet/"><u>Boost Your Android Phone's Endurance: Top 10 Settings Adjustments to Maximize Battery Life, Featured on ZDNET</u></a></li>
<li><a href="https://some-tips.techidaily.com/discover-the-ultimate-reading-experience-the-latest-chrome-extension-enhances-your-future-reading-game/"><u>Discover the Ultimate Reading Experience: The Latest Chrome Extension Enhances Your Future-Reading Game!</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-sign-excel-2023-document-with-digital-signature-tutorial-by-ldigisigner-sign-a-excel-sign-a-excel/"><u>How to Sign Excel 2023 document with Digital Signature - (Tutorial)</u></a></li>
<li><a href="https://android-location-track.techidaily.com/how-to-track-google-pixel-fold-by-phone-number-drfone-by-drfone-virtual-android/"><u>How to Track Google Pixel Fold by Phone Number | Dr.fone</u></a></li>
<li><a href="https://extra-skills.techidaily.com/in-2024-insightful-review-best-text-overlays-for-adobe-ae/"><u>In 2024, Insightful Review Best Text Overlays for Adobe AE</u></a></li>
<li><a href="https://some-tips.techidaily.com/mastering-google-keep-for-effective-group-task-management-insights-and-tips-from-zdnet/"><u>Mastering Google Keep for Effective Group Task Management: Insights & Tips From ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/step-by-step-guide-to-migrating-your-whatsapp-messages-when-upgrading-to-iphone/"><u>Step-by-Step Guide to Migrating Your WhatsApp Messages When Upgrading to iPhone</u></a></li>
<li><a href="https://some-tips.techidaily.com/step-by-step-tutorial-on-activating-proactive-email-notifications-in-gmail-zdnet/"><u>Step-by-Step Tutorial on Activating Proactive Email Notifications in Gmail | ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-ranking-student-friendly-chromebooks-thorough-reviews-and-comparisons-by-industry-experts-zdnet/"><u>Top-Ranking Student-Friendly Chromebooks: Thorough Reviews & Comparisons by Industry Experts | ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/unboxing-the-future-of-computing-zdnet-review-on-the-most-upgradeable-and-repairable-laptop-the-framework-chromebook/"><u>Unboxing the Future of Computing: ZDnet Review on the Most Upgradeable & Repairable Laptop - The Framework Chromebook</u></a></li>
<li><a href="https://techno-recovery.techidaily.com/unraveling-the-differences-a-side-by-side-look-at-cat5-vs-cat6-ethernet-cables/"><u>Unraveling the Differences: A Side-by-Side Look at Cat5 vs Cat6 Ethernet Cables</u></a></li>
<li><a href="https://video-creation-software.techidaily.com/updated-the-ultimate-list-of-gif-speed-changer-apps-and-websites/"><u>Updated The Ultimate List of GIF Speed Changer Apps and Websites</u></a></li>
<li><a href="https://win11.techidaily.com/windows-without-bitlocker-here-are-4-steps-to-stay-secure/"><u>Windows Without Bitlocker? Here Are 4 Steps to Stay Secure</u></a></li>
</ul></div>

