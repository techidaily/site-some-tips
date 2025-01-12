---
title: Navigating the New Wave of Precision with AWS Lake Formation Updates by Amazon | Tech Insights on Data Lakes
date: 2025-01-09T17:05:10.907Z
updated: 2025-01-12T18:07:55.764Z
tags:
  - amazon
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/fa262754a0a509cce346c46f20d6465b8567441f/2021/06/28/20a585a6-81ff-4046-bba5-b4f43a73ca87/aws-bugfest-competition-to-find-and-fix-amazon-bugs.jpg?width=278&height=156&fit=crop&auto=webp
---

## Navigating the New Wave of Precision with AWS Lake Formation Updates by Amazon | Tech Insights on Data Lakes

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
<li><a href="https://facebook-videos.techidaily.com/new-discover-unlimited-stories-free-extensions-and-mobile-marvels/"><u>[New] Discover Unlimited Stories – FREE Extensions & Mobile Marvels</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/20-complimentary-luts-available-for-dji-miniair-2-users/"><u>20 Complimentary LUTs Available for DJI Mini/Air 2 Users</u></a></li>
<li><a href="https://tech-revival.techidaily.com/ais-influence-on-software-development-changing-the-coding-landscape/"><u>AI's Influence on Software Development: Changing the Coding Landscape</u></a></li>
<li><a href="https://some-tips.techidaily.com/boost-your-efficiency-expert-techniques-and-apps-i-use-for-streamlining-everyday-task-management-insights-from-zdnet/"><u>Boost Your Efficiency: Expert Techniques & Apps I Use for Streamlining Everyday Task Management - Insights From ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/comprehensive-guide-for-securing-your-iphone-content-via-icloudmac-backup-techniques-zdnet/"><u>Comprehensive Guide for Securing Your iPhone Content via iCloud/Mac Backup Techniques | ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/discover-how-the-latest-iphone-12-models-embrace-improved-qi-standards-for-effortless-charge-no-magsafe-required-cnet/"><u>Discover How the Latest iPhone 12 Models Embrace Improved Qi Standards for Effortless Charge - No MagSafe Required! | CNET</u></a></li>
<li><a href="https://tech-haven.techidaily.com/essays-in-the-digital-age-is-ai-overruling-student-effort/"><u>Essays in the Digital Age: Is AI Overruling Student Effort?</u></a></li>
<li><a href="https://some-tips.techidaily.com/experts-choice-for-ultimate-apple-watches-of-2c34-detailed-reviews-and-ratings-zdnet/"><u>Experts' Choice for Ultimate Apple Watches of 2C34: Detailed Reviews and Ratings | ZDNET</u></a></li>
<li><a href="https://fox-access.techidaily.com/gopro-hero-series-clash-with-polaroid-cube-which-wins-for-2024/"><u>GoPro Hero Series Clash with Polaroid Cube Which Wins for 2024</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-erase-private-data-from-iphone-14-pro-max-drfone-by-drfone-ios-full-data-eraser-ios-full-data-eraser/"><u>How To Erase Private Data From iPhone 14 Pro Max | Dr.fone</u></a></li>
<li><a href="https://youtube-clips.techidaily.com/in-2024-achieving-high-clickthrough-rates-with-yt-thumbnails/"><u>In 2024, Achieving High Clickthrough Rates with YT Thumbnails</u></a></li>
<li><a href="https://some-tips.techidaily.com/mastering-the-customization-of-your-iphones-control-center-on-ios-18/"><u>Mastering the Customization of Your iPhone's Control Center on iOS 18</u></a></li>
<li><a href="https://extra-support.techidaily.com/navigating-youtubes-photo-publishing-for-2024/"><u>Navigating YouTube's Photo Publishing for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-apple-security-alert-how-the-latest-espionage-malware-threatens-iphones-are-your-devices-safe/"><u>New Apple Security Alert: How the Latest Espionage Malware Threatens iPhones - Are Your Devices Safe?</u></a></li>
<li><a href="https://some-tips.techidaily.com/thousands-access-apples-latest-ai-education-program-exclusive-opportunity-for-students-and-alumni-zdnet/"><u>Thousands Access Apple's Latest AI Education Program: Exclusive Opportunity for Students & Alumni - ZDNet</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/win-and-mac-users-elevate-your-workflow-with-our-top-8-tools-to-convert-sub-into-srtr/"><u>Win and Mac Users, Elevate Your Workflow with Our Top 8 Tools to Convert SUB Into SRTR</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/ZblaBc-v2vs?si=CKW1gJwXQT2vZJYo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

