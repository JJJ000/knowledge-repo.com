---
title: What key triggered the jquery event keypress?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The key that was pressed in Javascript can be determined by using the event.which or event.keyCode properties of the event object.
---

**Contents**

[TOC]

### Event Properties

The `keypress` event includes the following properties:

- `key`: The character code of the pressed key.
- `charCode`: The Unicode character code of the pressed key.
- `which`: The Unicode character code of the pressed key, same as `charCode`.

### Event Methods

The `keypress` event includes the following methods:

- `getCharCode()`: Returns the Unicode character code of the pressed key.
- `getKeyCode()`: Returns the character code of the pressed key.

### Examples

To get the character code of the pressed key, you can use the `getCharCode()` method:

```javascript
$('#myInput').keypress(function(e){
    var charCode = e.getCharCode();
    // do something with the charCode
});
```

To get the character code of the pressed key, you can use the `getKeyCode()` method:

```javascript
$('#myInput').keypress(function(e){
    var keyCode = e.getKeyCode();
    // do something with the keyCode
});
```
