---
title: What is the process for redirecting a page using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: To redirect with JavaScript, use the window.location.href or window.location.replace methods.
---

**Contents**

[TOC]

# Redirecting with `window.location`

The `window.location` object in JavaScript can be used to get the current page address (URL) and to redirect the browser to a new page.

## Syntax

The syntax for redirecting using `window.location` is as follows:

```javascript
window.location = "http://www.example.com";
```

## Parameters

The `window.location` object has several properties and methods, but the most important ones are `href`, `hostname`, `pathname`, `search`, and `hash`.

## Examples

Here are some examples of how to use `window.location` to redirect the browser to a new page:

To redirect to a new page:

```javascript
window.location = "http://www.example.com";
```

To redirect to a new page with query string parameters:

```javascript
window.location = "http://www.example.com?param1=value1&param2=value2";
```

To redirect to a new page and add a hash fragment:

```javascript
window.location = "http://www.example.com#fragment";
```
