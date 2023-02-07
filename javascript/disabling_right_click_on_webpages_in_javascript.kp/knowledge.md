---
title: What is the process for turning off the right-click function on my webpage?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To disable right click on a web page in Javascript, use the `oncontextmenu` event.
---

**Contents**

[TOC]

## Option 1:
1. Add the following code to the page's HTML, between the `<head>` and `</head>` tags:
   ```html
   <script>
       document.addEventListener('contextmenu', event => event.preventDefault());
   </script>
   ```
2. This will disable the right-click context menu for all elements on the page.

## Option 2:
1. Create an event listener for the `oncontextmenu` event on the page, and add the following code to the listener:
   ```javascript
   event.preventDefault();
   ```
2. This will disable the right-click context menu for all elements on the page.
