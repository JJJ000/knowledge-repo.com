---
title: What is the process of programmatically making firefox headless in selenium using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The Firefox browser can be made headless programmatically in Selenium with Python by setting the options for the Firefox driver and creating an instance of the FirefoxOptions class.
---

**Contents**

[TOC]

## Requirements 

Before proceeding with the steps, the following requirements must be installed:

- Selenium WebDriver
- Firefox browser
- geckodriver

## Steps

### Step 1: Import Required Libraries
```python
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.firefox.options import Options
```


### Step 2: Set Firefox Options to Headless Mode
```python
options = Options()
options.headless = True
```


### Step 3: Create a Firefox WebDriver Instance with Headless Options
```python
driver = webdriver.Firefox(options=options)
```


### Step 4: Use WebDriver in Headless Mode to Automate Firefox
```python
driver.get("https://www.google.com")
print(driver.title)
search_box = driver.find_element_by_name("q")
search_box.send_keys("Headless Firefox Selenium Python")
search_box.send_keys(Keys.RETURN)
print(driver.page_source)
driver.quit()
``` 

Through the above code, Firefox browser will work in the headless mode and will perform web automation. The output generated could be saved or utilized for further purposes.


## Summary

We can make Firefox headless programmatically in Selenium with Python by using the above mentioned steps to create options that will tell Firefox which mode to run in. The key function of this option is the ability to run Firefox silently in the background, without actually opening a browser window. The above code is very concise and shows an elegant way of working with Firefox in headless mode.
