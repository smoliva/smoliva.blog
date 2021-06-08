---
title: Computer Chronicles Revisited, Part 9 — The VOTAN V5000 and the Speech Plus CallText
description: The Computer Chronicles discusses speech synthesis.
date: 2021-06-08
thumbnail: "img/cc-voice.png"
categories:
  - "Computer Chronicles Revisited"
tags:
  - "Stewart Cheifet"
  - "Herbert Lechner"
  - "Carl Berney"
  - "Rodney Stephens"
  - "David Murray"
  - "Stephen Hawking"
  - "John Medeiros"
  - "Speech Plus"
  - "VOTAN"
  
---

David Murray, who goes by [The 8-Bit Guy](https://www.youtube.com/channel/UC8uT9cgJorJPWu7ITLGo9Ww) on YouTube, had a great video a couple of years back on ["How Speech Synthesizers Work."](https://www.youtube.com/watch?v=XsMRxNSDccc&t=375s) He explained that early devices like the [Texas Instruments "Speak & Spell"](http://www.99er.net/spkspell.html) were not true speech synthesizers, as they relied on a limited vocabulary of pre-recorded words. But even in the mid-1980s there were speech synthesizers that could build words out of basic sounds.

Today's episode of *The Computer Chronicles* from early 1984 also examined the status of speech synthesis during this time period. In fact, Stewart Cheifet even displayed a smaller version of the Speak & Spell during the introduction. He also demonstrated the [Minolta AF-S V](https://petapixel.com/2017/01/12/minolta-af-s-v-talker-80s-camera-spoke/), a "talking" camera that could vocalize basic warning messages to the user, such as that lighting conditions were "too dark!" and the operator needed to "use flash!"

Cheifet was joined in the co-host's chair this week by Herbert Lechner of SRI International. With respect to the Minolta, Cheifet noted the talking feature wasn't strictly necessary; a blinking light worked fine for most cameras. So he asked Lechner if the use of speech in such devices was a "marketing gimmick" or if there were useful applications for speech in computers. Lechner replied that he found himself not paying attention to the warning lights in his car, yet he paid attention when it talked to him. And there were a number of voice terminals in use today that relied on telephone technology.

Cheifet then transitioned into our B-roll feature for the week, which provided an overview of the research into not just speech synthesis, but also digital speech and speech recognition. There was footage of a person operating an electron microscope. This device required total darkness to operate due to the machine's sensitivity to light. In addition, the operator's eyes and hands were kept continually busy simply dealing with the microscope. So the attached computer was trained to "respond to verbal commands encoded previously by the operator in his own voice." 

Cheifet said machines that could understand and carry out such verbal commands had been in development since the late 1960s. And even in the mid-1980s, the applications of such technologies were still limited. He said the "breakthrough" would come with the perfection of more recently developed speech systems that recognized context-sensitive rules of language and could mimic the more flexible patterns of actual human speech.

## Massaging the Phonemes

Carl Berney, a vice president with Speech Plus, Inc., joined Cheifet and Lechner for the next segment. Lechner opened the discussion by asking Berney to explain how a computer synthesized speech. Berney said his company's product--a Speech Plus CallText synthesizer connected to an [Epson HX-20](http://oldcomputers.net/hx-20.html) computer--could take any ASCII text and convert it into intelligible speech. The circuitry first looked at the words, decided which phonemes (the basic elements of speech) were in those words, and then put those phonemes together. The machine also "massaged" the words to make sure that they flow in the same way as natural speech. This was then converted to a set of parameters for the speech synthesizer, which produced the final speech.

Cheifet asked Berney to explain phonemes further. Berney said a phoneme was basically a "short sound." It was a fundamental element of language such that changing a phoneme would also change the meaning of a word. He said there were roughly 38 to 45 phonemes in the Englisgh language depending on which linguist you asked. Other languages had roughly the same number.

Lechner asked if the CallText covered the entire English language. Berney replied that it did. Lechner asked what type of computer was necessary for the speech synthesizer to work. Berney said the product was based on a commercially available 16-bit microcomputer.

Cheifet asked what would happen if you typed French words into the CallText. Berney said the device would attempt to pronounce the words, but they would not come out right, because French uses a different phoneme model than English. Cheifet said that meant the CallText was language dependent. Berney said that was correct, noting that it was not just the phonemes that differed between languages, but also the rules of pronunciation. The CallText contained pronunciation rules specific to English. This helped the final speech come out with a "reasonably natural inflection."

Cheifet asked for clarification on what it meant to "massage" the phonemes. Berney explained that when a person speaks, they did not normally articulate everything. For example, if you were giving directions and said, "Make a left turn at the corner," you might not clearly articulate "left" and "turn" separately; the words would probably run together. Put another way, some words are strung together in normal speech and some sounds are not spoken at all in certain words. There were rules for how to adjust a phoneme depending on which sound came first and which sounds came afterwards. It was therefore necessary to know when a sound appeared within a word (and a sentence) to get the proper inflection.

Lechner followed up, asking if the manipulation of the phonemes included volume and inflection. Berney said yes, the phoneme was not a fixed element. It needed to flow to another point depending on what sound came next.

Cheifet noted that during the introduction, he and Lechner described this technology in terms of "speech synthesis." But that was different than "speech coding." Could Berney explain the latter? Berney said the CallText did "synthesis by rule." The CallText did not use any pre-recorded or stored speech. Instead, it took written text and produced speech based on its understanding of the pronunciation rules of English. Other speech devices relied on "synthesis by analysis," where the information was recorded from a human voice and then compressed or processed by a computer so it could be stored and reconstructed later. These devices had "no knowledge of what the words were" and thus no idea about how they flowed together. It was essentially a "sophisticated tape recording process."

Berney then demonstrated the CallText on the HX-20. He had stored some text messages ahead of time, which the device played. Cheifet asked if it were possible for him to call up his computer remotely and have the CallText read back his electronic mail messages to him. Bernery said it could. The CallText could access "any text database over the telephone." Lechner asked how big was the market for such a feature. Berney replied it was a new application, and as of now there were no commercial online services that supported the CallText. However, Speech Plus was talking to "most of the major electronic mail suppliers" about potential adoption.

Cheifet then asked Berney to show the actual CallText product. Berney explained it was an expansion board that plugged into an IBM Persona Computer. The board had its own microprocessor and both a standard telephone interface and an [RS-232 serial port](https://en.wikipedia.org/wiki/RS-232). 

### An Early Voice Menu System

For the final segment, Rodney Stephens of VOTAN joined Cheifet, Lechner, and Berney. Stephens demonstrated the VOTAN V5000. This device could control a personal computer using voice recognition. Like the CallText, it connected to an IBM PC using an RS-232 connection. The included software package controlled a color monitor. 

Basically, the demonstration consisted of Stephens talking into a microphone and using simple verbal commands to navigate menus within a sample program that displayed sales figures for a company. Stephens also demonstrated an application that enabled the user to verbally access their brokerage account, check their portfolio, and even leave a voicemail message for their stockbroker.

Cheifet remarked the V5000's speech was so good, it was hard to believe that it was computer generated. Stephens said the V5000 relied on "analysis and coding" technology that was similar to that used by major telecommunications networks. The main difference was that those networks used 64,000 bits of speech per second to modulate digital speech, while the V5000 only used about 10,000 bits per second. This made his device more cost effective and feasible for use with a personal computer.

Lechner observed the V5000 relied on a pre-recorded and digitized vocabulary that was then sampled at 10,000 bits per second. Stephens said yes, the V5000 stored about 1,000 messages altogether that could be accessed by the included software, which could call out one message at a time. It was also possible to combine several messages together.

Lechner then asked about where "the state of the art" was with respect to speech recognition technology. Stephens replied there were several factors to consider. First, the V5000 relied on speaker-dependent recognition using discrete words. Speaker-independent recognition was a more difficult technology and it would offer a more limited vocabulary. Second, there was the problem of discrete versus continuous words. Stephens said we would not see speaker-independent recognition of continuous words anytime soon. Finally, there was the scale of the vocabulary. The technology for accomplishing unlimited vocabulary with speech recognition--something akin to what the CallText could do with speech synthesis now--was probably 2 to 4 years away.

## Hawking Makes the CallText Famous

I could not find much about VOTAN or its president, Rodney Stephens. The company existed from 1979 until 1991. And according to one source, the V5000 retailed for $5,000. 

As for Speech Plus, its CallText line of speech synthesizers became famous for its association with the late [Professor Stephen Hawking](https://www.youtube.com/watch?v=OH8s4N15zdg). In a 2015 article for [*Wired*](https://www.wired.com/2015/01/intel-gave-stephen-hawking-voice/), writer John Medeiros explained that when Hawking lost his ability to speak in 1985 after contracting pneumonia, he started using a computer program called Equalizer to type out words and commands, which were then synthesized into speech by a Speech Plus CallText card attached to an Apple II. The use of the American-produced card was why Hawking's famous digital voice carried an American accent. Speech Plus later gave Hawking an updated model--the CallText 5010--in 1988, but he asked to keep his "original" voice, as he'd become accustomed to it.

Medeiros noted that years later, one of Hawking's graduate assistants wanted to make a software-based version of the professor's voice so that they would not have to "rely on these old hardware cards" anymore. That required finding the original Speech Plus team. The company itself was long gone. Centigram Communications purchased Speech Plus in 1990. Centigram itself then went through several rounds of corporate acquisitions. Eventually, the graduate assistant managed to track down a backup take of Hawking's original synthesized voice at Nuance Communications. 

### Berney Makes His Mark with Software and Sculpture

[Carl Berney](https://www.linkedin.com/in/carl-berney-613169/), the Speech Plus executive who demonstrated the CallText on *Chronicles*, went on to have an interesting career both inside and outside of technology. Berney worked at Speech Plus, and later Centigram, for more than two decades. During his tenure, he managed the development of Voice Gateway, a widely used integrated telephone voicemail and response system. Since 2014, Berney has been involved in mobile software development, publishing the app [ShotPut](https://apps.apple.com/us/app/shotput-insulin-site-rotation/id916980792?mt=8), which helps diabetics rotate the sites of their insulin injections.

Berney has also had a prolific career as a stone carver. He owns and operates [Standing Stone Studios](http://www.standingstonesstudio.com/bio.html) in San Luis Obispo, California, where he produces artistic works based on marble, limestone, and alabaster. Berney also spent three years as a sculpture instructor with the [Poeh Cultural Center](https://poehcenter.org/) in New Mexico.

## Notes from the Random Access File

+ This episode is available on the [Internet Archive](https://archive.org/details/SpeechSy1984), which provides a date of April 9, 1984.
+ There was a *lot* of Herb Lechner in this episode, as he also presented a number of interstitial segments from the *Computer Chronicles Telecourse*.
+ Lechner mentioned his car talking to him. David Murray's video discussed this feature of early 1980s cars, which basically involved using a small phonograph to play short, prerecorded messages.
+ We will see Carl Berney again in at least one future *Chronicles* episode. 
+ The Epson HX-20 used for the CallText demonstration was itself a noteworthy device. It was widely considered the "first laptop computer." A Japanese import introduced to North America in late 1982, the HX-20 came with 16 kilobytes of onboard RAM (expandable to 32 KB), a 4-line LCD display, and two 8-bit Hitachi 6301 microprocessors that combined to provide basic 16-bit functionality. The machine also had a built-in dot matrix printer.
+ A sign of the pre-Internet age: Stewart Cheifet and other participants kept calling it "electronic mail" rather than "e-mail."
+ I almost managed to get through this entire post on speech synthesis technology without remarking how this episode's demo products probably work better than Siri. Almost.
