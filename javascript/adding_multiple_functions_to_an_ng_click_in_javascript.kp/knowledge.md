---
title: What is the best way to include multiple functions within a single ng-click?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use an anonymous function to call multiple functions within an ng-click.
---

**Contents**

[TOC]

1. Using `$scope.functionName = function() {...}`

The simplest way to add multiple functions to one ng-click is to define the function on the `$scope` object. This way, each function can be added as an attribute on the `$scope` object, and then referenced in the ng-click directive.

For example, to add two functions to an ng-click, the code would look like this:

```javascript
$scope.function1 = function() {
    // function1 code
};

$scope.function2 = function() {
    // function2 code
};

<button ng-click="function1(); function2();">Click Me</button>
```

2. Using `$scope.functions = {...}`

Another way to add multiple functions to an ng-click is to create an object on the `$scope` object, and then add each function as an attribute on the object.

For example, to add two functions to an ng-click, the code would look like this:

```javascript
$scope.functions = {
    function1: function() {
        // function1 code
    },
    function2: function() {
        // function2 code
    }
};

<button ng-click="functions.function1(); functions.function2();">Click Me</button>
```

3. Using `$scope.callFunction = function(funcName) {...}`

A third way to add multiple functions to an ng-click is to create a single function on the `$scope` object that takes a function name as an argument. This function can then be used to call any of the other functions defined on the `$scope` object.

For example, to add two functions to an ng-click, the code would look like this:

```javascript
$scope.function1 = function() {
    // function1 code
};

$scope.function2 = function() {
    // function2 code
};

$scope.callFunction = function(funcName) {
    if (funcName in $scope) {
        $scope[funcName]();
    }
};

<button ng-click="callFunction('function1'); callFunction('function2');">Click Me</button>
```

4. Using `$scope.execute = function(func) {...}`

The fourth way to add multiple functions to an ng-click is to create a single function on the `$scope` object that takes a function as an argument. This function can then be used to call any function passed to it.

For example, to add two functions to an ng-click, the code would look like this:

```javascript
$scope.function1 = function() {
    // function1 code
};

$scope.function2 = function() {
    // function2 code
};

$scope.execute = function(func) {
    func();
};

<button ng-click="execute(function1); execute(function2);">Click Me</button>
```
