---
title: What is the process for connecting a list of checkbox values with angularjs?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the ng-model directive to bind the list of checkbox values to a variable in the scope.
---

**Contents**

[TOC]

1. Setting Up the HTML 

First, you will need to set up the HTML page with the necessary checkboxes and associated values. You can create a list of checkboxes with the following code:

```html
<input type="checkbox" ng-model="myCheckbox" value="Option1" />Option1
<input type="checkbox" ng-model="myCheckbox" value="Option2" />Option2
<input type="checkbox" ng-model="myCheckbox" value="Option3" />Option3
```

2. Creating the AngularJS Model 

Next, you will need to create an AngularJS model to bind the checkbox values to. You can do this by creating a variable in the controller, and then assigning the checkbox values to it. For example,

```javascript
$scope.myCheckbox = [];
```

3. Binding the Values 

Once you have set up the HTML page and created the AngularJS model, you can bind the checkbox values to the model. You can do this by using the ng-model directive in the HTML page. For example,

```html
<input type="checkbox" ng-model="myCheckbox" value="Option1" />Option1
<input type="checkbox" ng-model="myCheckbox" value="Option2" />Option2
<input type="checkbox" ng-model="myCheckbox" value="Option3" />Option3
```

4. Accessing the Values 

Finally, you can access the checkbox values from the AngularJS model. You can do this by using the $scope.myCheckbox variable. For example,

```javascript
var checkedValues = $scope.myCheckbox;
```
