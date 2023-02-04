---
title: Is it possible for a website to recognize that selenium and chromedriver are being used?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Yes, a website can detect when you are using Selenium with chromedriver in Javascript by looking for specific user agent strings.
---

**Contents**

[TOC]

## Detection

Yes, a website can detect when you are using Selenium with chromedriver in Javascript. This is done by detecting certain characteristics of the browser, such as its user agent string and other browser-specific settings.

## User Agent String

The user agent string is a piece of text that is sent by the browser to the web server when a request is made. It contains information about the browser, such as its name, version, and operating system. By examining the user agent string, a website can determine if the browser is being run by Selenium with chromedriver.

## Browser Settings

In addition to the user agent string, websites can also detect if Selenium with chromedriver is being used by examining other browser settings. These settings include the window size, timezone, language, and other browser-specific settings. If these settings match the expected values for Selenium with chromedriver, then the website can detect that the browser is being run by Selenium with chromedriver.

## Conclusion

In conclusion, a website can detect when you are using Selenium with chromedriver in Javascript by examining the user agent string and other browser-specific settings. By doing so, the website can determine if the browser is being run by Selenium with chromedriver.
