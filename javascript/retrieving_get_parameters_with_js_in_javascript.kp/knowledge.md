---
title: What is the process for accessing get parameters using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can retrieve GET parameters from JavaScript using the URLSearchParams API.
---

**Contents**

[TOC]

1. Using `URLSearchParams`
   
   The `URLSearchParams` interface provides a way to easily access the GET parameters in the URL. It can be used as follows:

```javascript
const urlParams = new URLSearchParams(window.location.search);
const myParam = urlParams.get('myParam');
```

2. Using `location.href`
   
   The `location.href` property contains the entire URL of the current page. We can use this to extract the GET parameters as follows:

```javascript
const queryString = window.location.href.split('?')[1];
const params = queryString.split('&');
const myParam = params.find(p => p.startsWith('myParam')).split('=')[1];
```

3. Using `location.search`
   
   The `location.search` property contains the query string of the current page. We can use this to extract the GET parameters as follows:

```javascript
const queryString = window.location.search;
const params = queryString.substring(1).split('&');
const myParam = params.find(p => p.startsWith('myParam')).split('=')[1];
```

4. Using `location.hash`
   
   The `location.hash` property contains the fragment identifier of the current page. We can use this to extract the GET parameters as follows:

```javascript
const queryString = window.location.hash.substring(1);
const params = queryString.split('&');
const myParam = params.find(p => p.startsWith('myParam')).split('=')[1];
```
