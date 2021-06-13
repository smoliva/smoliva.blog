---
title: Computer Chronicles Revisited, Part 10 — The Sytek LocalNet
description: The Computer Chronicles discusses local area networks.
date: 2021-06-12
thumbnail: "img/cc-sytek.png"
categories:
  - "Computer Chronicles Revisited"
tags:
  - "Stewart Cheifet"
  - "Gary Kildall"
  - "Charlie Bass"
  - "Michael Pliner"
  - "Phil Edholm"
  - "John Couch"
  - "John Cavalier"
  - "James Pelkey"
  - "Sytek"
  - "Ungermann-Bass"
  - "IBM"
  - "CompuServe"
  - "Atari"
  - "Zilog"

---

Today, we think of networking as synonymous with the Internet--a global interconnected network that encompasses not just computers but also millions of "smart" devices. But in this episode of *The Computer Chronicles* from late 1983, the focus was on *local area networking* or LANs. Stewart Cheifet and Gary Kildall talked with representatives from two companies that were at the forefront of developing the still-emerging standards for computer networking.

Cheifet opened by asking Kildall to define a local area network. Kildall noted that ever since we'd had computers, people had beeen trying to hook them up to transmit data back and forth between them. LANs were generally used in office environments and limited to a relatively small geographic area. This limited area allowed for better performance relative to more traditional network systems.

Cheifet then narrated our B-roll for the episode. He explained that the "countertop" computers--i.e., terminals--typical of modern offices had a built-in limitation: They could only talk to a central computer linking it and other terminals to one body of data. Networking was a relatively new field that allowed an organization or community to connect its various branches into an integrated, decentralized resource. At Stanford University's central computer facility, for example, a library network gave researchers instant access to material stored all over the country. Individual campus terminals could tap into the system through a yellow cable that "snakes through the campus like a subway line." Although a LAN can operate along traditional telephone wires, known as [twisted pairs](https://audiouniversityonline.com/twisted-pairs/), Cheifet noted that newer single-cable systems like *baseband* and *broadband* offered more flexibility, a greater data rate, and could bring the tangle of cables and wires "almost under control." 

Cheifet noted there were a number of ways that information could be shared within a network: Along the arms of a star, around a ring, or through a BUS. Messages traveling on the network could receive automatic priority or use travel-like "tokens" to get from one station to another. But the real advantage of this system was for the user, whose access to multiple sources of information became easier and faster.

### Broadband vs. Baseband

Dr. Charlie Bass and Dr. Michael Pliner joined Cheifet and Kildall for the next segment. Kildall asked Bass, the vice president of Ungermann-Bass, Inc., to explain the characteristics of a LAN. Bass replied that a LAN involved "total connectivity" between devices and "peer-to-peer relationships," meaning the goal was to get rid of the central computer entirely, thus allowing individual devices to talk freely among themselves.

Kildall asked about the types of networking applications used in office environments with smaller computers. Bass said the main goal was to share resources and information, so that a single terminal can talk to more than one computer, and a user could share resources they might not ordinarily be able to afford. Pliner, the president of Sytek, Inc., added that LANs were now common in office automation environments. For instance, they were used on manufacturing floors to collect and transfer data back to an operations center. LANs were also used for general communications utilities. Indeed, the network itself was now becoming a utility much like electricity. Newer broadband networks could even provide video, voice, and data on the same cable system.

