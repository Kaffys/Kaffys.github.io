---
layout: page-fullwidth
title: "Google Chrome - Stopping support for NPAPI plugins"
teaser: "What does this mean for games like RuneScape?"
header:
    image_fullwidth: "chrome.png"
image:
    homepage: chrome.png
categories:
    - design
comments: true
show_meta: false
---

One of my favorite games growing up was RuneScape. I would spend hours running around completing quests and exploring the vast and ever changing world. In the 10+ years that RuneScape has been around, you have been able to play the game right from your browser. No downloads. The game was programmed in Java, which back in 2001 when it was originally released, was awesome. But with the web technologies growing, Java isn't a viable option anymore. It's harder to run in a browser, and the performance isn't getting better. Even today, RuneScape is still mostly written and ran in using Java. Today, that leaves companies like Jagex, the company that develops and supports RuneScape, in a bit of a pickle. 

Slowly, browsers are starting to phase out Java support by default, starting with Google Chrome. In September 2013, [Chrome announced][goodbye] that it will be dropping support for the Netscape Plugin Application Programming Interface, or "NPAPI". NPAPI works by a plugin saying "Hey I handle this type of data!". NPAPI then streams that data to the plugin, and then the plugin is responsible for processing and rendering the data for the user. 

Chrome version 42 is [launching in April 2015][april], and with that NPAPI support will be discontinued and any NPAPI plugins will be unpublished. Some of the plugins that will be affected are:

- SilverLight
- Unity
- Google Earth
- Java
- Google talk
- Facebook Video

So games like RuneScape will no longer be supported in Chrome. Which I think is kind of funny, considering [Jagex teamed up with Google ][teamed] in December 2011 to make sure the game would run on their browser. #oops

Jagex is exploring other platforms for their game engine. In 2013, Jagex released an HTML5 Beta, which has made significant progress with performance, but not so much graphically. And even then, it is still limited. Right now, [Jagex is developing an engine in C++][c], so that they can target multiple platforms and have a better performance for their users. 

[goodbye]: http://blog.chromium.org/2013/09/saying-goodbye-to-our-old-friend-npapi.html
[april]: https://www.chromium.org/developers/npapi-deprecation
[teamed]: http://services.runescape.com/m=news/exclusive-goggles-only-in-chrome
[c]: http://services.runescape.com/m=forum/forums.ws?198,199,113,65596566