---
title: "Simplifying the Shift of Helping Hands Records: Expert Techniques and Insights"
date: 2024-09-17 10:23:41
updated: 2024-09-20 11:24:17
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/380c0bd99725d564144c554e3495dbd9ae260fd185cc36120b3c443e5fa292b5.JPEG
---

## Simplifying the Shift of Helping Hands Records: Expert Techniques and Insights

![help-desk-migration.jpg](https://www.zdnet.com/a/img/resize/538c24693b3c1b7a84eaa04517a814ed200c0c42/2021/09/07/8522bcfc-f094-4d94-9fbe-3aa9c916d7d2/help-desk-migration.jpg?auto=webp&width=1280)

By Rawpixel.com -- Shutterstock

It's a tough decision. On the one hand, you've got a ton of mission-critical data deeply entwined with an existing software solution that manages it all. On the other hand, that software solution is failing, and it looks like it's only going to get worse. Do you migrate (with all the pitfalls that might entail), or do you just ride it down until your solution inevitably crashes and burns? 

I was recently faced with that decision over my help desk software. I had about five years of customer cases tied up inside a product called [Awesome Support](https://wordpress.org/plugins/awesome-support/). This WordPress plugin provides help desk capability right inside the WordPress dashboard. Awesome Support was originally awesome and was still awesome when it worked, but it was starting to fail. Getting support for problems with Awesome Support was anything but awesome. It was nonexistent. 

### **ZDNET** Recommends

[The best web hosting services We take a look at some of the best web hosting providers and help you understand how to choose the best for your needs.  Read now](https://www.zdnet.com/article/best-web-hosting/)

I did some digging and found that it had [changed owners via auction](https://flippa.com/6410433-the-best-support-plugin-for-wordpress-earning-over-15k-net-in-the-ttm). There's a lead developer listed on the site's about page, but when you visit [the lead developer's personal home page](https://julienliabeuf.com/about), it says he sold the plugin way back in 2016\. And finally, the person who bought Awesome Support lists himself on [the about page](https://getawesomesupport.com/team/) as a "Reluctant Business Manager". 

It looked like Awesome Support was skating along without any serious developer attention for all intents and purposes. That was reasonably evident by the complete lack of response to tickets I submitted about the freemium add-ons I had purchased and couldn't get to work. 

The thing was, I had more than 600 customers I was supporting with well over a thousand support tickets. I relied on the help desk software on a daily basis. As a solo developer (and that's not even my main day job), I don't have the luxury of spending all day digging through emails to understand the history of a given customer problem. The help desk software consolidates everything about a customer issue in one place, allowing me to do support in an hour or so a day. 

Without good help desk software, I just wouldn't be able to keep up. 

It was a relatively obvious decision: I needed to move my support environment. A lot of other WordPress developers use [Help Scout](https://helpscout.com). There are [extensions available](https://wphelpscout.com/) that integrate it into WordPress. So Help Scout was a viable substitute solution for Awesome Support. 

The gotcha was there was no clear way to move all my data from Awesome Support to Help Scout. Help Scout does not offer an Awesome Support import feature. 

It's not just a simple import of customer accounts. There was often more than one ticket per customer, more than one entry per ticket, and very often screenshots associated with those entries. To be able to support my users, I needed to have access to all that data, organized by user and ticket. 

I toyed with the idea of just starting over with a new support system. I could declare [Help Desk Zero](https://blog.doist.com/inbox-zero/) and move on. But the history of interactions with my users was invaluable. Not only did those tickets tell me about each customer's situation, but they also contained symptoms and solutions I often mined when trying to track down solutions to bugs. 

It was data I did not want to lose. And, as it turns out, I didn't have to. 

It was a rainy, cold overcast January afternoon when I decided to don my cloak of Google-fu and set out on a quest to find a migration solution. I charged my brain with a hot cup of the methylxanthine class central nervous system stimulant known as caffeine, combined with a bit of milk and sweetener. I flexed my fingers, cracked my knuckles, made sure my [Logitech MX Master 3 mouse and MX Keys keyboard](https://www.zdnet.com/article/logitech-easy-switch-switching-mice-and-keyboards-between-computers-is-so-un-kvm/) were fully charged and launched my search strings. 

After roughly a thousand seconds of searching, I had what seemed like a possible answer to my quest: the service at [help-desk-migration.com](https://help-desk-migration.com/). This came as a bit of a surprise because I had ventured out hopeful but with low expectations. After all, Awesome Support is just a languishing WordPress support plugin, not a mainstream help desk service. And yet, help-desk-migration.com claimed to be able to migrate it. 

Spoiler alert: they did. Fabulously. 

As you can see from the image below, the company offers a wide range of source and destination services to convert between. 

##  The migration process 

You start by choosing your source platform and providing any necessary credentials or API keys so help-desk-migration.com can read in the data. 

Next, you choose the index you're going to use to match records. In my case, the email address of my users was the key identifier. You can also specify other mappings. In my case, the maps didn't work perfectly, but I'll talk more about that in a minute. 

Then you tell the program what you want to move across. I wasn't concerned about agents (I'm the only one), but I did need to move all Awesome Support users to Help Scout customers and all Awesome Support tickets to Help Scout conversations.

Then you do a test import. This helps determine how many records you have and what your fee will be. In my case, the test import failed. 

**Also:** [**Ukrainian software developers share their stories and photos from the war zone**](https://www.zdnet.com/article/ukrainian-software-developers-share-their-stories-and-photos-from-the-war-zone/)

This began my conversation with the folks at [Relokia](https://relokia.com/), the Ukrainian company behind help-desk-migration.com. As it turned out, I got awesome support from them. A quick email to them resulted in the answer that I had a corrupted contact I needed to remove before attempting the migration test. 

**Also:** [**How you can help Ukraine: Donation sites and resources**](https://www.zdnet.com/article/how-you-can-help-ukraine-donation-sites-and-resources/)

The next time, the migration test worked, but Help Scout wasn't properly representing the names of my users. 

I knew the data was there because it was showing in my Awesome Support dashboard. 

It's at this point that Relokia went in and actually modified their migration code for me. I deleted the destination records from Help Scout and did another test. This time, the business logic was a bit off for first and last names. 

Here's what it looked like:

Basically, if there was either a first or a last name, but not both, dumping "Last Name" in the field was troublesome. After some back-and-forth email about what their system could handle and what would work for me, we settled on putting a dash in place if there was no last name in the user record. 

We ran into one more snag where there was a record in my source database that was somehow a problem. The Relokia folks helped me find and clear that record, at which point I was able to fully complete the migration. 

##  The rest of the story 

All told, the migration process took four days. Most of that was because of the 27 emails we sent back and forth working through the issues involved. 

As the image above shows, a total of 1943 records were moved. That consisted of 655 user records and 1288 ticket threads. 

In addition to all the conversations back and forth, Relokia went in and hand-modified my import and did some custom programming to tweak their interface for Awesome Support, which was far from one of their most common migration platforms. 

So, instead of losing all my support records or somehow trying to spend weeks hand copying and pasting all the ticket data between services, I used Relokia's help-desk-migration.com and got the job done in four days, where most of the work on my end consisted of me replying to email messages. 

And just how much did all this customized help and support cost me? A grand total of $153\. It was a bargain, it worked, and support was exceptional. 

So, yeah. Migrating your help desk data is definitely not as impossible as it seems. Just use this service. 

Are you considering a migration project? Have you migrated other data recently? Do you have any recommendations or war stories you want to share? Let us know in the comments below. 

---

_You can follow my day-to-day project updates on social media. Be sure to follow me on Twitter at [@DavidGewirtz](https://twitter.com/davidgewirtz), on Facebook at [Facebook.com/DavidGewirtz](https://www.facebook.com/davidgewirtz), on Instagram at [Instagram.com/DavidGewirtz](https://www.instagram.com/DavidGewirtz/), and on YouTube at [YouTube.com/DavidGewirtzTV](https://www.youtube.com/user/DavidGewirtzTV)._

#### Cloud

[​What is digital transformation? Everything you need to know](https://www.zdnet.com/article/what-is-digital-transformation-everything-you-need-to-know-about-how-technology-is-reshaping/ "​What is digital transformation? Everything you need to know")

[The best cloud providers compared: AWS, Azure, Google Cloud, and more](https://www.zdnet.com/article/the-top-cloud-providers-of-2021-aws-microsoft-azure-google-cloud-hybrid-saas/ "The best cloud providers compared: AWS, Azure, Google Cloud, and more")

[The top 6 cheap web hosting services: Find an affordable option](https://www.zdnet.com/article/best-cheap-web-hosting/ "The top 6 cheap web hosting services: Find an affordable option")

[What is cloud computing? Here's everything you need to know](https://www.zdnet.com/article/what-is-cloud-computing-everything-you-need-to-know-about-the-cloud/ "What is cloud computing? Here's everything you need to know")

* [​What is digital transformation? Everything you need to know](https://www.zdnet.com/article/what-is-digital-transformation-everything-you-need-to-know-about-how-technology-is-reshaping/ "​What is digital transformation? Everything you need to know")
* [The best cloud providers compared: AWS, Azure, Google Cloud, and more](https://www.zdnet.com/article/the-top-cloud-providers-of-2021-aws-microsoft-azure-google-cloud-hybrid-saas/ "The best cloud providers compared: AWS, Azure, Google Cloud, and more")
* [The top 6 cheap web hosting services: Find an affordable option](https://www.zdnet.com/article/best-cheap-web-hosting/ "The top 6 cheap web hosting services: Find an affordable option")
* [What is cloud computing? Here's everything you need to know](https://www.zdnet.com/article/what-is-cloud-computing-everything-you-need-to-know-about-the-cloud/ "What is cloud computing? Here's everything you need to know")

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