Kildall asked about the differences between broadband and baseband technologies. Pliner said the distinguishing feature was the modulation technique. In a baseband system, you directly modulated the cable with electrical signals. In a broadband system, you are essentially using the same technology that distributes cable television into homes. It uses an RF-modulation technique or [frequency division multiplexing](https://www.tutorialspoint.com/frequency-division-multiplexing), i.e. stacking different channels of data, information, or video that run along the same cable simultaneously.

Kildall asked about the data-transfer rates of these networking technologies. Pliner said it ranged from around 9.2 kb/s to Ethernet-type networks that could get up to 10 MB/s. And newer technologies like broadband and fiber-optics could get even faster.

Cheifet asked how decisions were made regarding which networking technology was best for a particular application. Bass said that much of the media discussion over "broadband vs. baseband" was missing the point. Most people now realized that both technologies had their strengths and applications and would continue to co-exist. This would not be a case where one technology killed off or dominated the other to its exclusion. That said, choosing between the two was difficult. It was a matter of application, cost, and efficiency. Baseband offered simplicity, which resulted in savings not just in terms of cost, but also installation and maintenance times. Broadband was more complex and costly, but if you needed the ability to transfer something other than a simple data stream, that was the only way to go.

Kildall asked about the software issues related to LANs. Did they require a lot of specialized software to operate? And were operating systems doing enough to support networking? Bass said there was an entire body specialized software used for networking, which were known as *protocols*. This software was necessary for most existing computer systems, as they were built "without any knowledge of the network." Over time, Bass said he expected you would start to see these protocols permeate the operating systems themselves. That is, future operating systems would be built with the assumption that a network existed. This would allow for networking to incorporate more applications and become more powerful.

Pliner agreed with Bass that as things stood now, the LAN vendor still had to take a lot of the software and "move it into" the computer. He pointed to Sytek's networking devices, which included its own microprocessor as well as a "significant amount" of communications software. In the future, you would likely see specialized software on individual host machines to provide networking applications such as distributed process, file sharing, and electronic mail.

Cheifet asked about the problem of technical standards in LANs. Was it possible to link hardware and operating systems from different vendors? Pliner said it was possible. Both he and Bass' companies produced networking equipment that relied on [RS-232](https://www.codrey.com/embedded-systems/rs232-serial-communication) connections. This allowed for the interconnection of multiple vendors' equipment at the cost of some limits in performance and function. Pliner said the Institute of Electrical and Electronics Engineers (IEEE) was currently developing future networking standards with the participation of both Sytek and Ungermann-Bass.

Kildall followed up by asking about the importance of standards. Did a standard really matter if you have a LAN that was self-contained in one geographic area? Bass said standards activity was driven by the need to interconnect different devices. The more commonly accepted a standard, the simpler that would be. But since the standards process had to start from scratch, the first step was looking for the "lowest common denominator," which in this case was RS-232. It wasn't ideal for networking, he said, but it existed and was a well-established standard. 

Bass added that right now, much of the standards discussion was focused on very low-level issues, such as the types of cables that should be used for LANs. Once those issues were resolved, standards bodies could focus on higher-level problems. And while the process began with the hopes of a single standard emerging, we would probably end up with a few different standards and need to develop gateways to bridge the gap between them.

### A Step Towards Transparency

For the final segment, Sytek engineer Phil Edholm demonstrated the company's LocalNet product line. The first demonstration involved a terminal connected to a small prototype network. As Pliner explained earlier, the LocalNet had its own procesor, memory, and software that enabled networking over a cable. Edholm noted this technology could be used to support "thousands of terminals" on a single cable.

Edholm also demonstrated how the LocalNet could be connected directly to an IBM Personal Computer. He connected a demo PC to the LAN and download a file using a local terminal simulation program. Edholm also showed that the same networking cable could carry a video signal--in this case the live feed from the *Chronicles* taping--to a [Sony Watchman](https://en.wikipedia.org/wiki/Sony_Watchman).

Kildall asked if LANs were limited to file transfers, or could they be used to distribute an entire operating system over the network? Put another way, could a local computer simply access the files remotely without downloading them first? Edholm said that the network communicated with the IBM PC as if it were a terminal. The PC had to initiate the file transfer using a small piece of locally installed software. But, Kildall said, in the long term this operation would become completely [transparent](https://en.wikipedia.org/wiki/Transparency_(telecommunication)). Edholm said yes, that was the goal. Charlie Bass added that with transparency, the commands the user saw would be natural and that they would have "no idea" where the resource was. The file transfer would take place behind the scenes and not because the user explicitly requested it. And such transparency would come with the next generation of devices that included built-in networking capabilities.

Kildall returned to the discussion of standards. He noted that Xerox, Intel, and Digital Equipment Corporation had proposed a networking standard called Ethernet. What was the status of that proposal? Bass said in some terms it was already "very successful." A number of companies had endorsed Ethernet and were making equipment based on that standard. That said, Ethernet was not an end-all in itself. It represented a basic technology. But it was not the only technology available, as there were alternatives such as broadband, which Sytek used. 

Bass noted that the problem with standardization up to this point was that everyone was looking for something that would solve all of the problems and they didn't find it. It was similar to the search for a "universal computer"--there wasn't one and we probably would not be happy with it if it existed. Pliner ended the discussion, and the episode, by noting there was a danger that if the industry adopted a networking standard too early, there was the danger of picking the wrong technology. And in any event, the real question going forward was, "What will IBM do?" 

### "Now That's Networking!"

This episode was followed by a Random Access segment hosted by Stewart Cheifet, which dates this program sometime in October 1983.

+ C.D. Anderson, a discount stockbroker, announced plans to publish the "first home brokerage computer system" that would cost $300. [Charles Schwab](https://www.washingtonpost.com/archive/business/1984/11/25/full-automation-near-in-securities-trading/81539d82-4723-40d7-ad52-af909e90f158/) said it would introduce its own software sometime in 1984.
+ A new survey found that 86 percent of U.S. high schools had at least one personal computer available for student use; that figure was 61 percent for elementary schools. Cheifet noted that some educational experts said it was a "waste of time to teach kids programming." Another research firm estimated it would cost $4.5 billion to equip all U.S. schools with computers.
+ Another study, this one from Stanford University, suggested boys were more interested than girls in computers. The study noted the vast majority of students enrolled in computer camps were boys, as was the case with computer ownership and computer game purchases. Cheifet said that could "create real problems for women in the workplace of the future."
+ IBM and Hitachi [settled their lawsuit](https://www.nytimes.com/1983/10/07/business/hitachi-ltd-and-ibm-settle-case.html) over the latter allegedly stealing the former's trade secrets. Hitachi agreed to return and not use the stolen information, and to disclose the names of the people who offered to sell the trade secrets in the first place.
+ AT&T announced the sale of a $70 million computer software system to Nippon, the Japanese telephone company. Nippon also planed to buy a $12 million [Cray supercomputer](https://simpsonspics-blog-blog.tumblr.com/post/107469683953/burns-you-call-this-a-supercomputer) to run the software.
+ In Silicon Valley news, [John Couch left Apple](https://www.smoliva.blog/post/computer-chronicles-revisited-002-apple-lisa-vs-visi-on/) after running the company's Lisa division. But Apple gained another executive, [luring John Cavalier away from Atari](https://www.nytimes.com/1983/10/11/business/business-people-head-of-atari-unit-is-hired-by-apple.html).
+ The publishing industry said there were now more than 2,000 computer how-to books in print. Cheifet said that computer books now outsold all other business-related books--a growth matched only by romance novels. In addition, there were now 72 computer magazines on the market, which was remarkable given this market did not exist just six year ago.
+ Cheifet gave a rundown of the week's top-selling computer games: *Zaxxon*, *Wizardry*, *Microsoft Flight Simulator*, *Pinball Construction Set*, and *Zork One*.
+ Finally, Cheifet relayed the story of what may have been the first successful online romance. Two [CompuServe](https://en.wikipedia.org/wiki/CompuServe) users, known as "SweetLady" and "MrMike", met in the service's CB channel. Cheifet said the couple recently got married on CompuServe with 70 guests logged in. Cheifet added, "Now that's networking!" 

## IBM Adopted--Then Abandoned--Sytek

Let's start with the answer to Michael Pliner's question, "What will IBM do?" As it turned out, IBM went with Charlie Bass' Sytek. In 1984, IBM released its first LAN system, the [IBM PC Network](https://www-01.ibm.com/common/ssi/ShowDoc.wss?docURL=/common/ssi/rep_ca/0/897/ENUS184-100/index.html&lang=en&request_locale=en), which was built on Sytek's broadband protocols. 

But let's back up a bit and talk about the background of Pliner and Sytek. Pliner earned a doctorate in computer science and began his career in the early 1970s with the National Security Agency. In 1975, he joined Ford Aerospace in California to work on software development. During his time at Ford, Pliner met four other individuals and together the five of them became the founders of Sytek.

In an interview with [James Pelkey](http://www.historyofcomputercommunications.info/About/JimPelkey.html), Pliner explained that Sytek was 
originally founded as a technology consulting firm, not a networking company. Their first contract was to write protocols for Xerox's X10 telecommunications network. 

During their early consulting work, Pliner said he began to hear talk about LANs, and broadband technology in particular. Around 1980, Pliner said Sytek decided to take its consulting money--about $300,000 at that point--and reinvest it into developing broadband. Sytek's initially focued on selling broadband networks to large college campuses. [Pliner told Pelkey](http://www.historyofcomputercommunications.info/Book/10/10.5-Sytek.html) that after a talk at Brown University in 1983, IBM representatives approached him about adopting Sytek's broadband to build "metropolitan" networks of IBM Personal Computers. This eventually led IBM to "re-engineer" the Sytek LocalNet into the original IBM PC LAN. 

In September 1984, IBM purchased approximately 5 percent of Sytek for $6 million. But IBM also quickly abandoned Sytek and broadband in favor favor of another technology called [token ring](https://en.wikipedia.org/wiki/Token_Ring) networking. By the end of 1985, Sytek was "fifth in sales among LAN vendors," according to Pelkey. Sytek's plans for an initial public offering fizzled. The company failed to post any profit until 1988, and it was [sold to Hughes Aircraft](https://techmonitor.ai/technology/hughes_aircraft_to_acquire_local_net_maker_sytek), a subsidiary of General Motors, in 1989, and re-branded as Hughes LAN Systems. This subsidiary was in turn sold to Whittaker Communications in 1995.

Michael Pliner left Sytek in 1987. A year later, he founded Verity, a software company that focused on document search and distribution. He served as Verity's CEO until 1993 before moving over to [KLA-Tencor](https://www.kla-tencor.com/) as vice president and general manager of its software division. In 1997, Pliner founded Vuent, which developed 3-D streaming models for the Internet. After selling Vuent in 2000, Pliner went on to serve as interim CEO for three different companies before founding yet another startup, FusionSeven, in 2011, which provided financial services software-as-a-service. 

The other Sytek employee featured in this episode, engineer [Phil Edholm](https://twitter.com/PEdholm), continues to work in the industry as a [communications and networking consultant](http://www.pkeconsulting.com/). Edholm remained with Sytek through its acquisition by Hughes. He left the company in 1991. In 1995, he joined Nortel Networks, eventually rising to become chief technology officers of its enterprise business before departing in 2009. 

### UB Struggled to Market Vendor-Independent LAN

Ungermann-Bass--also known as UB--was started by Ralph Ungermann and Charlie Bass. Both men previously worked at [Zilog](http://www.zilog.com/), which famously developed the Z80 microprocessor used in many 8-bit computers of the 1980s. According to James Pelkey, Ungermann was "forced out" at Zilog and decided to start a LAN company. He recruited Bass and other disgruntled Zilog employees to form UB in 1979. 

While Sytek focused on broadband-based LANs, UB's specialty was Ethernet. As Bass alluded to during his *Chronicles* segments, Ethernet did become an industry standard, specifically the [IEEE 802.3](https://en.wikipedia.org/wiki/IEEE_802.3) standard that is still in use today. Bass had led the charge for Ethernet at UB and he decided to base the company's early networking products on the Z80, which he was obviously quite familiar with from his Zilog days. 

During the 1980s, UB adopted other networking technologies, including broadband and token ring, in an attempt to cement its position as a "vendor-independent" LAN company. Unlike its rival Sytek, UB managed to go public in June 1983. But the company was never very profitable, and following the October 1987 stock market crash, Ungermann went looking for a buyer, which he found in Tandem Computers. Tandem formally acquired UB in February 1988 for $260 million, with Ungermann staying on as a vice president. Tandem was later acquired by Compaq in 1997.

There's limited information on Charlie Bass' post-UB career. Like many former Silicon Valley executives, he formed a venture capital firm, Bass Associates, in the late 1980s. He co-founded at least two other companies, Starlight Networks (a 1990s streaming media software developer) and [Socket Mobile](https://www.socketmobile.com/), which is still in business today. Bass also spent a number of years as a consulting professor of electrical engineering at Stanford. 

## Notes from the Random Access File

+ This episode was recorded on September 26, 1983, although it aired sometime in October based on the "Random Access" segment.
+ You can watch this episode at the [Internet Archive](https://archive.org/details/Networki1984).
+ It's never made clear exactly which Sytek device is used in Edholm's demo. Based on the available [product brochures](http://bitsavers.org/pdf/sytek/brochures/) from the time, my guess is it was the [LocalNet 20/100 Z01 Option](http://bitsavers.org/pdf/sytek/brochures/LocalNet_20_100_Z01_Secure_Packet_Communications_Unit_Brochure_Apr83.pdf). 
+ When Charlie Bass referred to RS-232 as a "well-established standard," he wasn't kidding. The original RS-232 standard was introduced in 1960, so it was well over 20 years old when this *Chronicles* episode taped. 
+ Stewart Cheifet mentioned AT&T's sale of software systems to its Japanese counterpart, Nippon. In an interesting historical footnote, AT&T controlled Japan's telephone network during the post-World War II occupation until it was turned over to the state-created monopoly Nippon in 1952. 