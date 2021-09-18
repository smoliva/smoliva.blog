---
title: Blogging with Hugo, Part 3
description: Getting started with open source web development tools.
date: 2021-04-27
categories:
  - "Open Source"
tags:
  - "Hugo"
---

[My last post](https://www.smoliva.blog/post/blogging-with-hugo-2/) detailed the process of setting up the virtual private server (VPS) to host this blog. In this final post, I'll go into the mechanics of actually developing the blog using [Hugo](https://gohuo.io).

If you're not familiar with Hugo, it is software written in the Go language to function as a static website generator. *Static* means the entire website is generated at once, as opposed to a dynamic content management system like WordPress, which builds a particular page upon request from a database. The main reason I prefer to use static site generators is they do not require managing a database.

Hugo is under active development and releases frequent updates. As such, I opted not to install the version provided by my desktop distribution's package manager (Linunx Mint), which was about 14 releases behind the developers. Hugo does publish an official package through Canonical's snap system, but I don't use snaps on my local machine. So I simply downloaded the most recent .deb package directly from [Hugo's GitHub releases page](https://github.com/gohugoio/hugo/releases). 

## Working with Hugo Themes & Markdown

Hugo is a command line utility. It does not rely on any graphical user interface. To create this particular websiste, I started by going into my terminal and entering ``hugo new site smoliva.blog``. This created a folder in my home directory called `/smoliva.blog`. 

Inside this main website director there is a file called ``config.toml``. This is the key settings file used to control the website. For example, there are fields that set the title of the website, the base URL (e.g., smoliva.blog), and select the theme. 

By default, there are no themes installed. Hugo's website actually provides a [helpful directory of up-to-date themes](https://themes.gohugo.io/) developed by members of the community. Like Hugo itself, these themes are open source and free to use. I ended up selecting the [Mainroad](https://github.com/vimux/mainroad/) theme developed by Vimux. 

The easiest way to install a new theme is by using the [Git](https://git-scm.com/) utility. To install Mainroad, I went to the ``/smoliva.blog/themes`` folder and entered ``git clone https://github.com/vimux/mainroad``. This copied the current version of Mainroard directly from Vimux's GitHub repository. 

My next step was then to copy the sample files from the ``exampleSite`` subfolder in the Mainroad directory to the main ``/smoliva.blog`` directory. This included a sample ``config.toml`` file. It's a good idea to work off of the theme's sample configuration file, as each theme relies on slightly different fields and settings to work. 

For instance, you'll notice this blog has a sidebar, which contains separate widgets with links to my social media, recent posts, categories, and tags. These widgets can be modified or turned off in the ``config.toml`` file. Similarly, I customized the social media settings to add a link to my [Mastodon](https://mastodon.social/@smoliva) page, which is not one of the defaults provided by Mainroad.

As for the actual posts for this blog, they exist as individual [Markdown](https://daringfireball.net/projects/markdown/) files in the ``smoliva.blog/content/post`` subfolder. Each content page also has a header that contains some basic meta-information, including title, date, categories, and tags. I can even mark a post as a "draft" if I do not want to render it immediately.

When I'm read to preview the website, or any changes that I've made, I enter ``hugo serve`` in the website directory. This starts up an internal web server that I can access via my browswer at ``localhost:1313/``. This server is dynamic, so if I make and save any edits to an individual Markdown file, they will appear nearly instantaneously on the preview.

## Publishing the Blog

After I'm satisfied with my changes or additions, I simply type ``hugo`` to create the static website. The actual files are written to the ``/smoliva.blog/public`` subfolder. All that remains is to copy the contents of that subfolder to my VPS.

Back when I first developed static web pages over 10 years ago, I would use an FTP client to do this sort of transfer. But FTP is not secure. And as I explained in [Part 2](https://www.smoliva.blog/post/blogging-with-hugo-2/), there is a firewall installed on the VPS that blocks all outside connections that are not either SSH or HTTP/HTTPS. So even if I tried to use a FTP client, the VPS would block it.

This leaves me with transferring the files over an SSH connection. The tool I use for this is [rsync](https://rsync.samba.org/). This utility, as you might have guessed, syncs the contents of two folders. In this case, each time I want to update this blog, I enter ``rsync -avz -e ssh public/ username@smoliva.blog:/var/www/smoliva.blog``, with *username* representing the non-root user I created on the VPS (and which I obviously will not disclose here). Since most of the files that make up this blog are simple text, the sync process only takes a few seconds.

