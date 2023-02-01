---
title: Retrieve the html source code of a webelement in selenium webdriver using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can get the HTML source of a WebElement in Selenium WebDriver using Python by using the `get\_attribute()` method.
---

**Contents**

[TOC]

# Solution 1

## Using `get_attribute()`

We can use the `get_attribute()` method to get the HTML source of a WebElement.

```python
element = driver.find_element_by_id('example')
html_source = element.get_attribute('innerHTML')
```

## Using `page_source`

We can also get the HTML source of a WebElement by getting the page source of the page and then parsing it.

```python
page_source = driver.page_source
element = driver.find_element_by_id('example')
html_source = page_source.split(element.get_attribute('outerHTML'))[1]
```

# Solution 2

## Using `get_attribute()`

We can use the `get_attribute()` method to get the HTML source of a WebElement.

```python
element = driver.find_element_by_id('example')
html_source = element.get_attribute('innerHTML')
```

## Using `execute_script()`

We can also use the `execute_script()` method to get the HTML source of a WebElement.

```python
element = driver.find_element_by_id('example')
html_source = driver.execute_script("return arguments[0].innerHTML;", element)
```

## Using `page_source`

We can also get the HTML source of a WebElement by getting the page source of the page and then parsing it.

```python
page_source = driver.page_source
element = driver.find_element_by_id('example')
html_source = page_source.split(element.get_attribute('outerHTML'))[1]
```
