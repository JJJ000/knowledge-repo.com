---
title: Retrieve the protocol, domain name, and port number from the url
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The protocol, domain, and port can be extracted from a URL in Javascript using the URL API`s `protocol`, `hostname`, and `port` properties.
---

**Contents**

[TOC]

### Protocol

The protocol can be extracted from the URL using the `protocol` property of the `URL` object.

```javascript
const url = new URL('http://example.com:8080/path');
const protocol = url.protocol; // "http:"
```

### Domain

The domain can be extracted from the URL using the `hostname` property of the `URL` object.

```javascript
const url = new URL('http://example.com:8080/path');
const domain = url.hostname; // "example.com"
```

### Port

The port can be extracted from the URL using the `port` property of the `URL` object.

```javascript
const url = new URL('http://example.com:8080/path');
const port = url.port; // "8080"
```
