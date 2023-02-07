---
title: Run scripts in sequence
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Scripts are executed in the order they are encountered in the document, with deferred and async scripts executing in the order they are encountered as well.
---

**Contents**

[TOC]

### Scripts in the <head>

When a page is loaded, scripts in the `<head>` are loaded and executed first, before the page is rendered. This allows the scripts to set up any global variables or functions that will be used in the page.

### Scripts at the Bottom of the <body>

Scripts at the bottom of the `<body>` are loaded and executed after the page is rendered. This allows the scripts to access and manipulate the DOM, as it has already been loaded.

### Asynchronous Scripts

Asynchronous scripts are loaded and executed in the background, without blocking the page from loading. This can be used to speed up page load times, as the scripts are not required to be loaded before the page can be rendered.

### Deferred Scripts

Deferred scripts are scripts that are loaded and executed after the page has been rendered. This can be used to optimize page load times, by delaying the loading and execution of scripts that are not necessary for the page to render.
