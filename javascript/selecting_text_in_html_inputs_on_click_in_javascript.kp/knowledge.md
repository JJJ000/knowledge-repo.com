---
title: When an html text input is clicked, all of the text inside it will be highlighted
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To select all text in an HTML text input when clicked, use the `select()` method.
---

**Contents**

[TOC]

**Solution**

**Section 1: Adding an onClick Event Listener to the HTML Text Input**

We can add an onClick event listener to the HTML text input that will trigger a JavaScript function when clicked.

```html
<input type="text" id="textInput" onClick="selectAllText()">
```

**Section 2: Creating the JavaScript Function**

We can create the JavaScript function that will be triggered when the HTML text input is clicked. This function will select all the text in the text input.

```javascript
function selectAllText() {
  document.getElementById("textInput").select();
}
```

**Section 3: Testing the Function**

We can test the function by clicking on the HTML text input. The text should be selected when clicked.

**Section 4: Conclusion**

In conclusion, we can select all the text in an HTML text input when clicked by adding an onClick event listener to the HTML text input and creating a JavaScript function to select all the text.
