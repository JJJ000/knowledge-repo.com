---
title: What is the syntax for opening a url in a new tab using JavaScript or jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the window.open() method with the `\_blank` parameter to open a URL in a new tab using JavaScript or jQuery.
---

**Contents**

[TOC]

## Using JavaScript

1. Use the `window.open()` method to open the URL in a new tab. The syntax is as follows:

```javascript
window.open(url, '_blank');
```

2. The `_blank` argument specifies that the URL should be opened in a new tab.

## Using jQuery

1. Use the `attr()` method to set the `target` attribute of a link to `_blank`. The syntax is as follows:

```javascript
$('#myLink').attr('target', '_blank');
```

2. This will open the link in a new tab when clicked.
