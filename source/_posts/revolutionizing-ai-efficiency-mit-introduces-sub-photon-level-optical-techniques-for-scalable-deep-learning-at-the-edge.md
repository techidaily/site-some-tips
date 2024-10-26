---
title: "Revolutionizing AI Efficiency: MIT Introduces Sub-Photon Level Optical Techniques for Scalable Deep Learning at the Edge"
date: 2024-10-25T18:43:23.570Z
updated: 2024-10-26T17:42:10.741Z
tags:
  - edge-computing
categories:
  - tech
thumbnail: https://thmb.techidaily.com/4af354c0c4f31e85da7815990d834961f2e7342ecb73532a36e97929bcf9934e.jpg
---

## Revolutionizing AI Efficiency: MIT Introduces Sub-Photon Level Optical Techniques for Scalable Deep Learning at the Edge

![Photonic equation against colorful background.](https://www.zdnet.com/a/img/resize/d6c457c11a76b01750b56667c46c5e64a2920514/2022/10/31/2478f28e-dfe4-4c71-92c7-fde978a3deb9/photonic-equation-landscape.jpg?auto=webp&width=1280)

MIT scientists used special photodetectors to perform an AI equation just by beaming light to a low-power client device. The approach could be especially useful in deep space. 

Tiernan Ray/ZDNET

One of the most pressing concerns for the industrial application of [artificial intelligence](https://www.zdnet.com/article/what-is-ai-heres-everything-you-need-to-know-about-artificial-intelligence/) is how to run the programs on small computing devices that have very little processing power, very little memory, and possibly a limit in terms of energy available, in the case of batteries.

### Innovation

* [Apple Vision Pro review: Fascinating, flawed, and needs to fix 5 things](https://www.zdnet.com/article/apple-vision-pro-review/)
* [Apple builds a slimmed-down AI model using Stanford, Google innovations](https://www.zdnet.com/article/apple-builds-a-slimmed-down-ai-model-using-stanford-google-innovations/)
* [I tested the AI gadget that got the internet buzzing and it left me wanting more](https://www.zdnet.com/article/i-tested-the-ai-gadget-that-got-the-internet-buzzing-and-it-left-me-wanting-more/)
* [9 biggest announcements at Google I/O 2024: Gemini, Search, Project Astra, and more](https://www.zdnet.com/article/is-openai-sweating-9-google-features-announced-for-gemini-search-android-and-more/)

The so-called edge market for AI has been a huge area of late, with [startups receiving tens of millions in venture capital](https://www.zdnet.com/article/the-ai-edge-inference-chip-market-is-raging/) to come up with chips and software. The edge effort has led to special development tools for machine-learning forms of AI, such as the [TinyML initiative from Google](https://www.zdnet.com/article/machine-learning-at-the-edge-tinyml-is-getting-big/). 

Those two paths represent two philosophies: Either make edge devices more powerful, or slim down AI programs to use fewer calculations. 

**Also:** [**AI's true goal may no longer be intelligence**](https://www.zdnet.com/article/ai-true-goal-may-no-longer-be-intelligence/)

There is third possible approach, and that is to try and balance more carefully what work is done on constrained devices and by what means. That's the plan put forward in October [by MIT researchers in the scholarly journal Science](https://www.science.org/doi/10.1126/science.abq8271). 

Researcher Alexander Sludds and colleagues at MIT's Research Laboratory of Electronics, Computer Science and Artificial Intelligence Laboratory, and Lincoln Laboratory, in partnership with Nokia and [NTT Research](https://ntt-research.com/about/), have developed a system that uses photonics to beam data to a client device where it can be calculated in the optical domain in a vastly more energy-efficient manner.

Their network setup, which they call Netcast, can perform the fundamental operation of manipulating the weights, or parameters, of a deep neural network, using about 10 femtoJoules of power, or 10 fJ, which, they relate, "is three orders of magnitude lower than is possible in existing digital CMOS" -- meaning standard semiconductor chips.

A femtoJoule, written as a decimal point followed by 14 zeros and a 1, is one-quadrillionth, with is a very tiny fraction of a joule, a joule being the amount of electricity to run a 1-watt device for a second. 

That tiny, tiny fraction of a watt is a major energy savings and is important because many edge devices, the authors note, will have a total power budget in milliwatts, or thousandths of a watt, versus typical computing devices using tens or hundreds of watts. The femtoJoule operation of Netcast effectively gets the program below what had to date been "a stubborn bottleneck near 1 pJ," aka one picoJoule, or one-trillionth of a joule.

**Also:** [**The AI edge chip market is on fire, kindled by 'staggering' VC funding**](https://www.zdnet.com/article/the-ai-edge-inference-chip-market-is-raging/)

The key to Netcast was how to reduce the work the client has to perform for the fundamental operation of a neural net in order to get within that 10-femtoJoule budget. 

A neural net makes predictions by passing some input data to its parameters or weights, and multiplying the input by the weight. That mathematical operation, the product of an input vector and a parameter matrix, is called a multiply-accumulate, or MAC, operation, and neural net programs do tons of them every second as the multiple weights of each network layer are applied to the input.

The biggest power hog for most neural nets in general is fetching data from RAM memory chips and accessing the network. That's a problem because the neural weights are usually stored in RAM, so every layer of MAC operations can require multiple trips out over the PCIe bus to RAM and perhaps even to a network line card for remote memory stores. 

Hence, the key to Netcast was how to minimize memory access and network traffic for the client device. 

Sludds et al.

The solution is an existing photonic technology called wavelength division multiplexing. Using WDM, as it's commonly referred to, multiple pieces of data can be sent across a fiber-optic line simultaneously by assigning each piece of data its own wavelength of light so that the multiple data share the total available spectrum of radiation in the fiber. WDM is a very mature, solid technology that is used in all modern telecom networks to increase the capacity of fiber-optic data transmission; it forms the backbone of the Internet. 

Each row of a matrix can be encoded on a wavelength of light and then "broadcast" to the client device, so that a multi-wavelength WDM signal can send an entire weight matrix or even multiple matrices. At the client device, an optical receiver recovers the data encoded in each wavelength and combines it with the input data to perform the matrix multiply in the optical domain rather than electrically. The product can then be stored electrically on local RAM once converted from the optical signal.

Sludds and team write that this results in a dramatic simplification of the components that need to be in a client device at the edge. 

"This architecture minimizes the active components at the client, requiring only a single optical transceiver modulator, digital-to-analog converter (DAC), and analog-to-digital converter (ADC)."

The authors constructed an actual version of Netcast that runs over 84 kilometers of fiber using WDM with a capacity of 2.4 terabits per second, running from the main MIT campus to the Lincoln Lab and back. Their test of the system is to perform predictions on a classic machine learning task, the MNIST [database of handwritten characters](https://en.wikipedia.org/wiki/MNIST%5Fdatabase). The images of the handwritten characters are input to the neural net, and the net has to carry out an image recognition task, identifying which character each picture represents.

"Using 1,000 test images locally, we demonstrate 98.7% accurate computation, comparable with the model's baseline accuracy of 98.7%," they report.

The authors go even further. Anticipating deployment in satellites and other exotic locales, they worked on coming up with photodetectors, called integrating receivers, that can work with very small numbers of photons. 

"Applications of Netcast, including free-space deployment to drones or spacecraft, can operate in deeply photon-starved environments," they write. A version of their integrating receivers is able to detect the results of a MAC operation operating at only fractions of a femtoJoule, known as an attoJoule, which requires only 100 photons for the MAC operation. 

But the authors go even further. They were able to go all the way to a theoretical limit of Netcast where each Mac requires less than a single photon to be detected. Using what are called superconducting nanowire single-photon detectors (SNSPDs), they construct a receiver that can measure the results of each MAC with less than a photon of information. 

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2100537/7443" target="_top" id="2100537">
  <img src="//a.impactradius-go.com/display-ad/7443-2100537" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2100537/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Space

* [What is Artemis? Everything you need to know about NASA's new moon mission](https://www.zdnet.com/article/what-is-artemis-everything-you-need-to-know-about-nasas-moon-mission/)
* [NASA has solved the mystery of Voyager 1's strange data transmissions](https://www.zdnet.com/article/nasa-has-solved-the-mystery-of-voyager-1s-strange-data-transmissions/)
* [NASA's new tiny, high-powered laser could find water on the Moon](https://www.zdnet.com/article/nasa-develops-a-tiny-high-powered-laser-to-find-water-on-the-moon/)
* [NASA is blazing an inspirational trail. We need to make sure everyone can follow it](https://www.zdnet.com/article/nasa-is-blazing-an-inspirational-trail-we-need-to-make-sure-everyone-can-follow-it/)

"This result may at first seem surprising given that less than a single photon per MAC is counterintuitive," wrote Sludds and team. "We can understand this measurement better by noting that at readout, we have performed a vector-vector product with M = 100 MACs. Each MAC can have less than a single photon in it, but the measured signal will have many photons in it."

The implications for computing could be profound. 

"The realization of computing with less than one photon per MAC," they wrote, "could enable a new class of computing systems that protect both client input and server weight data" from the standpoint of data privacy. It could also make computing on spacecraft more reliable. "Weight data from a directional base station could be transmitted to the spacecraft and classified on the craft, before the results are transmitted to Earth."

All the parts of Netcast can be made today in any standard semiconductor chip factory, Sludds and team noted.

In concluding, they wrote, "Our approach removes a fundamental bottleneck in edge computing, enabling high-speed computing on deployed sensors and drones."

#### Artificial Intelligence

[Photoshop vs. Midjourney vs. DALL-E 3: Only one AI image generator passed my 5 tests](https://www.zdnet.com/article/is-photoshops-new-text-to-image-as-good-as-midjourney-and-dall-e-we-test-it-and-see/ "Photoshop vs. Midjourney vs. DALL-E 3: Only one AI image generator passed my 5 tests")

[AI-powered 'narrative attacks' a growing threat: 3 defense strategies for business leaders](https://www.zdnet.com/article/ai-powered-narrative-attacks-a-growing-threat-3-defense-strategies-for-business-leaders/ "AI-powered 'narrative attacks' a growing threat: 3 defense strategies for business leaders")

[Copilot Pro vs. ChatGPT Plus: Which AI chatbot is worth your $20 a month?](https://www.zdnet.com/article/copilot-pro-vs-chatgpt-plus-which-is-ai-chatbot-is-worth-your-20-a-month/ "Copilot Pro vs. ChatGPT Plus: Which AI chatbot is worth your $20 a month?")

[How my 4 favorite AI tools help me get more done at work](https://www.zdnet.com/article/how-my-4-favorite-ai-tools-help-me-get-more-done-at-work/ "How my 4 favorite AI tools help me get more done at work")

* [Photoshop vs. Midjourney vs. DALL-E 3: Only one AI image generator passed my 5 tests](https://www.zdnet.com/article/is-photoshops-new-text-to-image-as-good-as-midjourney-and-dall-e-we-test-it-and-see/ "Photoshop vs. Midjourney vs. DALL-E 3: Only one AI image generator passed my 5 tests")
* [AI-powered 'narrative attacks' a growing threat: 3 defense strategies for business leaders](https://www.zdnet.com/article/ai-powered-narrative-attacks-a-growing-threat-3-defense-strategies-for-business-leaders/ "AI-powered 'narrative attacks' a growing threat: 3 defense strategies for business leaders")
* [Copilot Pro vs. ChatGPT Plus: Which AI chatbot is worth your $20 a month?](https://www.zdnet.com/article/copilot-pro-vs-chatgpt-plus-which-is-ai-chatbot-is-worth-your-20-a-month/ "Copilot Pro vs. ChatGPT Plus: Which AI chatbot is worth your $20 a month?")
* [How my 4 favorite AI tools help me get more done at work](https://www.zdnet.com/article/how-my-4-favorite-ai-tools-help-me-get-more-done-at-work/ "How my 4 favorite AI tools help me get more done at work")

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
<li><a href="https://fox-boxes.techidaily.com/new-step-by-step-kinemaster-guidance-for-flawless-green-screen-techniques/"><u>[New] Step-by-Step Kinemaster Guidance for Flawless Green Screen Techniques</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-inshots-ecosystem-a-detailed-editor-app-study/"><u>[Updated] InShot’s Ecosystem A Detailed Editor App Study</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-ultimate-bundle-6-powerful-apps-to-remove-signature-borders/"><u>[Updated] The Ultimate Bundle – 6 Powerful Apps to Remove Signature Borders</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-top-15-nba-live-stream-techniques/"><u>[Updated] Top 15 NBA LIVE STREAM Techniques</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-ultimate-facetune-guide-elevating-your-image-quality/"><u>[Updated] Ultimate Facetune Guide Elevating Your Image Quality</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-perfect-your-content-with-tiktoks-number-manipulation-tricks/"><u>2024 Approved Perfect Your Content with TikTok's Number Manipulation Tricks</u></a></li>
<li><a href="https://location-fake.techidaily.com/a-detailed-guide-on-faking-your-location-in-mozilla-firefox-on-apple-iphone-15-pro-max-drfone-by-drfone-virtual-ios/"><u>A Detailed Guide on Faking Your Location in Mozilla Firefox On Apple iPhone 15 Pro Max | Dr.fone</u></a></li>
<li><a href="https://extra-hints.techidaily.com/constructing-home-made-vr-headgear-with-google-cards/"><u>Constructing Home-Made VR Headgear with Google Cards</u></a></li>
<li><a href="https://fox-blue.techidaily.com/cutting-edge-or-outdated-full-review-and-guide-to-vitas-editor-for-2024/"><u>Cutting Edge or Outdated? Full Review & Guide to Vita's Editor for 2024</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-sign-docm-file-by-digital-signature-by-ldigisigner-sign-a-word-sign-a-word/"><u>How to sign .docm file by digital signature</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-strategic-steps-to-elevate-your-podcast-imagery/"><u>In 2024, Strategic Steps to Elevate Your Podcast Imagery</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unveiling-modern-techniques-for-gesture-interpretation/"><u>In 2024, Unveiling Modern Techniques for Gesture Interpretation</u></a></li>
<li><a href="https://hardware-help.techidaily.com/instant-access-amd-ryzen-5-2600-quick-and-easy-method/"><u>Instant Access: AMD Ryzen 지팬 5 2600의 드라이버를 저장하세요 | Quick & Easy Method</u></a></li>
<li><a href="https://voice-adjusting.techidaily.com/new-unveiling-key-features-a-deep-dive-into-twistedwave-audio-processor/"><u>New Unveiling Key Features A Deep Dive Into TwistedWave Audio Processor</u></a></li>
<li><a href="https://article-tips.techidaily.com/superior-web-destinations-alarm-ringtone-downloads-guide/"><u>Superior Web Destinations Alarm Ringtone Downloads Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-next-level-of-immersion-top-10-vr-gear-for-2024/"><u>The Next Level of Immersion (Top 10 VR Gear) for 2024</u></a></li>
<li><a href="https://video-screen-grab.techidaily.com/top-15-open-world-games-to-beat-the-climb/"><u>Top 15 Open World Games to Beat the Climb</u></a></li>
</ul></div>

