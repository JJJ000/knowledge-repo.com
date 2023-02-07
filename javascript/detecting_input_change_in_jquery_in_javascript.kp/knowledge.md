---
title: What is the process for detecting changes in user input using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the jQuery .change() event to detect changes in input fields.
---

**Contents**

[TOC]

# Section 1: Detecting Input Change

In jQuery, detecting an input change can be done by using the `.change()` method. This method is used to detect changes to the value of an input element, such as when the user types in a new value.

# Section 2: Syntax

The syntax for the `.change()` method is as follows:

```
$(selector).change(function() {
    // code to be executed when an input value changes
});
```

# Section 3: Example

The following example shows how to detect when the value of an input element has changed:

```
$('#myInput').change(function() {
    alert('The value of the input has changed!');
});
```

# Section 4: Event Delegation

It is also possible to use event delegation to detect an input change. This means that the `.change()` method can be applied to an ancestor element of the input element, and the event will be triggered when the value of the input element is changed. The following example shows how to do this:

```
$('#myForm').change(function() {
    alert('The value of the input has changed!');
});
```
