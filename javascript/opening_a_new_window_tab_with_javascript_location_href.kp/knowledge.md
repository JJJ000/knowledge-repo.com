---
title: How to open a new window/tab using JavaScript location.href?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use window.open() with the `\_blank` parameter to open a URL in a new window/tab.
---

**Contents**

[TOC]

## Location.href

The `location.href` property can be used to get the current URL of a page, and also to redirect the user to a different URL.

## Opening a New Window

To open a URL in a new window or tab, you can use the `window.open()` method. This method takes two arguments: the URL to open, and a string of window features.

## Syntax

The syntax for the `window.open()` method is as follows:

```javascript
window.open(url, windowName, [windowFeatures]);
```

Where `url` is the URL to open, `windowName` is a name for the window, and `windowFeatures` is a string of features for the window.

## Example

For example, to open a URL in a new window or tab, you can use the following code:

```javascript
window.open(location.href, '_blank');
```

This will open the current URL in a new window or tab.
