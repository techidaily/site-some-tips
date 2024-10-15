---
title: Can Advanced AI Propel Apple's Next Big Leap with the iPhone 16? Insights & Predictions
date: 2024-10-14T05:00:29.969Z
updated: 2024-10-15T10:01:17.548Z
tags:
  - apple
categories:
  - tech
thumbnail: https://thmb.techidaily.com/c572e526911ff13873cfea2690ee252e9ff11a89ced90101624b46320eed1514.jpg
---

## Can Advanced AI Propel Apple's Next Big Leap with the iPhone 16? Insights & Predictions

![Apple iPhone 15 Pro (in Blue Titanium) camera lenses](https://www.zdnet.com/a/img/resize/0b61ec84d772cbbb6f96fa06bfbbcd63410591ec/2023/10/10/5d6ca44c-691b-45da-a20c-e9ea693c9ce6/dsc01721-enhanced-nr.jpg?auto=webp&width=1280)

Jason Hiner/ZDNET

Wall Street is predicting a rough 2024 for Apple's iPhone franchise because of a lack of interesting new hardware features. Could artificial intelligence software [make an iPhone 16 shine brighter](https://www.zdnet.com/article/apple-reportedly-eyeing-generative-ai-push-and-siri-overhaul-for-the-iphone/)?

Some Apple stock bulls think so. Morgan Stanley analyst Erik Woodring this month opined that 2024 "will be the year that Apple's 'Edge AI' opportunity comes to fruition," and that it could power the new crop of iPhones this fall to greater heights. 

**Also: [The iPhone 16 Ultra camera will integrate the biggest leap in photos since B&W-to-color](https://www.zdnet.com/article/the-iphone-16-ultra-camera-will-integrate-the-biggest-leap-in-photos-since-b-w-to-color-report/)** 

Apple's iPhone sales, led by the [current iPhone 15](https://www.zdnet.com/article/iphone-15-plus-review/), are expected to decline by about 2% this year, according to estimates compiled by FactSet Systems, to 229 million units, as the current iPhone cycle underwhelms with merely iterative hardware features. 

But come 2025, wrote analyst Woodring, current Wall Street expectations for growth of 4%, to 237 million units, could turn out to be 15% higher if an iPhone 16 has enhanced AI capabilities.

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

"If we are correct, and new LLM-enabled software features drive an upgrade cycle, then we see the potential for up to 15% upside to our FY25 iPhone shipment forecast," wrote Woodring. The acronym "LLM" refers to "large language models" such as OpenAI's GPT-4.

Woodring speculates that the world will see [details at Apple's Worldwide Developer Conference](https://www.zdnet.com/article/apple-reportedly-eyeing-generative-ai-push-and-siri-overhaul-for-the-iphone/) this summer, "highlighted by an LLM-powered Siri 2.0 and a broader GenAI-enabled operating system that has the potential to catalyze an iPhone upgrade cycle." 

Why is "LLM-powered" such a big deal? To use large language models akin to OpenAI's GPT-4 requires a phone to go back and forth to the network, sending prompts and retrieving responses. Even on a desktop computer with an ethernet connection, the round-trip means waiting a while for a response. In a mobile device on a cellular network, relying on the cloud connection could result in one of those awkward moments where Siri seems brain-dead.

**Also:** [**iPhone 15 review: I spent a month with Apple's base model and found it more 'Pro' than ever**](https://www.zdnet.com/article/iphone-15-plus-review/)

Instead, what's needed is to eliminate the cloud reliance and move more of the LLM processing locally, on the device. Apple already has what it calls the "Neural Engine" in the iPhone, a separate collection of circuits for running AI. However, the AI tasks performed by the Neural Engine -- tasks much less demanding than an LLM -- are likely to involve very carefully defined functions such as face recognition, where the use of the circuits has been carefully curated. 

Taking an off-the-shelf large language model and running it locally is bound to be a much more demanding task. 

Woodring bases much of his enthusiasm about this year's AI on a paper published this month by Apple researchers Keivan Alizadeh and colleagues, titled, "LLM in a flash: Efficient large language model inference with limited memory," which is [posted on the arXiv pre-print server](https://arxiv.org/abs/2312.11514).

**Also: [Humane's aspiring smartphone-killer 'Ai Pin' may be the most 2023 product yet](https://www.zdnet.com/article/humanes-aspiring-smartphone-killer-ai-pin-may-be-the-most-2023-product-yet/)**

The crux of the paper is that LLMs take up a lot of memory, and Apple has found a clever way to use the vast storage of the resident flash memory -- the stuff that holds the iPhone's files. With special software, an LLM can be easily moved into and out of main memory, DRAM, with the illusion of having a lot more DRAM than is typical on the phone.

As Alizadeh and colleagues write, the tactics they use with memory "enable running models up to twice the size of the available DRAM," and speed up the making of predictions on a device by as much as 25 times. 

The problem the authors tackle is that there just isn't enough DRAM on most mobiles, while LLMs keep getting bigger and bigger. "A 7-billion-parameter model requires over 14GB of memory just to load the parameters in half-precision floating point format, exceeding the capabilities of most edge devices," write Alizadeh and team, referring to the neural "weights" or "parameters," values that are stored in memory that give shape to a trained neural network. 

**Also:** [**Samsung's new Galaxy S24 beats the iPhone 15 Pro in one very meaningful way**](https://www.zdnet.com/article/samsungs-new-galaxy-s24-beats-the-iphone-15-pro-in-one-very-meaningful-way/)

Apple doesn't disclose amounts of onboard DRAM, but the site Everymac [cites third-party data](https://everymac.com/systems/apple/iphone/specs/apple-iphone-15-pro-max-united-states-a2849-specs.html) suggesting that the iPhone 15 Pro Max has 8GB of DRAM. Samsung's recently unveiled [Galaxy S24 Ultra](https://www.zdnet.com/article/samsung-unpacked-2024-recap-galaxy-ai-s24-ultra-smart-ring-and-more/) has 12GB of DRAM, [according to Samsung](https://shop-links.co/link/?exclusive=1&publisher_slug=itechdaily19598&url=https%3A%2F%2Fwww.samsung.com%2Fus%2Fsmartphones%2Fgalaxy-s24-ultra%2Fcompare%2F%3Fdevice-1%3Dsamsung-galaxy-s24-ultra%26device-2%3Dsamsung-galaxy-s24%2B%26device-3%3Dsamsung-galaxy-s24). 

Much more memory, of course, is available in the NAND flash storage in phones. The Pro Max has a terabyte of memory, as does the S24 Ultra. The greater issue is moving data back and forth. NAND flash is slower than DRAM memory, so fetching data from it each time is slower than operating out of DRAM entirely. 

Apple experiments with keeping the neural network in flash memory and putting only some of it in DRAM. 

Apple

What's more, moving data from the flash memory into the DRAM memory entails a transfer time, which introduces a delay, called latency, between what the user tries to do and the results. That could mean the user waiting seconds between, say, typing into an LLM prompt and getting a response -- just as bad as going to the cloud. Even moving from DRAM into the phone's central processor introduces a delay, the authors note. 

Their solution is to use a fundamental aspect of neural networks including LLMs: sparsity. Sparsity means that a lot of those neural weights that make up the neural network are actually empty. They have a numeric value of zero. They can be ignored, therefore, so that only a small number of the total weights need to be fetched from memory.

**Also: [Buying the Samsung Galaxy S24 for its AI features? Read the fine print first](https://www.zdnet.com/article/buying-the-samsung-galaxy-s24-for-its-ai-features-read-the-fine-print-first/)**

"LLMs exhibit a high degree of sparsity," write Alizadeh and team. "We exploit this sparsity to selectively load only parameters from flash memory that either have non-zero input or are predicted to have non-zero output."

The authors also come up with many clever techniques about _which_ of those non-zero weights to call from flash memory, things such as pre-fetching the weights that are most likely to be needed based on the prediction task that the user may trigger next.

The report demonstrates dramatic speed-ups when running two open-sourceLLMs: Meta's [Open Pretrained Transformer](https://arxiv.org/abs/2205.01068), and the [Falcon series of language models](https://arxiv.org/pdf/2311.16867.pdf) from the Technology Innovation Institute of Abu Dhabi.

Apple was able to reduce the latency of serving large language models.

Apple

There's just one problem with the hopes of Woodring and others for an iPhone 16 as a supercomputer for AI: The work in the research paper was done on a Mac. Specifically, Alizadeh and team developed all of their techniques on Apple's "[M1 Max](https://www.zdnet.com/article/apple-silicon-rosetta-m1-m2-m3-soc-why-these-terms-matter-to-every-computer-buyer/)" processor, which is only in the MacBook Pro and Apple's Studio desktop. That chip is substantially bigger and more powerful than the "A17 Pro" found in the iPhone 15\. 

Moreover, as the authors state, their tests don't touch on one of the things that users of pocket computers care most about: battery life. "A critical aspect for future exploration is the analysis of power consumption and thermal limitations inherent in the methods we propose, particularly for on-device deployment," they write. 

**Also:** [**Apple Silicon, Rosetta, M1, M2, M3, SoC: Why these terms matter to every computer buyer**](https://www.zdnet.com/article/apple-silicon-rosetta-m1-m2-m3-soc-why-these-terms-matter-to-every-computer-buyer/)

Nevertheless, the M-series silicon from Apple has generally found its way into mobile devices. The original M1 and M2 chips have ended up in versions of Apple's iPad Pro and iPad Air tablets. That means there is a continuum to both Apple's chips and software efforts such as the kind Alizadeh and team explore. 

It's possible that an "A18" processor in an iPhone 16 Pro Max could strike a balance between running smart sparsity and conserving battery life. It's also possible that the kind of approach discussed in the paper could be used with very small versions of LLMs as a first step. Both models tested in the paper by Alizadeh have 7 billion parameters, which makes them fairly small as LLMs go. Apple could go even smaller, below a billion parameters, to preserve energy _and_ memory usage _and_ CPU usage. 

Regardless of what shows up at WWDC, or in September's expected iPhone unveiling, one can presume the structure of the research by Alizadeh and team shows AI is coming out of the cloud and into your pocket sooner or later.

#### Apple

[iPhone 16 Pro upgrade: If you have a 3 year-old iPhone, here are all the new features you'll get](https://www.zdnet.com/article/iphone-16-pro-and-pro-max-hands-on/ "iPhone 16 Pro upgrade: If you have a 3 year-old iPhone, here are all the new features you'll get")

[My biggest regret with upgrading my iPhone to iOS 18 (and I'm not alone)](https://www.zdnet.com/article/my-biggest-regret-with-upgrading-my-iphone-to-ios-18-and-im-not-alone/ "My biggest regret with upgrading my iPhone to iOS 18 (and I'm not alone)")

[We've used every iPhone 16 model and here's our best buying advice for 2024](https://www.zdnet.com/article/iphone-16-pro-max-buying-advice-2024/ "We've used every iPhone 16 model and here's our best buying advice for 2024")

[6 iOS 18 settings I changed immediately - and why you should too](https://www.zdnet.com/article/6-ios-18-settings-i-changed-immediately-and-why-you-should-too/ "6 iOS 18 settings I changed immediately - and why you should too")

* [iPhone 16 Pro upgrade: If you have a 3 year-old iPhone, here are all the new features you'll get](https://www.zdnet.com/article/iphone-16-pro-and-pro-max-hands-on/ "iPhone 16 Pro upgrade: If you have a 3 year-old iPhone, here are all the new features you'll get")
* [My biggest regret with upgrading my iPhone to iOS 18 (and I'm not alone)](https://www.zdnet.com/article/my-biggest-regret-with-upgrading-my-iphone-to-ios-18-and-im-not-alone/ "My biggest regret with upgrading my iPhone to iOS 18 (and I'm not alone)")
* [We've used every iPhone 16 model and here's our best buying advice for 2024](https://www.zdnet.com/article/iphone-16-pro-max-buying-advice-2024/ "We've used every iPhone 16 model and here's our best buying advice for 2024")
* [6 iOS 18 settings I changed immediately - and why you should too](https://www.zdnet.com/article/6-ios-18-settings-i-changed-immediately-and-why-you-should-too/ "6 iOS 18 settings I changed immediately - and why you should too")

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
<li><a href="https://snapchat-videos.techidaily.com/new-in-2024-customize-confidently-express-optimizing-your-voice-on-snapchat/"><u>[New] In 2024, Customize, Confidently Express Optimizing Your Voice on Snapchat</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-understanding-the-transformations-in-vegaspro-19/"><u>[New] Understanding the Transformations in VegasPro '19</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unmatched-audio-and-video-elite-webcams-for-podcasting/"><u>[New] Unmatched Audio & Video Elite Webcams for Podcasting</u></a></li>
<li><a href="https://some-skills.techidaily.com/new-unveiling-exclusive-templates-for-tiktok-backdrops/"><u>[New] Unveiling Exclusive Templates for TikTok Backdrops</u></a></li>
<li><a href="https://fox-blue.techidaily.com/2024-approved-ultimate-flashy-game-collection-quick-and-lightweight/"><u>2024 Approved Ultimate Flashy Game Collection - Quick and Lightweight</u></a></li>
<li><a href="https://buynow-info.techidaily.com/experience-superior-connectivity-with-the-netgear-nighthawk-x4-a-deep-dive-into-its-mesh-capabilities/"><u>Experience Superior Connectivity with the Netgear Nighthawk X4: A Deep Dive Into Its Mesh Capabilities</u></a></li>
<li><a href="https://win-able.techidaily.com/get-back-in-the-game-fixes-when-multiversus-wont-open-on-your-computer/"><u>Get Back in the Game: Fixes When MultiVersus Won't Open on Your Computer</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-solve-mkv-lagging-problem-in-huawei-nova-y71-by-aiseesoft-video-converter-play-mkv-on-android/"><u>How to solve MKV lagging problem in Huawei Nova Y71?</u></a></li>
<li><a href="https://android-frp.techidaily.com/in-2024-how-to-bypass-google-frp-lock-on-nokia-xr21-devices-by-drfone-android/"><u>In 2024, How to Bypass Google FRP Lock on Nokia XR21 Devices</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/in-2024-life360-learn-how-everything-works-on-samsung-galaxy-a14-4g-drfone-by-drfone-virtual-android/"><u>In 2024, Life360 Learn How Everything Works On Samsung Galaxy A14 4G | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-maximizing-your-designs-with-free-clip-art/"><u>In 2024, Maximizing Your Designs with FREE Clip Art</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-swiftly-assemble-a-stunning-google-image-mosaic-with-ease/"><u>In 2024, Swiftly Assemble a Stunning Google Image Mosaic with Ease</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-experts-method-for-timestamping-your-youtube-videos/"><u>In 2024, The Expert's Method for Timestamping Your YouTube Videos</u></a></li>
<li><a href="https://some-tips.techidaily.com/tiktokplusinstagram-social-media-fusion-guide-for-2024/"><u>TikTok+Instagram Social Media Fusion Guide for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-10-sci-fi-vr-adventures-new-realms-unveiled-for-2024/"><u>Top 10 Sci-Fi VR Adventures New Realms Unveiled for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-potential-the-right-propeller-match-in-fpv-flight-for-2024/"><u>Unlocking Potential The Right Propeller Match in FPV Flight for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-potential-through-virtualization-for-2024/"><u>Unlocking Potential Through Virtualization for 2024</u></a></li>
<li><a href="https://games-able.techidaily.com/upgraded-visuals-on-xbox-via-secondary-laptop-display/"><u>Upgraded Visuals on Xbox via Secondary Laptop Display</u></a></li>
<li><a href="https://facebook-record-videos.techidaily.com/whats-the-best-youtube-thumbnail-size-in-2024/"><u>What's the Best YouTube Thumbnail Size, In 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2130874/7443" target="_top" id="2130874">
  <img src="//a.impactradius-go.com/display-ad/7443-2130874" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2130874/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

