---
title: What is the difference between a 'click()' method called by webdriver and one triggered by javascript?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: WebDriver click() simulates a user clicking on an element, whereas JavaScript click() triggers the click event of an element directly.
---

**Contents**

[TOC]

Section 1: Introduction 

In web application testing using Python, clicking on various elements is an essential task. There are two methods of performing a click on an element in Python. One is using WebDriver's click() method, and the other is JavaScript click().

Section 2: WebDriver click() in Python

WebDriver click() is a method provided by the Selenium WebDriver package that allows performing a click operation on an element within a web page. It is a standard method to trigger a click event using Python. 

Below is an example of the same where the click method is used on a "Submit" button:

```python
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.common.by import By
from selenium.webdriver.support import expected_conditions as EC

# Wait for the Submit button to appear
submit_button = WebDriverWait(driver, 10).until(
EC.presence_of_element_located((By.XPATH, "//button[@id = 'submit_button']")))

# Click on the Submit button using WebDriver
submit_button.click()
```

WebDriver click() method is less prone to errors compared to JavaScript click() method since WebDriver automatically waits for the page's elements to load.

Section 3: JavaScript click() in Python

JavaScript click() is a method that uses JavaScript's in-built click() function to simulate a click event on the element. It is executed through WebDriver's execute_script() method as shown below:

```python
submit_button = driver.find_element_by_xpath("//button[@id = 'submit_button']")

# Click on the button using JavaScript click() method
driver.execute_script("arguments[0].click();", submit_button)
```

While JavaScript click() provides a way to bypass waiting for the web page to load fully in case it's taking time, it is not recommended due to the following reasons:

• It does not ensure that the element's events have fired correctly. 
• It can cause problems if the element is not visible, and you have to scroll it manually. 
• It bypasses browser security measures, which could potentially break code in unexpected ways. 

Section 4: Conclusion

In conclusion, both WebDriver click() and JavaScript click() have their use cases, and you should choose the best option depending on your web application's situation. Suppose the page loading time is not an issue, we recommend using WebDriver click() method, which ensures that the element is visible and its events have fired correctly. However, if page loading time is a concern, the JavaScript click() method will do the work but at the risk of breaking code in unexpected ways.
