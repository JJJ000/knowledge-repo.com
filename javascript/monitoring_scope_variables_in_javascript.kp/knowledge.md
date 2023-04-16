---
title: Observe multiple variables within the scope
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can watch multiple $scope attributes in Javascript by using the $scope.$watchGroup() method.
---

**Contents**

[TOC]

#### Using $watch

The `$scope.$watch` function allows you to watch multiple scope variables. It takes two parameters: a scope variable and a callback function. The callback function will be called whenever the scope variable changes.

#### Using $watchGroup

The `$scope.$watchGroup` function allows you to watch multiple scope variables at once. It takes an array of scope variables and a callback function. The callback function will be called whenever any of the scope variables change.

#### Using $watchCollection

The `$scope.$watchCollection` function allows you to watch multiple scope variables in a collection. It takes two parameters: a scope variable and a callback function. The callback function will be called whenever the scope variable changes.

#### Using $watchSet

The `$scope.$watchSet` function allows you to watch multiple scope variables in a set. It takes two parameters: a scope variable and a callback function. The callback function will be called whenever the scope variable changes.
