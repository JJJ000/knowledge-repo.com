---
title: What is the process for including a conditional attribute in angular 2?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the NgIf directive to add conditional attributes in Angular 2.
---

**Contents**

[TOC]

## Section 1: Import the Directive

In order to add a conditional attribute in Angular 2, you must first import the directive from the @angular/common library. This directive is called NgClass.

## Section 2: Create an Object

The next step is to create an object that will contain the attributes and values that you want to be conditionally applied. This object should be created as a variable in the component class.

## Section 3: Use NgClass Directive

Once the object has been created, you can use the NgClass directive to conditionally apply the attributes and values to the element. The NgClass directive takes an object as an argument and will apply the attributes and values to the element when the condition is met.

## Section 4: Example Usage

For example, if you wanted to conditionally apply a class to a button if a certain condition is met, you would use the following syntax:

```html
<button [ngClass]="{'my-class': condition}">My Button</button>
```

In this example, the class "my-class" will be applied to the button when the condition is true.
