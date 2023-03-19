---
title: The warning message "selenium Python deprecationwarning executable_path has been deprecated" should be noted
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The use of executable\_path is deprecated in Selenium Python.
---

**Contents**

[TOC]

Section 1: What is the `executable_path` in Selenium Python?

In Selenium Python, the `executable_path` is a parameter that is used to specify the path of the web driver executable file. This parameter is used in the `webdriver` class constructor. For example, if you want to use Chrome as your web browser, you need to specify the path to the ChromeDriver executable file using the `executable_path` parameter.

Section 2: What is the DeprecationWarning regarding `executable_path` in Selenium Python?

According to the Selenium documentation, the `executable_path` parameter has been deprecated in Selenium Python. This means that the parameter is still available but it is no longer recommended to use it. Instead, you should use the `Service` class to start the web driver service.

Section 3: How to use `Service` class to start the web driver service?

To use the `Service` class to start the web driver service, you need to create an instance of the class and pass the path to the web driver executable file as a parameter. Here is an example of how to use the `Service` class to start the Chrome web driver service:

```
from selenium.webdriver.chrome.service import Service
from selenium.webdriver import Chrome

service = Service('/path/to/chromedriver')
driver = Chrome(service=service)
driver.get('https://www.google.com')
```

In this example, we first import the `Service` class from the `selenium.webdriver.chrome.service` module. We then create an instance of the `Service` class and pass the path to the ChromeDriver executable file as a parameter. Finally, we create an instance of the `Chrome` class and pass the `service` parameter as an argument. 

Section 4: Why use `Service` class instead of `executable_path`?

The `Service` class provides more control over the web driver service than the `executable_path` parameter. For example, you can use the `Service` class to specify various service options such as the port number, log file location, and more. Additionally, the `Service` class allows you to start and stop the service programmatically, which can be useful in certain scenarios.
