---
title: What is the value of the selected radio button?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `checked` property of the selected radio button to get its value.
---

**Contents**

[TOC]

# Section 1: Selecting the Radio Button

To get the value of the selected radio button, we first need to access it. To do this, we can use the `querySelector` method to select the radio button by its name attribute.

```
let radioButton = document.querySelector('input[name="radioName"]:checked');
```

# Section 2: Retrieving the Value

Once we have the radio button element, we can use the `value` property to get its value.

```
let radioValue = radioButton.value;
```

# Section 3: Setting the Value

We can also set the value of the radio button using the `value` property.

```
radioButton.value = "newValue";
```

# Section 4: Checking for Selected Radio Button

Before retrieving or setting the value of the radio button, it's important to check if it is actually selected. We can do this by checking the `checked` property of the element.

```
if (radioButton.checked) {
  // Radio button is selected
}
```
