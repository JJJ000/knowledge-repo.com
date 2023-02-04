---
title: Determining if a checkbox has been selected using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: To test if a checkbox is checked with jQuery, use the .is(`checked`) method.
---

**Contents**

[TOC]

## Checking a Checkbox

The simplest way to check if a checkbox is checked using jQuery is with the `:checked` selector. This selector will return true if the checkbox is checked and false if it is not.

```javascript
if ($('#checkbox').is(':checked')) {
    // code to execute if checkbox is checked
}
```

## Unchecking a Checkbox

To uncheck a checkbox using jQuery, use the `prop` method to set the `checked` property to `false`.

```javascript
$('#checkbox').prop('checked', false);
```

## Toggling a Checkbox

To toggle a checkbox using jQuery, use the `prop` method to set the `checked` property to `true` or `false`.

```javascript
$('#checkbox').prop('checked', !$('#checkbox').is(':checked'));
```

## Event Listening

To listen for a change in the state of a checkbox, you can use the `change` event listener. This listener will fire whenever the checkbox is checked or unchecked.

```javascript
$('#checkbox').change(function() {
    if ($(this).is(':checked')) {
        // code to execute if checkbox is checked
    }
});
```
