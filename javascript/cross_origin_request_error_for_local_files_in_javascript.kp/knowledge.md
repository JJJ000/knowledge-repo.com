---
title: Error when attempting to load a local file "cross origin requests are not supported for non-http protocols."
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Cross origin requests are not allowed when loading local files, so this error is expected.
---

**Contents**

[TOC]

# Overview
Cross origin requests are only supported for HTTP. This error occurs when a web page attempts to make a request to a different domain than the one it originated from. This is done to prevent malicious activities such as data theft or cross-site scripting attacks.

# Local Files
When loading a local file in JavaScript, the browser will not make a cross-origin request. This means that the file must be located on the same domain as the web page making the request. If the file is located on a different domain, the browser will throw the error "Cross origin requests are only supported for HTTP."

# Solutions
In order to fix this issue, the file must be located on the same domain as the web page making the request. If the file is located on a different domain, the web page must specify the URL of the file in the script tag. For example, if the file is located at http://example.com/myfile.js, the script tag should look like this:

```
<script src="http://example.com/myfile.js"></script>
```

Alternatively, the file can be uploaded to the same domain as the web page and the relative path can be specified in the script tag. For example, if the file is located at /js/myfile.js, the script tag should look like this:

```
<script src="/js/myfile.js"></script>
```
