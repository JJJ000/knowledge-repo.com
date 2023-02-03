---
title: Determine if a checkbox has been selected using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: To check if a checkbox is checked with jQuery, use the .is(`checked`) method.
---

**Contents**

[TOC]

# Method 1

Using the `:checked` selector:

```javascript
if ($('input[type="checkbox"]').is(':checked')) {
    // Checkbox is checked.
} else {
    // Checkbox is not checked.
}
```

# Method 2

Using the `.prop()` method:

```javascript
if ($('input[type="checkbox"]').prop('checked')) {
    // Checkbox is checked.
} else {
    // Checkbox is not checked.
}
```

# Method 3

Using the `.attr()` method:

```javascript
if ($('input[type="checkbox"]').attr('checked')) {
    // Checkbox is checked.
} else {
    // Checkbox is not checked.
}
```

# Method 4

Using the `.val()` method:

```javascript
if ($('input[type="checkbox"]').val() == 'checked') {
    // Checkbox is checked.
} else {
    // Checkbox is not checked.
}
```
