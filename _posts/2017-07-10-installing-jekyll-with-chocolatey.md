---
layout: post
title: Installing Jekyll with Chocolatey
date: 2017-07-10 12:05
categories: jekyll windows
description: If you are on Windows 7 and want to install Jekyll, follow these instructions to install the package manager for Windows called Chocolatey.
---

If you are on Windows 7 and want to install Jekyll, follow these instructions to install the package manager for Windows called Chocolatey.

### Install the Chocolatey package manager
Access the instructions to install Chocolatey [here](https://chocolatey.org/install).

### Install Ruby via Chocolatey
    choco install ruby -y

### Open command prompt and isntall Jekyll
    gem install jekyll

### *Note*
Updates in the infrastructure of Ruby may cause SSL errors when attempting to use gem install with versions of the RubyGems package older than 2.6. (The RubyGems package installed via the Chocolatey tool is version 2.3) If you have installed an older version, you can update the RubyGems package using the directions [here](http://guides.rubygems.org/ssl-certificate-update/#installing-using-update-packages).

And that's it!
