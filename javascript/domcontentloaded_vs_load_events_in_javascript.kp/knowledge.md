---
title: What is the distinction between the domcontentloaded and load events?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: DOMContentLoaded fires when the HTML document has been completely loaded and parsed, while the load event fires when all resources (images, stylesheets, scripts) have been completely loaded.
---

**Contents**

[TOC]

# DOMContentLoaded
The DOMContentLoaded event is fired when the initial HTML document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading.

# load
The load event is fired when the whole page has loaded, including all dependent resources such as stylesheets and images.

# Difference
The main difference between the DOMContentLoaded and load events is that the DOMContentLoaded event is fired when the initial HTML document has been completely loaded and parsed, while the load event is fired when the whole page has loaded, including all dependent resources.
