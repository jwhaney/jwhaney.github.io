---
layout: post
title: Installing Jekyll with Chocolatey
date: 2017-07-10 12:05
author: john
categories: web-development
description: If you are on Windows 7 and want to install Jekyll, there are some hoops you have to jump through since Windows is not an officially supported platform. However, it is super simple to get up and running with Jekyll if you follow these instructions and install the package manager for Windows called Chocolatey.
---

If you are on Windows 7 and want to install Jekyll, there are some hoops you have to jump through since Windows is not an officially supported platform. However, it is super simple to get up and running with Jekyll if you follow these instructions and install the package manager for Windows called Chocolatey.

### Install the Chocolatey package manager
Access the instructions to install Chocolatey [here](https://chocolatey.org/install). I wanted to just use the regular command line, not the powershell, but it is basically the same process either way. Just copy and paste the command they provide in the install instructions into your command prompt and hit enter. You now have Chocolatey installed!

### Install Ruby via Chocolatey
In your command prompt (terminal) enter the following command and press Enter:

    choco install ruby -y

### Install Jekyll
Enter the following command prompt to install Jekyll:

    gem install jekyll

### *Note from official Jekyll documentation:*
Updates in the infrastructure of Ruby may cause SSL errors when attempting to use gem install with versions of the RubyGems package older than 2.6. (The RubyGems package installed via the Chocolatey tool is version 2.3) If you have installed an older version, you can update the RubyGems package using the directions [here](http://guides.rubygems.org/ssl-certificate-update/#installing-using-update-packages).

And thats it!
