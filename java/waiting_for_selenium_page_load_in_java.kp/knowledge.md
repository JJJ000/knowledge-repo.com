---
title: Wait for the page to finish loading in selenium
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Wait until the page is fully loaded by using WebDriverWait with ExpectedConditions.
---

**Contents**

[TOC]

### Implicit Wait

An implicit wait is a type of wait used in Selenium, where the webdriver will wait a certain amount of time before throwing an exception if an element is not found on the page. The implicit wait will tell the webdriver to poll the DOM for a certain amount of time when trying to find an element or elements if they are not immediately available.

### Syntax

The syntax for an implicit wait is as follows:

```java
driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
```

In this example, the webdriver will wait for 10 seconds before throwing an exception if an element is not found on the page.

### Advantages

The main advantage of using an implicit wait is that it allows the webdriver to wait for a certain amount of time before throwing an exception if an element is not found on the page. This can be useful if the page is taking a long time to load or if the element is not immediately available on the page.

### Disadvantages

The main disadvantage of using an implicit wait is that it can slow down the execution of the script if the page takes a long time to load or if the element is not immediately available on the page. Additionally, the implicit wait can cause flaky tests if the element is not found within the specified timeout.
