---
title: Adjusting the size of an iframe based on its content
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The size of an iframe can be dynamically adjusted by setting its width and height attributes in Javascript.
---

**Contents**

[TOC]

1. **Get the Content Height**

The first step to resizing an iframe based on its content is to get the content’s height. This can be done by accessing the `contentWindow` property of the iframe and then using the `.document` property to get the `documentElement` of the iframe. From there, the `.scrollHeight` property can be accessed to get the height of the content.

2. **Set the iframe Height**

Once the content height has been retrieved, the height of the iframe can be set to the content height. This can be done by setting the `.style.height` property of the iframe to the content height.

3. **Check for Resize**

It is important to check for any potential resizing of the content. This can be done by using an event listener for the `resize` event. When the event is fired, the content height should be checked again and the iframe height should be adjusted accordingly.

4. **Adjust the iframe Height**

Once the content height has been checked and the iframe needs to be resized, the `.style.height` property of the iframe can be set to the new content height. This will ensure that the iframe is resized properly to fit the content.
