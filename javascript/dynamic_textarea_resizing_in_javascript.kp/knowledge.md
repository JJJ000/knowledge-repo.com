---
title: Generating a text box with the ability to automatically adjust its size
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Create an element with a textarea tag, set its overflow to auto, and set its rows attribute to 1.
---

**Contents**

[TOC]

**Section 1: Create the Textarea**

To create the textarea, we can use the HTML `<textarea>` element. This element requires two attributes: `rows` and `cols`, which dictate the size of the textarea.

```
<textarea rows="5" cols="50"></textarea>
```

**Section 2: Add the Event Handler**

In order to auto-resize the textarea, an event handler needs to be added to listen for changes. We can use the `oninput` event handler, which will trigger whenever the contents of the textarea change.

```
<textarea rows="5" cols="50" oninput="resizeTextarea(this)"></textarea>
```

**Section 3: Write the Resize Function**

Now that the event handler is in place, we need to write the `resizeTextarea()` function. This function should take the textarea element as an argument and adjust the size of the textarea based on the contents.

```javascript
function resizeTextarea(textarea) {
  // Adjust the size of the textarea
}
```

**Section 4: Adjust the Size**

To adjust the size of the textarea, we can use the `scrollHeight` property, which returns the total height of the textarea in pixels. We can then set the `rows` attribute of the textarea to match the `scrollHeight`, which will automatically resize the textarea.

```javascript
function resizeTextarea(textarea) {
  textarea.rows = textarea.scrollHeight;
}
```
