---
title: Advanced AWS Lake Formation Customization Now Available via Amazon Services
date: 2024-12-09T18:15:30.796Z
updated: 2024-12-12T18:19:07.022Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/fa262754a0a509cce346c46f20d6465b8567441f/2021/06/28/20a585a6-81ff-4046-bba5-b4f43a73ca87/aws-bugfest-competition-to-find-and-fix-amazon-bugs.jpg?width=278&height=156&fit=crop&auto=webp
---

## Advanced AWS Lake Formation Customization Now Available via Amazon Services

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
<li><a href="https://fox-http.techidaily.com/new-in-2024-cutting-edge-creations-yearly-free-text-files/"><u>[New] In 2024, Cutting-Edge Creations Yearly, Free Text Files</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/new-snappy-solution-seconds-for-ssgnature-bg-purge/"><u>[New] Snappy Solution Seconds for Ssgnature BG Purge</u></a></li>
<li><a href="https://win-superb.techidaily.com/1-quickly-restore-your-system-files-on-a-hard-drive-with-windows-11-10-8-or-7-a-step-by-step-guide/"><u>1. Quickly Restore Your System Files on a Hard Drive with Windows 11, 10, 8, or 7: A Step-by-Step Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/abbyy-elevates-global-finance-management-for-renault-argentina/"><u>ABBYY Elevates Global Finance Management for Renault Argentina</u></a></li>
<li><a href="https://extra-resources.techidaily.com/behind-the-scenes-a-comprehensive-review-of-lgs-digital-cinema-31mu97-b-monitor/"><u>Behind the Scenes A Comprehensive Review of LG's Digital Cinema 31MU97-B Monitor</u></a></li>
<li><a href="https://change-location.techidaily.com/how-to-come-up-with-the-best-pokemon-team-on-samsung-galaxy-m14-4g-drfone-by-drfone-virtual-android/"><u>How to Come up With the Best Pokemon Team On Samsung Galaxy M14 4G? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/leverage-cookiebot-technology-for-superior-user-analytics-and-seo-performance/"><u>Leverage Cookiebot Technology for Superior User Analytics and SEO Performance</u></a></li>
<li><a href="https://buynow-info.techidaily.com/navigating-through-connectivity-on-wheels-an-in-depth-review-of-suminds-adaptable-bluetooth-fm-transmitter-bt70b/"><u>Navigating Through Connectivity on Wheels: An In-Depth Review of Sumind's Adaptable Bluetooth FM Transmitter (BT70B)</u></a></li>
<li><a href="https://some-tips.techidaily.com/optimize-your-online-marketing-with-cookiebots-advanced-ad-management-technology/"><u>Optimize Your Online Marketing with Cookiebot's Advanced Ad Management Technology</u></a></li>
<li><a href="https://some-tips.techidaily.com/optimized-with-cookiebot-technology-enhance-your-sites-personalization/"><u>Optimized with Cookiebot Technology: Enhance Your Site's Personalization</u></a></li>
<li><a href="https://some-tips.techidaily.com/revolutionarer-ansatz-des-abbyy-sdks-zur-verbesserung-der-mobilgerate-onboarding-erfahrungen/"><u>Revolutionärer Ansatz Des ABBYY-SDKs Zur Verbesserung Der Mobilgeräte-Onboarding-Erfahrungen</u></a></li>
<li><a href="https://some-tips.techidaily.com/selecting-abbyy-vantage-the-reason-behind-sidetrades-choice-for-enhanced-payment-solutions/"><u>Selecting ABBYY Vantage: The Reason Behind Sidetrade's Choice for Enhanced Payment Solutions</u></a></li>
<li><a href="https://facebook.techidaily.com/social-media-identity-update-made-simple/"><u>Social Media Identity Update Made Simple</u></a></li>
<li><a href="https://win11-tips.techidaily.com/steps-to-find-windows-11s-authorize-center/"><u>Steps to Find Windows 11'S Authorize Center</u></a></li>
<li><a href="https://ios-location-track.techidaily.com/top-6-appsservices-to-trace-any-apple-iphone-7-plus-location-by-mobile-number-drfone-by-drfone-virtual-ios/"><u>Top 6 Apps/Services to Trace Any Apple iPhone 7 Plus Location By Mobile Number | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveiling-the-influence-of-ai-on-economic-progress-insights-from-abbyy-experts/"><u>Unveiling the Influence of AI on Economic Progress: Insights From ABBYY Experts</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/3koT_-kvbks?si=sQV7FzPiz6GYITrE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

