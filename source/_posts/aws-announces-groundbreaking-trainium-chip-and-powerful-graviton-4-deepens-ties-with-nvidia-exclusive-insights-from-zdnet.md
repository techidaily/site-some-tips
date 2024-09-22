---
title: AWS Announces Groundbreaking Trainium Chip and Powerful Graviton 4, Deepens Ties with Nvidia – Exclusive Insights From ZDNET
date: 2024-09-17 14:45:30
updated: 2024-09-20 11:59:46
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/cloud/    https://www.zdnet.com/a/img/resize/4753a31a7fbbdfea66337a561ae5bccb114837e7/2023/11/28/7eb1230f-dad4-4b7a-ba26-711a10fae110/awsreinvent.jpg?width=170&height=96&fit=crop&auto=webp
---

## AWS Announces Groundbreaking Trainium Chip and Powerful Graviton 4, Deepens Ties with Nvidia – Exclusive Insights From ZDNET

![aws-graviton4-and-aws-trainium2-prototype](https://www.zdnet.com/a/img/resize/8bb8eca0bb19370c3224e9c0d3911db25745f15b/2023/11/28/68ef1aa8-81cf-4c41-b1de-ef4b2a78301b/aws-graviton4-and-aws-trainium2-prototype.jpg?auto=webp&width=1280)

The Graviton 4 chip, left, is a general-purpose microprocessor chip being used by SAP and others for large workloads, while Trainium 2 is a special-purpose accelerator chip for very large neural network programs such as generative AI.

Amazon AWS

At its annual AWS re:Invent developer conference in Las Vegas, Amazon on Tuesday announced a new version of Trainium 2, its dedicated chip for training neural networks. Trainium 2 is tuned specifically for training so-called large language models (LLMs) and foundation models -- the kinds of generative AI programs such as OpenAI's GPT-4.

The company also unveiled a new version of its custom microprocessor, Graviton 4, and said it is extending its partnership with Nvidia to run Nvidia's most advanced chips in its cloud computing service. 

**Also: [The future of cloud computing, from hybrid to edge to AI-powered](https://www.zdnet.com/article/the-future-of-cloud-computing-from-hybrid-to-edge-to-ai-powered/)**

The Trainium 2 is designed to handle neural networks with trillions of parameters, or neural weights, which are the functions of the program's algorithm that give it scale and power, generally speaking. Scaling to larger and larger parameters is a focus of the entire AI industry. 

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

The trillion-parameter count has become something of an industry obsession because of the fact that the human brain is believed to contain 100 trillion neuronal connections -- making a trillion-parameter neural network program seem related to the human brain, whether or not it in fact is.

The chips are "designed to deliver up to four times faster training performance and three times more memory capacity" than their predecessor, "while improving energy efficiency (performance/watt) up to two times," said Amazon.

Amazon is making the chips available in instances of its EC2 cloud computing service known as "Trn2" instances. The instance offers 16 of the Trainium 2 chips operating in concert, which can be extended to 100,000 instances, Amazon said. Those larger instances are interconnected using the company's networking system, called the Elastic Fabric Adapter, which can provide for a total of 65 exaFLOPs of computing power. ([One exaFLOP](https://en.wikipedia.org/wiki/FLOPS) is a billion, billion floating point operations per second.)

**Also: [AWS unveils local cloud zones for exclusive customer use](https://www.zdnet.com/article/aws-unveils-local-cloud-zones-for-exclusive-customer-use/)**

At that scale of compute, said Amazon, "Customers can train a 300-billion parameter LLM in weeks versus months." 

Besides serving customers, Amazon has additional incentives to continue to push the envelope on AI silicon. The company [has invested $4 billion](https://www.zdnet.com/article/amazon-ups-generative-ai-ante-with-4b-investment-in-anthropic/) in privately held generative AI startup Anthropic, a group that broke off from OpenAI. That investment puts the company in a position to compete with Microsoft's exclusive deal with OpenAI.

The Graviton 4 chip, which is built on the microprocessor intellectual property of ARM Holdings, competes with processors from Intel and Advanced Micro Devices based on the older x86 chip standard. The Graviton 4 has "30% better compute performance," Amazon said. 

**Also: [Why Nvidia is teaching robots to twirl pens and how generative AI is helping](https://www.zdnet.com/article/why-nvidia-is-teaching-robots-to-twirl-pens-and-how-generative-ai-is-helping/)**

Unlike the Trainium chips for AI, Graviton processors are meant to run more conventional workloads. Amazon AWS said customers -- including Datadog, DirecTV, Discovery, Formula 1, Nielsen, Pinterest, SAP, Snowflake, Sprinklr, Stripe, and Zendesk -- use the Graviton chips "to run a broad range of workloads, such as databases, analytics, web servers, batch processing, ad serving, application servers, and microservices."

SAP said in prepared remarks that it has been able to achieve "35% better price performance for analytical workloads" running its HANA in-memory database on the Graviton chips, and that "we look forward to evaluating Graviton4, and the benefits it can bring to our joint customers." 

The new chips follow by two years [the introduction in 2021](https://www.zdnet.com/article/aws-fleshes-out-processor-roadmap-with-graviton3-trainium-new-instances/) of Graviton 3 and the original Trainium. 

Amazon's news follows the introduction by [Microsoft last week](https://www.zdnet.com/article/microsoft-unveils-first-ai-chip-maia-100-and-cobalt-cpu/) of its first chips for AI. Alphabet's Google, the other cloud titan alongside Amazon and Microsoft, preceded both in 2016 with the first cloud chip for AI, the TPU, or Tensor Processing Unit, of which it has since offered multiple generations. 

**Also: [Amazon turns Fire TV Cube into a thin client for enterprises](https://www.zdnet.com/article/amazon-turns-fire-tv-cube-into-a-thin-client-for-enteprises/)**

In addition to the two new chips, Amazon said it extended its strategic partnership with AI chip giant Nvidia. AWS will be the first cloud service to run the forthcoming GH200 Grace Hopper multi-chip product from Nvidia, which combines the Grace ARM-based CPU and the Hopper H100 GPU chip. 

The GH200 chip, which is supposed to start shipping next year, is the next version of the [Grace Hopper combo chip](https://www.zdnet.com/article/nvidia-boosts-its-superchip-grace-hopper-with-faster-memory-for-ai/), announced earlier this year, which is already shipping in its initial version in computers from Dell and others. 

The GH200 chips will be hosted on AWS via Nvidia's purpose-built AI computers, the DGX, which the two companies said will speed up the training of neural networks with more than a trillion parameters. 

Nvidia said it will make AWS its "primary cloud provider for its ML research and development."

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
