---
title: Does safari on ios 6 store the results of $.ajax requests in its cache?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Yes, Safari on iOS 6 will cache $.ajax results in Javascript.
---

**Contents**

[TOC]

#Yes

Safari on iOS 6 does cache $.ajax results in Javascript.

#How

Safari on iOS 6 caches $.ajax results in Javascript by utilizing the browser’s HTTP cache. When the browser requests a resource, it will first check its cache to see if it has a copy of the resource. If it does, it will return the cached version instead of requesting a new version from the server.

#Options

When making an Ajax request, you can set the cache parameter to false to ensure that the browser does not use a cached version of the resource. You can also set the If-Modified-Since header to ensure that the browser only requests a new version of the resource if it has been modified since the last request.

#Benefits

Caching $.ajax results can improve the performance of your application by reducing the number of requests that need to be made to the server. This can reduce the amount of time it takes for the application to load, as well as reduce the amount of bandwidth being used.
