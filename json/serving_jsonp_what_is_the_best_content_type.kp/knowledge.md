---
title: What is the most effective way to serve jsonp?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The best content type to serve JSONP in JSON is `application/javascript`.
---

**Contents**

[TOC]

### Advantages of Serving JSONP

1. Cross Domain Requests: JSONP allows for cross domain requests, which is not possible with regular AJAX requests. This makes it a great choice for making requests across different domains.

2. Improved Performance: JSONP requests are usually faster than regular AJAX requests, since they are cached by the browser. This can lead to improved page load times and overall performance.

3. Easy to Use: JSONP is relatively easy to implement, since it requires minimal changes to existing code.

### Disadvantages of Serving JSONP

1. Security Risks: JSONP requests can be vulnerable to cross-site scripting attacks, since the data is exposed to the public.

2. Limited Browser Support: JSONP is not supported by all browsers, so it may not work in certain browsers.

3. Limited Data Types: JSONP only supports a limited set of data types, so more complex data structures may not be possible.
