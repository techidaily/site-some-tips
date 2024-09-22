---
title: "Understanding Torrenting: Dive Into BitTorrent, Navigate Legal Concerns & Explore the Mechanics"
date: 2024-09-19 15:21:37
updated: 2024-09-20 12:32:12
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/0f7cc598462e00e671398d3de2bdb7c71a59af5f2607e912d55b8b85ab2b5c83.jpg
---

## Understanding Torrenting: Dive Into BitTorrent, Navigate Legal Concerns & Explore the Mechanics

![download concept](https://www.zdnet.com/a/img/resize/317a98656cae892c475eae1937a6387aa2c5b279/2024/08/06/6d420bf8-bd6b-486e-98ba-7f0928e4be4b/gettyimages-1139549767.jpg?auto=webp&width=1280)

FlashMovie/Getty Images

Torrenting is a term used for distributing and downloading files using the BitTorrent protocol. Because of how that protocol works, torrenting is particularly well-suited to the distribution of very large files. Once you understand how it works, you'll understand why it's so incredibly powerful… and so incredibly controversial.

## How big are files?

Let's make sure we're all on the same page when it comes to understanding how big certain kinds of files are. You'll need to understand this to truly understand what a game-changer BitTorrent is.

A byte is eight bits, or eight items that can either be a one or a zero. A character like "a" is 1 byte. Back in the day (before 2017) a Twitter tweet was limited to 140 characters, which would have been 140 bytes. Today, of course, [a tweet maxes out at 280 characters or 280 bytes](https://www.zdnet.com/article/twitter-opens-floodgates-on-280-character-tweets-after-few-use-it/). Depending on context, a kilobyte (KB) is either 1,000 bytes or 1,024 bytes (or roughly four maxed-out tweets).

**Also: [How to send large files in Gmail - up to 10GB](https://www.zdnet.com/home-and-office/work-life/how-to-send-large-files-up-to-10gb-in-gmail/)**

I took a look at a recent email thread where a colleague and I had emailed back and forth five or six times, and found it took up a little over 6,000 characters. A typical 1,200-word article (again, text only) is about 7,200 characters. We generally measure pure text in kilobytes.

A megabyte is about one million bytes or about 1,024KB (about 4,000 maxed-out tweets). You could store 142 typical articles in a single megabyte. We generally measure photos and music in megabytes, because photos and music need to contain a lot more data. A typical iPhone photo is about 3.5MB. An MP3 track is roughly 8MB. And a 10-minute 1080p YouTube video is 158MB (with a lot of compression).

Okay, let's get even bigger. Remember that a megabyte is about a thousand kilobytes. A gigabyte is roughly a thousand megabytes. You can store about 125 MP3 tracks in 1GB. We use gigabytes for measuring the size of big files, like movies and operating system distributions.

The [Ubuntu Linux](https://www.zdnet.com/article/ubuntu-linux-tries-for-the-office-desktop/) installer clocks in at 3.6GB. A DVD can hold 4.7GB. The Windows 11 ISO (the downloadable installer) [is 5.4GB](https://helpdeskgeek.com/windows-11/how-much-space-does-windows-11-take-up/). The MacOS installer is about 12GB. And a Blu-ray movie can range from 25GB to 50GB depending on how the Blu-ray disc is produced.

**Also: [Here's the best way to transfer large files between your laptop and desktop](https://www.zdnet.com/home-and-office/work-life/heres-the-best-way-to-transfer-large-files-between-your-laptop-and-desktop/)**

Today, most hard drives are sold in terabyte sizes (although stand-alone SSDs are still available with capacities as little as 64GB and many laptops ship with 256GB SSDs as their default loadout). A terabyte is roughly 1,000GB or… hold on tight now… 1,000,000,000 kilobytes.

## What is BitTorrent?

BitTorrent is a file-sharing and data distribution protocol created by programmer Bram Cohen in 2001\. BitTorrent changed the way files were distributed to computers across the internet, making it much more practical to distribute large and even giant files.

**Also:** [**The 5 best Linux distros for beginners: You can do this**](https://www.zdnet.com/article/best-linux-desktops-for-beginners/)

Before BitTorrent, if you wanted to distribute a file (say a [Linux distro](https://www.zdnet.com/article/here-come-the-new-red-hat-enterprise-linux-distros/)), you'd put it up on a server and individual users would download it. The server had to have the bandwidth to be able to handle all the users who wanted to download the file, which meant that popular files that were also large files would often clog the server's pipes rather quickly.

Some of the more popular large files were mirrored onto other sites, but each mirror also had to distribute the entire file to a given user. This meant that the mirror's bandwidth would also get used up rather quickly -- and many people downloading files either didn't know about the mirrors or preferred to download from the originating server anyway.

BitTorrent changed that up. Rather than distributing an entire file from one server, the BitTorrent protocol splits the file up into hundreds and even thousands of chunks and sends those chunks to BitTorrent client software running on users' machines. The BitTorrent client software then reassembles the original file, chunk-by-chunk, from those other individual machines, for the user doing the downloading.

**Also: [How to run dozens of AI models on your Mac or PC - no third-party cloud needed](https://www.zdnet.com/article/how-to-run-dozens-of-ai-models-on-your-mac-or-pc-no-third-party-cloud-needed/?ftag=TRE-03-10aaa6b&utm%5Femail=%7B%7B#sha256}}{{email}}{{/sha256}}&utm%5Fcampaign%5Fid={{campaignId}}&utm%5Femail%5Fid={{#sha256}}{{campaignId}}{{templateId}}{{email}}{{/sha256}}&utm%5Fnewsletter%5Fid={{messageTypeId}}&medium=email&source=iterable)**

Take a minute to wrap your head around this idea. Rather than using one server to distribute a file, every person who wants that file runs an app that turns their own computer into a mini server that then distributes parts of that file to other users. Essentially, every user downloading the file becomes part of the network that's distributing it.

You may have heard of [SETI@Home](https://setiathome.berkeley.edu/), which used the distributed computer power of thousands of volunteer computers all across the world to help analyze radio signals in the search for extraterrestrial life. [Folding@Home](https://foldingathome.org/?lng=en-US) also uses the distributed computing power of volunteered computers across the planet to analyze protein dynamics in an attempt to cure some diseases. BitTorrent is another example of the same idea. It uses thousands of computers -- the computers of those who want the file or files being shared -- to help distribute those files.

You can see how this might be a game-changer. Where, previously, it might have taken a considerable investment in resources and bandwidth to distribute a big file like an operating system release (or a popular movie), that investment is no longer necessary because the crowd of users doing the downloading are also sharing the file chunks amongst themselves.

**Also: [How to find which files are taking up the most storage space in Google Drive](https://www.zdnet.com/home-and-office/work-life/how-to-find-which-files-are-taking-up-the-most-storage-space-in-google-drive/)**

BitTorrent effectively removed the barrier of entry for the distribution of ginormous data files. This enormous change in the dynamics of data distribution has been used as a force of good… and not so good. More on that in a bit.

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

## Is there a special jargon for BitTorrent?

BitTorrent uses its own special set of buzzwords to describe various aspects of how the system works. If you want to really understand what's happening, it helps to understand what the terms mean.

**Seed:** This is the machine that originally distributes the shared file. Technically, any peer that has 100% of the shared file also becomes a seed.

**Peer:** This is a machine that downloads the shared file and then shares parts of the file to other peers. When you run a BitTorrent client on your machine to get a file, you're running a peer.

**Piece:** Part of a shared file, to be combined with other pieces when reassembled into a usable whole.

**Torrent:** Torrent is used in two ways. When specified with the word file (as in "torrent file"), this is a file containing metadata describing all of the pieces of the shared file and its checksum (validation) data. When used on its own (as in "I downloaded a torrent of Ubuntu"), it means the shared file (and all its pieces).

**Swarm:** This is the full network that's sharing a file, consisting of all the peers and seeds.

**Tracker:** This is a server that keeps track of the seeds and peers in the swarm. A tracker is often not involved in the actual transfer of data, but acts as more of an index or search engine for people looking for torrents. Trackers are often the target of legal action, because they're seen as the enablers of illicit file sharing.

**Leech:** This is a term for a peer that does not share pieces of a shared file. Basically, this is someone who wants to download a file using BitTorrent, but is not willing to do their part to support the swarm. Some leeches on very low-bandwidth connections can't download and share, so they download first, then share. But most leeches simply choose to be a "bit piggy" and download files without giving back.

**Health:** Do not confuse the BitTorrent term "health" with quality or safety of a file. In BitTorrent, health means how much of a file is available to download (anything less than 100% health means you're not getting a full file today). Do not assume something that shows 100% health is, for example, free of viruses. This also spotlights one of the downfalls of torrenting: Not all files are fully available to download. You may have to wait until a peer shows up with the missing pieces or, for less popular files, you may never get those missing pieces.

**Fake:** A file that spoofs what it claims to have. Generally, it's a file that contains malware or just junk bytes, designed to either attack users or improve the uploader's ratio.

**Ratio:** This is a measure of how much you've uploaded. It is sometimes used by trackers to allow more access to more files.

**TOR:** Folks often get confused by this. [TOR](https://www.zdnet.com/article/tor-project-battles-russian-censorship-through-the-courts/) stands for [The Onion Router](https://www.torproject.org/) and is unrelated to BitTorrent. Because TOR is a way of communicating over the Internet anonymously, some people do run torrents over TOR. But the TOR Project and BitTorrent are completely separate beasts.

Have I missed any important terms for torrents? If I did, let us know in the comments below.

## What BitTorrent client should I use?

As you might imagine, there are quite a few BitTorrent clients out there. Some are even good. Among those available include two from Rainberry (formerly BitTorrent, Inc.) the company formed by BitTorrent's developer, Bram Cohen. Rainberry has since been bought out by a cryptocurrency firm, and [Cohen is no longer associated with it](https://twitter.com/bramcohen/status/1087577311715577856). We won't be recommending the BitTorrent clients BitTorrent and uTorrent from Rainberry, because both come with advertising, fees, and associated software.

**Also: [How to transfer data from Android to an iPhone: 2 simple and fast ways](https://www.zdnet.com/article/how-to-transfer-data-from-android-to-an-iphone/)**

With that, let's look at some BitTorrent apps you might want to install.

**qBittorent:** My strongest recommendation is the free and open-source qBittorrent. While its interface is a bit cumbersome, it's been around for a long time, is a clean distribution, works with Macs, Windows, and Linux, and is generally quite powerful. It's not quite as extensible and customizable as other clients, but if you're just getting started, this will get you going.

**Transmission:** Transmission is another free and open-source implementation, this time tuned for MacOS. While there are builds of Transmission for Windows and Linux, this is a gorgeous implementation designed with MacOS users in mind. If you're a Mac user, you probably want to start here.

**Deluge:** Deluge is another free and open-source BitTorrent client. Its claim to fame is that it is very lightweight, meaning it uses very few system resources. You can run this on an old, retired machine and it will do just fine. Deluge also has a pile of extensions and add-ons if you want to customize it.

There are lots more, and some commercial applications. But, honestly, I haven't found a commercial application that has enough to offer for its fee, given the considerable capabilities of the three programs spotlighted above.

## Is it legal to use BitTorrent?

And now we come to the elephant in the room. BitTorrent is a protocol and is perfectly legal. But what people do with BitTorrent can be illegal, immoral, and possibly fattening.

If you're using BitTorrent to distribute a Linux distribution or large dataset, what you're doing is legal. One of my favorite sources for large gobs of data to explore (what can I say, I'm a geek) is [Academic Torrents](https://academictorrents.com/), a site that more than 127TB of torrentable data.

**Also:** [**How I recovered 'irreplaceable' photos off an SD card for free**](https://www.zdnet.com/article/how-i-recovered-irreplaceable-photos-off-an-sd-card-for-free/)

Did you know you could download the HAM10000 dataset, a 3.6GB collection of multi-source dermatoscopic images of common pigmented skin lesions? You can, and it's legal. Did you know you can download 115 paintings (2.6GB) from the Hermitage Museum, in high resolution? You can, and it's legal. Did you know you can download the 2.8GB NASA Astronomy Picture of the Day Archive, which currently has 7,800 images? Yep. You can. And it's legal.

But…

A lot of people aren't using BitTorrent to download legal skin lesion libraries. Instead, they're downloading pirated movies. 

Think about it. Most DVDs are more than 4GB and Blu-rays can be as much as 50GB. That amount of data is very hard to share from a centralized server. But if all of that is distributed across thousands of clients, it becomes easy and inexpensive to share copyrighted material.

Worse, it's hard to go after thousands of peer machines, so it's very difficult for the movie studios to shut down illegal BitTorrent sharing. They have managed to [go after tracker sites like The Pirate Bay](https://www.zdnet.com/article/does-piracy-pay-not-for-the-pirate-bay/), but if a group of individuals wants to seed and share movies, it's hard to stop them.

**Also: [This feature lets you transfer folders between Android and Windows](https://www.zdnet.com/home-and-office/work-life/users-discover-overlooked-nearby-share-feature-that-lets-you-transfer-entire-folders-between-android-and-windows-devices/)**

So let's be clear: Do not download pirated movies and television using BitTorrent. First, it may well be illegal. And second, many of those files may not be what they claim. Many torrents that claim to be recent popular movie releases are fakes designed to help distribute malware.

Just get yourself a subscription to Paramount+ to support the production of more Star Trek or to [MotorTrend+](https://www.motortrendondemand.com/) to support more car shows. Yes, I know there are other streaming services, but I'm writing this article and I like car shows and Star Trek.

My point though is this: Before there was fairly affordable streaming, torrenting media was popular. But when you can spend $15 bucks a month or so and get all the content you could possibly watch, why take the chance?

## Final thoughts

Torrenting is still a "thing" now. But it was huge piracy problem back in the 2000s and early 2010s, before streaming services made so much content available for relatively affordable rates. 

Torrents are still out there. You should probably install a torrent client in case you need to download Linux or a dataset, but it's not as big an issue as it once was. 

That said, as we continue to produce more and more huge files, it's a nice resource to have in our file-sharing kit bag. 

Are you a torrenter? Have you downloaded legitimate content via BitTorrent? Have you been a "bit piggy"? Do you regret downloading anything you really shouldn't have? What's your favorite BitTorrent client? Let us know in the comments below. 

#### Innovation

[Apple Vision Pro review: Fascinating, flawed, and needs to fix 5 things](https://www.zdnet.com/article/apple-vision-pro-review/ "Apple Vision Pro review: Fascinating, flawed, and needs to fix 5 things")

[Apple builds a slimmed-down AI model using Stanford, Google innovations](https://www.zdnet.com/article/apple-builds-a-slimmed-down-ai-model-using-stanford-google-innovations/ "Apple builds a slimmed-down AI model using Stanford, Google innovations")

[I tested the AI gadget that got the internet buzzing and it left me wanting more](https://www.zdnet.com/article/i-tested-the-ai-gadget-that-got-the-internet-buzzing-and-it-left-me-wanting-more/ "I tested the AI gadget that got the internet buzzing and it left me wanting more")

[9 biggest announcements at Google I/O 2024: Gemini, Search, Project Astra, and more](https://www.zdnet.com/article/is-openai-sweating-9-google-features-announced-for-gemini-search-android-and-more/ "9 biggest announcements at Google I/O 2024: Gemini, Search, Project Astra, and more")

* [Apple Vision Pro review: Fascinating, flawed, and needs to fix 5 things](https://www.zdnet.com/article/apple-vision-pro-review/ "Apple Vision Pro review: Fascinating, flawed, and needs to fix 5 things")
* [Apple builds a slimmed-down AI model using Stanford, Google innovations](https://www.zdnet.com/article/apple-builds-a-slimmed-down-ai-model-using-stanford-google-innovations/ "Apple builds a slimmed-down AI model using Stanford, Google innovations")
* [I tested the AI gadget that got the internet buzzing and it left me wanting more](https://www.zdnet.com/article/i-tested-the-ai-gadget-that-got-the-internet-buzzing-and-it-left-me-wanting-more/ "I tested the AI gadget that got the internet buzzing and it left me wanting more")
* [9 biggest announcements at Google I/O 2024: Gemini, Search, Project Astra, and more](https://www.zdnet.com/article/is-openai-sweating-9-google-features-announced-for-gemini-search-android-and-more/ "9 biggest announcements at Google I/O 2024: Gemini, Search, Project Astra, and more")

---

_You can follow my day-to-day project updates on social media. Be sure to follow me on Twitter at [@DavidGewirtz](https://twitter.com/davidgewirtz), on Facebook at [Facebook.com/DavidGewirtz](https://www.facebook.com/davidgewirtz), on Instagram at [Instagram.com/DavidGewirtz](https://www.instagram.com/DavidGewirtz/), and on YouTube at [YouTube.com/DavidGewirtzTV](https://www.youtube.com/user/DavidGewirtzTV)._

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
