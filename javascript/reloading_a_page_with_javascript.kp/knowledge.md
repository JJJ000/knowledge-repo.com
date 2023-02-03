---
title: How to refresh a page using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: To reload a page using JavaScript, use the location.reload() method.
---

**Contents**

[TOC]

# Section 1: Using the Location Object

The `location` object is a property of the `window` object in JavaScript. It can be used to get the current URL of the page, redirect the browser to a new page, and reload the same page.

To reload the current page, you can use the `reload()` method of the `location` object.

```javascript
location.reload();
```

# Section 2: Using the Reload Method

The `reload()` method of the `location` object can also be used to reload the page from the server. This is useful if you want to make sure that the latest version of the page is loaded.

```javascript
location.reload(true);
```

# Section 3: Using the Replace Method

The `replace()` method of the `location` object can also be used to reload the page. This method replaces the current page in the history with the specified URL.

```javascript
location.replace(location.href);
```

# Section 4: Using the History Object

The `history` object is a property of the `window` object in JavaScript. It can be used to navigate back and forth through the user's history.

To reload the current page, you can use the `go()` method of the `history` object.

```javascript
history.go(0);
```
