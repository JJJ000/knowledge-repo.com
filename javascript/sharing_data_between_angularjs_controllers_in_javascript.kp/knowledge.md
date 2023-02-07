---
title: Exchange information between angularjs controllers
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: AngularJS controllers can share data by using a shared service or by using the $rootScope object.
---

**Contents**

[TOC]

# Option 1: Using a Service

A service is a singleton object that can be used to store and share data between controllers. Services are usually injected into controllers using the AngularJS dependency injection system.

# Option 2: Using $rootScope

$rootScope is the parent scope of all other scopes in an AngularJS application. Data can be stored on the $rootScope object and accessed in any controller.

# Option 3: Using Events

AngularJS provides an event system which allows data to be shared between controllers. Events can be broadcast or emitted from one controller and listened for in another.

# Option 4: Using Local Storage

Local storage can be used to persist data between controllers. Data is stored in the browser and can be accessed from any controller.
