---
title: What is the syntax for setting the value property in an angularjs ng-options directive?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can set the value property in AngularJS` ng-options by using the `track by` syntax.
---

**Contents**

[TOC]

1. Using an Object

In order to set the value property in AngularJS ng-options using an object, you can use the following syntax:

`<select ng-model="selectedItem" 
        ng-options="item.value as item.name for item in items">
</select>`

In this example, the value property of the object is set to the value of the item.name property.

2. Using an Array

In order to set the value property in AngularJS ng-options using an array, you can use the following syntax:

`<select ng-model="selectedItem" 
        ng-options="item as item for item in items">
</select>`

In this example, the value property of the array is set to the value of the item.

3. Using a Function

In order to set the value property in AngularJS ng-options using a function, you can use the following syntax:

`<select ng-model="selectedItem" 
        ng-options="itemFn(item) as item.name for item in items">
</select>`

In this example, the value property of the array is set to the return value of the itemFn() function.

4. Using a Constant Value

In order to set the value property in AngularJS ng-options using a constant value, you can use the following syntax:

`<select ng-model="selectedItem" 
        ng-options="'constant' as item.name for item in items">
</select>`

In this example, the value property of the array is set to the constant value 'constant'.
