---
title: Using ng-options in angularjs to work with selections
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: ng-options allows you to bind the select element to an array of values in the controller, and dynamically generate the options in the select element using AngularJS expressions.
---

**Contents**

[TOC]

**Section 1: Overview**

AngularJS's ng-options directive is an essential part of working with select elements in Javascript. It allows developers to easily create dynamic select elements with options populated from an array or object. This allows developers to quickly create select elements that are populated with data from an API or other data source. 

**Section 2: Syntax**

The syntax for working with ng-options is as follows:

`<select ng-model="selected" ng-options="option.value as option.name for option in options">`

The ng-model directive is used to bind the selected value to a variable in the scope. The ng-options directive is used to iterate over an array or object and create options in the select element. The syntax is as follows:

`option.value as option.name for option in options`

The option.value is the value that will be set when an option is selected. The option.name is the text that will be displayed as the option in the select element. The for option in options is the array or object that contains the data that will be used to populate the select element.

**Section 3: Example**

Here is an example of using ng-options to create a select element with options populated from an array:

```
<select ng-model="selected" ng-options="option.value as option.name for option in options">
  <option value="">Select an option</option>
</select>

<script>
  var app = angular.module('myApp', []);
  app.controller('MyCtrl', function($scope) {
    $scope.options = [
      { value: '1', name: 'Option 1' },
      { value: '2', name: 'Option 2' },
      { value: '3', name: 'Option 3' }
    ];
  });
</script>
```

**Section 4: Conclusion**

In conclusion, ng-options is an essential part of working with select elements in Javascript. It allows developers to quickly create dynamic select elements with options populated from an array or object. With the use of ng-options, developers can easily create select elements that are populated with data from an API or other data source.
