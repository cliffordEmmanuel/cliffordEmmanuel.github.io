---
layout: post
title: Web Scrapping.
subtitle :  Why I'm learning to love it.
tags: [Scraping, Python]
author: Clifford
comments : True
---

![webscrape](/assets/project/webscrape.jpg)
<br>

At its core the process of scraping a particular website for data mimics how our browsers displays a particular webpage on our screen, except both are not so similar. When you type a url into your browser, typically the following steps occurs:
- the browser searches the internet for the web page that belongs to the url you specified by placing a request 
- a web server(just another computer located perhaps on another continent) responds to that request by and sends back the requested web page.
- the browser then serves up the page to your screen with the formating intact.

In web scraping however, we intercept the response of the server and search through it to extract the data we need. So typically web scrapers take something out of a web page or a web resource. Data scientist, engineers and any curious person for that matter usually employs the tool of scraping in order to quickly generate a source of data.

<br>

### Applications of web scraping

Scraping is usually a component a bigger process and it helps to quickly gather lots of data. This ability makes that scraping can be applied in diverse ways. For instance a 17 year old Jewish boy [Avi Shiffman](https://www.timesofisrael.com/updated-every-minute-17-year-old-whiz-kids-coronavirus-site-used-by-millions/) built a [dashboard](https://ncov2019.live/) that provided real-time updates to the spread of the corona-virus by writing alot of website scrapers.

<br>

Some scenarios where scraping can be applied are:
- Scrape product details (price, images, rating, reviews etc.) from retailer/manufacturer/eCommerce websites (Ex: Amazon, eBay, AliExpress, Alibaba etc.) to show on own websites, to provide price comparisons, to perform a price watch on competing sellers etc.
- Scrape people profiles from social networks like Facebook, LinkedIn etc. for tracking online reputation.
- Scrape reviews of products and places/hotels/restaurants
- Scrape data from various Government websites, most of which do not provide an easy way to download the data which they display.


There are two ways of scraping and that heavily depends on whether the website/web application being scraped has an API or not.

<br>

### Scraping with an API

Some web applications provide an API that enables one to easily access their data. Examples of such Twitter, Google search, LinkedIn etc. The advantage here is you’re provided with the methods you’ll need to access the data, and a lot of heavy lifting is done for you.  Other than that they may be some restrictions on how much info you can access and most have a payment structure.

<br>

### Scraping without an API

Here you create everything from scratch. You’ll write your own methods to fetch the data and handle all the complexities yourself. But the advantage is that you’re basically unlimited in what kind of information you want and you can get it however you want. So yeah!! it’s freedom. Just that every website is different so you may have to write a script for each one that you want to scrape. Aside that some websites change frequently so your web scraper can become useless if there's a slight change in the website codes.

<br>

### What you need to know and have

- A basic knowledge of programming. (usually beginner to intermediate level in a scripting language is cool) The python language is a very good option.
- A basic understanding of html and css (web technologies)
- Computer and good nternet
- Patience(lots and lots of it)

<br>

### So what makes it fun?

- You can easily and quickly generate your own dataset for your personal research
- Since you drive deep into the heart of the website or application, you get the chance to put your programming skills to the test
- There's a surreal feeling of writing a single script and watching your database grow with data as your script dutifully downloads data for you.
- Because of scraping you can no longer be limited by the unavailability of data for your project.

<br>

I hope you're inspired. 
Cover Photo by [Nicolas Picard](https://unsplash.com/@artnok?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText)

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
