---
title: Discover Advanced AWS Lake Formation Capabilities Unveiled by Amazon for Greater Data Oversight - Tech News on ZDNet
date: 2024-12-06T19:31:37.713Z
updated: 2024-12-12T19:24:30.000Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/fa262754a0a509cce346c46f20d6465b8567441f/2021/06/28/20a585a6-81ff-4046-bba5-b4f43a73ca87/aws-bugfest-competition-to-find-and-fix-amazon-bugs.jpg?width=278&height=156&fit=crop&auto=webp
---

## Discover Advanced AWS Lake Formation Capabilities Unveiled by Amazon for Greater Data Oversight - Tech News on ZDNet

Amazon Web Services on Tuesday announced the general availability of tools that bring more [fine-grained control to data lake management](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2Fblogs%2Faws%2Faws-lake-formation-general-availability-of-cell-level-security-and-governed-tables-with-automatic-compaction%2F%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7C028808e3-bbdd-46e7-960e-d96823e68d25%7Cdtp&dtb=1). 

First, Row and Cell-Level Security for Lake Formation "puts the right data in the hands of the right people," AWS CEO Adam Selipsky said during his AWS re:Invent keynote address. 

Lake Formation already enables customers to move data into S3 data lakes, clean, and classify it using machine learning and secure access to sensitive data. The new tool now lets customers enforce access controls for individual rows and cells. Instead of creating multiple tables for each user and managing data pipelines, a customer can define a set of policies for specific rows for specific users. Customers control access to specific rows and columns in query results and within AWS Glue ETL jobs based on the identity of who is performing the action. 

Meanwhile, Transactions for Governed Tables in Lake Formation eliminates the need for batching updates. "Data isn't static," Selipsky said. "More and more data is being added and moved rapidly."

Now customers can create a new type of table -- a governed table -- and Lake Formation automatically manages conflicts and errors for consistent view of data. Users will be able to keep up with the data in real-time. 

Governed tables support ACID transactions that let multiple users concurrently and reliably insert and delete data across multiple governed tables. ACID transactions also let customers run queries that return consistent and up-to-date data. In case of errors in ETL processes, or during an update, changes are not committed and will not be visible.

Customers using governed tables can use automatic compaction for storage optimization. When this option is enabled, Lake Formation automatically compacts small S3 objects in governed tables into larger objects to optimize access via analytics engines, such as[Amazon Athena](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2Fathena%2F%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7C028808e3-bbdd-46e7-960e-d96823e68d25%7Cdtp&dtb=1) and[Amazon Redshift Spectrum](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Fdocs.aws.amazon.com%2Fredshift%2Flatest%2Fdg%2Fc-getting-started-using-spectrum.html%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7C028808e3-bbdd-46e7-960e-d96823e68d25%7Cdtp&dtb=1). 

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
<li><a href="https://instagram-video-recordings.techidaily.com/new-cut-and-paste-success-enhancing-videos-for-instagram-shares-for-2024/"><u>[New] Cut & Paste Success Enhancing Videos for Instagram Shares for 2024</u></a></li>
<li><a href="https://fox-hovers.techidaily.com/new-in-2024-piecing-a-puzzle-of-cinematic-highlights/"><u>[New] In 2024, Piecing a Puzzle of Cinematic Highlights</u></a></li>
<li><a href="https://extra-skills.techidaily.com/updated-mastering-soft-melodies-pcos-guide/"><u>[Updated] Mastering Soft Melodies PC/OS Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-strategies-for-effective-b-roll-application/"><u>[Updated] Strategies for Effective B-Roll Application</u></a></li>
<li><a href="https://some-skills.techidaily.com/updated-the-animators-toolkit-windows-movie-maker-for-winning-projects/"><u>[Updated] The Animator's Toolkit Windows Movie Maker for Winning Projects</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-quest-for-visual-excellence-can-pickup-be-the-top-photo-editor-on-android/"><u>[Updated] The Quest for Visual Excellence – Can PickUp Be the Top Photo Editor on Android?</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-photographers-companion-to-master-color-correction-top-11/"><u>2024 Approved The Photographer's Companion to Master Color Correction (Top 11)</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/catch-the-limited-offer-amazons-top-notch-fire-tv-omni-qled-series-discounted-by-150-tech-savings-now/"><u>Catch the Limited Offer: Amazon's Top-Notch Fire TV Omni QLED Series Discounted by $150 | Tech Savings Now</u></a></li>
<li><a href="https://howto.techidaily.com/fix-unfortunately-settings-has-stopped-on-realme-11-5g-quickly-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Fix Unfortunately Settings Has Stopped on Realme 11 5G Quickly | Dr.fone</u></a></li>
<li><a href="https://fox-helps.techidaily.com/in-2024-finding-affordable-no-cost-artistic-elements/"><u>In 2024, Finding Affordable, No-Cost Artistic Elements</u></a></li>
<li><a href="https://ai-driven-video-production.techidaily.com/in-2024-say-goodbye-to-tiktok-watermarks-best-online-remover-tools/"><u>In 2024, Say Goodbye to TikTok Watermarks Best Online Remover Tools</u></a></li>
<li><a href="https://instagram-video-recordings.techidaily.com/in-2024-video-mastery-tips-add-3-captivating-captions-on-instagram/"><u>In 2024, Video Mastery Tips Add 3 Captivating Captions on Instagram</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-complete-list-of-11-advanced-color-correction-and-grading-tutorials-for-2024/"><u>The Complete List of 11 Advanced Color Correction & Grading Tutorials for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-oceans-archive-best-practices-in-capturing-professional-underwater-footage-for-2024/"><u>The Ocean’s Archive Best Practices in Capturing Professional Underwater Footage for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-transformative-power-of-augmented-vision-for-2024/"><u>The Transformative Power of Augmented Vision for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/unleashing-the-power-of-cross-platform-video-playback-software-for-2024/"><u>Unleashing the Power of Cross-Platform Video Playback Software for 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/2NU63YqpVqw?si=uoJs0-nZYAkILqXx" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

