---
title: Explore the Latest in Cloud Innovation with Azure's Radius Platform - The Key to Efficiently Managing Multi-Cloud Workloads on ZDNet
date: 2024-12-18T04:23:33.300Z
updated: 2024-12-21T22:04:10.511Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/c9d6a167ed41c7a19e897ff7ecbbd8652b5967c4/2023/10/27/170e8f0f-ffe9-4ee2-be8f-990d8e5fe867/gettyimages-952061104.jpg?width=278&height=156&fit=crop&auto=webp
---

## Explore the Latest in Cloud Innovation with Azure's Radius Platform - The Key to Efficiently Managing Multi-Cloud Workloads on ZDNet

![Microsoft logo](https://www.zdnet.com/a/img/resize/6f4a6e1fbcb34d1801c04af6e515d2052a8ccf14/2023/10/27/170e8f0f-ffe9-4ee2-be8f-990d8e5fe867/gettyimages-952061104.jpg?auto=webp&width=1280)

Kena Betancur/VIEWpress/Corbis via Getty Images

**Monterrey, California:** At the [Linux Foundation Members Summit](https://events.linuxfoundation.org/lf-member-summit/), [Microsoft Azure](https://azure.microsoft.com/en-us)'s CTO, Mark Russinovich, unveiled a groundbreaking open-source project, [Radius](https://radapp.io/). This cloud-native, application platform will enable developers and operators to define, deploy, and collaborate on cloud-native applications across public clouds and private infrastructure. 

First things first, if you're a serious enterprise user, you might be thinking: "That's not RADIUS!" You're right. It's not. The [Remote Authentication Dial-In User Service (RADIUS) protocol](https://www.techtarget.com/searchsecurity/definition/RADIUS) is commonly used in Microsoft software stacks to deliver remote and cloud Active Directory (AD) services. The cloud-native Radius has nothing to do with RADIUS. 

**Also: [Microsoft has over a million paying Github Copilot users: CEO Nadella](https://www.zdnet.com/article/microsoft-has-over-a-million-paying-github-copilot-users-ceo-nadella/)**

The new Radius aims to simplify the development, management, and operational hurdles in cloud-native computing's complex landscape. As Russionvitch said, "Cloud native technologies like Kubernetes have made building applications that can run anywhere easier." Indeed, as I've argued myself, [Kubernetes is the foundation for hybrid clouds.](https://www.zdnet.com/article/what-is-the-kubernetes-hybrid-cloud-and-why-it-matters/) 

But, that's much easier to say than to do. You may have noticed it's not simple at all to write an application that will run the same on Azure and, say, Amazon Web Services (AWS). 

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

As Russinovich explained, "While Kubernetes is a key enabler, we see many customers building abstractions over Kubernetes, usually focused on compute, to work around its limitations: Kubernetes has no formal definition of an application, it mingles infrastructure and application concepts, and it is overwhelmingly complex." You can say that again!

So, as "developers inevitably realize their applications require much more than Kubernetes, including support for dependencies like application programming interface (API) front ends, key-value stores, caches, and observability systems," Microsoft has introduced Radius to give them the additional tools.

**Also: [I took this free AI course for developers in one weekend and highly recommend it](https://www.zdnet.com/article/i-took-this-free-ai-course-for-developers-in-one-weekend-and-highly-recommend-it/)**

Russinovich added, "Radius meets application teams where they live by supporting not just Kubernetes, but other popular infrastructure tools such as Terraform and Bicep, and by integrating with existing [continuous integration and continuous delivery (CI/CD)](https://practical-tech.com/2018/07/10/continuous-integration-and-delivery-tool-basics/) systems such as [GitHub Actions](https://github.com/features/actions). Radius also supports multi-tier web-plus-data to complex microservice applications like [eShop](https://learn.microsoft.com/en-us/dotnet/architecture/cloud-native/introduce-eshoponcontainers-reference-app), a popular Microsoft microservices cloud reference application."

But, and this is the important bit, even though he mostly mentioned Microsoft and GitHub development tools, Radius is not an Azure-only program. It's meant to work over any cloud that uses Kubernetes. These days, that essentially means all clouds. 

He also noted that the modern shift from conventional two or three-tier [service-oriented architecture (SOA)](https://www.zdnet.com/article/soa-versus-microservices-how-are-they-different/) applications we learned in college or on our own to microservices and cloud-native-based applications is presenting us with new challenges around monitoring, management, and continuous updating. We're a long way from the bygone era of waterfall software development. 

**Also: [Microsoft is still paying for its mobile mistakes 10 years later](https://www.zdnet.com/article/microsoft-is-still-paying-for-its-mobile-mistakes-10-years-later/)**

Russinovich added that troubleshooting is notably tougher with the intertwined systems within applications. Furthermore, the enforcement of best practices within these applications remains a struggle for many developers.

So, it can be done, but the process of creating and deploying applications has become a convoluted exercise. Russiovich explained that today, our code is "tied together with baling wire and duct tape using Bash and PowerShell scripts. And so, creating an application has become just a jury-rigged kind of exercise. Not only that, but once you deploy the application, you can't see anything about the relationship between the resources. Find the front end here, the back end there, and you just don't understand what's going on here."

Radius is engineered to alleviate these challenges. For example, said Russonvich, "Radius automatically connects those components to their application by taking care of permissions, connection strings, and more." It also ensures the cloud infrastructure used by applications meets cost, operations, and security requirements. 

**Also: [Open source is actually the cradle of artificial intelligence. Here's why](https://www.zdnet.com/article/why-open-source-is-the-cradle-of-artificial-intelligence/)**

All these requirements are captured in [recipes](https://docs.radapp.io/guides/recipes/overview). These bind an application to its dependent infrastructure, which enables it to provide an [application graph](https://www.geeksforgeeks.org/applications-of-graph-data-structure/). This shows precisely how the application and infrastructure are interconnected. With these, your team can view and intuitively understand what makes up an application.

So, for example, you can have a recipe that calls on a [Redis](https://redis.io/) cache, a [MongoDB](https://www.mongodb.com/) database, and [Twilio](https://www.twilio.com/en-us) API communication links. The magic part is you can use a recipe to deploy an application not just to one cloud but to several different clouds at once. So, you can build hybrid or [multi-cloud](https://www.vmware.com/topics/glossary/content/multi-cloud.html) applications much more easily. On Azure, the recipe will call the appropriate Azure resources, on AWS, the AWS resources, and so on. 

**Also: [What Linux kernel maintainers do and why they need your help](https://www.zdnet.com/article/what-linux-kernel-maintainers-do-and-why-they-need-your-help/)**

This isn't just a good idea. Besides Microsoft, companies such as BlackRock, Comcast, and Millennium BCP are working together to ensure Radius defined and managed applications can run on any cloud. 

Want to join in and give it a try? Radius's code, which is licensed under the Apache license, is [ready to modify and run on GitHub.](https://github.com/radius-project/radius) Radius is not ready yet for production workloads, but its promise is great, and I'm eager to see what developers will make of it. This could be a real game changer for anyone developing or using hybrid/multi-cloud software.

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
<li><a href="https://some-tips.techidaily.com/new-the-key-to-smooth-auditory-transitions/"><u>[New] The Key to Smooth Auditory Transitions</u></a></li>
<li><a href="https://facebook-video-share.techidaily.com/updated-9-powerful-applications-for-saving-youtube-content-on-android-for-2024/"><u>[Updated] 9 Powerful Applications for Saving YouTube Content on Android for 2024</u></a></li>
<li><a href="https://vp-tips.techidaily.com/updated-in-2024-pinnacle-panoramics-selecting-the-best-8k-cameras/"><u>[Updated] In 2024, Pinnacle Panoramics Selecting the Best 8K Cameras</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-swift-shadowing-secrets/"><u>[Updated] Swift Shadowing Secrets</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unveiling-the-hidden-truths-behind-vrs-advantages-and-limitations/"><u>2024 Approved Unveiling the Hidden Truths Behind VR's Advantages and Limitations</u></a></li>
<li><a href="https://techtrends.techidaily.com/effective-strategies-for-fixing-lameencdll-error-encounters-when-using-audacity-with-lame-mp3-encoder/"><u>Effective Strategies for Fixing lame_enc.dll Error Encounters When Using Audacity with LAME MP3 Encoder</u></a></li>
<li><a href="https://win-amazing.techidaily.com/gigabyte-z370p-d3-download-current-bios-and-driver-updates-now/"><u>Gigabyte Z370p-D3: Download Current BIOS and Driver Updates Now</u></a></li>
<li><a href="https://android-location-track.techidaily.com/in-2024-how-to-intercept-text-messages-on-realme-c53-drfone-by-drfone-virtual-android/"><u>In 2024, How to Intercept Text Messages on Realme C53 | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unleash-your-full-potential-in-the-metaverse/"><u>In 2024, Unleash Your Full Potential in the Metaverse</u></a></li>
<li><a href="https://tech-haven.techidaily.com/opt-for-confidential-discussions-with-duckduckgos-advanced-ai-chatting-tools/"><u>Opt for Confidential Discussions with DuckDuckGo's Advanced AI Chatting Tools</u></a></li>
<li><a href="https://program-issues.techidaily.com/overcoming-timeout-interruptions-in-file-downloads-best-practices/"><u>Overcoming ‘Timeout’ Interruptions in File Downloads – Best Practices</u></a></li>
<li><a href="https://change-location.techidaily.com/pokemon-go-cooldown-chart-on-samsung-galaxy-a15-5g-drfone-by-drfone-virtual-android/"><u>Pokémon Go Cooldown Chart On Samsung Galaxy A15 5G | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/transform-your-tiktok-experience-with-new-user-numbers-for-2024/"><u>Transform Your TikTok Experience with New User Numbers for 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/c-BHGGIC0zE?si=FzUQKZa-bx8OlKuB" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

