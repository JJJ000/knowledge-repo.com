---
title: Retrieve the highlighted/selected text
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The selected text can be retrieved using the window.getSelection() method.
---

**Contents**

[TOC]

## Getting Selected Text

To get the highlighted/selected text, we can use the `window.getSelection()` method. This method returns a `Selection` object, which contains the text that is currently selected by the user.

## Accessing the Selected Text

Once we have the `Selection` object, we can use the `Selection.toString()` method to get the text that is currently selected. This method returns a string containing the text that is currently selected.

## Checking for Selection

Before we can use the `Selection` object, we need to make sure that the user has actually selected some text. To do this, we can use the `Selection.isCollapsed` property. If this property returns `true`, then the user has not selected any text and we can't use the `Selection` object.

## Example

Here is an example of how we can use the `window.getSelection()` method to get the currently selected text:

```javascript
let selection = window.getSelection();

if (!selection.isCollapsed) {
  let selectedText = selection.toString();
  // Do something with the selected text
}
```
