---
title: Rewording 'script tag - async & defer' would be 'incorporating asynchronous & deferred script tags'
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Async and defer are HTML attributes used to indicate to the browser that the script should be executed asynchronously or deferred until the page has finished loading.
---

**Contents**

[TOC]

#### What is a Script Tag?
A script tag is an HTML element used to define a client-side script, such as a JavaScript. It is placed in the <head> or <body> of an HTML document.

#### What are async and defer?
The async and defer attributes are boolean attributes that can be added to script tags in HTML. They indicate to the browser whether or not to execute the script as soon as it is encountered in the document, or to wait until the HTML document has been parsed.

#### What does async do?
The async attribute tells the browser to execute the script as soon as it is encountered, without waiting for the HTML document to finish parsing. This can be useful for scripts that do not depend on any other scripts or the HTML document structure.

#### What does defer do?
The defer attribute tells the browser to wait until the HTML document has been completely parsed before executing the script. This can be useful for scripts that depend on other scripts or the HTML document structure.
