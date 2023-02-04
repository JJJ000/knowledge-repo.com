---
title: What is the best way to access query parameters from a url in vue.js?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the `this.$route.query` object to get query parameters from a URL in Vue.js.
---

**Contents**

[TOC]

### 1. Using the `$route` Object

The `$route` object provides access to the current route information and can be used to get query parameters from the URL.

### 2. Accessing the `$route.query` Object

The `$route.query` object contains the query parameters for the current route. To access the query parameters, use the `$route.query` object with the key of the query parameter you wish to access.

### 3. Example

For example, if the URL is `http://example.com/page?name=John&age=25`, you can access the query parameters like this:

```javascript
let name = this.$route.query.name; // John
let age = this.$route.query.age; // 25
```

### 4. Using the `this.$route.params` Object

The `this.$route.params` object can also be used to access query parameters. This object will contain any parameters specified in the URL path, as well as any query parameters. For example, if the URL is `http://example.com/page/John?age=25`, you can access the query parameters like this:

```javascript
let name = this.$route.params.name; // John
let age = this.$route.params.age; // 25
```
