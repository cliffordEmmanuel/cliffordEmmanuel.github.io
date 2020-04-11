---
layout: post
title: Web scrapping real estate data.
subtitle : Using 
tags: [Pandas, BeautifulSoup, Requests]
author: Clifford
comments : True
image: "meqasa_scrape.jpg"

---

![Meqasa pic](/assets/project/meqasa_scrape.jpg)
With the influx of data in these modern times, its quite suprising that methods for collecting data is not so apparent. Most software companies like facebook, twitter, google have brigded this divide and provided us data sharks with APIs to ease the process of accessing data. but not all internet companies share the same sentiments. for those we rely on the trusty tools of web scrapping.

This project describes the process of scraping data from [meqasa](http://www.meqasa.com) using the python libraries: beautiful soup and requests without an API

Web scrapping is the process of extracting information from the internet. It involves a lot of parsing and cleaning hence some basic knowledge of the following can go a long way to increase your efficiency:

1. a <b> programming language</b> for scripting and automating the scraper.
2. <b>HTML:</b> for understanding the structure of the web pages.
3. <b>regular expressions</b> for pattern matching.

<br>

You can view web scrapping as a 3 step process.
1.  Identify the content of interest
Find the specific website containing the content you would like to scrape.
2.  Document web-clicks needed
Here you to list the individual webpage click needed to successfully arrive the data you need.
3. Identify patterns for retrieval
Note the pattern that will allow you to iteratively pull all the remaining data you need.

<br>


<!-- 
<h2>1. HTML headings</h2>
{% highlight html %}
<h1>This is heading 1</h1>
<h2>This is heading 2</h2>
<h3>This is heading 3</h3>
<h4>This is heading 4</h4>
<h5>This is heading 5</h5>
<h6>This is heading 6</h6>
{% endhighlight %}
<h1>This is heading 1</h1>
<h2>This is heading 2</h2>
<h3>This is heading 3</h3>
<h4>This is heading 4</h4>
<h5>This is heading 5</h5>
<h6>This is heading 6</h6>

<br>

<h2>2. bold text</h2>
{% highlight html %}
<p>This is normal text - <b>and this is bold text</b>.</p>
{% endhighlight %}
<p>This is normal text - <b>and this is bold text</b>.</p>

<h2>5. image</h2>
{% highlight html %}
![sample image]({{ site.baseurl }}/assets/img/koreaSunset.jpg)
{% endhighlight %}
![sample image]({{ site.baseurl }}/assets/img/koreaSunset.jpg)

<br>

<h2>5. table</h2>
{% highlight html %}
| Header 1  | Header 2 | Header 3 |
| :------- | :-------: | -------: |
| Content 1  | Content 2 | Content 3 |
| Content 1  | Content 2 | Content 3 |
{% endhighlight %}
| Header 1  | Header 2 | Header 3 |
| :------- | :-------: | -------: |
| Content 1 | Content 2 | Content 3 |
| Content 1 | Content 2 | Content 3 | -->
