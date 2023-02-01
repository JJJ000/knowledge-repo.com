---
title: Is it possible for a website to recognize when selenium and chromedriver are being used?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, a website can detect when you are using Selenium with chromedriver in Python by checking the user agent string.
---

**Contents**

[TOC]

# Yes

## Browser Fingerprinting
Browser fingerprinting is a technique used by websites to identify unique visitors. It involves collecting data about a user's browser, such as their operating system, browser type, and version, as well as the plugins and extensions they have installed. This data can then be used to create a unique “fingerprint” for each visitor, which can be used to determine if the same visitor has returned to the website.

When using Selenium with ChromeDriver in Python, the browser fingerprint will be unique and easily identifiable as it will be using a different user agent than a regular browser.

## JavaScript Detection
Another way a website can detect Selenium with ChromeDriver in Python is by using JavaScript. Websites can use JavaScript to detect if a browser is running in “headless” mode, which is what Selenium does when using ChromeDriver. If the website detects that the browser is running in headless mode, it can then alert the website administrator or take other appropriate action.

# No

## Inconsistent User Agent
When using Selenium with ChromeDriver in Python, the user agent is not consistent and can be changed at any time. This makes it difficult for a website to detect that Selenium is being used, as the user agent can be changed to match that of a regular browser.

## No Access to Internal Network
Finally, websites are unable to detect Selenium with ChromeDriver in Python because Selenium does not have access to the internal network of the website. This means that Selenium is unable to access any of the website's internal data, which is often used to detect automated scripts.
