---
title: Can you tell me the way to obtain the current url in selenium webdriver 2 using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: You can get the current URL in Selenium Webdriver 2 Python by using the command `current\_url`.
---

**Contents**

[TOC]

## Importing libraries

In order to get the current URL in Selenium Webdriver 2 Python, you need to import the necessary libraries. 

```python
from selenium import webdriver
```

## Creating a Webdriver object

Next, you need to create a Webdriver object for the browser you want to automate. In this example, we are using Chrome.

```python
driver = webdriver.Chrome()
```

## Getting the current URL

Finally, you can get the current URL by using the `current_url` method of the Webdriver object.

```python
current_url = driver.current_url
```

The `current_url` variable will now contain the current URL of the webpage you are automating. You can print it or use it in your automation script as needed. 

Here's the complete code:

```python
from selenium import webdriver

# create a webdriver object for Chrome
driver = webdriver.Chrome()

# navigate to a webpage
driver.get('https://www.google.com')

# get the current URL
current_url = driver.current_url

# print the current URL
print(current_url)

# quit the browser
driver.quit()
```
