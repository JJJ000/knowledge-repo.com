---
title: Using chrome to execute Python code that utilizes the selenium webdriver bindings
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To run Selenium WebDriver Python bindings in Chrome, you need to install ChromeDriver and set its path in the script.
---

**Contents**

[TOC]

## Setting up the Environment

Before you start running Selenium WebDriver Python bindings in Chrome, you need to set up the environment. Here are the steps you need to follow:

1. Install Python: Download and install Python from the official website https://www.python.org/ depending on the operating system you are using.
2. Install pip: Pip is a tool for managing Python packages. Run the command `python get-pip.py` to install pip.
3. Install Selenium: Run the command `pip install selenium` to install Selenium.
4. Install ChromeDriver: Download the compatible ChromeDriver for your version of Chrome from https://sites.google.com/a/chromium.org/chromedriver/downloads. Extract the zip file and place the chromedriver binary in your PATH.


## Importing the Required Libraries

After setting up the environment, you need to import the required libraries for running Selenium WebDriver Python bindings in Chrome. Here is how to do it:

```python
from selenium import webdriver
```

This imports the webdriver module from the selenium library.


## Starting the Chrome Driver

Once you have installed the ChromeDriver and imported the required libraries, you can start the Chrome driver by creating an instance of the webdriver.Chrome class. Here is how to do it:

```python
driver = webdriver.Chrome()
```

This creates a new Chrome driver instance.


## Running Selenium WebDriver Python Bindings in Chrome

Now that you have set up the environment, imported the necessary libraries and started the Chrome driver, you can run Selenium WebDriver Python bindings in Chrome. Here is how to do it:

```python
driver.get("http://www.google.com")
search_box = driver.find_element_by_name('q')
search_box.send_keys('ChromeDriver')
search_box.submit()
```

This opens the Google homepage in Chrome, finds the search box, enters the text 'ChromeDriver', and submits the form. You can then interact with the page using various methods provided by Selenium, such as find_element_by_* and click().
