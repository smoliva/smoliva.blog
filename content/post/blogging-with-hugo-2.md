---
title: Blogging with Hugo, Part 2
description: Getting started with open source web development tools.
date: 2021-04-26
categories:
  - "Open Source"
tags:
  - "Linux"
  - "Hugo"
  - "Hover"
  - "Linode"
  - "Digital Ocean"
  - "Debian"
  - "SSH"
---

In [Part 1](https://www.smoliva.blog/post/blogging-with-hugo-1/), I explained my decision to go with Hover for domain registation and Linode for the virtual private server (VPS) I use for this blog. Now, I'll briefly review the process of setting up the VPS and getting it to work with my domain.

Obviously, I relied principally on documentation prepared by others. Specifically, I used how-tos published by both Linode and one of its competitors, Digital Ocean. I actually find the Digital Ocean documentation a bit easier to read and follow. At the end of this post, I provide resource links to the main pages I relied upon from both providers.

## Selecting a Linux Distribution and Creating an SSH Key

As I noted in my last post, when you setup a VPS, you're essentially starting with an operating system and not much else. Linode allows you to choose from among a number of pre-installed Linux distributions. I went with [Debian 10](https://www.debian.org/). This was a choice based mostly on prior experience. In the nine-plus years I've used Linux, I've mostly worked with Debian and Debian-based distributions like Ubuntu. And I know from that experience that Debian is a good choice for running servers.

During the Linode setup process, you must create a root account password. You also have the option of providing an SSH key. If you're not familiar with SSH, it is a program that allows you to remotely login to anoher machine--in this case, my VPS--over an encrypted conection. Back when I first started using computers in the early 1990s, web-based connections often relied on insecure protocols, such as [Gopher](https://www.sysnettechsolutions.com/en/what-is-gopher/) and FTP. SSH not only replaces these older technologies, it also makes it possible to access a remote server without the need to enter a password each time.

SSH does this by relying on a "key pair." Basically, you generate an SSH key on your local machine--in this case, my laptop running Linux Mint--that consists of a public and private key. (The specific command is simply ``ssh-keygen``, which is entered from a terminal.) The private key stays on my laptop. The public key can then be copied to a remote server, such as my VPS. When attempting to access a server over SSH, the public key on the remote machine is then matched up with the private key on the local machine.

As I said, Linode allows you to copy a public key onto a new VPS during the setup process. It is also possible to copy a public key over SSH to the VPS. And in fact, I ended up doing this for reasons I'll explain in a moment.

## Logging in and Linking My Domain

When you first create a VPS, Linode provides the IP address, which for this server is 23.239.8.81. Since the only user account established during creation is ``root``, I logged in from my local terminal using the command, ``ssh root@23.239.8.81``. At this point, I had not yet established the link between the VPS and the smoliva.blog domain I registered with Hover. 

There are two key steps to creating that link. First, I logged in to my Hover account and changed the default nameservers. The nameservers are what tell the domain registrar where you actually plan to use your domain. By default, Hover points its registered domain to it own namesevers. I changed that to point to Linode's nameservers.

The second step is then to create specific entries in Linode's system linking the ``smoliva.blog`` domain to the VPS at 23.239.8.81. Fortunately, this can be done with a 1-click install in Linode's graphical backend. Linode basically creates all of the entries so you don't need to mess around with it. I did, however, need to edit a configuration file, located at ``/etc/hosts`` on the VPS, to confirm that this IP and domain were linked.

During the initial login, you do need to provide the password created during the initial Linode setup. At this point, the VPS still accepts remote logins using a password. Relying on the guidance in the documentation, I immediately changed that default. 

## Securing the VPS

Next, I turned my attention towards securing the VPS. This can be boiled down to 3 steps:

1. Creating a new, non-root user, with SSH access
2. Disabling root login and password-based authentication 
3. Installing and configuring a firewall

It is always best practice to have a non-root user on a Linux-based server. The root account has access to everything on the machine. This means that if someone compromises the root account, they basically control your server. Even on a simple VPS running a public website like mine, that is an unncessary security risk.

So the basic idea is to create a second, non-root account. This account is still granted administrative privileges, which are invoked by the ``sudo`` command. For example, if I want to check for updated packages in Debian, I could do so from the non-root account by entering, ``sudo apt update``. (*Apt* is the Debian package manager.) The first time that you invoke sudo during a session, the system prompts you to enter the password for the non-root account. 

Once I created my non-root account, I then effectively cut off outside access to the root account by changing a couple of entries in the SSH configuration file, which is located at ``/etc/ssh/sshd_config``. First, I turned off root login. This means that nobody, including me, can access the root account from an outside machine. (Once you login through the non-root account, however, you can switch to the root account.) Second, I disabled password authentication. By doing this, the only way to login from the outside was with a valid SSH key pair.

Now, this also meant that I needed to ensure the non-root account had SSH access. So before I turned off passowrd authentication, I copied the public key from my Linux Mint laptop to the VPS using the command ``ssh-copy-id username@23.239.8.81``. (*Usermane* is a placeholder for the actual login of my non-root user, which I'm not disclosing for obvious reasons.)

The final step in the security process was to install a firewall. The standard firewall tool for Debian- and Ubuntu-based distributions is [ufw](https://help.ubuntu.com/community/UFW). This stands for "uncomplicated firewall," and I think that's an apt description. Again, if you are not sure what a firewall does, it is a piece of software or hardware that monitors network traffic and can block certain types of connections. 

In this case of my VPS, I wanted to block every type of connection except for SSH--which I need to remotely login--and the HTTP and HTTPS protocols for the blog itself. This was simple enough to accomplish. By default, ufw has SSH enabled. So I just needed to add access to HTTP and HTTPS, which is done by issuing the command ``sudo ufw allow in "WWW Full"``. 

## Installing the Web Server and Obtaining an SSL Certificate

Actually, I need to take a step back. Before enabling firewall access, I installed the web server. In the Linux world there are basically two commonly used web servers, Apache and Nginx. My understanding is that Nginx is considered the more modern and robust server. But just as I stuck with Debian because it is what I'm used to, I went with Apache for this blog as I simply have more experience using it.

Apache is not installed by default on the VPS, so I remedied that by entering ``sudo apt install apache2``. You'll know Apache is up and running if you go to your website and see a default homepage. If you plan to run more complex web content management systems, such as WordPress, you typically need to install additional software. But since I went with Hugo for this project, Apache was all that I needed. 

Well, there was one more thing. Although you can still run an old-fasshioned HTTP website, I prefer to have any site I run work with HTTPS. This means obtaining an SSL certificate. Like most people these days, I went with the free service from [LetsEncrypt](https://letsencrypt.org/), which is a nonprofit certificate authority. 

The LetsEncrypt process is largely automated. I needed to install one package, called the ``certbot``. Based on ths Digital Ocean documentation, however, the certbot package is not available through the Debian package manager. So instead I had to first install ``snapd``, which is the Snap packaging system developed by Canonical, the publishers of Ubuntu. After installing and setting up snapd, I then installed and ran certbot. This gave me an SSL certificate that needs to be renewed every 3 months.

## Coming Up in Part 3: Working with Hugo

In the next post, I'll "finally get to the fireworks factory" and start working on the actual blog itself. I'll go over Hugo, the software I use to create the blog and explain how I deploy and backup my content.

## Resources

+ [Getting Started with Linode](https://www.linode.com/docs/guides/getting-started/)
+ [Securing Your Server (Linode)](https://www.linode.com/docs/guides/securing-your-server/)
+ [How to Install the Apache Web Server on Debian 10 (Digital Ocean)](https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-debian-10)
+ [How to Secure Apache with Let's Encrypt on Debian 10 (Digital Ocean)](https://www.digitalocean.com/community/tutorials/how-to-secure-apache-with-let-s-encrypt-on-debian-10)
