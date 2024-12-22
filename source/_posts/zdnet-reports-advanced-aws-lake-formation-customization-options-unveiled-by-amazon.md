---
title: "ZDNet Reports: Advanced AWS Lake Formation Customization Options Unveiled by Amazon"
date: 2024-12-19T23:00:27.553Z
updated: 2024-12-21T22:39:28.481Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/7111378cc0205319da99cc8db3992a3d311982c554186166a280e12ee8590487.png
---

## ZDNet Reports: Advanced AWS Lake Formation Customization Options Unveiled by Amazon

Amazon Web Services on Tuesday announced the general availability of tools that bring more [fine-grained control to data lake management](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2Fblogs%2Faws%2Faws-lake-formation-general-availability-of-cell-level-security-and-governed-tables-with-automatic-compaction%2F%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7C8e02bbff-f513-49eb-a927-f1c9646b5927%7Cdtp&dtb=1). 

First, Row and Cell-Level Security for Lake Formation "puts the right data in the hands of the right people," AWS CEO Adam Selipsky said during his AWS re:Invent keynote address. 

Lake Formation already enables customers to move data into S3 data lakes, clean, and classify it using machine learning and secure access to sensitive data. The new tool now lets customers enforce access controls for individual rows and cells. Instead of creating multiple tables for each user and managing data pipelines, a customer can define a set of policies for specific rows for specific users. Customers control access to specific rows and columns in query results and within AWS Glue ETL jobs based on the identity of who is performing the action. 

Meanwhile, Transactions for Governed Tables in Lake Formation eliminates the need for batching updates. "Data isn't static," Selipsky said. "More and more data is being added and moved rapidly."

Now customers can create a new type of table -- a governed table -- and Lake Formation automatically manages conflicts and errors for consistent view of data. Users will be able to keep up with the data in real-time. 

Governed tables support ACID transactions that let multiple users concurrently and reliably insert and delete data across multiple governed tables. ACID transactions also let customers run queries that return consistent and up-to-date data. In case of errors in ETL processes, or during an update, changes are not committed and will not be visible.

Customers using governed tables can use automatic compaction for storage optimization. When this option is enabled, Lake Formation automatically compacts small S3 objects in governed tables into larger objects to optimize access via analytics engines, such as[Amazon Athena](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Faws.amazon.com%2Fathena%2F%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7C8e02bbff-f513-49eb-a927-f1c9646b5927%7Cdtp&dtb=1) and[Amazon Redshift Spectrum](https://buy.geni.us/Proxy.ashx?TSID=368250&GR%5FURL=https%3A%2F%2Fdocs.aws.amazon.com%2Fredshift%2Flatest%2Fdg%2Fc-getting-started-using-spectrum.html%3Ftag%3Dzd-buy-button-20%26ascsubtag%3D%5F%5FCOM%5FCLICK%5FID%5F%5F%7C8e02bbff-f513-49eb-a927-f1c9646b5927%7Cdtp&dtb=1). 

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
<li><a href="https://facebook-video-footage.techidaily.com/new-youtube-to-webm-the-finest-video-converters-unveiled/"><u>[New] YouTube-to-WebM The Finest Video Converters Unveiled</u></a></li>
<li><a href="https://facebook-video-files.techidaily.com/updated-in-2024-fbstream-viewer-extractor/"><u>[Updated] In 2024, FbStream Viewer Extractor</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-transform-your-smartphone-photography-with-iphones-hdr/"><u>[Updated] Transform Your Smartphone Photography with iPhone’s HDR</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-using-b-roll-to-enhance-cinematic-quality/"><u>[Updated] Using B-Roll to Enhance Cinematic Quality</u></a></li>
<li><a href="https://twitter-videos.techidaily.com/updated-viral-visionaries-top-meme-creators-on-social-media-for-2024/"><u>[Updated] Viral Visionaries Top Meme Creators on Social Media for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-optimizing-unused-scenes-a-filmmakers-approach/"><u>2024 Approved Optimizing Unused Scenes A Filmmaker's Approach</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-the-core-language-of-cutting-edge-vr-experiences/"><u>2024 Approved The Core Language of Cutting-Edge VR Experiences</u></a></li>
<li><a href="https://extra-resources.techidaily.com/capture-memories-best-apps-to-enhance-photos-for-2024/"><u>Capture Memories Best Apps to Enhance Photos for 2024</u></a></li>
<li><a href="https://vp-tips.techidaily.com/fix-your-powerdvd-dvd-issue-step-by-step-guide/"><u>Fix Your PowerDVD DVD Issue – Step-by-Step Guide</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-restore-wiped-videos-on-samsung-by-fonelab-android-recover-video/"><u>How to restore wiped videos on Samsung</u></a></li>
<li><a href="https://android-transfer.techidaily.com/in-2024-8-ways-to-transfer-photos-from-motorola-moto-e13-to-iphone-easily-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>In 2024, 8 Ways to Transfer Photos from Motorola Moto E13 to iPhone Easily | Dr.fone</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/in-2024-becoming-a-leader-in-the-world-of-design-work/"><u>In 2024, Becoming a Leader in the World of Design Work</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-tips-for-writing-irresistible-podcast-intros/"><u>In 2024, Tips for Writing Irresistible Podcast Intros</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-upgrading-your-mp4s-integrating-premium-srt-sound/"><u>In 2024, Upgrading Your MP4s Integrating Premium SRT Sound</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveiling-techniques-for-harmonious-crossfades-in-tracks-for-2024/"><u>Unveiling Techniques for Harmonious Crossfades in Tracks for 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/S3Th6oa_isA?si=TTQ013BB9beUM4x6" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

