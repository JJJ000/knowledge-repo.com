---
title: How can I retrieve the current url using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: $(location).attr(`href`) can be used to get the current URL with jQuery in Javascript.
---

**Contents**

[TOC]

## Using the Location Object

The simplest way to get the current URL using jQuery is to use the `location` object. The `location` object contains information about the current URL.

```javascript
var currentURL = $(location).attr('href');
```

## Using the Window Object

Another way to get the current URL using jQuery is to use the `window` object. The `window` object contains information about the current window, including the URL.

```javascript
var currentURL = $(window).attr('location').href;
```

## Using the History Object

A third way to get the current URL using jQuery is to use the `history` object. The `history` object contains information about the user's browsing history, including the current URL.

```javascript
var currentURL = $(history).attr('location').href;
```

## Using the Document Object

Finally, another way to get the current URL using jQuery is to use the `document` object. The `document` object contains information about the current document, including the URL.

```javascript
var currentURL = $(document).attr('location').href;
```
