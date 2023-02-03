---
title: What is the best way to identify which browser a user is using (i.e. safari, chrome, ie, firefox and opera)?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the built-in navigator.userAgent property to detect the different browsers in JavaScript.
---

**Contents**

[TOC]

1. Using `navigator.userAgent` 
   
   You can detect the browser by using the `navigator.userAgent` property. This returns a string containing the browser name and version. You can then use this string to detect the browser.

2. Detecting Safari
   
   To detect Safari, you can use the `navigator.userAgent` string and look for the substring `Safari`. 

3. Detecting Chrome
   
   To detect Chrome, you can use the `navigator.userAgent` string and look for the substring `Chrome`. 

4. Detecting IE, Firefox and Opera
   
   To detect IE, Firefox and Opera, you can use the `navigator.userAgent` string and look for the substring `MSIE`, `Firefox` and `Opera` respectively.
