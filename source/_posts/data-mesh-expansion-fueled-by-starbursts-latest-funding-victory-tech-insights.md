---
title: Data Mesh Expansion Fueled by Starburst's Latest Funding Victory | Tech Insights
date: 2024-09-19 20:56:30
updated: 2024-09-20 12:35:41
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/7b30ded1356833dfaf76c7c0649ae9ac9da5d57f/2021/10/19/443ea188-eacb-49d7-9643-8a0384671c82/finance-cash-flow.jpg?width=278&height=156&fit=crop&auto=webp
---

## Data Mesh Expansion Fueled by Starburst's Latest Funding Victory | Tech Insights

[Starburst Data](https://www.starburst.io/) announced this week that it has more than doubled its financing with a new $250 million Series D round being announced this week and opening a new front end portal to its distributed query engine. The company claims this has roughly tripled its previous valuation, for which there were conflicting published numbers ([here](https://www.bloomberg.com/news/articles/2021-01-06/starburst-data-hits-1-2-billion-valuation-as-andreessen-invests?sref=SSBEOKlx) and [here](https://www.theinformation.com/articles/investors-pay-high-price-for-starburst-data-at-1-6-billion-valuation)). The announcements are coming in conjunction with [Datanova](https://www.starburst.io/info/datanova2022/), the company's annual online event.

### Cloud

* [​What is digital transformation? Everything you need to know](https://www.zdnet.com/article/what-is-digital-transformation-everything-you-need-to-know-about-how-technology-is-reshaping/)
* [The best cloud providers compared: AWS, Azure, Google Cloud, and more](https://www.zdnet.com/article/the-top-cloud-providers-of-2021-aws-microsoft-azure-google-cloud-hybrid-saas/)
* [The top 6 cheap web hosting services: Find an affordable option](https://www.zdnet.com/article/best-cheap-web-hosting/)
* [What is cloud computing? Here's everything you need to know](https://www.zdnet.com/article/what-is-cloud-computing-everything-you-need-to-know-about-the-cloud/)

Entering 2022, the company is continuing to double down on data mesh. The company's home page characterizes itself as "The Analytics Engine for Data Mesh." We'll have more to say about that in a moment.

This week at Datanova, it is announcing an extension that adds a catalog-like portal front end to its Trino-based distributed query engine. On the administrative side, the portal enables data producers and data engineers to define metadata, track usage, and apply role-based access and entitlements. On the end-user side, they can use the portal to discover, browse, and add reviews of data sets. Although a data catalog in the "lite" sense, it is not meant to replace enterprise data catalogs. As a lightweight catalog packing its own query engine, Starburst nonetheless continues to support integration to Alation and Collibra.

On the roadmap, Starburst is ramping up support for emerging open source data table formats, including [Delta Lake](https://delta.io/) and [Iceberg](https://iceberg.apache.org/), with Delta Lake support further along.

With the new funding, a key theme for Starburst this year is global expansion, especially in go-to-market; while it currently has a presence on the ground in North America and Europe, this year marks the point that it will set up shop in Asia and Pacific Rim. Underscoring that, it is adding Alibaba for its cloud service [Galaxy](https://www.starburst.io/platform/starburst-galaxy/) (which only went GA two months ago on AWS, Azure, and Google Cloud). Starburst is also playing up its partnership with Red Hat, both on private cloud and [supported on Red Hat OpenShift Dedicated](https://blog.starburst.io/starburst-joins-red-hat-openshift-data-science-ecosystem-to-accelerate-delivery-of-machine-learning-models), a Red Hat-managed service on AWS and Google Cloud. Starburst is certified on OpenShift, is available on the Red Hat marketplace, and is one of just four ISVs in [Red Hat's OpenShift Data Science cloud service](https://www.redhat.com/en/technologies/cloud-computing/openshift/openshift-data-science). And there is ramping of engagement with global systems integrator usual suspects.

Starburst Enterprise is also available on HPE Marketplace as a distributed query engine for HPE Ezmeral Runtime, and both will soon start joint go-to-market in North America and Europe. But, for the record, so is Starburst rival Ahana, where part of the management team shares common roots with the portion of the Ezmeral product team that came from MapR.

Starburst is still at the early stage where growth is geometric; its business has tripled annually for the past three years. The highlight is the recent launch of Starburst Galaxy, the managed cloud service; having only been released late last year, the cloud SaaS business is not yet showing up heavily in the revenue numbers. While Starburst is not about to abandon on-premises or self-managed customers for Starburst enterprise, there's a little secret that the company foresees the brunt of future growth coming from the cloud SaaS service.

And that's where a key new addition to the management team, [Javier Molina](https://www.linkedin.com/in/javiermolina10/) as chief revenue officer, will play a key role. Previously SVP for worldwide sales at MongoDB, the [Atlas SaaS service](https://www.mongodb.com/atlas/database) was front and center. Launched [nearly six years ago](https://www.mongodb.com/press/mongodb-unveils-mongodb-atlas-the-new-industry-standard-for-database-as-a-service), Atlas now accounts for more than half of MongoDB's revenue. A key lesson that Molina is taking is that Atlas didn't explosively grow overnight. It wasn't until the acquisition of mLab, which added self-service onboarding, that Atlas hit its current trajectory. With Starburst Galaxy launched barely two months ago, you can expect that there will be heavy emphasis on self-service, enabling customers to consume it on demand without the red tape of annual contracts.

Clearly, Starburst is positioning itself to get past the petty mindshare battles regarding [who has the open sourciest query engine](https://www.zdnet.com/article/ahana-gets-seed-funding-and-a-tale-of-two-prestos/) by positioning distributed query, which is at heart its Trino technology, as a key cog in building [data products](https://towardsdatascience.com/data-as-a-product-vs-data-products-what-are-the-differences-b43ddbb0f123). And building data products is central to Starburst's embrace of data mesh. They are promoting it to the point where data mesh has become the tagline for the company. And they are a [source of access to summarized draft chapters](https://blog.starburst.io/tag/data-mesh-book-summary) from [Zhamak Dehghani's](http://www.linkedin.com/in/zhamak-dehghani) ([author](https://martinfowler.com/articles/data-monolith-to-mesh.html) of the current concept of data mesh) upcoming book.

By billing itself as "the analytics engine of data mesh," Starburst is walking a fine line, as data mesh is not a technology; it is a set of best practices and architectural design patterns for localizing lifecycle control of data sets, which are to be treated as products. So, nope, Starburst isn't calling Starburst Enterprise or Galaxy a data mesh solution per se. But the distinction is pretty subtle.

Of course, tools and technologies will be essential to supporting the various tasks of data mesh. And there are many tasks that will outscale humans, from managing and automating data ingest, data pipelines, data quality, and the validation that the data is trustworthy, valid, and current. Humans clearly drive the process, but technology scales their efforts.

Cut to the chase: Starburst Enterprise or Galaxy is just one piece of the data mesh puzzle. But data mesh is just one piece of the Starburst puzzle. Let's explain.

As we've spelt out ([here](https://www.zdnet.com/article/data-mesh-should-you-try-this-at-home/) and [here](https://www.zdnet.com/article/data-2022-outlook-part-ii-reality-bytes-the-data-mesh/)), we expect that this year, data meshes will draw their first serious scrutiny and blowback. That's actually a good thing. It's to be expected for any technology practice that is undergoing serious vetting. While there are organizations that will claim overnight victories, data mesh will always be a journey, and not all organizations are going to embrace those practices.

Distributed query will be a key part of execution for any data-driven organization, whether or not they embrace data mesh practices. While Starburst is certainly on target in pointing out the role of distributed query and its hooks to governance, it would make sense for Starburst to also generalize its message and not get tied at the hip to data mesh. And that's where the synergies with data fabrics could begin. 

#### Big Data

[How to find out if you are involved in a data breach (and what to do next)](https://www.zdnet.com/article/were-you-caught-up-in-the-latest-data-breach-heres-how-to-tell/ "How to find out if you are involved in a data breach (and what to do next)")

[Fighting bias in AI starts with the data](https://www.zdnet.com/article/fighting-bias-in-ai-starts-with-the-data/ "Fighting bias in AI starts with the data")

[Fair forecast? How 180 meteorologists are delivering 'good enough' weather data](https://www.zdnet.com/article/fair-forecast-how-180-meteorologists-are-delivering-good-enough-weather-data/ "Fair forecast? How 180 meteorologists are delivering 'good enough' weather data")

[Cancer therapies depend on dizzying amounts of data. Here's how it's sorted in the cloud](https://www.zdnet.com/article/cancer-therapies-depend-on-dizzying-amounts-of-data-heres-how-its-getting-sorted-in-the-cloud/ "Cancer therapies depend on dizzying amounts of data. Here's how it's sorted in the cloud")

* [How to find out if you are involved in a data breach (and what to do next)](https://www.zdnet.com/article/were-you-caught-up-in-the-latest-data-breach-heres-how-to-tell/ "How to find out if you are involved in a data breach (and what to do next)")
* [Fighting bias in AI starts with the data](https://www.zdnet.com/article/fighting-bias-in-ai-starts-with-the-data/ "Fighting bias in AI starts with the data")
* [Fair forecast? How 180 meteorologists are delivering 'good enough' weather data](https://www.zdnet.com/article/fair-forecast-how-180-meteorologists-are-delivering-good-enough-weather-data/ "Fair forecast? How 180 meteorologists are delivering 'good enough' weather data")
* [Cancer therapies depend on dizzying amounts of data. Here's how it's sorted in the cloud](https://www.zdnet.com/article/cancer-therapies-depend-on-dizzying-amounts-of-data-heres-how-its-getting-sorted-in-the-cloud/ "Cancer therapies depend on dizzying amounts of data. Here's how it's sorted in the cloud")

#### Big Data

[How to find out if you are involved in a data breach (and what to do next)](https://www.zdnet.com/article/were-you-caught-up-in-the-latest-data-breach-heres-how-to-tell/ "How to find out if you are involved in a data breach (and what to do next)")

[Fighting bias in AI starts with the data](https://www.zdnet.com/article/fighting-bias-in-ai-starts-with-the-data/ "Fighting bias in AI starts with the data")

[Fair forecast? How 180 meteorologists are delivering 'good enough' weather data](https://www.zdnet.com/article/fair-forecast-how-180-meteorologists-are-delivering-good-enough-weather-data/ "Fair forecast? How 180 meteorologists are delivering 'good enough' weather data")

[Cancer therapies depend on dizzying amounts of data. Here's how it's sorted in the cloud](https://www.zdnet.com/article/cancer-therapies-depend-on-dizzying-amounts-of-data-heres-how-its-getting-sorted-in-the-cloud/ "Cancer therapies depend on dizzying amounts of data. Here's how it's sorted in the cloud")

* [How to find out if you are involved in a data breach (and what to do next)](https://www.zdnet.com/article/were-you-caught-up-in-the-latest-data-breach-heres-how-to-tell/ "How to find out if you are involved in a data breach (and what to do next)")
* [Fighting bias in AI starts with the data](https://www.zdnet.com/article/fighting-bias-in-ai-starts-with-the-data/ "Fighting bias in AI starts with the data")
* [Fair forecast? How 180 meteorologists are delivering 'good enough' weather data](https://www.zdnet.com/article/fair-forecast-how-180-meteorologists-are-delivering-good-enough-weather-data/ "Fair forecast? How 180 meteorologists are delivering 'good enough' weather data")
* [Cancer therapies depend on dizzying amounts of data. Here's how it's sorted in the cloud](https://www.zdnet.com/article/cancer-therapies-depend-on-dizzying-amounts-of-data-heres-how-its-getting-sorted-in-the-cloud/ "Cancer therapies depend on dizzying amounts of data. Here's how it's sorted in the cloud")

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
