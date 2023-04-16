---
title: What is the best way to change the url without reloading the page?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can modify the URL without reloading the page in Javascript by using the history.pushState() method.
---

**Contents**

[TOC]

##### 1. History API

The History API allows us to modify the URL without reloading the page. It has two methods: `pushState()` and `replaceState()`. `pushState()` adds a new history entry, while `replaceState()` modifies the current history entry.

##### 2. Example

To use `pushState()`, you would pass in three arguments: a state object, a title, and a URL. For example:

```javascript
history.pushState({page: 1}, "Page 1", "?page=1");
```

##### 3. Browser Support

The History API is supported in all major browsers.

##### 4. Additional Resources

For more information on the History API, check out the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/API/History_API).
