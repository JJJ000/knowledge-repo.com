---
title: What are the drawbacks of using document.write?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Document.write can overwrite the entire page, making it difficult to debug and maintain.
---

**Contents**

[TOC]

# Poor Performance

Document.write is a poor choice for performance because it can only be used during the page loading process. When the page is already loaded and the user is interacting with it, document.write will not work. This means that any updates to the page must be done manually, which can be time consuming and inefficient.

# Poor Usability

Document.write can also be difficult to use and can lead to unexpected results. For example, it may overwrite existing HTML, which can cause unexpected changes to the page layout. This can be especially problematic if the page layout is complex.

# Poor Readability

Document.write can also make code difficult to read and understand. It can add unnecessary complexity to the code and make it difficult for other developers to understand.

# Poor Maintainability

Document.write can also make it difficult to maintain code. If the code needs to be changed or updated, it can be difficult to track down all the places where document.write is used. This can lead to bugs and other issues that can be difficult to debug.
