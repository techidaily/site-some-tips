---
title: Understanding and Overcoming Current Azure Capacity Challenges as a Client
date: 2024-12-10T17:26:22.619Z
updated: 2024-12-12T19:00:38.724Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/c4ced3e743aac73832056f631bfd46a86102f3c9/2022/07/06/5414389b-d5d6-4013-8342-882244563f2b/azurecapacitylimits.jpg?width=278&height=156&fit=crop&auto=webp
---

## Understanding and Overcoming Current Azure Capacity Challenges as a Client

![azurecapacitylimits](https://www.zdnet.com/a/img/resize/c4a04d2aa4f3cea6ca9fdc27e040783c0f33cc24/2022/07/06/5414389b-d5d6-4013-8342-882244563f2b/azurecapacitylimits.jpg?auto=webp&width=1280)

Credit: Microsoft

At the start of the global COVID-19 pandemic in 2020, Microsoft officials were proactive in explaining [how the company was trying to head off cloud-computing capacity issues](https://www.zdnet.com/article/microsoft-cloud-services-demand-up-775-percent-prioritization-rules-in-place-due-to-covid-19/) in spite of increased demand. Two years later, Microsoft customers are still encountering capacity problems thanks to continuing supply-chain limitations. The difference now is officials aren't saying as much publicly about what's going on. Privately, however, they may be.   
  
A report by _The Information_ from last week indicates. Capacity issues are affecting Azure datacenters in Washington State, Europe and Asia due to supply chain issues. [More than two dozen Azure data centers in countries around the world](https://www.theinformation.com/articles/microsoft-cloud-computing-system-suffering-from-global-shortage) are operating with limited server capacity, the report says. And capacity is expected to remain limited until at least early next year, it adds.   
  
Talking to customers and partners, the reality that the Cloud isn't limitless and is bound by how rapidly big companies can scale out their datacenters has become almost common knowledge. The idea that [the Cloud was out of the room](https://www.zdnet.com/article/microsoft-azure-customers-reporting-hitting-virtual-machine-limits-in-u-s-east-regions/) two or three years ago seemed crazy. Now it's the new norm, not just for Microsoft but for AWS and Google.   
  
Microsoft notifies at least some customers that there are quotas on how much cloud capacity the company can provide. Not surprisingly, given that its customer base is largely enterprise customers, Microsoft prioritizes its capacity for existing business users, which means newer and pending customers are more likely to hit quotas and hard barriers. 

"I didn't think that Azure having capacity issues was news. I thought that thanks to all the jokes on social media, [everyone took it for granted that the effects of the pandemic and cargo crises had crippled electronics supplies the world over](https://aidanfinn.com/?p=22679)," blogged Aidan Finn, a Microsoft Most Valuable Professional (MVP) and Principal Consultant for Innofactor Norway.  
  
Microsoft officials said a couple of years ago that it would be limited in adding more datacenters because of shortages of chips and servers -- a situation that it seemingly rectified later. A year ago, officials said the company was on pace to [build annually 50 to 100 new datacenters](https://www.zdnet.com/article/microsoft-were-on-pace-to-build-50-to-100-new-datacenters-each-year/) (not datacenter regions, but actual physical datacenters). But supply chain uncertainties have continued to make fulfilling this goal challenging. It's not just chips and servers that are in short supply. Everything from power supplies to concrete also is hard to come by.   
  
Couple these shortages with Microsoft deciding to prioritize [spinning up cloud security services when needed to help with the war in Ukraine](https://aidanfinn.com/?p=22679), and you've got a situation where even the best workload balancing plans can't produce capacity miracles.   
  
Microsoft officials won't comment on the extent to which Azure's capacity is limited. But they do acknowledge that existing customers get first dibs. The official statement from a company spokesperson:   
  
_"Across the globe, we have seen unprecedented growth in the Cloud. With this surge, coupled with macro trends impacting the whole industry, we've taken steps to address customer increases in capacity while also expediting server deployment in our datacenters. Our priority remains ensuring business continuity for customers. In addition to managing and planning for growth, we actively load balance as needed. If it does become necessary to put capacity restrictions in place, we will first restrict trials and internal workloads to prioritize growth of existing customers."_   
  
So what can customers do to try to head off the impact of capacity issues?   
  
For one, customers should be looking at least two to three years out in planning their needs and Cloud spending. And they should talk to their Microsoft representatives about what Azure will be able to handle during that time period. They also should keep their eyes on quotas and anticipate any scale-out needs six months in advance, according to people I've asked about this.   
  
While some Microsoft partners advise clients to look at legacy virtual machine SKUs as a possible way to get around capacity issues, others say customers should try to use the latest SKUs even though they require newer and possibly less readily available hardware. And in cases where customers are big enough, multiregional architectures spanning multiple availability zones may help with supply -- as long as companies can afford to pay for it. 

Finn also suggested the [possible disablement of auto-scaling and potentially reserving VM capacity in advance](https://aidanfinn.com/?p=22679).

#### Cloud

[​What is digital transformation? Everything you need to know](https://www.zdnet.com/article/what-is-digital-transformation-everything-you-need-to-know-about-how-technology-is-reshaping/ "​What is digital transformation? Everything you need to know")

[The best cloud providers compared: AWS, Azure, Google Cloud, and more](https://www.zdnet.com/article/the-top-cloud-providers-of-2021-aws-microsoft-azure-google-cloud-hybrid-saas/ "The best cloud providers compared: AWS, Azure, Google Cloud, and more")

[The top 6 cheap web hosting services: Find an affordable option](https://www.zdnet.com/article/best-cheap-web-hosting/ "The top 6 cheap web hosting services: Find an affordable option")

[What is cloud computing? Here's everything you need to know](https://www.zdnet.com/article/what-is-cloud-computing-everything-you-need-to-know-about-the-cloud/ "What is cloud computing? Here's everything you need to know")

* [​What is digital transformation? Everything you need to know](https://www.zdnet.com/article/what-is-digital-transformation-everything-you-need-to-know-about-how-technology-is-reshaping/ "​What is digital transformation? Everything you need to know")
* [The best cloud providers compared: AWS, Azure, Google Cloud, and more](https://www.zdnet.com/article/the-top-cloud-providers-of-2021-aws-microsoft-azure-google-cloud-hybrid-saas/ "The best cloud providers compared: AWS, Azure, Google Cloud, and more")
* [The top 6 cheap web hosting services: Find an affordable option](https://www.zdnet.com/article/best-cheap-web-hosting/ "The top 6 cheap web hosting services: Find an affordable option")
* [What is cloud computing? Here's everything you need to know](https://www.zdnet.com/article/what-is-cloud-computing-everything-you-need-to-know-about-the-cloud/ "What is cloud computing? Here's everything you need to know")

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
<li><a href="https://article-knowledge.techidaily.com/new-in-2024-auditory-interpretation-accessible-at-no-expense/"><u>[New] In 2024, Auditory Interpretation Accessible at No Expense</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/updated-in-2024-build-a-custom-vr-device-diy-google-cardboard-guide/"><u>[Updated] In 2024, Build a Custom VR Device DIY Google Cardboard Guide</u></a></li>
<li><a href="https://twitter-videos.techidaily.com/updated-in-2024-utilizing-the-power-of-twitter-archive-data/"><u>[Updated] In 2024, Utilizing the Power of Twitter Archive Data</u></a></li>
<li><a href="https://some-tips.techidaily.com/1726222746499-movavi/"><u>網路直通無需付錢，改變音源格式：MOVAVI 自由型編排</u></a></li>
<li><a href="https://some-tips.techidaily.com/a-csata-megallo-az-on-mikroszamara-top-20-kiktatasokkal-gyujtott-el-pc-programokba-es-telefonokba-2024/"><u>A Csata Megálló Az Ön Mikroszámára: Top 20 Kiktatásokkal Gyújtott El PC-Programokba És Telefonokba, 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/free-online-conversion-easily-change-ppm-documents-with-movavi/"><u>Free Online Conversion: Easily Change PPM Documents with Movavi</u></a></li>
<li><a href="https://some-tips.techidaily.com/guia-de-edicion-vob-con-movavi-unirlos-cortarlos-y-dividirlos-para-mejorar-la-calidad-del-video/"><u>Guía De Edición VOB Con Movavi: Unirlos, Cortarlos Y Dividirlos Para Mejorar La Calidad Del Video</u></a></li>
<li><a href="https://location-social.techidaily.com/how-to-change-your-oppo-a78-5g-location-on-life360-without-anyone-knowing-drfone-by-drfone-virtual-android/"><u>How to Change Your Oppo A78 5G Location on life360 Without Anyone Knowing? | Dr.fone</u></a></li>
<li><a href="https://instagram-clips.techidaily.com/how-to-make-highlights-on-instagram/"><u>How to Make Highlights on Instagram</u></a></li>
<li><a href="https://some-tips.techidaily.com/movavii-tod-mov/"><u>MOVAvii 無限制網路上的還原服務 - 免費 TOD 到 MOV 格式轉換</u></a></li>
<li><a href="https://win-data.techidaily.com/recuperacion-facil-y-sin-costo-del-icono-de-papelera-en-tu-sistema-operativo-windows/"><u>Recuperación Fácil Y Sin Costo Del Icono De Papelera en Tu Sistema Operativo Windows</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/simplified-window-capturing-software/"><u>Simplified Window Capturing Software</u></a></li>
<li><a href="https://some-tips.techidaily.com/tips-for-att-andra-storleken-pa-videofilmer-i-windows-och-mac-os-en-lattlastande-resa-till-guide/"><u>Tips För Att Ändra Storleken På Videofilmer I Windows Och Mac OS - en Lättlästande Resa Till Guide</u></a></li>
<li><a href="https://extra-hints.techidaily.com/unpacking-the-advanced-capabilities-of-movavi-video-editor-2024plus/"><u>Unpacking the Advanced Capabilities of Movavi Video Editor 2024+</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/sn2STvYRVb8?si=Z-XhJJ1Mc-Em5Kqy" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

