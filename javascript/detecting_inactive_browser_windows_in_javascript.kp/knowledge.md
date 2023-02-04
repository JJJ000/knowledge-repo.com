---
title: How can I tell if a browser window is inactive?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: No, there is not a way to detect if a browser window is not currently active in Javascript.
---

**Contents**

[TOC]

## Checking Document Visibility

The `document.hidden` property can be used to detect if a browser window is not currently active. This property returns a boolean value (`true` or `false`) depending on the visibility of the document. If the document is visible, the value will be `false`. If the document is hidden, the value will be `true`.

## Event Listener

In addition to checking the `document.hidden` property, an event listener can be used to detect when a browser window is not currently active. The `visibilitychange` event is fired when the document's visibility state changes. This event can be used to detect when a browser window is not currently active.

## Browser Support

The `document.hidden` property and the `visibilitychange` event are supported in most modern browsers, including Chrome, Firefox, Safari, and Edge.

## Conclusion

To detect if a browser window is not currently active, the `document.hidden` property and the `visibilitychange` event can be used. Both of these are supported in most modern browsers.
