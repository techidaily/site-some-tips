---
title: "Advancing Development & Data Analysis: How Google Cloud Enhances Toolsets & Incorporates Generative AI"
date: 2024-09-19 22:58:56
updated: 2024-09-20 11:31:24
tags:
  - cloud
categories:
  - tech
thumbnail: https://thmb.techidaily.com/7b8336f5215e637e754158b1429078ceab1fa3c341406711596b3493655e21bb.jpg
---

## Advancing Development & Data Analysis: How Google Cloud Enhances Toolsets & Incorporates Generative AI

![Google Cloud logo on phone and on background](https://www.zdnet.com/a/img/resize/31794df6a01a84685b967a438bf0c2f434ab77e7/2023/08/28/55f4ebb2-6738-4630-8649-078b11eeabb5/gettyimages-1233514433.jpg?auto=webp&width=1280)

SOPA Images/Contributor/Getty Images

At this week's big Google Cloud conference, Google Next '23, executives at the tech giant made numerous announcements and forward-looking statements to help developers and IT managers plan for future cloud buildouts and innovations. 

The ZDNET editorial team deployed en mass to explore the wide range of announcements, which you can find here on ZDNET. My task was to look at Google's work in the areas of developer, data, and AI cloud. Here, Google is doing a lot to empower developers to build out the next generation of [cloud-based applications](https://www.zdnet.com/article/what-is-cloud-computing-everything-you-need-to-know-about-the-cloud/) and incorporate [generative AI capabilities](https://www.zdnet.com/article/what-is-generative-ai-and-why-is-it-so-popular-heres-everything-you-need-to-know/), where appropriate. 

**Also: [How Google is beefing up AI-powered search](https://www.zdnet.com/article/google-is-beefing-up-ai-powered-search-on-google-chrome-for-ios-and-android/)**

Back in May, at Google I/O, [Google announced a new capability called Duet AI](https://www.zdnet.com/article/every-major-ai-feature-announced-at-google-io-2023/) for developers. Duet AI's developer features are loosely similar to those in [Microsoft's GitHub AI-assisted Copilot](https://www.zdnet.com/article/is-github-copilots-code-legal-ethically-right/), because they aim to help developers produce code on the Google cloud platform. 

Moving forward to today, at Google Next '23, Google doubled down on Duet AI and provided more details not only on what Duet AI can do, but on how they've been expanding on the original premise. 

Before we dive into some of those capabilities, let's clear up what might be a source of confusion. Duet AI isn't just for developers. Back in May, [Google also announced Duet AI for Workspace](https://workspace.google.com/blog/product-announcements/duet-ai), showing how it can help create presentations, take notes in meetings, help you write documents, and more. What we'll be digging into here is the "and more", where Google also uses Duet AI to help craft code and build projects. 

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

##  Duet AI for cloud development 

In May, Google showed how Duet AI can be used for code and chat-level assistance. Since that time, "trusted developers" (their term) have been testing out the capability and providing feedback to Google's engineers. According to Google, Duet AI is intended to provide developer support across the entire development lifecycle, providing help for coding, source citation, test coverage, designing and publishing APIs, migrating and modernizing applications, and more. 

**Also:** [**Google Workspace's AI facelift is finally here. Meet Duet AI for Workspace**](https://www.zdnet.com/article/google-workspaces-ai-facelift-is-finally-here-meet-duet-ai-for-workspace/)

As a developer, one thing I find very interesting is that Duet AI is available via plugins or extensions into common coding environments. These include Microsoft's IDE VSCode, and JetBrains IDEs, such as CLion, GoLand, IntelliJ, PyCharm, Rider, and WebStorm. That integration makes the tool much more relevant since Google isn't requiring coders to switch platforms to use the helper tool. 

Here's where the potential of AI assistance shines. Let's ignore the fact that [AI coding has tended to be unreliable](https://www.zdnet.com/article/i-tested-google-bards-new-coding-skills-it-didnt-go-well/), and assume Google's developers will improve performance over time. In a blog post, Duet AI in Google Cloud Blog, Brad Calder, vice president, Google Cloud Platform and Technical Infrastructure, showed that a natural language prompt, such as "Convert this function to Go and use Cloud SQL", could be used to rewrite code in a new language and update the APIs, all from a single sentence. 

**Also:** [**Google debuts Duet AI to tackle new cybersecurity challenges in the cloud**](https://www.zdnet.com/article/google-debuts-duetai-to-tackle-new-cybersecurity-challenges-in-the-cloud/)

Migration efforts can be particularly taxing on developers. In my case, I have some old code written for PHP 5.6 that is no longer compatible with current PHP 8.x environments. If I do it by hand, I face weeks (or perhaps months) of finding all the bits and pieces that need conversion to bring that code up to date. But if an AI can do it (without screwing it up), the AI could potentially cut down my workload by weeks or months. That's a very big upside benefit, because it [frees up developers](https://www.zdnet.com/article/github-developer-survey-finds-92-of-programmers-using-ai-tools/) to add new features and innovate, rather than -- as specs change and incompatibilities manifest like rust on old metal -- just spending time migrating and updating the same code over and over and over. 

Google is also introducing what they call "context-aware code generation". Here, too, don't get confused. Normally, the term context-aware relates to some AI activity that's based on what's currently on screen. Context-aware fill in Photoshop fills in textures based on surrounding textures. Context-aware code would be expected to generate code based on what's in the current function. However, Google's use of the term refers to the corporate context, not the on-screen context. 

Calder says: "We have started to work with select enterprises to allow Duet Al to be customized with organization-specific knowledge from their libraries and code base to generate context-aware code suggestions." This approach means that if your organization has its own libraries, Duet AI could be smart enough to incorporate that institutional knowledge. Of course, what "select enterprises" means, and whether this is a feature to be released broadly, is not clear at this time. 

**Also: [Meet the post-AI developer: More creative, more business-focused](https://www.zdnet.com/article/meet-the-post-ai-developer-more-creative-more-business-focused/)**

Another compelling feature is that Duet AI can help developers publish APIs using natural language prompts. Once again, when it works, this has the potential to be a huge time-saver. 

##  Duet AI for databases and data analytics in the cloud 

Google has a laundry list of massive services for data and database management. At Google Next '23, the company indicated it's integrating Duet AI into most of them. 

It's very easy to get caught in the weeds when talking about Google's various data management offerings, so for the purposes of this article, I'll provide a very simple summary of each. 

* **Cloud Spanner:** A globally distributed, strongly consistent database service that offers high availability and scalability, designed for enterprises needing global reach and high transactional integrity.
* **AlloyDB:** A specialized, fully managed database service on Google Cloud Platform that focuses on PostgreSQL users, which is ideal for those who require a PostgreSQL-specific solution.
* **Cloud SQL:** A versatile, fully managed relational database service that supports multiple database types like PostgreSQL, MySQL, and MS SQL, suitable for a wide range of applications and business sizes.
* **BigQuery:** A serverless, highly scalable, and cost-effective multi-cloud data warehouse designed for business agility, which is perfect for those who need to run fast, SQL-like queries on large datasets.

Google has announced that Duet AI now supports Cloud Spanner. Duet AI can write code that manages and queries data using natural language. The blog post shows an example natural language query, "write a query to show all data in the messages table", that automatically generates the SQL, which users can then test and modify. 

**Also: [The other shoe finally dropped on my Google Enterprise cloud storage plan](https://www.zdnet.com/article/the-other-shoe-finally-dropped-on-my-google-enterprise-cloud-storage-plan/)**

The company says Duet AI will also be available for Alloy DB and Cloud SQL, with no delivery date specified yet. Google is offering a Duet AI service to migrate Oracle to AlloyDB and Oracle to Cloud SQL-for-PostgreSQL later this year. If that last sentence lights your fire, then you're a target customer for this new AI service. Expect other legacy systems to benefit from these sort of migrations in the future. 

##  Shifting down instead of shifting left 

Okay, time for some more buzzwords. In the DevOps world, the term "shifting left" applies to moving later stage processes like QA and security reviews earlier in the development process, so that they're incorporated into the design and evaluation of a project. 

The idea is you're moving tasks that are later on the project timeline to an earlier point. Since timelines are chronologically from left to right, shifting left, therefore, means doing it earlier. 

Google is advocating the practice of "shifting down". The idea was introduced in [a blog post](https://cloud.google.com/blog/products/application-development/richard-seroter-on-shifting-down-vs-shifting-left) by Richard Seroter, Google's director of outbound strategy and engagement. The timeline paradigm breaks here, because, of course, horizontal lines don't have depth. 

**Also: [AI will change the role of developers forever. Here's why that's good news](https://www.zdnet.com/article/ai-will-change-the-role-of-developers-forever-heres-why-thats-good-news/)**

Don't overthink it. If you start trying to parse tech buzzwords literally, the idea that the cloud lives in ginormous data centers won't make any sense. Just understand that the terms are built out of other ideas (like the cloud shape that is often drawn on network diagrams). In this case, Seroter is pushing the idea that the shifting should go in a different direction. 

His premise is that shifting left puts more work on developers, who are already overworked and over committed. Instead, he recommends that workloads be shifted down, from developers down into their development platforms. The idea is, essentially, to let the software do the work. 

As you might imagine, letting software do the work is pretty much a mission statement for generative AI. And that, finally, now that we have context, brings us to Google's next set of announcements -- an overall effort to [support the developer experience](https://www.zdnet.com/article/software-developers-dance-with-generative-ai-is-still-at-that-awkward-stage/). 

Google has announced a number of "shifting down" efforts: 

* **Jump Start Solutions:** These are application and infrastructure solutions that are essentially pre-canned starting points for projects, with assists provided by generative AI capabilities.
* **Duet AI for code completion and chat:** We talked about this effort above, and it's intended to offload the work from developers to the AI.
* **Shifting down interoperability:** Google has announced the general availability of Application Integration, a no-code integration platform-as-a-service offering, that contains a drag-and-drop interface for connecting services together. Think of it as a Zapier for enterprise-level cloud projects. Google also announced that Duet AI will help here, as well.
* **Cloud workstations:** Although this capability has been around for a while, Google is highlighting that the use of its virtual desktop service can "shift the burden of provisioning, scaling, managing and securing developer environments down to the platform."

##  David's hot take 

Google has quite a few more initiatives in the developer and data space, but all will likely be informed by, or soon be informed by, generative AI assistance. Whether it's in the form of a copilot, such as Duet AI, or an AI-driven tool to help "shift down" the effort into the platform, most of these endeavors, if they work, will be a definite boon to developers. 

On one hand, this is deeply exciting. A lot of [coding is pure burden](https://www.zdnet.com/article/chatgpt-can-write-code-now-researchers-say-its-good-at-fixing-bugs-too/). Updating to fix incompatibilities, building functional tests, and finding bugs are tasks that are definitely un-fun. Migrations and conversions take a tremendous amount of time, and rarely result in a lot of new capabilities. 

For one of my projects, I've spent probably 80% of my time doing conversions because the commerce platforms the project relies upon have changed over the years. I've actually spent less than 20% of my time adding features and capabilities. If even 25% of my migration and conversion burden could be delegated to an AI, I could double my new feature output. That's huge. 

**Also:** [**AI could automate 25% of all jobs. Here's which are most (and least) at risk**](https://www.zdnet.com/article/ai-could-automate-25-of-all-jobs-heres-which-are-most-and-least-at-risk/)

But here's the "on the other hand". My concern is that as we shift more and more of the coding burden to the platform, to the AI, we'll understand less and less of how it all works. That means that when there's a bug (and there will be), or if the AI does something stupid (and it will), it will be all that much harder to dig into unfamiliar computer-generated code to find and fix the problem. 

I'm reminded of a favorite saying by Rumpelstiltskin, played by the inimitable Robert Carlyle on the ABC fantasy series "Once Upon a Time". When asked to do something magical to solve one problem or another, Rumpel would say, "All magic comes with a price, dearie." 

That's my ending thought for you as we look at all the AI support features that Google and other companies are unveiling for developers: "All magic comes with a price, dearie." 

AI magic is really cool, but let's make sure we don't let it reduce our ability to maintain and improve our own code. A force multiplier is no excuse for getting rusty, or introducing code that's not maintainable by humans. 

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
