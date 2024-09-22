---
title: Meteorological Precision or Good Enough? Insights Into the Collaboration of 180 Forecasters
date: 2024-09-17 16:10:25
updated: 2024-09-20 12:44:49
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/965ac34e7c203b27ce0e30a0e9c41cd22515bc37/2022/06/30/431f83e7-d721-4fab-ab2a-b28258871259/dtn-simulation-image-f845ccbb6209856dd47728d6332f9dce56a009f0.png?width=278&height=156&fit=crop&format=pjpg&auto=webp
---

## Meteorological Precision or Good Enough? Insights Into the Collaboration of 180 Forecasters

What's a good enough weather prediction? That's a question most people probably don't give much thought to, as the answer seems obvious -- an accurate one. But then again, most people are not CTOs at DTN. Lars Ewe is, and his answer may be different than most people's. With 180 meteorologists on staff providing weather predictions worldwide, [DTN](https://www.dtn.com/) is the largest weather company you've probably never heard of.

### See also

[The best extreme weather tech: Top gear for power outages Some of us like to go off the grid, while others find themselves forced off the grid. Having the right gear can make a huge difference.  Read now](https://www.zdnet.com/article/best-extreme-weather-tech/)

Case in point: DTN is not included in ForecastWatch's "[Global and Regional Weather Forecast Accuracy Overview 2017 - 2020](https://www.forecastwatch.com/wp-content/uploads/Global%5Fand%5FRegional%5FWeather%5FForecast%5FAccuracy%5FOverview%5F2017-2020.pdf)." The report rates 17 weather forecast providers according to a comprehensive set of criteria, and a thorough data collection and evaluation methodology. So how come a company that started out in the 1980s, serves a global audience, and has always had a strong focus on weather, is not evaluated?

* **See also:** [**US weather, climate forecasting is about to get way better**](https://www.zdnet.com/article/us-weather-climate-forecasting-is-about-to-get-way-better/)

## Weather forecast as a big data and internet of things problem

DTN's name stands for 'Digital Transmission Network', and is a nod to the company's origins as a farm information service delivered over the radio. Over time, the company has adopted technological evolution, pivoted to providing what it calls "operational intelligence services" for a number of industries, and gone global.

Ewe has previous stints in senior roles across a range of corporations, including the likes of AMD, BMW, and Oracle. He feels strongly about data, data science, and the ability to provide insights to provide better outcomes. Ewe referred to DTN as a global technology, data, and analytics company, whose goal is to provide actionable near real-time insights for clients to better run their business.

[DTN's Weather as a Service](https://www.dtn.com/weather/)® (WAAS®) approach should be seen as an important part of the broader goal, according to Ewe. "We have hundreds of engineers not just dedicated to weather forecasting, but to the insights," Ewe said. He also explained that DTN invests in producing its own weather predictions, even though it could outsource them, for a number of reasons.

Many available weather prediction services are either not global, or they have weaknesses in certain areas such as image resolution, according to Ewe. DTN, he added, leverages all publicly available and many proprietary data inputs to generate its own predictions. DTN also augments that data with its own data inputs, as it owns and operates thousands of weather stations worldwide. Other data sources include satellite and radar, weather balloons, and airplanes, plus historical data.

DTN offers a range of operational intelligence services to customers worldwide, and weather forecasting is an important parameter for many of them.

DTN

Some examples of the higher-order services that DTN's weather predictions power would be storm impact analysis and shipping guidance. Storm impact analysis is used by utilities to better predict outages, and plan and staff accordingly. Shipping guidance is used by shipping companies to compute optimal routes for their ships, both from a safety perspective, but also from a fuel efficiency perspective.

What lies at the heart of the approach is the idea of taking DTN's forecast technology and data, and then merging it with customer-specific data to provide tailored insights. Even though there are baseline services that DTN can offer too, the more specific the data, the better the service, Ewe noted. What could that data be? Anything that helps DTN's models perform better.

It could be the position or shape of ships or the health of the infrastructure grid. In fact, since such concepts are used repeatedly across DTN's models, the company is moving in the direction of a digital twin approach, Ewe said.

In many regards, weather forecasting today is really a big data problem. To some extent, Ewe added, it's also an internet of things and data integration problem, where you're trying to get access to, integrate and store an array of data for further processing.

As a consequence, producing weather predictions does not just involve the domain expertise of meteorologists, but also the work of a team of data scientists, data engineers, and machine learning/DevOps experts. Like any big data and data science task at scale, there is a trade-off between accuracy and viability.

* [**Best extreme weather tech 2022: Power outage gear**](https://www.zdnet.com/home-and-office/yard-outdoors/best-extreme-weather-tech/)

## Good enough weather prediction at scale

Like most CTOs, Ewe enjoys working with the technology, but also needs to be aware of the business side of things. Maintaining accuracy that is just right, or "good enough", without cutting corners while at the same time making this financially viable is a very complex exercise. DTN approaches this in a number of ways.

One way is by reducing redundancy. As Ewe explained, over time and via mergers and acquisitions, DTN came to be in possession of more than five forecasting engines. As is usually the case, each of those had its strengths and weaknesses. The DTN team took the best elements of each and consolidated them in one global forecast engine.

Another way is via optimizing hardware and reducing the associated cost. [DTN worked with AWS](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2Fsolutions%2Fcase-studies%2Fdtn-case-study%2F%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7C3115acc5-0d8c-4a08-971f-f922e36b8dc7%7Cdtp&dtb=1) to develop new hardware instances suitable to the needs of this very demanding use case. Using the new AWS instances, DTN can run weather prediction models on demand and at unprecedented speed and scale.

In the past, it was only feasible to run weather forecast models at set intervals, once or twice per day, as it took hours to run them. Now, models can run on demand, generating a one-hour global forecast in about a minute, according to Ewe. Equally important, however, is the fact that those instances are more economical to use.

As to the actual science of how DTN's model's operate -- they contain [both data-driven, machine learning models, as well as models incorporating meteorology domain expertise](https://www.zdnet.com/article/raiders-of-the-storm-the-data-science-behind-weather-prediction/). Ewe noted that DTN takes an ensemble approach, running different models and weighing them as needed to produce a final outcome.

That outcome, however, is not binary -- rain or no rain, for example. Rather, it is probabilistic, meaning it assigns probabilities to potential outcomes -- 80% probability of 6 Beaufort winds, for example. The reasoning behind this has to do with what those predictions are used for: operational intelligence.

That means helping customers make decisions: Should this offshore drilling facility be evacuated or not? Should this ship or this airplane be rerouted or not? Should this sports event take place or not?

The ensemble approach is key in being able to factor predictions in the risk equation, according to Ewe. Feedback loops and automating the choice of the right models with the right weights in the right circumstances is what DTN is actively working on.

This is also where the "good enough" aspect comes in. The real value, as Ewe put it, is in downstream consumption of the predictions those models generate. "You want to be very careful in how you balance your investment levels, because the weather is just one input parameter for the next downstream model. Sometimes that extra half-degree of precision may not even make a difference for the next model. Sometimes, it does."

Coming full circle, Ewe noted that DTN's attention is focused on the company's daily operations of its customers, and how weather impacts those operations and allows the highest level of safety and monetary returns for customers. "That has proven much more valuable than having an external party measure the accuracy of our forecasts. It's our daily customer interaction that measures how accurate and valuable our forecasts are." 

#### Featured

[How to disable ACR (and greatly reduce ads) on every TV model - and why you should](https://www.zdnet.com/article/how-to-disable-acr-and-greatly-reduce-ads-on-every-tv-model-and-why-you-should/ "How to disable ACR (and greatly reduce ads) on every TV model - and why you should")

[I replaced my Samsung Galaxy S24 Ultra with the Pixel 9 Pro XL for two weeks - and can't go back](https://www.zdnet.com/article/i-replaced-my-samsung-galaxy-s24-ultra-with-the-pixel-9-pro-xl-for-two-weeks-and-cant-go-back/ "I replaced my Samsung Galaxy S24 Ultra with the Pixel 9 Pro XL for two weeks - and can't go back")

[Linus Torvalds talks AI, Rust adoption, and why the Linux kernel is 'the only thing that matters'](https://www.zdnet.com/article/linus-torvalds-talks-ai-rust-adoption-and-why-the-linux-kernel-is-the-only-thing-that-matters/ "Linus Torvalds talks AI, Rust adoption, and why the Linux kernel is 'the only thing that matters'")

[The best mini PCs you can buy: Expert recommended](https://www.zdnet.com/article/best-mini-pc/ "The best mini PCs you can buy: Expert recommended")

* [How to disable ACR (and greatly reduce ads) on every TV model - and why you should](https://www.zdnet.com/article/how-to-disable-acr-and-greatly-reduce-ads-on-every-tv-model-and-why-you-should/ "How to disable ACR (and greatly reduce ads) on every TV model - and why you should")
* [I replaced my Samsung Galaxy S24 Ultra with the Pixel 9 Pro XL for two weeks - and can't go back](https://www.zdnet.com/article/i-replaced-my-samsung-galaxy-s24-ultra-with-the-pixel-9-pro-xl-for-two-weeks-and-cant-go-back/ "I replaced my Samsung Galaxy S24 Ultra with the Pixel 9 Pro XL for two weeks - and can't go back")
* [Linus Torvalds talks AI, Rust adoption, and why the Linux kernel is 'the only thing that matters'](https://www.zdnet.com/article/linus-torvalds-talks-ai-rust-adoption-and-why-the-linux-kernel-is-the-only-thing-that-matters/ "Linus Torvalds talks AI, Rust adoption, and why the Linux kernel is 'the only thing that matters'")
* [The best mini PCs you can buy: Expert recommended](https://www.zdnet.com/article/best-mini-pc/ "The best mini PCs you can buy: Expert recommended")

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
