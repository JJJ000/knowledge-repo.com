---
title: What is the syntax to determine if a checkbox is selected using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the jQuery .is() method to check if a checkbox is checked.
---

**Contents**

[TOC]

### Using the `:checked` Selector

The simplest and most reliable way to check if a checkbox is checked is to use the `:checked` selector. This selector will return true only if the checkbox is checked.

```
if ($('input[type="checkbox"]').is(':checked')) {
    alert('Checkbox is checked.');
}
```

### Using the `.prop()` Method

The `.prop()` method can also be used to check if a checkbox is checked. This method will return true if the checkbox is checked and false if it is not.

```
if ($('input[type="checkbox"]').prop('checked')) {
    alert('Checkbox is checked.');
}
```

### Using the `.attr()` Method

The `.attr()` method can also be used to check if a checkbox is checked. This method will return a string with the value of the attribute if the checkbox is checked and undefined if it is not.

```
if ($('input[type="checkbox"]').attr('checked')) {
    alert('Checkbox is checked.');
}
```

### Using the `.val()` Method

The `.val()` method can also be used to check if a checkbox is checked. This method will return the value of the checkbox if it is checked and undefined if it is not.

```
if ($('input[type="checkbox"]').val()) {
    alert('Checkbox is checked.');
}
```
