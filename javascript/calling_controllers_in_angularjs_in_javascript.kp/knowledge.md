---
title: Is it possible for one angularjs controller to invoke another?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Yes, one AngularJS controller can call another using the $controller service.
---

**Contents**

[TOC]

Yes, one AngularJS controller can call another in Javascript.

## Using $scope

One way to call a controller from another is to use the `$scope` object. The `$scope` object is an object that is available to all controllers, and it allows communication between controllers. To call another controller, you can assign a function to the `$scope` object that is available to all controllers. The function can then be called from the other controller.

## Using Dependency Injection

Another way to call a controller from another is to use dependency injection. Dependency injection is a design pattern in which one object supplies the dependencies of another object. To call a controller from another, you can inject the controller into the other controller and then call the methods of the injected controller.

## Using Events

A third way to call a controller from another is to use events. Events are objects that allow objects to communicate with each other. To call a controller from another, you can emit an event from the first controller and then listen for the event in the other controller. When the event is emitted, the other controller can then execute its code.

## Using Services

A fourth way to call a controller from another is to use services. Services are objects that provide shared functionality between different components. To call a controller from another, you can create a service that contains the code that needs to be shared between the two controllers. The service can then be injected into both controllers, and the code can be executed from either controller.
