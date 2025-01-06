---
title: "Overcoming Irritating Limitations: A Guide to Bypassing Notion-Evernote Import Issues"
date: 2024-12-31T21:01:23.418Z
updated: 2025-01-05T22:38:32.650Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/10f40441e17c1fa8de82fe459b0ca66adaa7f77ee4510f8621b2c17f71bab5a7.jpg
---

## Overcoming Irritating Limitations: A Guide to Bypassing Notion-Evernote Import Issues

![notion-vs-evernote-switch-from-evernote-2022-08-28-16-10-17](https://www.zdnet.com/a/img/resize/a9e2334a282e965c626847c7df606aebeab5f517/2022/08/28/ce915024-5d73-4038-9922-5e57c5216723/notion-vs-evernote-switch-from-evernote-2022-08-28-16-10-17.jpg?auto=webp&width=1280)

Notion

I started writing my blog posts for ZDNET in Evernote back in 2012\. With a few minor exceptions, every one of those posts was written, and had a first edit, in Evernote. 

I quite like [Evernote](https://evernote.com/) and pay for a professional plan. One of the key benefits of Evernote was (note the past tense) that I could sync between computers. I usually write my articles on my MacBook Air. Once the article is done, my wife (who has years of experience as a managing editor) does an editing pass with me from the couch, using a Mac mini that is connected to a big screen in our family room. I then submit the edited article to ZDNET's editors for review. 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/1rCjQ09iG7s?si=Si1fUBric8MH1VHI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

##  Sync failures 

But then Evernote's sync started to regularly fail. Sometimes it wouldn't sync at all. Sometimes, the edited version would be reported as a conflict, and Evernote would create two copies of the article. 

I reached out to [Evernote's support team](https://help.evernote.com/hc/en-us/requests/new), and was told to make sure I had the most recent version of the app (I did). I was also told not to edit the same note on two devices at once. My practice has always been to quit the app on one machine before editing on another. Support also instructed me to check to see if the note synced to the web (which had already become an obsessive practice). And then, I was told: 

> I cannot guarantee that this will solve the issues, but rest assured that we are aware of this feedback, and we are doing our best to improve the syncing process of the Evernote app. 

Not encouraging, that. Then, when Evernote decided to create three separate copies of an article, I realized it was time to find a different solution. 

This kind of thing gets old after awhile.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/RBN1gYY5hUs?si=p89CMiMzeJzU0wGu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

##  The need to import Evernote notes 

The key requirement, for whatever Evernote alternative I found, was that it had to be able to import Evernote notebooks. I have two key writing notebooks I use every day: Blogs Complete and Blogs-in-Progress. 

Blogs Complete contains all my posts once they've been published. It has 1,364 notes. It needs to be searchable, because I often reference it to see what I said in a previous post. 

Blogs-in-Progress is the mission-critical notebook. It not only has the current blog post I'm writing, but ideas and notes for upcoming posts and projects. I often mine this notebook for new post ideas if I don't have a topic for the day. And as I work on bigger projects, I keep track of the details of each project in its own note. I then turn those notes into articles when the projects are complete. Blogs-in-Progress has 406 notes. 

A whole bunch of programs import Evernote, including Apple Notes, [Obsidian](https://obsidian.md/), [Ulysses](https://ulysses.app/), [Notion](https://www.notion.so/), the open source [Joplin](https://joplinapp.org/) note app, and even [Microsoft's OneNote](https://www.microsoft.com/en-us/microsoft-365/onenote/digital-note-taking-app). Since I'm a heavy user of Notion, I decided it would make the most sense to bring my blogging notebooks into Notion. 

**Review:** [**Notion app: Why (and how) I rely on this powerful productivity tool**](https://www.zdnet.com/article/notion-app-review/)

This did not go smoothly. Part of it was Evernote's fault. Part of it was Notion's fault. 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/n-66V-LRK3Y?si=fNeB2pXCePeQli6E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

##  The Notion conundrum 

Evernote, as it turns out, has [a published and reliable export format called .enex](https://evernote.com/blog/how-evernotes-xml-export-format-works/). You can export a set of notes, or even a set of notebooks containing notes, and Evernote will create an XML file that other programs can import. 

So, does Notion use this published and reliable export format to import Evernote notes? Nope. Why make anything easy? 

Instead, Notion uses the Evernote API and becomes an application client to Evernote. This requires Evernote to authenticate in Notion, and grant your Notion instance permission to access Evernote data from the cloud. 

So I did this. I first tried importing the smaller notebook, but it only imported 350 of the 406 notes. I tried importing the larger notebook, but that just hung. I let the import dialog sit there overnight, but nothing happened. 

So, I contacted Notion. Apparently, they know there's an issue because I was told this: 

> I'm sorry to hear you're having trouble importing content from Evernote. This has been happening for a small number of users and it's on our to-do list to fix, but we don't currently have a timeline for when it will be resolved. 

The support agent suggested that imports sometimes fail with large Evernote notes (like notes with graphics on them). The agent also suggested splitting the notebooks into smaller batches and trying again. 

It's here we start going down the rabbit hole. It starts with the problem of splitting notebooks into smaller batches. There are three things you need to know about moving notes in Evernote: 

1. You can only select and drag multiple notes in the desktop application.
2. You can only move 50 notes at once.
3. Once you move notes from one notebook to another, you need to wait for that action to sync to the cloud in order to be able to import them into Notion.

But, as we've established, Evernote has sync reliability issues. So the idea of flinging thousands of mission-critical notes around and hoping they sync properly and don't break was a deal-breaker. But that's the only way Notion can get notes out of Evernote. 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/zWYVKFk3yPQ?si=Yu7xsjIYgRiq8zHk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

##  How I eventually solved the problem 

Let's recap. 

1. Evernote has a perfectly good export format that doesn't rely on syncing, but Notion won't use it.
2. Evernote has numerous sync reliability issues, which Evernote acknowledges.
3. To bring Evernote notes into Notion, we have to break up notebooks and rely on Evernote sync operations to work, and they often don't.

My solution was to leave my Blogs-in-Progress and Blogs Complete folders untouched in Evernote. Instead, from the desktop application, I exported both of those notebooks separately and saved them to two .enex files. 

Still in the Evernote desktop app, I then imported those two .enex files, creating a Blogs-in-Progress (Import) notebook and a Blogs Complete (Import) notebook. In this way, I bypassed the 50 note at a time move limit, and effectively cloned my notebooks in Evernote. My plan was to use these clones for chopping up and moving the notes around, leaving my originals untouched and preserving a backup in the .enex files. 

I waited for the two notebook clones to properly sync to the cloud. I kept checking the Evernote Web client. About three hours later, the sync completed. The new, fresh sync of the notebook clones succeeded with no loss of notes. 

Back in the Evernote desktop app, I created a series of seven notebooks, named Part 1 through Part 7\. My plan was to start with the Blogs Completed notebook, and put 200 notes in each of the seven Part notebooks. Very carefully, I moved four blocks of 50 notes from my cloned notebook into the first Part notebook. I waited for that sync to work by confirming the notes had arrived in the right notebook in the Evernote web app. This took about 15-20 minutes for each tranche. 

Once I verified all seven parts were properly in the cloud, I went back into Notion and imported each, one at a time. Most came into Notion with no issues, but a few failed. I checked Notion to find out which note the import failed on, then went back into the appropriate Evernote part notebook to see if there was a problematic note. 

On each of those occasions, there was a note with graphics in it, and it was that note that killed the import. Depending on how important the note was for my records or work, I either deleted the full failing note, or removed the graphics from the failing note. In any case, after dealing with the failing notes, I was able to complete the imports into Notion. 

I followed the same process with my Blogs-in-Progress notebook, but because there were fewer notes, it went faster. All told, it took about six hours of tweaking, fiddling, and waiting for syncs to complete to move the data from Evernote to Notion, but it did, eventually, work. 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/465CTOm8om0?si=63RxowNMCFA4fPUa" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

##  Some obvious conclusions 

First, a note for Evernote. When your service is a premium, paid-for service that specifically promotes the idea of having your information on any device you need it on, letting bugs remain in the sync implementation is mission failure. Telling customers, "We are aware of this feedback, and we are doing our best to improve the syncing process of the Evernote app" does not inspire confidence. Evernote, you need to make this work. 

I've been a paying Evernote user for about a decade, and have even written here on ZDNET about [how Evernote came to the rescue during a hurricane evacuation](https://www.zdnet.com/article/why-cloud-sync-not-backup-worked-better-for-business-continuity-during-the-hurricane/). But when a fundamental feature fails repeatedly, it's time to move on. I'm going to keep using Evernote as an archive for some older records, but I'm not going to rely upon it for day-to-day use. 

Now, a note for Notion. Folks, you're clearly aware of Evernote. In fact, you have [an entire page devoted to convincing folks to move from Evernote to Notion](https://www.notion.so/evernote). You must be aware of the sync problems Evernote users encounter, because you spotlight so many users who have moved between the services. So, what could have possibly possessed your engineering team to use a highly unreliable cloud sync option when there's a published and reliable export format? 

I keep finding new ways to put Notion to use, which goes a long way to substantiating how much of a help it is as a productivity and management tool. But Notion is making a big pitch to its competitor's users. It needs a better solution than the cloud import mechanism it is currently using, and a better answer when it fails than "We don't currently have a timeline for when it will be resolved." 

That having been said, this article was written in the new Blogs-in-Progress notebook in Notion, and edited on a different machine with no sync issues. So, yay! 

Do you use Notion or Evernote? Have you migrated away from Evernote to another application? Let us know in the comments below. 

---

_You can follow my day-to-day project updates on social media. Be sure to follow me on Twitter at [@DavidGewirtz](https://twitter.com/davidgewirtz), on Facebook at [Facebook.com/DavidGewirtz](https://www.facebook.com/davidgewirtz), on Instagram at [Instagram.com/DavidGewirtz](https://www.instagram.com/DavidGewirtz/), and on YouTube at [YouTube.com/DavidGewirtzTV](https://www.youtube.com/user/DavidGewirtzTV)._

#### **ZDNET** Recommends

[The best smartwatches you can buy: Apple, Samsung, Google, and more compared](https://www.zdnet.com/article/best-smartwatch/ "The best smartwatches you can buy: Apple, Samsung, Google, and more compared")

[The 5 best VPN services (and tips to choose the right one for you)](https://www.zdnet.com/article/best-vpn/ "The 5 best VPN services (and tips to choose the right one for you)")

[The best Android phones you can buy (including a surprise pick)](https://www.zdnet.com/article/best-android-phone/ "The best Android phones you can buy (including a surprise pick)")

[The best robot vacuum and mop combos (and if they're worth the money)](https://www.zdnet.com/article/best-robot-vacuum-mop/ "The best robot vacuum and mop combos (and if they're worth the money)")

* [The best smartwatches you can buy: Apple, Samsung, Google, and more compared](https://www.zdnet.com/article/best-smartwatch/ "The best smartwatches you can buy: Apple, Samsung, Google, and more compared")
* [The 5 best VPN services (and tips to choose the right one for you)](https://www.zdnet.com/article/best-vpn/ "The 5 best VPN services (and tips to choose the right one for you)")
* [The best Android phones you can buy (including a surprise pick)](https://www.zdnet.com/article/best-android-phone/ "The best Android phones you can buy (including a surprise pick)")
* [The best robot vacuum and mop combos (and if they're worth the money)](https://www.zdnet.com/article/best-robot-vacuum-mop/ "The best robot vacuum and mop combos (and if they're worth the money)")

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
<li><a href="https://win-solutions.techidaily.com/remnant-from-the-ashes-overcoming-game-crash-dilemma/"><u>'Remnant: From the Ashes - Overcoming Game Crash Dilemma</u></a></li>
<li><a href="https://fox-helps.techidaily.com/new-affordable-asmr-capturing-selecting-premium-gear-for-budget-conscious-users/"><u>[New] Affordable ASMR Capturing Selecting Premium Gear for Budget-Conscious Users</u></a></li>
<li><a href="https://facebook-video-recording.techidaily.com/new-quick-access-to-fb-vids-as-mp4-files-for-2024/"><u>[New] Quick Access to FB Vids as MP4 Files for 2024</u></a></li>
<li><a href="https://tiktok-clips.techidaily.com/updated-how-to-pinpoint-the-perfect-tag-for-your-personalized-tiktok-stream/"><u>[Updated] How to Pinpoint the Perfect Tag for Your Personalized TikTok Stream</u></a></li>
<li><a href="https://some-tips.techidaily.com/80-off-premium-smallcloud-storage-solutions-now-available-on-zdnet-shop/"><u>$80 Off: Premium SmallCloud Storage Solutions Now Available on ZDnet Shop</u></a></li>
<li><a href="https://extra-tips.techidaily.com/2024-approved-cartoonkingdom-comprehensive-24-guide/"><u>2024 Approved CartoonKingdom Comprehensive '24 Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/australian-authorities-advocate-for-rapid-deployment-of-essential-security-patches-in-businesses-zdnet/"><u>Australian Authorities Advocate for Rapid Deployment of Essential Security Patches in Businesses | ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/continued-access-guaranteed-office-2016-and-2019-seamless-connection-to-microsoft-365-in-the-coming-year/"><u>Continued Access Guaranteed: Office 2016 & 2019 Seamless Connection to Microsoft 365 in the Coming Year</u></a></li>
<li><a href="https://discover-brilliant.techidaily.com/heic-to-jpg-conversion-seamless-cross-platform-transformation-with-movavi-image-converter/"><u>HEIC to JPG Conversion: Seamless Cross-Platform Transformation with Movavi Image Converter</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/how-to-use-pokemon-go-joystick-on-oppo-f25-pro-5g-drfone-by-drfone-virtual-android/"><u>How to use Pokemon Go Joystick on Oppo F25 Pro 5G? | Dr.fone</u></a></li>
<li><a href="https://fox-friendly.techidaily.com/in-2024-building-an-intriguing-vlog-conversation-guide/"><u>In 2024, Building an Intriguing Vlog Conversation Guide</u></a></li>
<li><a href="https://fake-location.techidaily.com/ispoofer-is-not-working-on-samsung-galaxy-s24plus-fixed-drfone-by-drfone-virtual-android/"><u>iSpoofer is not working On Samsung Galaxy S24+? Fixed | Dr.fone</u></a></li>
<li><a href="https://some-tips.techidaily.com/microsoft-unveils-innovative-ai-co-pilots-boosting-customer-support-and-sales-efficiency-insights-from-zdnet/"><u>Microsoft Unveils Innovative AI Co-Pilots Boosting Customer Support & Sales Efficiency – Insights From ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/overcoming-azures-ongoing-resource-constraints-strategies-for-users/"><u>Overcoming Azure's Ongoing Resource Constraints: Strategies for Users</u></a></li>
<li><a href="https://some-tips.techidaily.com/prioritizing-cloud-safety-why-relying-solely-on-service-providers-isnt-enough/"><u>Prioritizing Cloud Safety: Why Relying Solely on Service Providers Isn't Enough</u></a></li>
<li><a href="https://some-tips.techidaily.com/the-linux-foundation-advocates-for-cutting-edge-exascale-performance-a-deep-dive-into-future-computing/"><u>The Linux Foundation Advocates for Cutting-Edge Exascale Performance: A Deep Dive Into Future Computing</u></a></li>
<li><a href="https://some-tips.techidaily.com/1726808538468-top-rated-cloud-migration-services-of-2022-insights-from-zdnet/"><u>Top Rated Cloud Migration Services of 2022 - Insights From ZDNet</u></a></li>
</ul></div>

