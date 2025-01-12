---
title: "Bypassing the Hurdles of Notion’s Evernote Integration: Innovative Solutions for a Seamless Workflow | ZDNet Insights"
date: 2025-01-07T17:09:14.823Z
updated: 2025-01-12T18:01:56.080Z
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/50ec9f96a3862eafb44f6037d6d07d4292a04cc1b5866ca0d81d1cb562971c20.jpg
---

## Bypassing the Hurdles of Notion’s Evernote Integration: Innovative Solutions for a Seamless Workflow | ZDNet Insights

![notion-vs-evernote-switch-from-evernote-2022-08-28-16-10-17](https://www.zdnet.com/a/img/resize/a9e2334a282e965c626847c7df606aebeab5f517/2022/08/28/ce915024-5d73-4038-9922-5e57c5216723/notion-vs-evernote-switch-from-evernote-2022-08-28-16-10-17.jpg?auto=webp&width=1280)

Notion

I started writing my blog posts for ZDNET in Evernote back in 2012\. With a few minor exceptions, every one of those posts was written, and had a first edit, in Evernote. 

I quite like [Evernote](https://evernote.com/) and pay for a professional plan. One of the key benefits of Evernote was (note the past tense) that I could sync between computers. I usually write my articles on my MacBook Air. Once the article is done, my wife (who has years of experience as a managing editor) does an editing pass with me from the couch, using a Mac mini that is connected to a big screen in our family room. I then submit the edited article to ZDNET's editors for review. 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/GPk8_xpN_rA?si=YbAdgsjAKsCn_UsB" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

##  Sync failures 

But then Evernote's sync started to regularly fail. Sometimes it wouldn't sync at all. Sometimes, the edited version would be reported as a conflict, and Evernote would create two copies of the article. 

I reached out to [Evernote's support team](https://help.evernote.com/hc/en-us/requests/new), and was told to make sure I had the most recent version of the app (I did). I was also told not to edit the same note on two devices at once. My practice has always been to quit the app on one machine before editing on another. Support also instructed me to check to see if the note synced to the web (which had already become an obsessive practice). And then, I was told: 

> I cannot guarantee that this will solve the issues, but rest assured that we are aware of this feedback, and we are doing our best to improve the syncing process of the Evernote app. 

Not encouraging, that. Then, when Evernote decided to create three separate copies of an article, I realized it was time to find a different solution. 

This kind of thing gets old after awhile.

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/3C51hzX46eY?si=o5qiDSkT7mXUGm3F" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

##  The need to import Evernote notes 

The key requirement, for whatever Evernote alternative I found, was that it had to be able to import Evernote notebooks. I have two key writing notebooks I use every day: Blogs Complete and Blogs-in-Progress. 

Blogs Complete contains all my posts once they've been published. It has 1,364 notes. It needs to be searchable, because I often reference it to see what I said in a previous post. 

Blogs-in-Progress is the mission-critical notebook. It not only has the current blog post I'm writing, but ideas and notes for upcoming posts and projects. I often mine this notebook for new post ideas if I don't have a topic for the day. And as I work on bigger projects, I keep track of the details of each project in its own note. I then turn those notes into articles when the projects are complete. Blogs-in-Progress has 406 notes. 

A whole bunch of programs import Evernote, including Apple Notes, [Obsidian](https://obsidian.md/), [Ulysses](https://ulysses.app/), [Notion](https://www.notion.so/), the open source [Joplin](https://joplinapp.org/) note app, and even [Microsoft's OneNote](https://www.microsoft.com/en-us/microsoft-365/onenote/digital-note-taking-app). Since I'm a heavy user of Notion, I decided it would make the most sense to bring my blogging notebooks into Notion. 

**Review:** [**Notion app: Why (and how) I rely on this powerful productivity tool**](https://www.zdnet.com/article/notion-app-review/)

This did not go smoothly. Part of it was Evernote's fault. Part of it was Notion's fault. 

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/zAzTErKy6h8?si=vi5z3M9_7fW6qiAJ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<iframe width="560" height="315" src="https://www.youtube.com/embed/W5aJC8okA8s?si=L2rnYAp-gmGlLQSf" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<iframe width="560" height="315" src="https://www.youtube.com/embed/Q-mXUpVQijU?si=f1MzflPJ8-bD2_iQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
<li><a href="https://remote-screen-capture.techidaily.com/new-in-2024-digital-vault-for-internet-streams-a-recording-blueprint/"><u>[New] In 2024, Digital Vault for Internet Streams A Recording Blueprint</u></a></li>
<li><a href="https://article-posts.techidaily.com/new-streamline-your-storage-with-these-30-great-android-video-compressors-for-2024/"><u>[New] Streamline Your Storage with These 30 Great Android Video Compressors for 2024</u></a></li>
<li><a href="https://fox-access.techidaily.com/updated-in-2024-engage-audiences-with-impactful-podcast-descriptions/"><u>[Updated] In 2024, Engage Audiences with Impactful Podcast Descriptions</u></a></li>
<li><a href="https://fox-helps.techidaily.com/updated-photography-editing-tips-for-creating-stunning-photos-for-2024/"><u>[Updated] Photography Editing Tips for Creating Stunning Photos for 2024</u></a></li>
<li><a href="https://tiktok-video-files.techidaily.com/2024-approved-visual-impact-discover-these-essential-font-tools-for-tiktoks-2023/"><u>2024 Approved Visual Impact Discover These Essential Font Tools for TikTok's 2023</u></a></li>
<li><a href="https://novels-ebooks.techidaily.com/211152150-9781739495657-5th-dimensional-earth/"><u>5th Dimensional Earth | Free Book</u></a></li>
<li><a href="https://techno-recovery.techidaily.com/establishing-various-local-area-networks-lan-in-macos-enhancing-connectivity-flexibility-insights/"><u>Establishing Various Local Area Networks (LAN) in macOS: Enhancing Connectivity Flexibility - Insights</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/real-strategies-how-i-cut-down-on-social-networking-by-following-these-7-practical-steps/"><u>Real Strategies: How I Cut Down on Social Networking by Following These 7 Practical Steps</u></a></li>
<li><a href="https://some-tips.techidaily.com/stream-uninterrupted-with-the-top-vpns-of-the-year-comprehensive-expert-reviews-zdnet/"><u>Stream Uninterrupted with the Top VPNs of the Year: Comprehensive Expert Reviews | ZDNET</u></a></li>
<li><a href="https://technical-tips.techidaily.com/the-ultimate-walkthrough-on-leveraging-copilot-features-within-microsoft-teams/"><u>The Ultimate Walkthrough on Leveraging Copilot Features Within Microsoft Teams</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-ranked-vpns-for-enhanced-streaming-comprehensive-tests-and-reviews-by-experts-insights-from-zdnet/"><u>Top-Ranked VPNs for Enhanced Streaming: Comprehensive Tests & Reviews by Experts - Insights From ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-ranking-traveler-friendly-vpn-services-of-2024-comprehensive-experts-reviews-techradar/"><u>Top-Ranking Traveler Friendly VPN Services of 2024: Comprehensive Experts' Reviews | TechRadar</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-rated-android-vpn-apps-comprehensive-reviews-and-comparisons-by-tech-experts-zdnet/"><u>Top-Rated Android VPN Apps : Comprehensive Reviews & Comparisons by Tech Experts | ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-rated-travel-vpn-services-comprehensive-experts-reviews-and-comparisons-techradar/"><u>Top-Rated Travel VPN Services : Comprehensive Experts' Reviews & Comparisons - TechRadar</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-rated-vpn-service-trials-comprehensive-analysis-by-tech-specialists-zdnet-reviews/"><u>Top-Rated VPN Service Trials : Comprehensive Analysis by Tech Specialists - ZDNet Reviews</u></a></li>
<li><a href="https://some-tips.techidaily.com/ultimate-guide-to-choosing-a-reliable-vpn-for-your-mac-insights-from-detailed-expert-reviews-zdnet/"><u>Ultimate Guide to Choosing a Reliable VPN for Your Mac - Insights From Detailed Expert Reviews | ZDNet</u></a></li>
<li><a href="https://some-tips.techidaily.com/ultimate-guide-to-choosing-the-top-gaming-vpn-in-depth-analysis-by-tech-experts-zdnet/"><u>Ultimate Guide to Choosing the Top Gaming VPN: In-Depth Analysis by Tech Experts - ZDNet</u></a></li>
<li><a href="https://games-able.techidaily.com/unveiling-offscreen-patterns-on-xbox-sx-a-4-step-guide/"><u>Unveiling Offscreen Patterns on Xbox S/X: A 4-Step Guide</u></a></li>
<li><a href="https://some-tips.techidaily.com/unveiling-the-performance-expert-review-of-surfshark-vpn-by-zdnet-professionals/"><u>Unveiling the Performance: Expert Review of Surfshark VPN by ZDNet Professionals</u></a></li>
</ul></div>

