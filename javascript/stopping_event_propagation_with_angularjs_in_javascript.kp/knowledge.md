---
title: Preventing angularjs ng-click event propagation
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Using `event.stopPropagation()` in the ng-click expression will prevent the event from bubbling up the DOM tree.
---

**Contents**

[TOC]

#### Stopping Propagation with AngularJS

The ng-click directive in AngularJS provides a way to prevent the propagation of click events when an element is clicked. To do this, the ng-click directive must be used in conjunction with the $event object, which is a built-in object in AngularJS. 

#### Using $event Object

The $event object is used to access the event object that is passed to the ng-click function. This event object can then be used to call the stopPropagation() method, which will prevent the click event from propagating up the DOM tree.

#### Example

For example, if we have the following HTML code:

```html
<div ng-click="doSomething($event)">
  <button>Click Me</button>
</div>
```

We can add the stopPropagation() method to the doSomething() function in the controller:

```javascript
$scope.doSomething = function(event) {
  // Do something
  event.stopPropagation();
};
```

This will prevent the click event from propagating up the DOM tree when the button is clicked.
