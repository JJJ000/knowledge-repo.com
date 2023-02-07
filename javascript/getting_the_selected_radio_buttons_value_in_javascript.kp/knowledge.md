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
tldr: The selected radio button`s value can be retrieved using the `value` property of the radio button element.
---

**Contents**

[TOC]

# Section 1: Selecting the Radio Button

In order to get the value of the selected radio button, the radio button must first be selected. This can be done using the `.checked` method. This will return `true` if the radio button is selected, and `false` if it is not.

# Section 2: Getting the Value

Once the radio button is selected, the value of the radio button can be retrieved using the `.value` method. This will return the value associated with the radio button.

# Section 3: Putting It All Together

In order to get the value of the selected radio button, the following code can be used:

```javascript
var radios = document.getElementsByName('name');

for (var i = 0, length = radios.length; i < length; i++) {
   if (radios[i].checked) {
       // do whatever you want with the checked radio
       var value = radios[i].value;

       // only one radio can be logically checked, don't check the rest
       break;
   }
}
```

# Section 4: Conclusion

In conclusion, the value of the selected radio button can be retrieved using the `.checked` and `.value` methods. By looping through all the available radio buttons and checking which one is selected, the value of the selected radio button can be retrieved.
