---
layout: default

---

# Search Term: "EVICTION"
  
In August of this year, the supreme court ended the federal eviction moratorium established by the Centers for Disease Control and Prevention (CDC) nearly a year prior. While the moratorium was in place, [Eviction Lab](https://evictionlab.org/) estimated that the US saw at least 1.55 million fewer eviction filings than normal.<sup>1</sup> The moratorium was a crucial security measure for millions of Americans facing economic uncertainty during the COVID-19 pandemic. Philadelphia pioneered the widely successful Eviction Diversion Program using the federal COVID-19 relief packages passed by Congress, which began on September 1st, 2020. This program facilitated a mandated mediation process between landlord and tenant to reach an agreement before an eviction could be legally filed.  "Before the pandemic, Philadelphia Averaged 20,000 evictions per year -- fourth in total filings among the largest U.S. cities. Now, Philadelphia Municipal Court sees far fewer -- just 5,000 this year to date." <sup>2</sup>  Similarly to the federal eviction moratorium, the Eviction Diversion Program was a safety net for low income Philadelphians at the local level. Without such programs, cost burdened renters across America are at the mercy of their landlords, and are a few missed rent payments away from homelessness.

This analysis pulls tweets containing the search term "eviction", identifies common words associated with the term, and maps geographic locations of where the tweets were made. We create a bar chart showing the count of each associated word, and a word cloud to summarize the top results visually. We expected an array of words that are political and activism oriented. However, as we know, expectations are not always met by reality. The top word associated with "eviction" on twitter from the last 14 days is "vote", with over 14,000 counts. This, at first glance, may make sense in a political context, however upon further inspection of the results, we notice the second most common word is "kumu" at over 8,000 counts. As it turns out, Kumu is the largest social entertainment app in the Philippines, and it airs reality TV show, "Pinoy Big Brother, Season 10", weekly<sup>3</sup> . Our analysis set out to view twitter's political landscape around the topic of eviction appears to be overrun with Big Brother fans discussing the weekly "eviction" "vote" by viewers. While we may further filter our results to exclude key words related to Kumu, we are reminded of the very real limitations of data.


## Method

 **Our analysis was conducted on Sunday Dec. 12th at 11pm.** [See our Jupyter Notebooks Here](https://github.com/bri-ne/MUSA500_Assignment6/tree/main/JupyterNotebooks)
We pulled from the Twitter API v2 using Python and Tweepy. In total we pulled 50,000 tweets in an effort to capture a reasonable amount of tweets with location information. At the end, only ~ 170 of the tweets we pulled had location information.

We then used `nltk` and `string` to remove common stop words such as `'don', 'these', 'couldn', 'they', 'be', 'once',` and any punctuation and non-letters, as well as the word "rt" and usernames. Further we removed urls using a function provided by **Geospatial Data Science in Python** professor Nick Hand.

A simple bar chart shows the most common words associated with the tweets using the word "eviction".

![bar graph of most common words]({{ site.url }}{{ site.baseurl }}/assets/img/commonwords.png)


## Word Cloud

Below is a word cloud of the terms associated with eviction on twitter.

![wordcloud of most common words]({{ site.url }}{{ site.baseurl }}/assets/img/wordcloud.png)


## Map

Below is a map of where tweets containing our search words came from around the world.
![map of tweets across the world]({{ site.url }}{{ site.baseurl }}/assets/img/tweetsWorld.png)

### REFERENCES

<sup>1</sup> Jacob Haas, Jasmine Rangel, Juan Pablo Garnham, Peter Hepburn [Preliminary Analysis: Eviction Filing Trends After the CDC Moratorium Expiration](https://evictionlab.org/updates/research/eviction-filing-trends-after-cdc-moratorium/), Eviction Lab, December 9, 2021

<sup>2</sup> U.S. Rep. Mary Gay Scanlon [Philadelphia's evictionn diversion program is a national model -- let it continue](https://billypenn.com/2021/10/26/philadelphia-eviction-diversion-program-rental-assistance-pa-supreme-court-scanlon/), BillyPenn, October 26, 2021

<sup>3</sup> Kumu, [PBB Kumunity: Pinoy Big Brother Season 10 is here!](https://blog.kumu.ph/pbb-kumunity-pinoy-big-brother-season-10/) August 27, 2021
