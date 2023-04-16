---
title: What is the significance of the html "no-js" class?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The HTML `no-js` class is used to identify elements that should not be affected by Javascript.
---

**Contents**

[TOC]

#### Purpose

The HTML "no-js" class is used to detect if a user has JavaScript enabled in their browser.

#### How it Works

The "no-js" class is added to the HTML element of a webpage when it is initially loaded. If JavaScript is enabled, the browser will automatically remove the "no-js" class from the HTML element. If the "no-js" class remains, it indicates that JavaScript has not been enabled.

#### Benefits

This allows developers to create two different versions of a website - one for users who have JavaScript enabled and one for users who don't. This allows the website to display correctly for both types of users.

#### Limitations

The "no-js" class is not supported by all browsers, and some browsers may not recognize it. Additionally, users may have JavaScript enabled, but disabled for a specific website. In this case, the "no-js" class will not be removed and the website may not display correctly.
