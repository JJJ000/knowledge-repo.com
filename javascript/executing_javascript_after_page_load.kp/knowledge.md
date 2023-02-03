---
title: What is the process for running JavaScript after the page has loaded?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the window.onload event handler to execute JavaScript after the page has loaded.
---

**Contents**

[TOC]

## Using the window.onload Event
The `window.onload` event is triggered when the page has finished loading. This event is often used to perform actions after the page has loaded, such as setting the page title, displaying a message, or running a script.

To use the `window.onload` event, add an event listener to the `window` object:

```javascript
window.addEventListener('load', myFunction);
```

The `myFunction` function will be called when the page has finished loading.

## Using the document.ready Event
The `document.ready` event is triggered when the DOM (Document Object Model) is ready to be manipulated. This event is often used to perform actions after the DOM has been fully loaded, such as setting the page title, displaying a message, or running a script.

To use the `document.ready` event, add an event listener to the `document` object:

```javascript
document.addEventListener('ready', myFunction);
```

The `myFunction` function will be called when the DOM is ready to be manipulated.

## Using the jQuery ready Event
If you are using the jQuery library, you can use the `ready` event to execute code after the page has loaded.

To use the `ready` event, call the `ready` function on the `$` object:

```javascript
$(document).ready(myFunction);
```

The `myFunction` function will be called when the page has finished loading.
