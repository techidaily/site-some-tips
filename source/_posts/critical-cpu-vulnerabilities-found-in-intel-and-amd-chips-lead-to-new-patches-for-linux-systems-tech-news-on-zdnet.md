---
title: Critical CPU Vulnerabilities Found in Intel and AMD Chips Lead to New Patches for Linux Systems | Tech News on ZDNet
date: 2024-09-19 15:43:27
updated: 2024-09-20 10:29:57
tags:
  - cloud
categories:
  - tech
thumbnail: https://www.zdnet.com/topic/cloud/    https://www.zdnet.com/a/img/resize/51145981afa00deb9d3fc2dad425716f71e5523d/2023/08/10/a237ed07-d113-4519-86bd-956dc030e76d/penguin-gettyimages-1473514702.jpg?width=170&height=96&fit=crop&auto=webp
---

## Critical CPU Vulnerabilities Found in Intel and AMD Chips Lead to New Patches for Linux Systems | Tech News on ZDNet

![penguin-gettyimages-1473514702](https://www.zdnet.com/a/img/resize/85c723141a0f13d36023f9e495157d6a6a6d339f/2023/08/10/a237ed07-d113-4519-86bd-956dc030e76d/penguin-gettyimages-1473514702.jpg?auto=webp&width=1280)

Dimitrios Manias/Getty Images

It's not really a Linux problem, but as is so often the case, Linux kernel developers have to clean up after AMD and Intel. It happened again with the chipmakers' latest CPU vulnerabilities: AMD [Inception](https://www.amd.com/en/resources/product-security/bulletin/amd-sb-7005.html) and Intel [Downfall](https://downfall.page/). To fix these, Linux creator [Linus Torvalds has released a new set of patches.](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=138bcddb86d8a4f842e4ed6f0585abc9b1a764ff)

Oddly, both are speculative side-channel attacks, which can lead to privileged data leakage to unprivileged processes. Torvalds described them as "yet another issue where userspace poisons a microarchitectural structure which can then be used to leak privileged information through a side channel."

**Also:** [**How to choose the right Linux desktop distribution for you**](https://www.zdnet.com/article/how-to-choose-the-right-linux-desktop-distribution-for-you/)

Does that sound familiar? It will be to Linux security experts. Yes, it's yet another example of the kind of security vulnerabilities that made [Intel's Meltdown and Spectre infamous in Linux circles](https://www.zdnet.com/article/how-linux-is-dealing-with-meltdown-and-spectre/). Fortunately, unlike those two earlier cases, developers this time knew well in advance that there was trouble with the silicon, so the patches came out before news of the latest holes appeared. 

In this recent merge, Torvalds and company incorporated kernel-side measures that counteract AMD's Speculative Return Address Stack (RAS) overflow vulnerability to its Zen 3 and Zen 4 architectures**.** This vulnerability allows userspace to contaminate a microarchitectural structure, which can subsequently be exploited to siphon privileged information via a side channel. 

#### Newsletters

ZDNET Tech Today

ZDNET's Tech Today newsletter is a daily briefing of the newest, most talked about stories, five days a week.

 Subscribe

[See all](https://www.zdnet.com/newsletters/)

AMD will tell you it's not that big a deal: The chip giant believes this vulnerability is only _potentially_ exploitable locally, such as via downloaded malware. Nevertheless, AMD "recommends customers employ security best practices, including running up-to-date software and malware detection tools."

However, the [ETH Zurich](https://css.ethz.ch/en/) security researchers who found the flaw aren't so optimistic. They believe Inception could be used by an attacker in cloud computing, where customers commonly share the same processing hardware resources.

The researchers say that [Inception is a new class of transient execution attacks](https://comsec.ethz.ch/research/microarch/inception/) that uses Training in Transient Execution (TTE). Instead of attempting to leak data in a transient window, TTE attacks abuse the transient window to insert new predictions into the branch predictor. Combined with the Phantom, which is a way of triggering transient windows from arbitrary instructions, Inception can be a nasty way to vacuum down private data. 

**Also:** [**If you're looking to up your desktop computer security, Linux might be your best bet**](https://www.zdnet.com/article/if-youre-looking-to-up-your-desktop-computer-security-linux-might-be-your-best-bet/)

Amusingly, veteran Linux kernel developer [Peter Zijlstra, who is affiliated with Intel, refined the AMD patches](https://lore.kernel.org/lkml/20230809071218.000335006@infradead.org/T/#m67fc62b9e46b5fadf1876dcd142604a443a64e1b). It's somewhat ironic to witness an Intel engineer spearheading the kernel's refinement of AMD mitigation code. Welcome to the open-source community spirit!

The Linux kernel developers also addressed the Intel Gather Data Sampling (GDS) vulnerability, known as Downfall. This [particular vulnerability affects Intel Core processors](https://www.intel.com/content/www/us/en/developer/topic-technology/software-security-guidance/processors-affected-consolidated-product-cpu-model.html) from the 6th-generation Skylake to the 11th-generation Tiger Lake. In short, chances are your PC, your servers, and your cloud processors are all vulnerable. 

According to Daniel Moghimi, the Google senior research scientist who discovered Downfall, "The vulnerability is caused by memory optimization features in Intel processors that unintentionally reveal internal hardware registers to software. This allows untrusted software to access data stored by other programs, which should not normally be accessible." 

So, how bad is it? Moghimi has shown that an exploit can be used to steal another user's security keys and passwords. Worst still, such attacks are "Highly practical," Moghimi notes. "It took me two weeks to develop an end-to-end attack stealing encryption keys from OpenSSL. It only requires the attacker and victim to share the same physical processor core, which frequently happens on modern-day computers, implementing preemptive multitasking and simultaneous multithreading."

**Also:** [**AMD vs Intel: Which desktop processor is right for you?**](https://www.zdnet.com/article/amd-vs-intel-which-desktop-processor-is-right-for-you/)

[Intel Software Guard Extensions (SGX)](https://www.intel.com/content/www/us/en/architecture-and-technology/software-guard-extensions.html), an Intel hardware security feature available on Intel CPUs to protect users' data against malicious software, is also helpless against this vulnerability.

For some users, the fix may seem more trouble than the problem. According to Intel, some workloads may experience up to 50% overhead. That's some slowdown! Moghimi warns, however, "This is a bad idea. Even if your workload does not use vector instructions, modern CPUs rely on vector registers to optimize common operations, such as copying memory and switching register content." 

For Linux, however, the slowdown may not be that bad. Michael Larabel, a Linux software engineer and editor-in-chief of the hardcore Linux site [Phoronix](https://www.phoronix.com/), has [benchmarked the Downfall patches](https://www.phoronix.com/review/intel-downfall-benchmarks). Larabel found that instead of impacting I/O or user-space and kernel interactions -- as the fixes for Meltdown, Spectre, and their relatives did -- Downfall's fix impairs user-space bound software only. He also found that while the performance hit tended to be not as bad as Intel predicted, there were still some significant slowdowns.

The Linux security patches have been incorporated into the Linux Git for the upcoming Linux 6.5 kernel. The latest stable point releases incorporating these patches include Linux versions 6.4.9, 6.1.44, 5.15.125, 5.10.189, 4.19.290, and 4.14.321\. These releases encompass the current Linux 6.4 stable series and the supported Long-Term Support (LTS) series kernels. 

**Also:** [**The best all-in-one computers: Mac, Lenovo, and more compared**](https://www.zdnet.com/article/best-all-in-one-computer/)

The patches facilitate the reporting of the CPU speculative execution vulnerabilities state and introduce new controls to modify their behavior in conjunction with the latest CPU microcode. Of course, for these patches to work, you must also install the AMD and Intel microcode updates.

So, what should you do? Get ready to install the new microcode as soon as it's available. Then, follow up, by patching your Linux systems as the patches become available. This won't be a big deal for Linux desktop users, but it will be for those of you running Linux on your servers and clouds. 

#### See also

[How to replace Windows with Linux Mint on your PC](https://www.zdnet.com/article/how-to-replace-windows-with-linux-mint-on-your-pc/ "How to replace Windows with Linux Mint on your PC")

[5 best Linux commands for troubleshooting problems (and how I use them)](https://www.zdnet.com/article/5-best-linux-commands-for-troubleshooting-problems-and-how-i-use-them/ "5 best Linux commands for troubleshooting problems (and how I use them)")

[5 reasons why Pop!\_OS is this Linux pro's favorite distro](https://www.zdnet.com/article/5-reasons-why-pop-os-is-this-linux-pros-favorite-distro/ "5 reasons why Pop!_OS is this Linux pro's favorite distro")

[5 best open-source email clients for Linux (and why Geary is my go-to)](https://www.zdnet.com/article/5-best-open-source-email-clients-for-linux-and-why-geary-is-my-go-to/ "5 best open-source email clients for Linux (and why Geary is my go-to)")

* [How to replace Windows with Linux Mint on your PC](https://www.zdnet.com/article/how-to-replace-windows-with-linux-mint-on-your-pc/ "How to replace Windows with Linux Mint on your PC")
* [5 best Linux commands for troubleshooting problems (and how I use them)](https://www.zdnet.com/article/5-best-linux-commands-for-troubleshooting-problems-and-how-i-use-them/ "5 best Linux commands for troubleshooting problems (and how I use them)")
* [5 reasons why Pop!\_OS is this Linux pro's favorite distro](https://www.zdnet.com/article/5-reasons-why-pop-os-is-this-linux-pros-favorite-distro/ "5 reasons why Pop!_OS is this Linux pro's favorite distro")
* [5 best open-source email clients for Linux (and why Geary is my go-to)](https://www.zdnet.com/article/5-best-open-source-email-clients-for-linux-and-why-geary-is-my-go-to/ "5 best open-source email clients for Linux (and why Geary is my go-to)")

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
