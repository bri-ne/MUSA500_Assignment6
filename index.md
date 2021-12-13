---
layout: default

---

# Title

A 1-2 paragraph explanation of the urban problem for which you are doing this analysis. Be sure to talk about the significance of the problem, and to provide a brief description of the Twitter search term which you will be using, as well as the date and time you conducted the analysis. **Our analysis was conducted on Sunday Dec. 12th at 11pm.**

## Method

We pulled from the Twitter API v2 using Python and Tweepy. In total we pulled 50,000 tweets in an effort to capture a reasonable amount of tweets with location information. At the end, only ~ 170 of the tweets we pulled had location information. 

We then used `nltk` and `string` to remove common stop words such as `'don', 'these', 'couldn', 'they', 'be', 'once',` and any punctuation and non-letters, as well as the word "rt". Further we urls using a function provided by Geospatial Data Science in Python professor Nick Hand and removed the word "rt". 

A first glance, shows the most common words associated with the tweets using the word "eviction".
![alt-text]({{ site.url }}{{ site.baseurl }}/assets/images/commonwords.png


## Word Cloud

Below is a word cloud of the terms associated with eviction on twitter.

## Map 

Below is a map of where tweets containing our search words came from around the world. 

![alt-text]({{ site.url }}{{ site.baseurl }}/assets/images/tweetsWorld.png

<div id="hv-chart-1"></div>
