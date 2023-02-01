---
title: What is the procedure for locating elements by class?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: In Python, elements can be found by using the `find\_elements\_by\_class\_name()` method.
---

**Contents**

[TOC]

# Section 1: Using the find_element_by_class_name Method

The find_element_by_class_name() method is a part of the Selenium webdriver that allows you to find an element on a web page by its class name. To use this method, you must first import the webdriver module.

```python
from selenium import webdriver
```

Then you can create a webdriver instance:

```python
driver = webdriver.Chrome()
```

Finally, you can use the find_element_by_class_name() method to find the element:

```python
element = driver.find_element_by_class_name('class_name')
```

# Section 2: Using the find_elements_by_class_name Method

The find_elements_by_class_name() method is similar to the find_element_by_class_name() method, but it returns a list of elements that match the specified class name. To use this method, you must first import the webdriver module.

```python
from selenium import webdriver
```

Then you can create a webdriver instance:

```python
driver = webdriver.Chrome()
```

Finally, you can use the find_elements_by_class_name() method to find the elements:

```python
elements = driver.find_elements_by_class_name('class_name')
```

# Section 3: Using the find_element_by_css_selector Method

The find_element_by_css_selector() method is a part of the Selenium webdriver that allows you to find an element on a web page by its CSS selector. To use this method, you must first import the webdriver module.

```python
from selenium import webdriver
```

Then you can create a webdriver instance:

```python
driver = webdriver.Chrome()
```

Finally, you can use the find_element_by_css_selector() method to find the element:

```python
element = driver.find_element_by_css_selector('.class_name')
```

# Section 4: Using the find_elements_by_css_selector Method

The find_elements_by_css_selector() method is similar to the find_element_by_css_selector() method, but it returns a list of elements that match the specified CSS selector. To use this method, you must first import the webdriver module.

```python
from selenium import webdriver
```

Then you can create a webdriver instance:

```python
driver = webdriver.Chrome()
```

Finally, you can use the find_elements_by_css_selector() method to find the elements:

```python
elements = driver.find_elements_by_css_selector('.class_name')
```
