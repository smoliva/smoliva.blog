---
title: Blogging with Hugo, Part 1
description: Getting started with open source web development tools.
date: 2021-04-25
categories:
  - "Open Source"
tags:
  - "Hugo"
---

In developing [my new blog](https://smoliva.blog), I opted to build a static website using [Hugo](https://gohugo.io) and other open source software tools, as opposed to using an all-in-one commercial service like Squarespace or WordPress. There are certain advantages to this DIY approach, as well as drawbacks. So in this series of posts, I'll walk through my thought process in deciding to use Hugo and explain the steps I took in building this blog "from scratch."

## Virtual Private Servers vs. "All-in-One" Web Hosting 

Generally speaking, you need at least two external services to build any website: A domain registrar and a web host. Many companies bundles theses services together. For example, I used to run a WordPress site, where the hosting included domain registration. These days, I prefer to keep things separate, as if you ever decide to leave the bundled service, it can be a chore to move or transfer your domain to another registrar.

[Hover](https://hover.com) is my domian registrar of choice. It currently hosts about a half-dozen domains that I use (or just park) for various projects. Hover has good pricing and an easy-to-use interface. The regular pricing for .com domains is $14.99, though for this blog I decided to splurge and buy a .blog domain for $29.99.

As for hosting, I use a virtual private server (VPS) run by [Linode](https://linode.com). Now, if you are not familiar with the concept of a VPS, here is a crash course: When you purchase a commercial hosting package, say from WordPress.com, you are restricted to using the software provided by the hosting company. You also do not have typically have access to the underlying server architecture, i.e. you cannot access the "backend" via a command line interface (CLI). Basically, all you get is access to a graphical front-end that allows you to modify the look and feel of your own website.

With a VPS, in contrast, you are basically renting blank space on a server to use as you see fit. A VPS normally comes with an operating system installed--usually, some form of Linux--but that's it. (Many commercial VPS providers, like Linode, do offer "one-click" installs of additional software packages, like WordPress). This means that you are responsible for all of the backend administration of the VPS, including making sure any software is kept up-to-date.

Overall, renting a VPS is cheaper and a better value than all-in-one commercial hosting. For instance, I pay $5 per month for the VPS that hosts this blog. For that $5, I get 25GB of storage and complete control over ths server. Compare this with an entry-level WordPress.com Personal managed hosting plan: For $7 per month (or $4 if you pay annually), you get just 6GB of storage. Now, the WordPress plan does include one year of domain registration. But you're obviously restricted to just using WordPress on the site--and that includes limitations on the themes you may use. Additionally, WordPress displays its own internal advertising on your blog unless you purchase a higher-tier plan.

## Coming Up in Part 2: Setting Up a VPS

Of course, when you purchased managed hosting, you do not have to do any of the legwork of setting up the server. This is not insignificant. Even having gone through the process several times in the past, it still took me a couple of hours to get the smoliva.blog VPS up and running. For the next post in this series, I will walk through how I did that.

