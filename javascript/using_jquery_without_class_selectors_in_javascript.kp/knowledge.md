---
title: Jquery does not have a class selector
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: A class selector in jQuery is a selector that uses the class attribute of an element to select elements in the DOM.
---

**Contents**

[TOC]

#### CSS Selectors
CSS selectors are used to select elements in HTML documents. jQuery uses the same selectors as CSS, including:

- Element Selector (e.g. `div`)
- Attribute Selector (e.g. `[type="text"]`)
- Class Selector (e.g. `.myclass`)
- ID Selector (e.g. `#myid`)

#### Not Class Selector

The not class selector is not part of the CSS selector syntax, and therefore it is not supported in jQuery. The not class selector is used to select elements that do not have a specific class. For example, `:not(.myclass)` would select all elements that do not have the class "myclass".
