---
title: Under what circumstances would it be preferable to use ajax long/short polling over html5 websockets?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: AJAX long/short polling should be preferred over HTML5 WebSockets in Javascript when real-time communication is not required.
---

**Contents**

[TOC]

1. Legacy Browsers:
AJAX long/short polling is preferred over HTML5 WebSockets in Javascript when the web application needs to support legacy browsers that do not have native support for WebSockets.

2. Bandwidth Limitations:
AJAX long/short polling is preferred over HTML5 WebSockets in Javascript when the web application needs to conserve bandwidth. AJAX long/short polling is more efficient in terms of bandwidth usage compared to WebSockets.

3. Security:
AJAX long/short polling is preferred over HTML5 WebSockets in Javascript when the web application needs to ensure security. AJAX long/short polling is more secure compared to WebSockets as it is not subject to the same Cross-Origin Resource Sharing (CORS) restrictions as WebSockets.

4. Compatibility:
AJAX long/short polling is preferred over HTML5 WebSockets in Javascript when the web application needs to be compatible with a wide range of devices. AJAX long/short polling is more compatible compared to WebSockets as it is not subject to the same browser compatibility issues as WebSockets.
