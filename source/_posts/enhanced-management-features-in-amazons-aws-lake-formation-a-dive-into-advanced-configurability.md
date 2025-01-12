---
title: "Enhanced Management Features in Amazon's AWS Lake Formation: A Dive Into Advanced Configurability"
date: 2025-01-10T17:50:04.243Z
updated: 2025-01-12T18:14:52.911Z
tags:
  - amazon
categories:
  - tech
thumbnail: https://thmb.techidaily.com/bc4c1fafbeb0a4b8e3066f1ca761f451b6c08fbe8e8ce84b7a7a9649ff05ac95.jpg
---

## Enhanced Management Features in Amazon's AWS Lake Formation: A Dive Into Advanced Configurability

Amazon Web Services on Tuesday announced the general availability of tools that bring more [fine-grained control to data lake management](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2Fblogs%2Faws%2Faws-lake-formation-general-availability-of-cell-level-security-and-governed-tables-with-automatic-compaction%2F%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7C3d788e6b-a42d-486e-8a48-2489b7430d1b%7Cdtp&dtb=1). 

First, Row and Cell-Level Security for Lake Formation "puts the right data in the hands of the right people," AWS CEO Adam Selipsky said during his AWS re:Invent keynote address. 

Lake Formation already enables customers to move data into S3 data lakes, clean, and classify it using machine learning and secure access to sensitive data. The new tool now lets customers enforce access controls for individual rows and cells. Instead of creating multiple tables for each user and managing data pipelines, a customer can define a set of policies for specific rows for specific users. Customers control access to specific rows and columns in query results and within AWS Glue ETL jobs based on the identity of who is performing the action. 

Meanwhile, Transactions for Governed Tables in Lake Formation eliminates the need for batching updates. "Data isn't static," Selipsky said. "More and more data is being added and moved rapidly."

Now customers can create a new type of table -- a governed table -- and Lake Formation automatically manages conflicts and errors for consistent view of data. Users will be able to keep up with the data in real-time. 

Governed tables support ACID transactions that let multiple users concurrently and reliably insert and delete data across multiple governed tables. ACID transactions also let customers run queries that return consistent and up-to-date data. In case of errors in ETL processes, or during an update, changes are not committed and will not be visible.

Customers using governed tables can use automatic compaction for storage optimization. When this option is enabled, Lake Formation automatically compacts small S3 objects in governed tables into larger objects to optimize access via analytics engines, such as[Amazon Athena](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2Fathena%2F%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7C3d788e6b-a42d-486e-8a48-2489b7430d1b%7Cdtp&dtb=1) and[Amazon Redshift Spectrum](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Fdocs.aws.amazon.com%2Fredshift%2Flatest%2Fdg%2Fc-getting-started-using-spectrum.html%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7C3d788e6b-a42d-486e-8a48-2489b7430d1b%7Cdtp&dtb=1). 

#### AWS re:Invent

