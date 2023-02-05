---
title: Code required to prevent a 'frame buster buster' from functioning
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: A buster code in Javascript is a script that prevents a page from being framed or embedded into another page.
---

**Contents**

[TOC]

# Section 1: What is a Frame Buster?
A frame buster is a type of JavaScript code that prevents a web page from being displayed inside a frame or iframe element on another web page. It is often used to prevent clickjacking attacks, where malicious code is injected into a web page and then displayed within an iframe on another page.

# Section 2: How Does a Frame Buster Work?
A frame buster works by detecting when a page is being embedded in a frame or iframe element on another page. When this is detected, the frame buster code will redirect the page to the top-level window, so that the page is no longer embedded in the frame. This helps to prevent malicious code from being injected into the page and displayed in the frame.

# Section 3: What Does a Frame Buster Look Like?
A frame buster typically looks like this:

```
if (top != self) {
  top.location.replace(self.location.href);
}
```

# Section 4: How to Implement a Frame Buster
To implement a frame buster, add the code above to the head section of the page that you want to protect. This code will detect if the page is being embedded in a frame or iframe element, and redirect the page to the top-level window if it is. This will help to protect the page from malicious code being injected into it and displayed in the frame.
