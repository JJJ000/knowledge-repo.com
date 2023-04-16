---
title: Retrieve the current domain name using JavaScript (not the path, etc.)
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The current domain name can be retrieved using the window.location.hostname property.
---

**Contents**

[TOC]

##### Using the Location Object

The `window.location` object can be used to get the current domain name. The `hostname` property of this object contains the domain name of the current URL.

```javascript
let domainName = window.location.hostname;
```

##### Using the Location Search

The `window.location.search` property can also be used to get the current domain name. This property returns the query string of the current URL. The domain name can be extracted from this string.

```javascript
let domainName = window.location.search.split('/')[2];
```

##### Using the Location Host

The `window.location.host` property can be used to get the current domain name. This property returns the hostname and port number of the current URL. The domain name can be extracted from this string.

```javascript
let domainName = window.location.host.split(':')[0];
```

##### Using the Location Origin

The `window.location.origin` property can be used to get the current domain name. This property returns the origin of the current URL, which is the combination of the protocol, hostname, and port number. The domain name can be extracted from this string.

```javascript
let domainName = window.location.origin.split('://')[1];
```
