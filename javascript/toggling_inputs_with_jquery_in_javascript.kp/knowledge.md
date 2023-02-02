---
title: How to use jquery to turn an input on or off?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: $(`input`).prop(`disabled`, true/false);
---

**Contents**

[TOC]

1. **Accessing the Element**

To access the element, you can use the `$()` jQuery function to select it. For example, if you wanted to access an input with the ID `myInput`, you can use the following code:

```javascript
const myInput = $('#myInput');
```

2. **Disabling an Input**

Once you have the element, you can use the `prop()` function to set the `disabled` property to `true`. This will disable the input.

```javascript
myInput.prop('disabled', true);
```

3. **Enabling an Input**

To enable the input, you can use the same `prop()` function, but set the `disabled` property to `false`.

```javascript
myInput.prop('disabled', false);
```

4. **Toggling an Input**

If you want to toggle the input between enabled and disabled, you can use the `prop()` function with the `toggle` argument. This will toggle the `disabled` property between `true` and `false`.

```javascript
myInput.prop('disabled', 'toggle');
```
