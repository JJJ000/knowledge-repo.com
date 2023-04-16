---
title: Jquery event for changing the checked state of a checkbox
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The `change` event can be used to detect when the checked state of a checkbox has changed in JavaScript.
---

**Contents**

[TOC]

1. Introduction 
Checkboxes are HTML elements that allow users to select one or more options from a set of predefined choices. The checked state of a checkbox can be changed by the user or programmatically. When the state of a checkbox is changed, an event is triggered that can be handled in JavaScript.

2. jQuery Event Handler
jQuery provides a convenient way to bind a function to an event handler for a checkbox. The `.change()` event handler can be used to detect when the checked state of a checkbox has changed. The syntax for this event handler is as follows:

```
$(selector).change(function() {
  // code to be executed when the checked state changes
});
```

3. JavaScript Event Handler
The `onchange` event handler can also be used to detect when the checked state of a checkbox has changed. The syntax for this event handler is as follows:

```
document.querySelector(selector).onchange = function() {
  // code to be executed when the checked state changes
});
```

4. Conclusion
In summary, the checked state of a checkbox can be detected in either jQuery or JavaScript using the `.change()` or `onchange` event handlers, respectively. By binding a function to these event handlers, code can be executed when the checked state of a checkbox is changed.
