---
title: Jsonp is a way of making cross-domain requests by exploiting the fact that script tags are allowed to make cross-domain requests. it was created to allow for data to be shared between different domains without the need for a server-side proxy
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: JSONP is a technique used to circumvent the same-origin policy in web browsers by allowing data to be requested from a server residing in a different domain, and was created in Javascript to facilitate cross-domain communication.
---

**Contents**

[TOC]

# Introduction
JSONP (JSON with Padding) is a technique used to bypass the same-origin policy, which prevents JavaScript from making requests to a different domain than the one it originated from.

# What is JSONP?
JSONP is a technique used to make cross-domain requests by exploiting the fact that browsers do not enforce the same-origin policy on <script> tags. Instead of making a regular AJAX request to a different domain, a <script> tag is added to the page that references a URL on the other domain. This URL should return a JavaScript file that contains a callback function, which is then executed by the browser.

# Why was it created?
JSONP was created to allow websites to make cross-domain requests without being blocked by the same-origin policy. This was especially useful for web applications that needed to access data from different domains.

# Conclusion
JSONP is a useful technique for bypassing the same-origin policy and making cross-domain requests in JavaScript. It was created to allow web applications to access data from different domains without being blocked by the browser.
