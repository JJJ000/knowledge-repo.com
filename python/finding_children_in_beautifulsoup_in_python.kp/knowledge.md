---
title: What is the process to locate nodes' child elements using beautifulsoup?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the .contents or .children attribute to find the direct children of a node in BeautifulSoup.
---

**Contents**

[TOC]

Section 1: Introduction to BeautifulSoup
---------------------------------------

BeautifulSoup is a Python library used for web scraping purposes to pull the data out of HTML and XML files. It creates a parse tree for parsed pages that can be used to extract data from HTML, which is useful for web scraping. It is capable of parsing both XML and HTML code.

Section 2: Finding Children of Nodes using BeautifulSoup
-----------------------------------------------------

To get the children of an HTML tag in BeautifulSoup, we can use the .contents attribute. This attribute returns a list containing all the children of the tag. Here's an example that demonstrates how to get the children of an HTML tag:

```python
from bs4 import BeautifulSoup
import requests

url = 'https://www.pythonforbeginners.com/'

response = requests.get(url)
soup = BeautifulSoup(response.text, 'html.parser')

# get the children of the 'div' tag
div = soup.find('div')
children = div.contents

print(children)
```

In this example, we are using the requests module to get the HTML code of a webpage. We are then creating a BeautifulSoup object and searching for the first div tag in the HTML code. We then use the .contents attribute to get a list of all the children of the div tag and print it to the console.

Section 3: Using the .children generator
---------------------------------------

Another way to get the children of an HTML tag is to use the .children generator. This generator returns an iterator that we can loop over. Here's an example:

```python
from bs4 import BeautifulSoup
import requests

url = 'https://www.pythonforbeginners.com/'

response = requests.get(url)
soup = BeautifulSoup(response.text, 'html.parser')

# get the children of the 'div' tag using the .children generator
for child in soup.find('div').children:
    print(child)
```

In this example, we are using the requests module to get the HTML code of a webpage. We are then creating a BeautifulSoup object and searching for the first div tag in the HTML code. We then use the .children generator to loop over all the children of the div tag and print them to the console.

Section 4: Conclusion
--------------------

In this tutorial, we have learned how to find children of nodes using BeautifulSoup in Python. We can use the .contents attribute to get a list of children, or use the .children generator to loop over them. By understanding these techniques, we can extract data from HTML in a more efficient and effective manner.
