---
title: What is the process for locating an element with a specific text string using selenium webdriver in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the `contains()` method to find an element with specific text in Selenium WebDriver (Python).
---

**Contents**

[TOC]

1. Using xpath:

XPath is a language for addressing parts of an XML document. It can be used to locate elements in an HTML document.

To locate an element that contains specific text, you can use the following xpath expression:

```
//*[contains(text(),'specific text')]
```

2. Using CSS Selectors:

CSS selectors are used to select elements in an HTML document. You can use the following CSS selector to find an element that contains specific text:

```
[text*="specific text"]
```

3. Using find_element_by_partial_link_text:

The find_element_by_partial_link_text() method is used to find an element by its partial link text. This method can be used to find an element that contains specific text.

For example, to find an element that contains the text “example”, you can use the following code:

```
element = driver.find_element_by_partial_link_text('example')
```

4. Using find_element_by_tag_name:

The find_element_by_tag_name() method is used to find an element by its tag name. You can use this method to find an element that contains specific text.

For example, to find an element that contains the text “example”, you can use the following code:

```
element = driver.find_element_by_tag_name('p').text
if 'example' in element:
    print('Element found')
```
