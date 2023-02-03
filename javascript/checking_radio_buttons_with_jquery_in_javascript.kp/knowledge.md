---
title: What is the jquery code to select a radio button?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the jQuery .prop() method to check a radio button with jQuery in JavaScript.
---

**Contents**

[TOC]

1. Select the Radio Element
2. Set the Checked Attribute

#### 1. Select the Radio Element

To select a radio button with jQuery, use the `$()` function to select the radio element.

```javascript
var radioElement = $('input[type="radio"]');
```

#### 2. Set the Checked Attribute

Once the radio element is selected, use the `attr()` method to set the `checked` attribute.

```javascript
radioElement.attr('checked', 'checked');
```

Alternatively, you can use the `prop()` method to set the `checked` property.

```javascript
radioElement.prop('checked', true);
```
