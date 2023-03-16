---
title: What is the method of utilizing beautifulsoup for extracting solely the visible text on a webpage?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Use the `.text` method on the `soup` object to extract only the visible text content of a webpage with BeautifulSoup in Python.
---

**Contents**

[TOC]

Section 1: Introduction
-----------------------

BeautifulSoup is a powerful library in Python for web scraping. It allows us to extract information from HTML and XML documents with ease. One common task in web scraping is to extract only the visible text on a webpage since there may be other elements such as images or invisible tags that are not relevant to our analysis. In this tutorial, we will learn how to scrape only visible webpage text with BeautifulSoup in Python.

Section 2: Retrieving webpage text with BeautifulSoup
------------------------------------------------------

To extract text from a webpage, we can use BeautifulSoup's `get_text()` method. This method returns all the text on the page including any markup tags. Here's an example:

```python
from bs4 import BeautifulSoup
import requests

# retrieve webpage content
url = 'https://en.wikipedia.org/wiki/Web_scraping'
response = requests.get(url)
html_content = response.content

# parse HTML with BeautifulSoup
soup = BeautifulSoup(html_content, 'html.parser')

# get all text on the page
page_text = soup.get_text()
print(page_text)
```

In this example, we retrieve the Wikipedia page on web scraping and extract all the text on the page. However, this will also include markup tags and other elements that we are not interested in.

Section 3: Filtering out non-visible text
-----------------------------------------

To extract only the visible text on a webpage, we need to filter out any non-visible elements. One way to do this is to use the `find_all()` method to search for all HTML elements and filter out those that have a `style` attribute containing the word `display:none`. Here's an example:

```python
from bs4 import BeautifulSoup
import requests

# retrieve webpage content
url = 'https://en.wikipedia.org/wiki/Web_scraping'
response = requests.get(url)
html_content = response.content

# parse HTML with BeautifulSoup
soup = BeautifulSoup(html_content, 'html.parser')

# find all HTML elements
elements = soup.find_all()

# filter out non-visible elements
visible_text = ''
for el in elements:
    if el.has_attr('style') and 'display:none' in el['style']:
        continue
    else:
        visible_text += el.get_text()

print(visible_text)
```

In this example, we retrieve the Wikipedia page on web scraping and filter out any elements with a `style` attribute containing the word `display:none`. We then concatenate the text from all the remaining elements to get only the visible text on the page.

Section 4: Conclusion
----------------------

In this tutorial, we learned how to scrape only visible webpage text with BeautifulSoup in Python. We first retrieved all the text on a page using `get_text()` and then filtered out any non-visible elements by searching for those with a `style` attribute containing `display:none`. This technique can be useful when we only want to analyze the visible content of a webpage and ignore any extraneous elements.
