---
title: What is the difference between location.host and location.hostname, and is it compatible across different web browsers?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: location.hostname is more cross-browser compatible than location.host, as it does not include the port number.
---

**Contents**

[TOC]

## location.host
The `location.host` property of the `location` object in Javascript returns the full host name of the URL. This includes both the hostname and the port number. For example, if the URL is `https://www.example.com:3000`, then `location.host` will return `www.example.com:3000`.

## location.hostname
The `location.hostname` property of the `location` object in Javascript returns the hostname of the URL. This does not include the port number. For example, if the URL is `https://www.example.com:3000`, then `location.hostname` will return `www.example.com`.

## Cross-Browser Compatibility
Both `location.host` and `location.hostname` are supported by all major browsers, including Chrome, Firefox, Safari, and Edge.

## Summary
The `location.host` and `location.hostname` properties of the `location` object in Javascript are used to get the hostname of the current URL. `location.host` returns the full hostname, including the port number, while `location.hostname` returns only the hostname without the port number. Both properties are supported by all major browsers, ensuring cross-browser compatibility.
