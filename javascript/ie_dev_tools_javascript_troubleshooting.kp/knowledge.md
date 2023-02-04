---
title: What is the purpose of needing to open developer tools in internet explorer before JavaScript will work?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: JavaScript is disabled by default in Internet Explorer, so it must be enabled in the developer tools in order for it to work.
---

**Contents**

[TOC]

#### Browser Cache

Internet Explorer caches JavaScript files, which means that the browser will not download a new version of the file until its cache is cleared. As a result, the JavaScript code will not be executed until the cache is cleared.

#### Developer Tools

When the developer tools are opened, the browser will automatically clear its cache. This ensures that the latest version of the JavaScript file is downloaded and executed.

#### Execution Order

The order in which the JavaScript code is executed is also important. JavaScript code is executed after the HTML and CSS code is parsed. If the developer tools are not opened, the JavaScript code will not be executed until the HTML and CSS code is parsed.

#### Caching Behavior

In some cases, Internet Explorer may also cache the JavaScript code even after the developer tools are opened. To prevent this from happening, developers can disable caching by setting the "Cache-Control" header to "no-cache".
