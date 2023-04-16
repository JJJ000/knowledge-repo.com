---
title: Triggering jquery events on checkbox change and click
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The jQuery change and click events can be triggered by using the jQuery .change() and .click() methods, respectively.
---

**Contents**

[TOC]

## jQuery Change Event
The jQuery change event is triggered when the value of an element has been changed. It is supported by most of the form elements like input, select, and textarea.

Syntax:
```
$(selector).change(function)
```

Example:
```
$("input[type='checkbox']").change(function() {
   alert("The checkbox's value has been changed.");
});
```

## jQuery Click Event
The jQuery click event is triggered when an element is clicked. It is supported by all HTML elements.

Syntax:
```
$(selector).click(function)
```

Example:
```
$("input[type='checkbox']").click(function() {
   alert("The checkbox has been clicked.");
});
```
