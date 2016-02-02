---
title: Blog post tagging in Jekyll
layout: post
tags: Jekyll
---

As I work on getting the new Jekyll site up and running, one of my primary concerns is tagging.  If I want to cover a wide variety of topics and do so for an expended period of time, I really need to organize everything to make it easy to consume years down the road.

<!--excerpt-->

Most dynamic CMS packages have tagging set up out of the box. Jekyll "supports" tag functionality, but because it requires the user to do all the heavy lifting, it's up to me to *implement* the tags.

Luckily, I'm not trailblazing by any stretch of the imagination.  I was able to find a variety of Jekyll tagging solutions online, but not all of them fit my use case. Many of the use cases I found simply extended Jekyll locally and pushed the new static HTML and Markdown pages to GitHub. Jekyll is written in ruby- which became a lot harder to play around with in OSX El Capitan [thanks to Apple's System Integrity Protection](https://en.wikipedia.org/wiki/System_Integrity_Protection). I wanted a solution that would be natively supported by GitHub Pages so I could hack away at my site from any web browser and let GH-pages do the building.

Developer Brandon Parsons [wrote a blog post about a year ago](https://blog.brandonparsons.me/2015-using-tags-in-a-jekyll-blog-on-github-pages/) tackling this very issue, from which I have borrowed liberally. Tags should be live soon!
