---
title: What is the syntax for refreshing a page using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the location.reload() method to refresh a page using JavaScript.
---

**Contents**

[TOC]

## Using window.location

The `window.location` object can be used to refresh the current page.

```javascript
window.location.reload();
```

## Using history.go

The `history.go` method can also be used to refresh the page.

```javascript
history.go(0);
```

## Using location.href

The `location.href` property can be used to reload the page by setting it to the current page's URL.

```javascript
location.href = location.href;
```

## Using location.replace

The `location.replace` method can be used to reload the page by replacing the current page's URL with itself.

```javascript
location.replace(location.href);
```
