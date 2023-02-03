---
title: Utilizing $scope.$emit and $scope.$on
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: $scope.$emit and $scope.$on allow components to communicate with each other by emitting and listening for events.
---

**Contents**

[TOC]

### What are $scope.$emit and $scope.$on?
$scope.$emit and $scope.$on are two methods that are used to communicate between controllers in AngularJS. $scope.$emit is used to send an event up the scope hierarchy, while $scope.$on is used to listen for events emitted by $scope.$emit.

### How do they Work?
$scope.$emit will send an event up the scope hierarchy, starting from the current scope. Any parent scopes of the current scope will be able to listen for the event using $scope.$on. When an event is emitted, any $scope.$on listeners will be triggered and can take action based on the event.

### When to Use $scope.$emit and $scope.$on
$scope.$emit and $scope.$on are useful for communicating between controllers in an AngularJS application. For example, if one controller needs to update the data in another controller, it can emit an event with the new data and the other controller can listen for the event and update its data accordingly.

### Example
For example, if one controller needs to update the data in another controller, it can emit an event with the new data and the other controller can listen for the event and update its data accordingly.

Controller A:
```
$scope.$emit('updateData', newData);
```

Controller B:
```
$scope.$on('updateData', function(event, data) {
    $scope.data = data;
});
```
