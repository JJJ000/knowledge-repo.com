---
title: How can I locate an element on a webpage using xpath and JavaScript in selenium webdriver?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, the WebDriver.findElement() method can be used to locate an element by XPath in Selenium WebDriver using JavaScript.
---

**Contents**

[TOC]

**Answer:**

**Using XPath with JavaScript in Selenium WebDriver:**

1. Using `document.evaluate()`: The `document.evaluate()` method can be used to evaluate an XPath expression and retrieve the matching element in the DOM. It takes three parameters: an XPath expression, a context node (optional), and a namespace resolver (optional).

2. Using `document.querySelector()`: The `document.querySelector()` method can be used to select an element using an XPath expression. It takes one parameter, the XPath expression, and returns the first matching element.

3. Using `document.querySelectorAll()`: The `document.querySelectorAll()` method can be used to select multiple elements using an XPath expression. It takes one parameter, the XPath expression, and returns a list of matching elements.

4. Using `document.getElementsByXPath()`: The `document.getElementsByXPath()` method can be used to select multiple elements using an XPath expression. It takes one parameter, the XPath expression, and returns a list of matching elements.
