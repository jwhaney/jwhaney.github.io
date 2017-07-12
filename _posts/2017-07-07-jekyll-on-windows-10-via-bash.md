---
layout: post
title: Jekyll on Windows 10 via Bash
date: 2017-07-07 10:30
author: john
categories: web-development
description: I came across this documentation on the official Jekyll site. I have not attempted this yet (my work machine is Windows 7 so I used another method - see my Installing Jekyll with Chocolatey post) but it sparked my interest and I intend to give it a go soon on a virtual machine when I have the time.
---

I came across this documentation on the official Jekyll site. I have not attempted this yet (my work machine is Windows 7 so I used another method - *see my Installing Jekyll with Chocolatey* post) but it sparked my interest and I intend to give it a go soon on a virtual machine when I have the time.

### Installing Jekyll
If you are using Windows 10 Anniversary Update, the easiest way to run Jekyll is by [installing](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide) the new Bash on Ubuntu on Windows. The installation guide seems pretty straight-forward, so follow the guidelines at that link before proceeding.

### Installation via Bash on Windows 10
***Note:*** You must have [Bash on Ubuntu on Windows](https://msdn.microsoft.com/en-us/commandline/wsl/about) enabled.

First make sure all our packages / repositories are up to date. Open a new Command Prompt instance, and type the following:

    bash

Your Command Prompt instance should now be a Bash instance. Now we must update our repo lists and packages.

    sudo apt-get update -y && sudo apt-get upgrade -y

Now we can install Ruby. To do this we will use a repository from [BrightBox](http://brightbox.com/ruby/ubuntu/), which hosts optimized versions of Ruby for Ubuntu.

    sudo apt-add-repository ppa:brightbox/ruby-ng
    sudo apt-get update
    sudo apt-get install ruby2.3 ruby2.3-dev build-essential

Next update our Ruby gems:

    sudo gem update

Now all that is left to do is install Jekyll.

    sudo gem install jekyll bundler

Check if Jekyll installed properly by running:

    jekyll -v

**And thats it!**

To start a new project named `my_blog`, just run:

    jekyll new my_blog

You can make sure time management is working properly by inspecting your `_posts` folder. You should see a markdown file with the current date in the filename.

**Note:** Bash on Ubuntu on Windows is still under development, so you may run into issues.
