---
title: What is the best way to set a default value in an angular.js select box?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Set the `ng-model` attribute to a default value to have a default option in an Angular.js select box.
---

**Contents**

[TOC]

##### Setting Default Value

1. In the controller, set a variable to the value of the default option.

```javascript
$scope.selectedOption = 'default';
```

2. In the view, bind the variable to the select box.

```html
<select ng-model="selectedOption">
  <option value="default">Default</option>
  <option value="option1">Option 1</option>
  <option value="option2">Option 2</option>
</select>
```

##### Setting Default Option as Selected

1. In the view, add the `selected` attribute to the default option.

```html
<select ng-model="selectedOption">
  <option value="default" selected>Default</option>
  <option value="option1">Option 1</option>
  <option value="option2">Option 2</option>
</select>
```

2. In the controller, set the variable to the value of the default option.

```javascript
$scope.selectedOption = 'default';
```
