---
title: Wait for the page to finish loading with selenium webdriver for python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the WebDriverWait class to wait until the page is fully loaded.
---

**Contents**

[TOC]

## 1. Initialize WebDriver

Before attempting to wait for a page to load, you must first initialize the WebDriver. This involves creating an instance of the WebDriver class, specifying the browser that you want to use, and setting up the driver to communicate with the browser.

For example, to initialize the Chrome WebDriver:

```python
from selenium import webdriver

driver = webdriver.Chrome()
```

## 2. Navigate to Page

Once the WebDriver is initialized, you can navigate to the page that you want to wait for. This is done using the `driver.get()` method, which takes a URL as its argument.

For example, to navigate to the Google homepage:

```python
driver.get("https://www.google.com")
```

## 3. Wait for Page to Load

Once the page has been navigated to, you can wait for it to load by using the `WebDriverWait` class. This class takes two arguments: a WebDriver instance and a timeout. The timeout is the amount of time in seconds that the driver will wait for the page to finish loading before timing out.

For example, to wait for the page to load for up to 10 seconds:

```python
from selenium.webdriver.support.ui import WebDriverWait

wait = WebDriverWait(driver, 10)
```

## 4. Check for Page Load

Once the `WebDriverWait` instance has been created, you can use it to check if the page has finished loading. This is done by using the `wait.until()` method, which takes a condition as its argument. The condition is a function that will be called repeatedly until it returns a truthy value or the timeout is reached.

For example, to check if the page has finished loading:

```python
wait.until(lambda driver: driver.execute_script('return document.readyState') == 'complete')
```
