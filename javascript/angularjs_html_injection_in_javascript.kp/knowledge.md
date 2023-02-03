---
title: Add html to the view from an angularjs controller
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: AngularJS controllers can use the $scope object to insert HTML into the view by setting the $scope.html variable.
---

**Contents**

[TOC]

## Section 1: HTML

The HTML to be inserted into the view can be written directly in the HTML template, or it can be written in the AngularJS controller in the form of a string. The HTML string can be added to the view using the `ng-bind-html` directive.

## Section 2: AngularJS Controller

In the AngularJS controller, the HTML string can be created using the `$sce` service. The `$sce.trustAsHtml()` method can be used to create a trusted HTML string from a regular string.

```
$scope.myHtmlString = $sce.trustAsHtml('<p>This is my HTML string</p>');
```

## Section 3: HTML Template

In the HTML template, the `ng-bind-html` directive can be used to bind the HTML string to the view.

```
<div ng-bind-html="myHtmlString"></div>
```

## Section 4: Result

The result of the code will be the HTML string being added to the view.

```
<div>
  <p>This is my HTML string</p>
</div>
```
