---
title: Identify when a browser obtains a file download
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: A browser can detect a file download by listening for the `onclick` event on an anchor element with a download attribute.
---

**Contents**

[TOC]

1. Using the Fetch API

The Fetch API provides a `response.body` property which is a [ReadableStream](https://developer.mozilla.org/en-US/docs/Web/API/ReadableStream) object. This stream can be used to detect when a browser receives a file download.

2. Using the XMLHttpRequest (XHR) API

The XMLHttpRequest (XHR) API provides an `onload` event handler which is triggered when the response is received. This can be used to detect when a browser receives a file download.

3. Using the EventSource API

The EventSource API provides an `onmessage` event handler which is triggered when a message is received from the server. This can be used to detect when a browser receives a file download.

4. Using the WebSocket API

The WebSocket API provides an `onmessage` event handler which is triggered when a message is received from the server. This can be used to detect when a browser receives a file download.
