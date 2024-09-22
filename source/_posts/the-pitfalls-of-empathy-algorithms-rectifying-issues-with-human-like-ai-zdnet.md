---
title: "The Pitfalls of Empathy Algorithms: Rectifying Issues with Human-Like AI | ZDNet"
date: 2024-09-17 22:42:51
updated: 2024-09-20 11:36:32
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/0f32298889456fdaca83b5ae25e894332407ac3282ea5f03ad9ab479c2952ec4.jpg
---

## The Pitfalls of Empathy Algorithms: Rectifying Issues with Human-Like AI | ZDNet

![Humane AI Pin at MWC 2024](https://www.zdnet.com/a/img/resize/dc1fbca6eb4b7d8fa7e2e54f8d1bbf7c0287f2c6/2024/02/26/85b62067-3990-436e-9521-a26a799ece9c/dsc01335.jpg?auto=webp&width=1280)

Kerry Wan/ZDNET

Last week, startup [Humane](https://humane.com/) seeded its long-awaited [Ai Pin](https://humane.com/shop?) to reviewers and influencers, and the response has been overwhelmingly underwhelming. Most notable was [the review from Marques Brownlee](https://www.youtube.com/watch?v=TitZV6k8zfA) (aka [MKBHD](https://mkbhd.com/)), who -- with 18 million followers on YouTube and 6.2 million followers on X -- called Humane's AI pin "the new worst product I think I've ever reviewed, in its current state… this thing is bad at almost everything it does, basically all the time."

**Also: [Humane Ai Pin reviews: 5 takeaways on a promising but dangerously flawed wearable](https://www.zdnet.com/article/humane-ai-pin-reviews-5-takeaways-on-a-promising-but-dangerously-flawed-wearable/)**

The main complaints from Brownlee and other reviews focus not on the hardware itself -- the Pin appears well-built -- but on the utility and performance of the device. Here are some of the ways that the Ai Pin falls short:

* **Concept versus execution:** The Ai Pin is an innovative wearable AI assistant that functions independently and has high-quality hardware. However, it suffers from significant functionality issues, including slow responses and incorrect answers.
* **Challenges with user interface:** The device's novel gesture-based control and class 2 monochrome green laser projector interface are not user-friendly in various conditions, require a steep learning curve, and are difficult to see in bright environments.
* **Reliability concerns:** The Ai Pin has poor battery life and overheating issues, which necessitate frequent charges and cause discomfort.
* **Limited compatibility:** The device lacks integration with smartphones and popular apps, limiting its practical utility despite its standalone nature.
* **Cost and value:** Given its limited functionality compared to modern smartphones, the Ai Pin's high price and additional subscription fees are hard to justify.
* **Future potential versus current limitations:** Although aiming to reduce screen time, the Ai Pin's current limitations make it unappealing compared to the comprehensive capabilities of smartphones.

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

It is unclear whether Humane can improve the performance and reliability of the current device with embedded firmware updates and back-end software development. Certain aspects of the hardware -- such as the difficulties of using the laser projector under various lighting conditions-- might limit performance, and other constraints might only allow for slight incremental improvements.

The issues with battery charging and overheating may not be solvable with the current hardware either.

## The connectivity problem

However, there may be a few things that Humane can do. Let's start with the connectivity response time.

The device uses 4G LTE data provided by T-Mobile. This is fine for well-connected areas, but if you don't have coverage, as with any mobile device, it becomes a roaming issue (provided Humane's contract with T-Mobile allows for roaming). Not every area has good wireless coverage across multiple providers. 

**Also: [What is Wi-Fi 7 and just how fast is it?](https://www.zdnet.com/home-and-office/networking/what-is-wi-fi-7-and-just-how-fast-is-it/)**

Also, there's the issue of connectivity degradation to slower access speeds on 4G networks when you are in a highly congested area; that's one reason carriers have spent so much money on 5G deployments -- to deal with congestion issues in urban areas.

For wearables to function properly, they require reliable data connections. The Humane Pin offers dual-frequency Wi-Fi, equipped with both 2.4Ghz and 5Ghz antennae. However, it is almost useless due to the limited availability of compatible Wi-Fi networks. The device struggles to authenticate with public Wi-Fi networks (such as those requiring web portals for authentication), including most networks outside your home -- airports, airplanes, cafes, restaurants, and workplaces. 

Even a simple password-type connection to a broadcast SSID can be a pain. Humane's [documentation](https://support.humane.com/hc/en-us/articles/23291121900173-Connect-to-Wi-Fi) says that joining a Wi-Fi network requires voice and laser UX intervention or a QR code (that you're supposed to print out so the Ai Pin's camera can see it). 

**Also: [The best hotspots you can buy](https://www.zdnet.com/article/best-hotspot/)**

Oh, and T-Mobile public hotspots? Good luck with that -- [they don't exist](https://www.t-mobile.com/dialed-in/tips-tricks/how-to-get-wifi-on-the-go). AT&T and Verizon have those, as do many broadband providers like Comcast Xfinity, but… _the Pin can't access them_.

Can you use your 5G smartphone as a hotspot? Yes, you can -- but that defeats the purpose of paying Humane $25/month for 4G service. 

In terms of independent data connectivity, it would make a lot more sense if the Humane Pin could use any provider's eSIM (assuming its 4G LTE radio worked with any US provider as the iPhone and most Android phones do), and you could pay the typical $15 per month smartwatch fee to whatever carrier you want.

Of course, the $25 fee also covers cloud storage for your videos and photos, GenAI computing, and other infrastructure costs. But that could be knocked down at least $10 if the device was Wi-Fi-only or could utilize your existing provider.

**Also: [Apple Watch Series 9 review: Why I'm not settling for the less expensive models](https://www.zdnet.com/article/apple-watch-series-9-review/)**

To fix the Wi-Fi problem, the device needs passthrough-style authentication -- similar to how the iPhone works with the Apple Watch -- via Bluetooth to a smartphone. Of course, this would require the development of a smartphone app, at least a minimal one to work around the connectivity problems. 

My iPhone can store many Wi-Fi networks (that I have authenticated) in its memory. Using Bluetooth, it passes those to my Apple Watch, and that's completely transparent to me. That's exactly what the Pin needs.

## 4G and Wi-Fi are not the only answer for wearable connectivity

Wi-Fi, however, is power-hungry, even with low-power transceiver implementations. A possible solution for future Pin hardware would be to include [Matter](https://csa-iot.org/all-solutions/matter/), an IoT connectivity standard adopted by many vendors, including Apple, Amazon, Google, and Samsung. Matter enables smart home products from different manufacturers to work together by providing a universal language for wireless (and wired) IoT devices. 

**Also: [Everything you need to build out a smart home](https://www.zdnet.com/home-and-office/smart-home/everything-you-need-to-start-a-smart-home-setup/)**

Wireless Matter devices can connect with each other using [Zigbee's wireless protocol](https://csa-iot.org/all-solutions/zigbee/). Smart home bridges such as Amazon Echo, Amazon eero, Philips Hue, Apple TV 4K, Apple HomePod, and other devices with Matter and Zigbee built-in can be used for this purpose. Zigbee supports data rates of up to 250 kbps at 2.4 GHz and 40 kbps at 915 MHz in North America and has a range of up to 100 meters. Zigbee's repeaters and mesh networking capabilities can extend that signal range greatly. [Amazon's Sidewalk](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Fwww.amazon.com%2FAmazon-Sidewalk%2Fb%3Fie%3DUTF8%26node%3D21328123011%26tag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7Ca5d52c69-0c0f-4d2b-99af-dc8ec350853a%7Cdtp&dtb=1) is one example of a long-range mesh network that uses 915 MHz Zigbee and Bluetooth Low Energy, a combination that also could be used for the Pin.

Matter's data transmission speeds may not be as fast as Wi-Fi for moving large amounts of data (such as photos and videos to cloud storage), but as a side-channel communications mechanism for text-based LLM queries and sensor data on wearable devices, it makes a lot of sense.

## The LLM and cloud provisioning dilemma

However, not all of the device's slowness can be attributed to connectivity. The query response from Humane's AI is also said to be slow and unreliable, and that's probably due to underprovisioned cloud resources. The pin's back-end GenAI LLM is [apparently OpenAI](https://www.theverge.com/2023/11/9/23953901/humane-ai-pin-launch-date-price-openai). It is unclear whether it uses GPT4 or GPT 3.5, but it must be done via an API call. 

It's unlikely the pin is doing [direct API calls to OpenAI](https://platform.openai.com/docs/api-reference) on Azure. It's more likely that the queries will be proxied, and prompt modifications will be done by cloud infrastructure running on any number of providers, such as [Azure OpenAI](https://www.googleadservices.com/pagead/aclk?sa=L&ai=DChcSEwi6x5mP1cmFAxXzoloFHUr6DqoYABAAGgJ2dQ&ase=2&gclid=CjwKCAjw5v2wBhBrEiwAXDDoJUJs-Bz4HzISnBFyK7oAu96B57-MNgWXiWenk2l3vyWIrcDORIDjDRoC614QAvD%5FBwE&ohost=www.google.com&cid=CAESVuD2KcdWNnPO9mfTb68XyFte7R2sA8vgs-qJkyerCeeDX56heCx69jf%5FHoCWQHEZXIFCR%5FU%5F6oafb7rOtvjVWJQwO2AmnP7biMf%5FgrcKuyAvlzY0keMl&sig=AOD64%5F2klCobkBiJj1mq42HQGmJvY3oT4w&q&nis=4&adurl&ved=2ahUKEwjCq5CP1cmFAxVEgoQIHf6aD0cQ0Qx6BAgGEAE) (very likely), AWS, or Google Cloud. Depending on how well that is provisioned, it will contribute to the service's overall performance. 

**Also: [GPT-4 Turbo reclaims the 'best AI model' crown from Anthropic's Claude 3](https://www.zdnet.com/article/gpt-4-turbo-reclaims-best-ai-model-crown-from-anthropics-claude-3/)**

Here's the question: Is it sensible to restrict the Pin to OpenAI/ChatGPT? Other LLMs are currently being developed, including Meta's LLAMA2, Google Gemini, and Amazon Titan. AI advancements are coming fast and furious, with models increasing in parameter size multiple times a year. Competition among these models is intense. An AI-driven product, one not confined to any particular ecosystem, should be service-agnostic and have access to the best-of-breed model at any time and to whichever LLM the user prefers.

## Can the Pin be fixed - or will rivals capitalize on Humane's failure?

Standing at the crossroads of innovation and practicality, Humane's Ai Pin marks a daring foray into the future of wearable technology. However, its path forward -- from a groundbreaking concept to an essential device -- will be difficult. The issues of connectivity, user interface, and overall utility underscore a divergence between Humane's visionary ambitions and the practical expectations of its user base.

Humane must enhance -- urgently -- the Ai Pin's performance to narrow this divide. Enhancements include improving connectivity with updates like eSIM support and more sophisticated WiFi solutions; making the user interface more accessible; and boosting cloud service resiliency. Adopting IoT standards like Matter could further integrate the Ai Pin into the broader digital ecosystem, enhancing its versatility and appeal.

**Also: [Limitless' $99 AI wearable to promises to remember your meetings and, well, everything else](https://www.zdnet.com/article/limitless-99-ai-wearable-to-promises-to-remember-your-meetings-and-well-everything-else/)**

However, Humane is not operating in a vacuum. Tech giants such as Apple, Amazon, and Google -- with their vast resources, established device ecosystems, and advanced GenAI cloud capabilities -- are well-positioned to capitalize on any stumbles by Humane. These tech giants have the expertise and infrastructure to swiftly implement similar innovations, potentially refining and integrating wearable AI technologies into their product lines more successfully. Their established user base and robust cloud services could allow them to outpace Humane by delivering more polished, user-friendly alternatives that align more closely with consumer expectations.

As the landscape of personal technology continues to evolve, the pressure is on Humane to iterate and improve the Ai Pin rapidly. If they can respond effectively to user feedback and refine their product, they still have a chance to compete in this dynamic market. Otherwise, they risk being overshadowed as competitors like Apple, Amazon, and Google leverage their technological prowess to capture the imagination and trust of consumers looking for the next big thing in wearable tech.

#### Wearables

[I put the Apple Watch Ultra through a Tough Mudder: How it held up](https://www.zdnet.com/article/apple-watch-ultra-review/ "I put the Apple Watch Ultra through a Tough Mudder: How it held up")

[The 5 best smartwatches: Apple and Samsung battle for your wrist](https://www.zdnet.com/article/best-smartwatch/ "The 5 best smartwatches: Apple and Samsung battle for your wrist")

[How to use your Apple Watch's built-in Walkie Talkie](https://www.zdnet.com/article/how-to-use-your-apple-watchs-built-in-walkie-talkie/ "How to use your Apple Watch's built-in Walkie Talkie")

[Google Pixel Buds Pro review: AirPods Pro, but for Android](https://www.zdnet.com/article/google-pixel-buds-pro-review/ "Google Pixel Buds Pro review: AirPods Pro, but for Android")

* [I put the Apple Watch Ultra through a Tough Mudder: How it held up](https://www.zdnet.com/article/apple-watch-ultra-review/ "I put the Apple Watch Ultra through a Tough Mudder: How it held up")
* [The 5 best smartwatches: Apple and Samsung battle for your wrist](https://www.zdnet.com/article/best-smartwatch/ "The 5 best smartwatches: Apple and Samsung battle for your wrist")
* [How to use your Apple Watch's built-in Walkie Talkie](https://www.zdnet.com/article/how-to-use-your-apple-watchs-built-in-walkie-talkie/ "How to use your Apple Watch's built-in Walkie Talkie")
* [Google Pixel Buds Pro review: AirPods Pro, but for Android](https://www.zdnet.com/article/google-pixel-buds-pro-review/ "Google Pixel Buds Pro review: AirPods Pro, but for Android")

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
