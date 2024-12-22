---
title: Enhanced Management with New Features in Amazon's AWS Lake Formation - ZDNet Insights
date: 2024-12-15T23:45:43.101Z
updated: 2024-12-20T22:25:13.748Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/fa262754a0a509cce346c46f20d6465b8567441f/2021/06/28/20a585a6-81ff-4046-bba5-b4f43a73ca87/aws-bugfest-competition-to-find-and-fix-amazon-bugs.jpg?width=278&height=156&fit=crop&auto=webp
---

## Enhanced Management with New Features in Amazon's AWS Lake Formation - ZDNet Insights

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
<li><a href="https://twitter-videos.techidaily.com/new-2024-approved-screen-spectaculum-hitting-720p-with-twitter-vids/"><u>[New] 2024 Approved Screen Spectaculum Hitting 720P with Twitter Vids</u></a></li>
<li><a href="https://twitter-videos.techidaily.com/new-2024-approved-twitmedia-mastery-elevate-your-tweet-game/"><u>[New] 2024 Approved TwitMedia Mastery Elevate Your Tweet Game</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-top-30-windows-10-utilities-you-cant-ignore/"><u>[New] Top 30 Windows 10 Utilities You Can't Ignore</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-unveiling-studio-magic-comprehensive-xreview/"><u>[New] Unveiling Studio Magic Comprehensive XReview</u></a></li>
<li><a href="https://instagram-video-files.techidaily.com/updated-harness-the-power-of-instagram-best-free-video-converter-apps-for-windowsmacos/"><u>[Updated] Harness the Power of Instagram Best Free Video Converter Apps for Windows/macOS</u></a></li>
<li><a href="https://fox-glue.techidaily.com/updated-in-2024-unlock-visual-brilliance-top-11-videos-on-color-techniques/"><u>[Updated] In 2024, Unlock Visual Brilliance Top 11 Videos on Color Techniques</u></a></li>
<li><a href="https://on-screen-recording.techidaily.com/updated-strategies-for-efficient-business-teleconferencing-for-2024/"><u>[Updated] Strategies for Efficient Business Teleconferencing for 2024</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-revolutionary-storage-solutions-select-from-the-best-20-free-options-1tbplus/"><u>2024 Approved Revolutionary Storage Solutions - Select From the Best 20 Free Options (1TB+)</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-subject-emphasis-background-cleanse/"><u>2024 Approved Subject Emphasis Background Cleanse</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unlocking-your-sound-potential-a-modern-look-at-pazeras-techniques/"><u>2024 Approved Unlocking Your Sound Potential A Modern Look at Pazera's Techniques</u></a></li>
<li><a href="https://some-tips.techidaily.com/2024-approved-unveiling-the-secrets-to-professional-sound-capture-in-audacity/"><u>2024 Approved Unveiling the Secrets to Professional Sound Capture in Audacity</u></a></li>
<li><a href="https://ios-location-track.techidaily.com/9-best-phone-monitoring-apps-for-apple-iphone-x-drfone-by-drfone-virtual-ios/"><u>9 Best Phone Monitoring Apps for Apple iPhone X | Dr.fone</u></a></li>
<li><a href="https://blog-min.techidaily.com/in-2024-how-to-teleport-your-gps-location-on-samsung-galaxy-f15-5g-drfone-by-drfone-virtual-android/"><u>In 2024, How To Teleport Your GPS Location On Samsung Galaxy F15 5G? | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-unveiling-the-power-of-free-countdown-tools-for-time-management/"><u>In 2024, Unveiling the Power of Free Countdown Tools for Time Management</u></a></li>
<li><a href="https://smart-video-editing.techidaily.com/new-movie-magic-at-your-fingertips-effortless-video-enhancement/"><u>New Movie Magic at Your Fingertips Effortless Video Enhancement</u></a></li>
<li><a href="https://vp-tips.techidaily.com/quick-fix-techniques-for-speeding-up-videos-discover-5-easy-methods/"><u>Quick-Fix Techniques for Speeding up Videos: Discover 5 Easy Methods</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-finest-10-online-spots-to-download-pristine-photos-for-2024/"><u>The Finest 10 Online Spots to Download Pristine Photos for 2024</u></a></li>
<li><a href="https://tiktok-videos.techidaily.com/the-viral-trend-you-need-to-try-here-it-is/"><u>The Viral Trend You Need to Try - Here It Is</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-5-zero-price-screen-capture-software-for-windows-10-users-for-2024/"><u>Top 5 Zero Price Screen Capture Software for Windows 10 Users for 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/f3PFn06LijE?si=zHrmlTOzrKxXe-k4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

