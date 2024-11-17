---
title: Shared Frustrations After Apple iOS 18 Update - A Common User Experience
date: 2024-11-12T02:01:31.996Z
updated: 2024-11-17T01:40:34.024Z
tags:
  - apple
categories:
  - tech
thumbnail: https://www.zdnet.com/a/img/resize/74bc24e794dd353ae7e177f5407df4a4b168dd67/2024/09/17/14454a98-f7e5-4d5e-ada7-08bd016aeacf/2.jpg?width=278&height=156&fit=crop&auto=webp
---

## Top 7 Strategies Suggested by Apple for Creating Seamless Experiences on VisionOS - Insights

![Apple Vision Pro headset at WWDC 2023](https://www.zdnet.com/a/img/resize/025f723fae72cfe10cd99a1fcdb86dabdd8a1c92/2023/06/06/48689ad3-bca3-447a-b958-bfea14736233/img-8838.jpg?auto=webp&width=1280)

Jason Hiner/ZDNET

As the calendar turns from 2023 to 2024, Apple is getting closer to releasing its shockingly expensive and entirely experimental [Vision Pro headset](https://www.zdnet.com/article/i-tried-apple-vision-pro-and-its-far-ahead-of-where-i-expected/). Just this week, Apple announced that the iPhone 15 Pro and Pro Max can [capture spatial video for the Vision Pro](https://www.zdnet.com/article/the-iphone-15-pro-can-officially-capture-spatial-video-for-the-apple-vision-pro/).

You could say that Apple's vision of artificial reality is getting closer to real reality. And yes, I am pretty proud of that sentence. 

**Also: [I tried Apple Vision Pro and it's far ahead of where I expected](https://www.zdnet.com/article/i-tried-apple-vision-pro-and-its-far-ahead-of-where-i-expected/)**

Recently, Apple also started to release design guidelines for developers. One that caught my eye is the company's "[Q&A: Spatial design for visionOS](https://developer.apple.com/news/?id=fi8ne6ji)." This document provides some best practices for developers creating apps for VisionOS. 

Since VisionOS is a very different beast from all of the other Apple OS implementations, particularly in the user interface department, I thought it would be interesting to share with you some of those best practice recommendations. 

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

That way, if you're a developer, you can start thinking about how to build your apps. And if you're a user considering purchasing a set of these solid gold goggles, you'll have a better feel for how designers are constructing their apps and what your experience might be. 

Let's dig in, shall we? 

>  Disclaimer: This post includes affiliate links
>
>  If you click on a link and make a purchase, I may receive a commission at no extra cost to you.
>

##  1\. Gradual immersion

Apple recommends you gradually introduce users to your app, starting with a window view within the augmented reality environment. 

That way, they're not suddenly dropped into a whole new world, but they can slowly get their "VR legs" and feel they have some level of control over their immersion level, at least until they get comfortable with their environment. 

**Also: [Two breakthroughs made 2023 tech's most innovative year in over a decade](https://www.zdnet.com/article/two-breakthroughs-made-2023-techs-most-innovative-year-in-over-a-decade/)**

<!-- affiliate ads begin -->
<a href="https://bluettius.sjv.io/c/5597632/2139107/17108" target="_top" id="2139107">
  <img src="//a.impactradius-go.com/display-ad/17108-2139107" border="0" alt="https://techidaily.com" width="250" height="90"/>
</a>
<img height="0" width="0" src="https://bluettius.sjv.io/i/5597632/2139107/17108" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  2\. Identify your key moments

Let's say you're a developer who has an existing app for the iPad. Let's say you want to bring said iPad app into VisionOS. The iPad app, by its nature, is flat and rectangular. But VisionOS allows users to see all around. Is there anything in your app that clearly lends itself to VRification? 

**Also: [Inside VisionOS: 17 things developers need to know right now](https://www.zdnet.com/article/inside-visionos-17-things-developers-need-to-know-right-now/)**

Apple uses its Photos app as an example. A key moment for Apple's Photos app might be showing a panoramic photo by wrapping it around the user completely. Panoramas are a long-standing feature of the Photos app, but spatially wrapping the pano is something that would showcase the mixed-reality environment. 

In a writing app, VRification might involve going from a typical windowed user interface for most writing to a focus mode that shuts out the outside world and lets your users concentrate, by providing a calming background and perhaps some calming music. 

##  3\. Adjust UI elements to accommodate the new environment

Some UI elements translate directly from iPadOS to VisionOS, but others aren't an exact match. Apple has a [spatial design guidelines video](https://developer.apple.com/videos/play/wwdc2023/10072/) that's well worth watching to come up to speed. 

**Also: [Would you believe a VR headset outsold AirPods during Black Friday? It happened](https://www.zdnet.com/article/would-you-believe-a-vr-headset-outsold-airpods-during-black-friday-it-happened/)**

One area to pay particular attention to is when you use hover effects. When you hover over a button in a flat UI, you just need to see some highlighting. But when you hover over -- or in front of -- something in VR space, you've got the entire room to work in. So pay attention to how things look and feel, and try to avoid inducing vertigo by rapidly moving objects and buttons. 

##  4\. Utilize grid systems where appropriate

Apple says that apps designed with the [iPadOS grid system](https://developer.apple.com/design/human-interface-guidelines/designing-for-ios) will translate very nicely to the Vision Pro. The grid works well for designing windows. Point sizes translate well from the iPad to Vision Pro. 

But as you deal with more 3D-centric objects, grid systems break down. Once you're moving in 3D space, be careful about where you place your controls. For example, it can be somewhat confusing if you have nearby controls for a faraway object. 

<!-- affiliate ads begin -->
<span id="1304647">
					<video width="240" height="200" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1304647.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/15852-1304647">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1304647.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:150px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fthefitville.pxf.io%2Fc%2F5597632%2F1304647%2F15852'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1304647/15852" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  5\. Incorporate sound design strategically

Sound -- that is, _audio_ \-- design plays a crucial role in spatial computing. Sound may not be as critical for flat UI experiences, but we humans rely on sound -- and the spatial awareness that sound provides -- to orient ourselves in our real-world environment. So keep in mind that sound not only makes your environment more interesting, it can serve as an orientation tool as well. 

To that end, even if you're building a non-entertainment app that would normally not focus on sound, consider how sound elements, no matter how subtle, might be used for user spatial orientation while in VR space. 

**Also: [Apple's Vision Pro: A concept prototype with this enormous potential](https://www.zdnet.com/article/apples-vision-pro-a-concept-prototype-with-this-enormous-potential/)**

And while you're at it, allow your users to control the sound, setting its volume and even turning it off. Give the sound cues that may be helpful, but give users control over how those cues are applied. Here's [a great resource from Apple on sound design](https://developer.apple.com/wwdc23/10271). 

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2094476/7443" target="_top" id="2094476">
  <img src="//a.impactradius-go.com/display-ad/7443-2094476" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2094476/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  6\. Focus on key details, but don't overwhelm

Apple recommends always rendering a ground plane so users feel grounded. If you're putting someone inside a theatre, provide key details (like a stage, lighting, and curtains), but don't get carried away trying to reproduce the cola stains in the carpet or that unique crackle that comes from walking over scraps of petrified popcorn. If you're rendering an outdoor landscape, show slowly moving clouds but keep things subtle. 

Of course, if you're putting people into a game where the whole idea is to overwhelm them, then go for it. But Apple is much more interested in using VR and AR as an augmented tool, rather than purely as a gaming platform. And in that context, it's probably wise to avoid making your customers barf up their lunches inside their $3,500+ head-mounted [uncanny valley](https://en.wikipedia.org/wiki/Uncanny%5Fvalley)in a can. 

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135406/19272" target="_top" id="2135406">
  <img src="//a.impactradius-go.com/display-ad/19272-2135406" border="0" alt="https://techidaily.com" width="120" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135406/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

##  7\. Use the VisionOS simulator

There is, in fact, a VisionOS simulator available inside Xcode, Apple's development environment. Here's a [guide to all of the Xcode simulators](https://developer.apple.com/documentation/xcode/running-your-app-in-simulator-or-on-a-device). And here's a [guide to interacting with your app](https://developer.apple.com/documentation/visionos/interacting-with-your-app-in-the-visionos-simulator) inside the Xcode VisionOS simulator. 

So there you go. Seven helpful tips for keeping your users' insides inside. 

**Also: [The iPhone 15 Pro can officially capture spatial video for the Apple Vision Pro](https://www.zdnet.com/article/the-iphone-15-pro-can-officially-capture-spatial-video-for-the-apple-vision-pro/)**

What do you think? Are you building apps for VisionOS? Are you planning on buying a Vision Pro? Let us know in the comments below. 

---

_You can follow my day-to-day project updates on social media. Be sure to subscribe to my weekly update newsletter [on Substack](https://advancedgeekery.substack.com/), and follow me on Twitter at [@DavidGewirtz](https://twitter.com/davidgewirtz), on Facebook at [Facebook.com/DavidGewirtz](https://www.facebook.com/davidgewirtz), on Instagram at [Instagram.com/DavidGewirtz](https://www.instagram.com/DavidGewirtz/), and on YouTube at [YouTube.com/DavidGewirtzTV](https://www.youtube.com/user/DavidGewirtzTV)._

#### AR + VR

[I replaced my boring workouts with Meta Quest's Supernatural app, and can't imagine going back](https://www.zdnet.com/article/supernatural-on-meta-quest-hands-on/ "I replaced my boring workouts with Meta Quest's Supernatural app, and can't imagine going back")

[This Finnish startup's new VR headset rivals Apple's Vision Pro - and business users will love it](https://www.zdnet.com/article/this-finnish-startups-new-vr-headset-rivals-apples-vision-pro-and-business-users-will-love-it/ "This Finnish startup's new VR headset rivals Apple's Vision Pro - and business users will love it")

[Meta's $500 Quest 3 is the mainstream VR headset I've been waiting for, and it delivers](https://www.zdnet.com/article/meta-quest-3-review/ "Meta's $500 Quest 3 is the mainstream VR headset I've been waiting for, and it delivers")

[I tried Apple Vision Pro and it's far ahead of where I expected](https://www.zdnet.com/article/i-tried-apple-vision-pro-and-its-far-ahead-of-where-i-expected/ "I tried Apple Vision Pro and it's far ahead of where I expected")

[The best VR headsets right now (and they're not just from Meta)](https://www.zdnet.com/article/best-vr-headset/ "The best VR headsets right now (and they're not just from Meta)")

* [I replaced my boring workouts with Meta Quest's Supernatural app, and can't imagine going back](https://www.zdnet.com/article/supernatural-on-meta-quest-hands-on/ "I replaced my boring workouts with Meta Quest's Supernatural app, and can't imagine going back")
* [This Finnish startup's new VR headset rivals Apple's Vision Pro - and business users will love it](https://www.zdnet.com/article/this-finnish-startups-new-vr-headset-rivals-apples-vision-pro-and-business-users-will-love-it/ "This Finnish startup's new VR headset rivals Apple's Vision Pro - and business users will love it")
* [Meta's $500 Quest 3 is the mainstream VR headset I've been waiting for, and it delivers](https://www.zdnet.com/article/meta-quest-3-review/ "Meta's $500 Quest 3 is the mainstream VR headset I've been waiting for, and it delivers")
* [I tried Apple Vision Pro and it's far ahead of where I expected](https://www.zdnet.com/article/i-tried-apple-vision-pro-and-its-far-ahead-of-where-i-expected/ "I tried Apple Vision Pro and it's far ahead of where I expected")
* [The best VR headsets right now (and they're not just from Meta)](https://www.zdnet.com/article/best-vr-headset/ "The best VR headsets right now (and they're not just from Meta)")

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
<li><a href="https://fox-glue.techidaily.com/new-2024-approved-realms-intersecting-delving-into-vr-augmented-and-mixed-immersion/"><u>[New] 2024 Approved Realms Intersecting Delving Into VR, Augmented & Mixed Immersion</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/new-in-2024-video-creation-simplified-key-elements-of-using-aiseesofts-tech/"><u>[New] In 2024, Video Creation Simplified Key Elements of Using Aiseesoft's Tech</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-streamline-screen-capabilities-building-in-frame-video-experiences-on-sierra/"><u>[New] Streamline Screen Capabilities Building In-Frame Video Experiences on Sierra</u></a></li>
<li><a href="https://some-tips.techidaily.com/new-the-easy-way-to-craft-your-digital-self-in-virtual-worlds/"><u>[New] The Easy Way to Craft Your Digital Self in Virtual Worlds</u></a></li>
<li><a href="https://instagram-video-files.techidaily.com/updated-in-2024-can-instagrams-video-selfies-be-trusted/"><u>[Updated] In 2024, Can Instagram's Video Selfies Be Trusted?</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-transform-your-flip-to-flash-with-android/"><u>[Updated] Transform Your Flip to Flash with Android</u></a></li>
<li><a href="https://some-tips.techidaily.com/updated-unlock-new-dimensions-of-sound-best-free-valorant-audio-alterer-revealed/"><u>[Updated] Unlock New Dimensions of Sound Best Free Valorant Audio Alterer Revealed</u></a></li>
<li><a href="https://some-tips.techidaily.com/in-2024-streamlined-editing-best-apps-compatible-with-macos-big-sur/"><u>In 2024, Streamlined Editing Best Apps Compatible with macOS Big Sur</u></a></li>
<li><a href="https://extra-hints.techidaily.com/next-gen-camera-showcase-2024-edition/"><u>Next-Gen Camera Showcase - 2024 Edition</u></a></li>
<li><a href="https://extra-guidance.techidaily.com/srt-conversion-essentials-ttml-xml-ssa-and-beyond-for-2024/"><u>SRT Conversion Essentials TTML, XML, SSA, and Beyond for 2024</u></a></li>
<li><a href="https://some-guidance.techidaily.com/the-intersection-of-business-and-immersive-vr-technology-for-2024/"><u>The Intersection of Business and Immersive VR Technology for 2024</u></a></li>
</ul></div>

