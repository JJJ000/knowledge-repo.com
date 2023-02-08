---
title: What is the procedure for verifying if a checkbox has been selected?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the `.checked` property to check if a checkbox is checked in JavaScript.
---

**Contents**

[TOC]

## Using the Checked Property

The simplest way to check if a checkbox is checked is to use the `checked` property of the checkbox element. This property is a boolean that specifies whether the checkbox is checked or not.

```javascript
let checkbox = document.querySelector("input[type=checkbox]");

if (checkbox.checked) {
  // The checkbox is checked!
}
```

## Using the Click Event

You can also check if a checkbox is checked by using a click event listener on the checkbox. This will allow you to detect when the user has clicked the checkbox and perform an action accordingly.

```javascript
let checkbox = document.querySelector("input[type=checkbox]");

checkbox.addEventListener('click', function() {
  if (checkbox.checked) {
    // The checkbox is checked!
  }
});
```

## Using the Change Event

Another way to check if a checkbox is checked is to use the `change` event listener. This event will fire whenever the checked state of the checkbox changes, either when the user clicks the checkbox or when the `checked` property is changed programmatically.

```javascript
let checkbox = document.querySelector("input[type=checkbox]");

checkbox.addEventListener('change', function() {
  if (checkbox.checked) {
    // The checkbox is checked!
  }
});
```

## Using the Onchange Attribute

You can also use the `onchange` attribute to check if a checkbox is checked. This attribute will fire an event whenever the checked state of the checkbox changes.

```html
<input type="checkbox" onchange="checkboxChanged()" />

<script>
  function checkboxChanged() {
    let checkbox = document.querySelector("input[type=checkbox]");
    if (checkbox.checked) {
      // The checkbox is checked!
    }
  }
</script>
```
