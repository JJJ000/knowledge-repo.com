---
title: What is the process for adding an element after another element in JavaScript without using an external library?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Create a new element, use the insertAdjacentElement() method on the element you want to insert after, and pass in the new element as an argument.
---

**Contents**

[TOC]

**Section 1: Select the Element**

The first step to inserting an element after another element in JavaScript without using a library is to select the element that you want to insert the new element after. To do this, you can use the `document.querySelector()` method. This method takes a CSS selector as an argument, and returns the first element that matches the selector. For example, if you wanted to select the first `<p>` element on the page, you could use the following code:

```javascript
const myPara = document.querySelector('p');
```

**Section 2: Create the New Element**

The next step is to create the element that you want to insert. To do this, you can use the `document.createElement()` method. This method takes a tag name as an argument, and returns a new element with the specified tag name. For example, if you wanted to create a new `<div>` element, you could use the following code:

```javascript
const myDiv = document.createElement('div');
```

**Section 3: Insert the Element**

Once you have selected the element that you want to insert the new element after, and created the new element, you can insert the element using the `Element.insertAdjacentElement()` method. This method takes two arguments: a position and an element. The position argument specifies where the new element should be inserted relative to the element that you are inserting it after. For example, if you wanted to insert the new element after the element that you selected, you could use the following code:

```javascript
myPara.insertAdjacentElement('afterend', myDiv);
```

**Section 4: Test the Result**

Once you have inserted the element, you should test the result to make sure that it was inserted correctly. To do this, you can use the `Element.nextElementSibling` property to check that the element that you inserted is the next element after the element that you inserted it after. For example, if you wanted to check that the `myDiv` element was inserted correctly after the `myPara` element, you could use the following code:

```javascript
if (myPara.nextElementSibling === myDiv) {
  console.log('Element inserted successfully!');
}
```
