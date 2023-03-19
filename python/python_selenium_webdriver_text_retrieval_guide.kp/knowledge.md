---
title: How can selenium webdriver be used to obtain text in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-17 00:00:00
updated_at: 2023-03-17 00:00:00
tldr: Use the `text` attribute to get the visible text of an element in Selenium WebDriver with Python.
---

**Contents**

[TOC]

## Setup

Before getting started with Selenium, you need to install the Selenium Python package. You can install it via pip by running the following command in a terminal or command prompt:

```
pip install selenium
```

You also need to download the appropriate web driver for the browser you want to automate. Selenium supports various web drivers for different browsers such as Chrome, Firefox, Safari, Edge, and more. You can download the web driver from the official source or use a third-party package such as webdriver-manager.


## Finding Elements

To get text with Selenium WebDriver in Python, you first need to locate the element that contains the text you want to retrieve. There are several methods available to find elements using Selenium, such as:

- `find_element_by_id`
- `find_element_by_name`
- `find_element_by_xpath`
- `find_element_by_css_selector`
- `find_element_by_tag_name`

Once you have located the element, you can use the `text` property to retrieve the text content of the element. For example, if you want to retrieve the text content of an HTML element with an ID of `my-element`, you can use the following code:

```python
from selenium import webdriver

driver = webdriver.Chrome()

element = driver.find_element_by_id('my-element')
text = element.text
print(text)

driver.quit()
```

This will open a Chrome browser instance, locate the HTML element with an ID of `my-element`, retrieve its text content using the `text` property, print it to the console, and then terminate the browser instance.


## Retrieving Attributes

In addition to the `text` property, Selenium also provides other properties that you can use to retrieve attributes of an HTML element, such as:

- `get_attribute('attribute_name')`

For example, if you want to get the value of the `href` attribute of an anchor element, you can use the following code:

```python
from selenium import webdriver

driver = webdriver.Chrome()

element = driver.find_element_by_xpath('//a[@id="my-link"]')
href = element.get_attribute('href')
print(href)

driver.quit()
```

This will open a Chrome browser instance, locate the anchor element with an ID of `my-link` using XPath, retrieve its `href` attribute using the `get_attribute()` method, print it to the console, and then terminate the browser instance.


## Handling Exceptions

When using Selenium WebDriver to find elements or retrieve their attributes, you may encounter several exceptions. Some of the most common ones are:

- `NoSuchElementException`: Raised when the element is not found on the web page.
- `TimeoutException`: Raised when the element is not found within a certain time limit.
- `StaleElementReferenceException`: Raised when the element is no longer on the web page.

To handle exceptions in Selenium WebDriver, you can use `try`-`except` blocks. For example, if you want to find an element with an ID of `my-element` and handle any `NoSuchElementException` exception that may occur, you can use the following code:

```python
from selenium import webdriver
from selenium.common.exceptions import NoSuchElementException

driver = webdriver.Chrome()

try:
    element = driver.find_element_by_id('my-element')
    text = element.text
    print(text)
except NoSuchElementException:
    print('Element not found')

driver.quit()
```

This will open a Chrome browser instance, attempt to locate the HTML element with an ID of `my-element`, retrieve its text content using the `text` property, print it to the console if found, print a message to the console if not found, and then terminate the browser instance.
