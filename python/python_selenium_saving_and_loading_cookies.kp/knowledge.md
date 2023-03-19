---
title: How to utilize Python + selenium webdriver for saving and loading cookies
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To save and load cookies using Python + Selenium WebDriver, use the `cookies` property of the WebDriver instance to get and set cookies as a dictionary, and save or load this dictionary using the `pickle` module.
---

**Contents**

[TOC]

# Introduction
When performing web automation with Selenium WebDriver, it is often necessary to save and load cookies for a particular session. Cookies are small text files containing data that a website sends to and saves on a user's computer or device. They are often used to remember user preferences, login information, and other session-specific information. In this tutorial, we will discuss how to save and load cookies using Python and Selenium WebDriver.

# Saving cookies using Python + Selenium

To save cookies in Selenium, we can use the `get_cookies()` method of the WebDriver object to retrieve all cookies associated with the current session. We can then save these cookies as a JSON file using the `json` module in Python. Here is an example code snippet for saving cookies:

```
import json
from selenium import webdriver

# create webdriver object
driver = webdriver.Chrome()

# load target web page
driver.get('https://example.com')

# get all cookies
cookies = driver.get_cookies()

# save cookies to file
with open('cookies.json', 'w') as file:
    json.dump(cookies, file)
```

In this example, we first created a WebDriver object using Chrome driver. We then loaded a web page using `get()` method. Next, we retrieved all saved cookies by calling `get_cookies()` method. Finally, we saved the cookies as a JSON file using Python's `json.dump()` method. By default, the `get_cookies()` method returns a list of dictionaries containing information about each cookie. Once we saved these cookies to a file, we can load them again later using the `json.load()` method.

# Loading cookies using Python + Selenium

To load cookies in Selenium, we can use the `add_cookie()` method of the WebDriver object to add each cookie loaded from our saved JSON file. Here is an example code snippet for loading cookies:

```
import json
from selenium import webdriver

# create webdriver object
driver = webdriver.Chrome()

# load target web page
driver.get('https://example.com')

# load cookies from file
with open('cookies.json', 'r') as file:
    cookies = json.load(file)

# add cookies to webdriver
for cookie in cookies:
    driver.add_cookie(cookie)

# refresh page to apply cookies
driver.refresh()
```

In this example, we used the `json.load()` method to load cookies from our saved JSON file. We then loop through each dictionary in the list of cookies and add each cookie to the WebDriver using the `add_cookie()` method. Once all cookies have been added, we can refresh the page (or navigate to a new page) to apply the cookies. 

# Conclusion
Saving and loading cookies is an important part of web automation with Selenium. By following the steps in this tutorial, we can easily save and load cookies using Python and Selenium WebDriver. This allows for more efficient and streamlined automation, as we can save session-specific information and preferences for future sessions.
