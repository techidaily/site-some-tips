---
title: Enhanced Management Features in AWS Lake Formation Now Available on Amazon - Insights From ZDNet
date: 2024-12-16T04:55:02.273Z
updated: 2024-12-20T21:35:56.802Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/fa262754a0a509cce346c46f20d6465b8567441f/2021/06/28/20a585a6-81ff-4046-bba5-b4f43a73ca87/aws-bugfest-competition-to-find-and-fix-amazon-bugs.jpg?width=278&height=156&fit=crop&auto=webp
---

## Enhanced Management Features in AWS Lake Formation Now Available on Amazon - Insights From ZDNet

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
<li><a href="https://some-knowledge.techidaily.com/new-influencing-minds-with-music-selection-for-movie-previews/"><u>[New] Influencing Minds with Music Selection for Movie Previews</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-image-editors-ultimate-toolkit-review/"><u>[New] The Image Editor's Ultimate Toolkit Review</u></a></li>
<li><a href="https://video-capture.techidaily.com/updated-in-2024-high-quality-video-calling-solutions-top-10-best-apps-ranked/"><u>[Updated] In 2024, High-Quality Video Calling Solutions Top 10 Best Apps Ranked</u></a></li>
<li><a href="https://instagram-clips.techidaily.com/updated-perfecting-instagrams-audio-emoji-placement-for-2024/"><u>[Updated] Perfecting Instagram's Audio Emoji Placement for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-the-significance-of-video-in-client-promotional-power/"><u>[Updated] The Significance of Video in Client Promotional Power</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-ultimate-guide-top-20-cost-free-video-editing-websites/"><u>2024 Approved Ultimate Guide Top 20 Cost-Free Video Editing Websites</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-the-beginners-guide-to-converting-spoken-words-to-written-form-ms-word/"><u>In 2024, The Beginner’s Guide to Converting Spoken Words to Written Form (MS Word)</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/process-of-screen-sharing-infinix-note-30-vip-racing-edition-to-pc-detailed-steps-drfone-by-drfone-android/"><u>Process of Screen Sharing Infinix Note 30 VIP Racing Edition to PC- Detailed Steps | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/quick-methods-syncing-ios-images-and-movies-to-windows-for-2024/"><u>Quick Methods Syncing iOS Images & Movies to Windows for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-riders-eye-view-unveiling-23s-finest-action-camera-hats-for-bike-enthusiasts-for-2024/"><u>The Rider's Eye View – Unveiling '23’S Finest Action Camera Hats for Bike Enthusiasts for 2024</u></a></li>
<li><a href="https://techidaily.com/three-solutions-to-hard-reset-sony-xperia-5-v-drfone-by-drfone-reset-android-reset-android/"><u>Three Solutions to Hard Reset Sony Xperia 5 V? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/timeless-thread-triumphs-reddits-all-time-fave-list-top-10-for-2024/"><u>Timeless Thread Triumphs Reddit’s All-Time Fave List (Top 10) for 2024</u></a></li>
<li><a href="https://win-trending.techidaily.com/top-applications-to-remove-for-enhanced-computer-speed-expert-tips-from-yl-computing/"><u>Top Applications to Remove for Enhanced Computer Speed: Expert Tips From YL Computing</u></a></li>
<li><a href="https://tech-hub.techidaily.com/understanding-the-turing-test-and-its-beatability/"><u>Understanding The Turing Test & Its Beatability</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveiling-14-dynamic-text-animation-samples-for-2024/"><u>Unveiling 14 Dynamic Text Animation Samples for 2024</u></a></li>
<li><a href="https://extra-information.techidaily.com/your-quick-guide-to-excellent-zoom-meetings/"><u>Your Quick Guide to Excellent Zoom Meetings</u></a></li>
<li><a href="https://howto.techidaily.com/zte-blade-a73-5g-camera-not-working-unexpected-error-fix-it-now-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>ZTE Blade A73 5G Camera Not Working Unexpected Error? Fix It Now | Dr.fone</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/c17xsnbinCQ?si=xHKslFgC3QbxY4qW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

