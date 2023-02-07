---
title: Cause the parent window to be redirected from an iframe action
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The parent window can be redirected from an iframe action using the parent.window.location.replace() method.
---

**Contents**

[TOC]

## Using Location.replace()

The `location.replace()` method replaces the current document with a new one. This can be used to redirect the parent window from an iframe action.

```javascript
parent.location.replace("http://www.example.com/");
```

## Using Window.open()

The `window.open()` method can be used to open a new window and then redirect the parent window from an iframe action.

```javascript
window.open("http://www.example.com/", "_parent");
```

## Using Window.location.href

The `window.location.href` property can be used to set the URL of the parent window from an iframe action.

```javascript
parent.window.location.href = "http://www.example.com/";
```

## Using Window.top.location

The `window.top.location` property can be used to set the URL of the top window from an iframe action.

```javascript
window.top.location = "http://www.example.com/";
```
