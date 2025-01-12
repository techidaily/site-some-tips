---
title: Enhanced Management Features with AWS Lake Formation on Amazon
date: 2025-01-07T16:52:27.931Z
updated: 2025-01-12T16:24:47.118Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/fa262754a0a509cce346c46f20d6465b8567441f/2021/06/28/20a585a6-81ff-4046-bba5-b4f43a73ca87/aws-bugfest-competition-to-find-and-fix-amazon-bugs.jpg?width=278&height=156&fit=crop&auto=webp
---

## Enhanced Management Features with AWS Lake Formation on Amazon

Amazon Web Services on Tuesday announced the general availability of tools that bring more [fine-grained control to data lake management](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2Fblogs%2Faws%2Faws-lake-formation-general-availability-of-cell-level-security-and-governed-tables-with-automatic-compaction%2F%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7Ce02710da-7eb7-4cd1-83ad-5bcd5f170aa0%7Cdtp&dtb=1). 

First, Row and Cell-Level Security for Lake Formation "puts the right data in the hands of the right people," AWS CEO Adam Selipsky said during his AWS re:Invent keynote address. 

Lake Formation already enables customers to move data into S3 data lakes, clean, and classify it using machine learning and secure access to sensitive data. The new tool now lets customers enforce access controls for individual rows and cells. Instead of creating multiple tables for each user and managing data pipelines, a customer can define a set of policies for specific rows for specific users. Customers control access to specific rows and columns in query results and within AWS Glue ETL jobs based on the identity of who is performing the action. 

Meanwhile, Transactions for Governed Tables in Lake Formation eliminates the need for batching updates. "Data isn't static," Selipsky said. "More and more data is being added and moved rapidly."

Now customers can create a new type of table -- a governed table -- and Lake Formation automatically manages conflicts and errors for consistent view of data. Users will be able to keep up with the data in real-time. 

Governed tables support ACID transactions that let multiple users concurrently and reliably insert and delete data across multiple governed tables. ACID transactions also let customers run queries that return consistent and up-to-date data. In case of errors in ETL processes, or during an update, changes are not committed and will not be visible.

Customers using governed tables can use automatic compaction for storage optimization. When this option is enabled, Lake Formation automatically compacts small S3 objects in governed tables into larger objects to optimize access via analytics engines, such as[Amazon Athena](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2Fathena%2F%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7Ce02710da-7eb7-4cd1-83ad-5bcd5f170aa0%7Cdtp&dtb=1) and[Amazon Redshift Spectrum](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Fdocs.aws.amazon.com%2Fredshift%2Flatest%2Fdg%2Fc-getting-started-using-spectrum.html%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7Ce02710da-7eb7-4cd1-83ad-5bcd5f170aa0%7Cdtp&dtb=1). 

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
<li><a href="https://facebook-video-share.techidaily.com/new-is-screening-youtube-footage-illegal/"><u>[New] Is Screening YouTube Footage Illegal?</u></a></li>
<li><a href="https://fox-glue.techidaily.com/updated-integrated-activity-evaluation-guide/"><u>[Updated] Integrated Activity Evaluation Guide</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/updated-the-ultimate-ninja-techniques-for-instagram-reels/"><u>[Updated] The Ultimate Ninja Techniques for Instagram Reels</u></a></li>
<li><a href="https://fox-hovers.techidaily.com/beyond-expectations-the-new-samsung-ubd-k8500-edition-for-2024/"><u>Beyond Expectations The New Samsung UBD-K8500 Edition for 2024</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-transfer-contacts-from-htc-u23-to-iphone-xs11-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>How to Transfer Contacts from HTC U23 to iPhone XS/11 | Dr.fone</u></a></li>
<li><a href="https://blog-min.techidaily.com/in-2024-how-to-teleport-your-gps-location-on-motorola-edge-2023-drfone-by-drfone-virtual-android/"><u>In 2024, How To Teleport Your GPS Location On Motorola Edge 2023? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/revolutionize-your-yard-work-discover-how-this-remote-controlled-mower-turns-chores-into-fun-exclusive-review-by-zdnet/"><u>Revolutionize Your Yard Work: Discover How This Remote-Controlled Mower Turns Chores Into Fun – Exclusive Review by ZDNET</u></a></li>
<li><a href="https://some-tips.techidaily.com/revolutionizing-home-security-how-a-facial-recognition-smart-lock-triumphed-over-traditional-devices-according-to-my-test-zdnet/"><u>Revolutionizing Home Security: How a Facial Recognition Smart Lock Triumphed Over Traditional Devices, According to My Test | ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/ring-spotlight-cam-pro-surprising-quality-at-a-labor-day-discount-a-review-you-dont-want-to-miss-tech-insights/"><u>Ring Spotlight Cam Pro: Surprising Quality at a Labor Day Discount - A Review You Don't Want to Miss! | Tech Insights</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/say-laughs-say-free-mememakers-tutorial-for-2024/"><u>Say Laughs, Say Free - MemeMaker's Tutorial for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/score-big-savings-grab-the-blink-outdoor-set-with-four-cameras-and-a-mounting-light-for-just-80-over-labor-day-tech-news/"><u>Score Big Savings: Grab the Blink Outdoor Set with Four Cameras and a Mounting Light for Just $80 Over Labor Day | Tech News!</u></a></li>
<li><a href="https://some-tips.techidaily.com/secure-your-home-with-blinks-advanced-four-cam-floodlight-kit-at-an-unbeatable-price-of-80-exclusive-labor-day-offer/"><u>Secure Your Home with Blink's Advanced Four-Cam Floodlight Kit at an Unbeatable Price of $80 - Exclusive Labor Day Offer!</u></a></li>
<li><a href="https://some-tips.techidaily.com/see-whos-there-the-ultimate-guide-to-the-latest-video-doorbell-tech-for-2-google-ranked-by-zdnet/"><u>See Who's There: The Ultimate Guide to the Latest Video Doorbell Tech for 2# Google, Ranked by ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-5-action-cameras-expert-reviews-and-buyers-guide-zdnet/"><u>Top 5 Action Cameras : Expert Reviews and Buyer's Guide - ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-5-affordable-prefabricated-homes-under-50000-innovative-house-in-a-box-solutions-featured-by-zdnet/"><u>Top 5 Affordable Prefabricated Homes Under $50,000: Innovative 'House-in-a-Box' Solutions Featured by ZDNet</u></a></li>
<li><a href="https://win-howtos.techidaily.com/transformer-un-fichier-swf-en-format-avi-gratuitement-sur-la-toile-guide-par-movavi/"><u>Transformer Un Fichier SWF en Format AVI Gratuitement Sur La Toile - Guide Par Movavi</u></a></li>
<li><a href="https://facebook-video-share.techidaily.com/unleashing-laughter-on-screen-essential-tactics-for-youtube-reaction-video-making-3-ways-for-2024/"><u>Unleashing Laughter on Screen Essential Tactics for YouTube Reaction Video Making (3 Ways) for 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/LeKJBWb6Jhk?si=AnViizAPiIT1YCRA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

