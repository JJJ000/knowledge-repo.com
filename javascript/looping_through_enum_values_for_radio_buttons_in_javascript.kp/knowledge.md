---
title: What is the best way to iterate through the values of an enumeration to show them as radio buttons?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use a for loop to iterate through the enum values and create a radio button for each value.
---

**Contents**

[TOC]

**Section 1: Create an array of the enum values**

Enums are objects in JavaScript, so you can use the `Object.values()` method to get an array of all the values in the enum.

```javascript
// Create an array of all the enum values
let enumValues = Object.values(MyEnum);
```

**Section 2: Loop through the array**

Once you have an array of the enum values, you can loop through it to create the radio buttons.

```javascript
// Loop through the array of enum values
for (let value of enumValues) {
  // Create a radio button for each value
  let radioButton = document.createElement('input');
  radioButton.type = 'radio';
  radioButton.name = 'myEnum';
  radioButton.value = value;
  
  // Append the radio button to the DOM
  document.body.appendChild(radioButton);
}
```

**Section 3: Add labels for the radio buttons**

You can also add labels for each radio button to make it easier for users to understand what each option represents.

```javascript
// Loop through the array of enum values
for (let value of enumValues) {
  // Create a radio button for each value
  let radioButton = document.createElement('input');
  radioButton.type = 'radio';
  radioButton.name = 'myEnum';
  radioButton.value = value;
  
  // Create a label for the radio button
  let label = document.createElement('label');
  label.innerHTML = value;
  
  // Append the radio button and label to the DOM
  document.body.appendChild(radioButton);
  document.body.appendChild(label);
}
```

**Section 4: Group the radio buttons**

Finally, you can group the radio buttons together by adding a `<fieldset>` element and setting the `name` attribute of each radio button to the same value.

```javascript
// Create a fieldset element
let fieldset = document.createElement('fieldset');

// Loop through the array of enum values
for (let value of enumValues) {
  // Create a radio button for each value
  let radioButton = document.createElement('input');
  radioButton.type = 'radio';
  radioButton.name = 'myEnum';
  radioButton.value = value;
  
  // Create a label for the radio button
  let label = document.createElement('label');
  label.innerHTML = value;
  
  // Append the radio button and label to the fieldset
  fieldset.appendChild(radioButton);
  fieldset.appendChild(label);
}

// Append the fieldset to the DOM
document.body.appendChild(fieldset);
```
