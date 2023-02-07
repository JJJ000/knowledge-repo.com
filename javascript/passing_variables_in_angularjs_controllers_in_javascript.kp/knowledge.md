---
title: What is the best way to transfer data between angularjs controllers?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Variables can be passed between controllers using the $rootScope service.
---

**Contents**

[TOC]

## 1. Using Services

One way to pass variables between controllers in AngularJS is to use services. Services are singleton objects that are created once and can be used by any controller in an application. Services can be used to pass data between controllers by storing the data in a service and then injecting the service into both controllers.

## 2. Using $rootScope

Another way to pass variables between controllers in AngularJS is to use the $rootScope service. The $rootScope is a global scope that is accessible from any controller in an application. Variables can be stored in the $rootScope and then accessed by any controller.

## 3. Using $emit and $broadcast

A third way to pass variables between controllers in AngularJS is to use the $emit and $broadcast methods. The $emit method is used to send an event from a controller to its parent controller, while the $broadcast method is used to send an event from a controller to its child controllers. Both methods can be used to pass data between controllers.

## 4. Using $location

A fourth way to pass variables between controllers in AngularJS is to use the $location service. The $location service allows you to set query parameters in the URL. These query parameters can be accessed by any controller in the application and used to pass data between controllers.
