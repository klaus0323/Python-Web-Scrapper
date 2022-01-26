PriceGrabber
============
PriceGrabber is a solo python project that enables the user to compare the price on different websites (such as amazon, bestbuy, and newegg) across the same product. 

This is a Python package to retrieve prices for specific products from all sorts of websites, such as Amazon, Aliexpress, or price comparison websites. The main teck stacks and frameworks used are: Scrapy, Scraper API, Beautiful Soup, Requests, Scikit-learn, Pandas, Numpy, Matplotlib, and Seaborn.

The scrapper also provides users with personalized data over different websites using GraphQL.

New websites can be supported by means of a simple configuration entry. Currently supported sites include:

* Amazon.(de, com, co.uk, ca, probably all)
* Newegg.com
* Aliexpress.com
* Bestbuy.com

Usage
-----

Usage is pretty simple. Mostly you should be able to put in an URL to the site of a product you're interested in, and you should get out a price (or a list of prices). Here is an Example for an AliExpress product:

```python
>>> from pricegrabber import Grabber
>>> cfg = {"url": "https://de.aliexpress.com/store/product/Cherry-cherry-shaft-shaft-mx-mechanical-keyboard-shaft-switch-black-shaft-tea-shaft-white-shaft-green/2230037_32682571027.html?spm=a2g0x.12010612.8148356.2.75987786TNUZUO"}
>>> g = Grabber(cfg)
>>> g.grab()
[(8.9, '$')]
```

So in this case we know that the pack of Cherry MX key switches from AliExpress costs $8,90. Note that a list is returned. Some sites may report multiple prices instead of just one.

The final result will be demonstrated through bar chart (or line chart under some occasion)，one demonstration of the result demonstration looks like below:

![image](https://user-images.githubusercontent.com/73679709/151211219-6ae85f39-5ea4-4ff8-bfe7-fa597d8c6a26.png)


This is my first solo project, and I know there are many things to be improved. But hey, that's how things start.
