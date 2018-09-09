---
layout: post
title: Web Scraping Revisited
tags: music pitchfork python scraping
---

Two years ago I took a [first stab at scraping Pitchfork reviews](http://www.rgreasons.net/2016/06/25/Scraping.html). Shortly afterward, I flung myself into a new position as pitchfork kept posting new reviews. I knew that at some point I wanted to revisit the data to attempt to try out some new ideas, but I also never got over the fragility of my initial implementaion.

As I referenced in my original blog post, the folks over at NPR had a pretty cool "just robust enough" [solution for web scraping](http://blog.apps.npr.org/2016/06/17/scraping-tips.html). They used the [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/) library just as I did, but their scraper design was more pythonic and they used some additonal tools to scale out the scraping. I used their methodology as a jumping-off point for my refactor. 

When I sat down this week to update my implementation, I made a point to hit on three big things:
* **Gracefully handle 404 errors and retries**. My previous implementation just collected the 404s and I ran the process again to retrieve the failed records. This time around I made sure to bake in some logic that would automatically retry a few times if it received a 404 to make sure it just a one-off server error and not a truly broken link.
* **Represent the review as a class**. Storing everything in one-off variables and dictionaries was easier in a jupyter notebook and allowed for smaller, more readable cells.  When translated into an actual script, however, it just looked sloppy.
* **Parallelize the scraping process.** Although I wasn't in a hurry, waiting hours and hours to scrape 20k reviews just felt kludgy. using [GNU parallel](https://www.gnu.org/software/parallel/) was a really easy way to get the entire process to complete in the time it took me to watch a movie ([Logan Lucky](https://www.imdb.com/title/tt5439796/), highly recommend).

I definitely have some next steps for this dataset, but I wanted to note that I've found the web scraping process really satisfying. Frontend web development has gotten so complicated that it's really satisfying to find ways to programmatically retrieve data meant for humans, not computers. Each new trick I run across (such as [this trick to use pandas to read HTML tables](https://medium.com/@ageitgey/quick-tip-the-easiest-way-to-grab-data-out-of-a-web-page-in-python-7153cecfca58)) makes me excited to continue digging into new datasets.