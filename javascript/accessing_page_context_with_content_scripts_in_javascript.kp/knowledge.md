---
title: Utilize a content script to obtain access to variables and functions that have been defined in the page context
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Content scripts can access variables and functions defined in page context using the window object.
---

**Contents**

[TOC]

#### Accessing Variables

Variables defined in the page context can be accessed using the `window` global object. For example, if the page context has defined a variable `foo` with the value `bar`, the content script can access the value of `foo` by using `window.foo`.

#### Accessing Functions

Functions defined in the page context can be accessed in a similar manner, by using the `window` global object. For example, if the page context has defined a function `foo` with the value `bar`, the content script can access the function by using `window.foo`.

#### Other Considerations

It is important to note that the page context and the content script are running in different contexts, and thus the content script cannot directly access variables and functions defined in the page context. To access these variables and functions, the content script must use the `window` global object.

Additionally, the content script must take care to ensure that the variables and functions that it is attempting to access have been defined in the page context. If the content script attempts to access a variable or function that has not been defined, an error will be thrown.
