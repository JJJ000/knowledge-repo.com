---
title: Determine if the internet connection is offline
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can detect if the internet connection is offline in Javascript by using the navigator.onLine property.
---

**Contents**

[TOC]

**Section 1: Checking the Online Status of the Browser**

The first step to detect an offline connection is to check the online status of the browser. The `navigator.onLine` property returns a boolean value that indicates whether the browser is online or not. 

```javascript
if (navigator.onLine) {
  // The browser is online
} else {
  // The browser is offline
}
```

**Section 2: Listening for Network Changes**

In addition to checking the browser's online status, it is also possible to listen for network changes. The `window.addEventListener` method can be used to register a callback function that will be executed when the online status of the browser changes.

```javascript
window.addEventListener('online', () => {
  // The browser is now online
});
window.addEventListener('offline', () => {
  // The browser is now offline
});
```

**Section 3: Testing Network Connectivity**

Another way to detect an offline connection is to test network connectivity. This can be done by sending an AJAX request to a server and checking the response. If the request fails, then it is likely that the internet connection is offline.

```javascript
const xhr = new XMLHttpRequest();
xhr.open('GET', 'https://example.com/status');
xhr.onreadystatechange = () => {
  if (xhr.readyState === XMLHttpRequest.DONE) {
    if (xhr.status === 200) {
      // The request was successful
    } else {
      // The request failed - the internet connection is likely offline
    }
  }
};
xhr.send();
```

**Section 4: Using the Fetch API**

Finally, the `fetch` API can also be used to test network connectivity. The `fetch` API returns a `Promise` that is resolved when the request is successful and rejected when the request fails.

```javascript
fetch('https://example.com/status')
  .then(() => {
    // The request was successful
  })
  .catch(() => {
    // The request failed - the internet connection is likely offline
  });
```