[AWS ups its industry ground game at re:Invent 2021](https://www.zdnet.com/article/aws-ups-its-industry-ground-game-at-reinvent-2021/ "AWS ups its industry ground game at re:Invent 2021")

[AWS CEO unveils new private 5G service](https://www.zdnet.com/article/aws-ceo-announces-private-5g-at-reinvent-2021/ "AWS CEO unveils new private 5G service")

[AWS takes aim at mainframes with migration service](https://www.zdnet.com/article/aws-takes-aim-at-mainframes-with-migration-service/ "AWS takes aim at mainframes with migration service")

[AWS, CrowdStrike, and Presidio partner for ransomware mitigation kit](https://www.zdnet.com/article/amazon-web-services-crowdstrike-and-presidio-partner-for-ransomware-mitigation-kit/ "AWS, CrowdStrike, and Presidio partner for ransomware mitigation kit")

[AWS launches quartet of serverless, on-demand solutions](https://www.zdnet.com/article/aws-goes-all-in-on-serverless-on-demand-solutions-with-quartet-of-launches/ "AWS launches quartet of serverless, on-demand solutions")

[AWS targets auto and industrial sectors with FleetWise, TwinMaker](https://www.zdnet.com/article/aws-targets-auto-and-industrial-sectors-with-fleetwise-twinmaker/ "AWS targets auto and industrial sectors with FleetWise, TwinMaker")

[Processor roadmap adds Graviton3, Trainium, new instances](https://www.zdnet.com/article/aws-fleshes-out-processor-roadmap-with-graviton3-trainium-new-instances/ "Processor roadmap adds Graviton3, Trainium, new instances")

[IoT RoboRunner aims to manage robot fleets](https://www.zdnet.com/article/aws-launches-aws-iot-roborunner-aims-to-manage-robot-fleets/ "IoT RoboRunner aims to manage robot fleets")

* [AWS ups its industry ground game at re:Invent 2021](https://www.zdnet.com/article/aws-ups-its-industry-ground-game-at-reinvent-2021/ "AWS ups its industry ground game at re:Invent 2021")
* [AWS CEO unveils new private 5G service](https://www.zdnet.com/article/aws-ceo-announces-private-5g-at-reinvent-2021/ "AWS CEO unveils new private 5G service")
* [AWS takes aim at mainframes with migration service](https://www.zdnet.com/article/aws-takes-aim-at-mainframes-with-migration-service/ "AWS takes aim at mainframes with migration service")
* [AWS, CrowdStrike, and Presidio partner for ransomware mitigation kit](https://www.zdnet.com/article/amazon-web-services-crowdstrike-and-presidio-partner-for-ransomware-mitigation-kit/ "AWS, CrowdStrike, and Presidio partner for ransomware mitigation kit")
* [AWS launches quartet of serverless, on-demand solutions](https://www.zdnet.com/article/aws-goes-all-in-on-serverless-on-demand-solutions-with-quartet-of-launches/ "AWS launches quartet of serverless, on-demand solutions")
* [AWS targets auto and industrial sectors with FleetWise, TwinMaker](https://www.zdnet.com/article/aws-targets-auto-and-industrial-sectors-with-fleetwise-twinmaker/ "AWS targets auto and industrial sectors with FleetWise, TwinMaker")
* [Processor roadmap adds Graviton3, Trainium, new instances](https://www.zdnet.com/article/aws-fleshes-out-processor-roadmap-with-graviton3-trainium-new-instances/ "Processor roadmap adds Graviton3, Trainium, new instances")
* [IoT RoboRunner aims to manage robot fleets](https://www.zdnet.com/article/aws-launches-aws-iot-roborunner-aims-to-manage-robot-fleets/ "IoT RoboRunner aims to manage robot fleets")

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
<li><a href="https://eaxpv-info.techidaily.com/updated-2024-approved-capture-it-right-essential-camera-lenses-for-video-blogging/"><u>[Updated] 2024 Approved Capture It Right Essential Camera Lenses for Video Blogging</u></a></li>
<li><a href="https://article-knowledge.techidaily.com/updated-the-efficient-use-of-slug-lines-in-content-writing/"><u>[Updated] The Efficient Use of Slug Lines in Content Writing</u></a></li>
<li><a href="https://some-tips.techidaily.com/1-secure-your-online-footprint-eliminate-tracking-data-from-safari-on-mac-os/"><u>1. Secure Your Online Footprint: Eliminate Tracking Data From Safari on Mac OS</u></a></li>
<li><a href="https://tech-savvy.techidaily.com/chatgpt-visionary-exploring-top-visual-computation-techniques/"><u>ChatGPT Visionary: Exploring Top Visual Computation Techniques</u></a></li>
<li><a href="https://techtrends.techidaily.com/effective-instant-chatting-in-mozilla-thunderbird-step-by-step-tutorial/"><u>Effective Instant Chatting in Mozilla Thunderbird – Step-by-Step Tutorial</u></a></li>
<li><a href="https://some-tips.techidaily.com/experts-picks-for-the-ultimate-ipad-air-cases-of-2nndie-tested-and-reviewed-zdnet/"><u>Experts' Picks for the Ultimate iPad Air Cases of 2Nndie: Tested & Reviewed | ZDNET</u></a></li>
<li><a href="https://buynow-help.techidaily.com/fm-transmitter-cp24-by-criacr-a-miniature-marvel-with-some-limitations-in-depth-analysis/"><u>FM Transmitter CP24 by Criacr - A Miniature Marvel with Some Limitations: In-Depth Analysis</u></a></li>
<li><a href="https://some-tips.techidaily.com/how-the-new-ipad-software-patch-resolves-the-quirky-issue-of-restored-deleted-photos-ios-1751-tech-analysis/"><u>How the New iPad Software Patch Resolves the Quirky Issue of Restored Deleted Photos (iOS 17.5.1) | Tech Analysis</u></a></li>
<li><a href="https://some-tips.techidaily.com/join-the-forefront-of-innovation-early-beta-access-to-apples-vision-pro-through-testflight-discover-how/"><u>Join the Forefront of Innovation: Early Beta Access to Apple's Vision Pro Through TestFlight - Discover How !</u></a></li>
<li><a href="https://win-howtos.techidaily.com/troubleshooting-the-infamous-google-chrome-black-screen-tips-and-solutions/"><u>Troubleshooting the Infamous Google Chrome Black Screen: Tips & Solutions</u></a></li>
<li><a href="https://win-ratings.techidaily.com/understanding-windows-defender-essential-security-insights-from-yl-computing/"><u>Understanding Windows Defender - Essential Security Insights From YL Computing</u></a></li>
<li><a href="https://some-tips.techidaily.com/unlocking-the-full-capabilities-of-apples-m1-ipad-pro-anticipated-revelations-at-wwdc-and-the-role-of-artificial-intelligence/"><u>Unlocking the Full Capabilities of Apple's M1 iPad Pro: Anticipated Revelations at WWDC & The Role of Artificial Intelligence</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/3C51hzX46eY?si=o5qiDSkT7mXUGm3F" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

