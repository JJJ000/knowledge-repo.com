---
title: Creating a dialogue with "ok" and "cancel" options
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: A dialog with `Ok` and `Cancel` options can be created in Javascript using the window.confirm() method.
---

**Contents**

[TOC]

# Section 1: Create the Dialog

The most basic way to create a dialog with "Ok" and "Cancel" options in Javascript is to use the `confirm()` function. This function will display a dialog with the specified message, as well as two buttons: one for "Ok" and one for "Cancel".

# Section 2: Invoke the Dialog

To invoke the dialog, you need to call the `confirm()` function and pass in the message you want to display. For example:

```javascript
var result = confirm("Are you sure you want to proceed?");
```

# Section 3: Handle the Response

The `confirm()` function will return a boolean value indicating whether the user clicked "Ok" or "Cancel". If the user clicked "Ok", the function will return `true`. If the user clicked "Cancel", the function will return `false`.

# Section 4: React to the Response

Once you have the response from the user, you can use it to determine how to proceed. For example:

```javascript
if (result) {
  // User clicked "Ok"
  // Do something...
} else {
  // User clicked "Cancel"
  // Do something else...
}
```
