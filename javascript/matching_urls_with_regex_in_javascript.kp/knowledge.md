---
title: What is an effective regular expression for identifying urls?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A good regular expression to match a URL in Javascript is /^(https?\/\/)([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
---

**Contents**

[TOC]

### Section 1: Basic URL Matching
`^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`

### Section 2: Matching Paths
`^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/([\w\.-]*)*\/?$`

### Section 3: Matching Query Parameters
`^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/([\w\.-]*)*\/?\?([\w=&]*)$`

### Section 4: Matching Fragments
`^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/([\w\.-]*)*\/?\?([\w=&]*)\#([\w-]*)$`
