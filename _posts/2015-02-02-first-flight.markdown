---
layout: post
title:  "First Flight"
date:   2015-02-03 14:46:39
categories: bizleg
---
This is my first blog post on my new website. I will be using this page for two classes I am taking this semester, Humanitarian FOSS Development and Business & Legal Aspects of Free/Open Source Software. This is my first time taking a class like this, and I'm really excited to explore the world of Open Source Software. 

To start off my open source adventure, I wanted to try something new and create a website with open source software. I heard of Jekyll from a friend, so I wanted to try and set it up. I've never used a command line tool before and I'm have some experience using Github. I installed [iTerm][iterm] to use at my command line client, and I installed [Homebew][brew] which made it really easy to install Ruby and all of the Ruby Gems I needed. 

{% highlight bash %}
gem install jekyll
{% endhighlight %}

Boom. Look I'm a pro. It's really easy for me to run a local instance of Jekyll, just by going to the directory that my project is in and typing a quick command. 

{% highlight bash %}
jekyll serve
{% endhighlight %}

Now, whenever I want to create a new blog post, I just create a new markdown file with the date and the title as the file name and drag and drop it into the _posts folder. I can write all of my posts in markdown, which would also makes my life pretty easy.

On Github, I'm using my github.io page to host my webpage, so I just push my website to that repo and it automagically updates it for me. Bam. Beautiful, simple blog page. 


[brew]:        http://brew.sh/
[iterm]: 	   http://iterm.sourceforge.net/
