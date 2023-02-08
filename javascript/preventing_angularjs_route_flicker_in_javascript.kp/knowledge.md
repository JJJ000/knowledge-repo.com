---
title: Postpone the angularjs route transition until the model is fully loaded to avoid flickering
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the resolve property of the route to ensure that the model is loaded before the route is changed.
---

**Contents**

[TOC]

# Section 1: Overview 
AngularJS is a popular JavaScript framework for creating single-page applications. When using AngularJS, developers often utilize the routing feature to create a single-page application that allows users to navigate between different views. However, when changing routes, there can be a noticeable flicker effect as the page re-renders. This can be particularly noticeable when the page contains a large model that needs to be loaded before the route change can be completed. In this article, we will discuss how to delay the route change until the model is loaded in order to prevent this flicker. 

# Section 2: Preloading the Model
The first step in preventing the flicker effect is to preload the model before the route change takes place. This can be done by using a service to make an asynchronous call to the server to retrieve the model. This can be done in the controller that is responsible for handling the route change. Once the model is retrieved, it can be stored in the service and referenced later when the route is changed.

# Section 3: Delaying the Route Change
Once the model has been preloaded, the route change can be delayed until the model is ready. This can be done by using the $routeChangeStart event in the $route service. This event is triggered whenever a route change is attempted and can be used to check if the model is loaded. If the model is not loaded, the route change can be cancelled and the model can be loaded before the route change is attempted again.

# Section 4: Conclusion 
Delaying the route change until the model is loaded can help to prevent flicker when using AngularJS. By preloading the model before the route change and using the $routeChangeStart event, developers can ensure that the page is rendered correctly before the route change is completed. This can help to improve the user experience and make the application more responsive.
