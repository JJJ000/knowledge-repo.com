---
title: What is the syntax for referencing the script tag that loaded the currently-executing script?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The script tag can be referenced using the `document.currentScript` property.
---

**Contents**

[TOC]

1. Accessing the Script Tag via the `document` Object 

The `document` object contains a `currentScript` property that references the script tag that loaded the currently-executing script. This property is supported in all modern browsers.

2. Accessing the Script Tag via the `document.scripts` Collection 

The `document` object also contains a `scripts` collection, which contains all of the script tags that have been loaded in the page. This collection can be looped through to find the script tag that loaded the currently-executing script. This method is supported in all modern browsers.

3. Accessing the Script Tag via the `document.getElementsByTagName` Method 

The `document.getElementsByTagName` method can be used to get a collection of all script tags in the page. This collection can be looped through to find the script tag that loaded the currently-executing script. This method is supported in all modern browsers.

4. Accessing the Script Tag via the `document.querySelector` Method 

The `document.querySelector` method can be used to query for the script tag that loaded the currently-executing script. This method is supported in all modern browsers.
