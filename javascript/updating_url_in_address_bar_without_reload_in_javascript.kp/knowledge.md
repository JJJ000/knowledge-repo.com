---
title: Changing the url in the address bar to a new one without a hash without reloading the page
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: It is not possible to update the address bar with a new URL without hash or reloading the page in Javascript.
---

**Contents**

[TOC]

# Section 1: History API

The History API is a modern browser API that allows us to manipulate the browser history, enabling us to update the URL in the address bar without reloading the page.

# Section 2: PushState

The most common way to use the History API is the pushState() method. This method allows us to push a new URL onto the browser's history stack, which will update the address bar without reloading the page.

# Section 3: Example

For example, if we wanted to update the address bar with the URL "example.com/foo", we could use the following code:

```
history.pushState(null, null, 'example.com/foo');
```

# Section 4: Browser Support

The History API is supported in all modern browsers, including Chrome, Firefox, Edge, and Safari.
