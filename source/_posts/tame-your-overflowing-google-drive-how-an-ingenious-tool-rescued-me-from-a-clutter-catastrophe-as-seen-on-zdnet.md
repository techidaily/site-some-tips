---
title: "Tame Your Overflowing Google Drive: How an Ingenious Tool Rescued Me From a Clutter Catastrophe, as Seen on ZDNET!"
date: 2024-09-17 16:29:10
updated: 2024-09-20 10:48:52
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/04440a12467eb00d2e76ab58c49996f10e544f909e1d6b3abfc42368ffd69851.jpg
---

## Tame Your Overflowing Google Drive: How an Ingenious Tool Rescued Me From a Clutter Catastrophe, as Seen on ZDNET!

![Data pie chart](https://www.zdnet.com/a/img/resize/aaa1c47496f8896547227fa737d7b262859266c9/2023/10/12/8eb5c7b8-b49a-4795-af70-89e55a91fa5f/gettyimages-1323621643.jpg?auto=webp&width=1280)

Andriy Onufriyenko/Getty Images

One of the oddest things about [Google Drive cloud storage](https://www.zdnet.com/article/best-cloud-storage/) is that it doesn't provide a mechanism for you to be able to tell how much storage a given folder takes up. Google is quick with how much overall storage you use, because that's how they bill you. But if you want to know which folders take up how much space, there's no cloud interface for that. 

When you ask Google's support team, their answer is this: Set up syncing and then use your local OS to tell you how much data you have in the synced directory. This is all well and good when you have 10GB in synced cloud storage, or even a terabyte or two.

**Also: [The other shoe finally dropped on my Google Enterprise cloud storage plan](https://www.zdnet.com/article/the-other-shoe-finally-dropped-on-my-google-enterprise-cloud-storage-plan/)**

But when you have an enterprise plan, and you have 58TB of cloud storage in use, it's not like you're going to download your data to a local computer just to find out which folders are taking up a lot of space. 

I faced this challenge recently [when Google capped my unlimited storage](https://www.zdnet.com/article/the-other-shoe-finally-dropped-on-my-google-enterprise-cloud-storage-plan/). I'm still smarting a bit about how unlimited always has a limit. Fortunately, after a lot of begging, Google did give me a bit more storage, so I was no longer suddenly at capacity. But the writing is on the wall. I need to prune my online storage usage. 

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

But even then, I still face the problem I described above -- how much storage is each of my folders taking up? I can't prune if I don't know what I'm pruning. 

**Also: [How to easily manage your Google Workspace storage](https://www.zdnet.com/article/how-to-easily-manage-your-google-workspace-storage/)**

Fortunately, while Google doesn't offer a solution, a developer named Brett Batie in Traverse City, MI has come up with a solution. It's called [Filerev](https://filerev.com/) and it does just what you would have expected Google Drive to do. It answers questions and helps manage vast amounts of data. 

##  Understanding (or not understanding) current storage utilization 

When we [last encountered this issue](https://www.zdnet.com/article/the-other-shoe-finally-dropped-on-my-google-enterprise-cloud-storage-plan/), I was trying to optimize my storage utilization, so that it didn't grow beyond its new 75TB bounds. 

Screenshot by David Gewirtz/ZDNET

My remote Google Drive storage is divided into two main folders: Cloud Backup, and Cloud Sync. 

The Cloud Backup folder holds incremental backups of my servers. With this setup, I can keep all files, including those that have been deleted. That way, I can execute a restore and grab the state of a folder or file on any given date. 

**Also: [Why that cheap 'lifetime cloud storage' deal might cost more than you bargained for](https://www.zdnet.com/article/why-that-cheap-lifetime-cloud-storage-deal-might-cost-more-than-you-bargained-for/)**

Cloud Sync is a 1-for-1 sync to the server folders, as they are right now. This folder allows me to get to a live file remotely, without having to go through the very long and convoluted process required by a restore. 

The Cloud Sync folder has come to my rescue numerous times when traveling, such as when I had to [evacuate Florida when the hurricanes struck](https://www.zdnet.com/article/road-tech-how-i-left-florida-to-escape-irma-and-never-went-back/). 

Screenshot by David Gewirtz/ZDNET

The picture above shows something quite odd. I did a backup early this morning. And yet, the "Last modified" date shown is from 2018\. When I drill down to a file I know I modified a day or so ago, it does show the current date. So, why is that happening? It's so frustrating. If that folder has changed, it should contain the date of the latest change. But no, it's just not that easy.

Screenshot by David Gewirtz/ZDNET

As for my ongoing challenge with finding the size of folders, you would think that by digging into the menu for a folder, as I've done here, the File Information > Details menu item would show additional details, such as how big a folder might be. But all it does is open Details pane, which, unamusingly, does not contain the details we need. 

Screenshot by David Gewirtz/ZDNET

As for the Details pane (pain?), it doesn't contain any data about size at all. It does include the correct date for the last time a folder was opened, but somehow "modified" still shows 2018, even though I modified it yesterday by adding some files and folders. 

Screenshot by David Gewirtz/ZDNET

So, how on Earth can I determine how much storage I am using in each of my folders? We're talking about an enterprise account with 58TB of storage. And yet, there's no visibility into storage utilization. It's not just bizarre, it's deeply inconvenient. 

##  Say hello to Filerev 

Batie's Filerev software seriously comes to the rescue in this situation. Filerev is available in a variety of different plans. I won't be doing a lot of scans, but the scan I did reveals that I have 4,875,461 files (a number I never would have known without Filerev), so I definitely need the Premium plan. 

Screenshot by David Gewirtz/ZDNET

Batie was kind enough to give me a free account. He also went above and beyond, and answered my questions while I was struggling to understand my file utilization. He incorporated my feedback and added a number of useful features, including the drill-down graphics, which I basically begged him for. 

**Also: [Google's Duet AI for Workspace can create presentations, write emails, and attend meetings for you](https://www.zdnet.com/article/google-workspaces-ai-facelift-is-finally-here-meet-duet-ai-for-workspace/)**

Filerev ascertains your storage structure by doing a file scan. For me, that took a few days. It's also a bit of a worry, because you have to open up access to your files to Filerev. But while I am a bit concerned by that security issue, Batie says that the tool retrieves mostly metadata and not file contents. Given the choice between losing access to all my data due to Google's limits on unlimited usage, and having this tool explore my metadata, opening up to Filerev is the lesser of two evils. 

Here's the most interesting detail. I can see how my Cloud Sync data compares to Cloud Backup: 

Screenshot by David Gewirtz/ZDNET

Clicking the More button gives me actual storage details. The big shock was that the Cloud Backup folder uses considerably less storage than the Cloud Sync folder. Until I saw that graphic, I had been convinced it was the other way around. 

Screenshot by David Gewirtz/ZDNET

You can click into either folder. Clicking into the Cloud Sync folder tells a very interesting story: 

Screenshot by David Gewirtz/ZDNET

Two of my top three storage usages make sense. The folder Backup Share is a mirror of the local machine backups on my local area network, which are different to the overall server backups that are in the main Cloud Backup folder. 

And the Studio Share folder, at 7.42TB, makes total sense. That's where I keep all my video work-in-progress for the various videos on my YouTube channel. 

**Also: [The best cloud storage services of 2023: Expert picks](https://www.zdnet.com/article/best-cloud-storage/)**

But it's Liberty Tank, at 11.1TB, that's most instructive. This was a server I previously backed up, but it's long out of date. All the files on Liberty Tank were moved to the current server and are being backed up separately. So the sync with Liberty Tank, all 11.1TB of it, is unnecessary storage utilization. 

Just nuking that, alone, will move my storage utilization from a stressful 58TB down to a more calming 47TB. 

And there's no way I would have known that without Filerev. 

Filerev has quite a few additional features, including a lot of customization. But one feature I'd like to point out is the File Groups summary: 

Screenshot by David Gewirtz/ZDNET

Although the closeness of the red-like colors make it a bit hard to tell, my videos do not take up the most storage. That honor goes to the category of Other. 

Drilling into Other shows this Octet-Stream category: 

Screenshot by David Gewirtz/ZDNET

As it turns out, that storage category accounts for all my virtual machines. And yes, it makes total sense that I have 36TB of virtual machines (VMs). I do a lot with VMs. More to the point, I once did a tremendous amount with VMs. For many years, I was running multiple virtual server racks on my computers that I used as part of my development process. 

It won't be easy to trim down those VM syncs, but it's definitely something I can look at, because I know a bunch of those VMs are very obsolete. 

##  Final thoughts 

I made a few interesting discoveries. My Cloud Backup share isn't the villain I thought it was. That honor goes to the Liberty Backups folder. Second, the biggest category of storage is my storage of old VMs. That's a homework assignment I need to follow up on to clear out more space. 

But also, this is a story of individual developers and the contribution they make to the industry. Filerev does what Google Drive should do. There's really no excuse for an enterprise-level cloud storage service to lack basic directory analytics. 

But this one dude in Traverse City, Brett Batie, stepped up and built a solution and a business. Not only did he provide a useful software solution, he also collaborated with me on some interesting value-adding features to Filerev, which helped me solve my problem and I'm sure will help others. 

Batie's efforts show the best of the indy developer phenomenon, and I very much appreciate his help. Give Filerev a look. It might help solve a critical storage situation for you, as well. 

---

_You can follow my day-to-day project updates on social media. Be sure to subscribe to my weekly update newsletter [on Substack](https://advancedgeekery.substack.com/), and follow me on Twitter at [@DavidGewirtz](https://twitter.com/davidgewirtz), on Facebook at [Facebook.com/DavidGewirtz](https://www.facebook.com/davidgewirtz), on Instagram at [Instagram.com/DavidGewirtz](https://www.instagram.com/DavidGewirtz/), and on YouTube at [YouTube.com/DavidGewirtzTV](https://www.youtube.com/user/DavidGewirtzTV)._

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
