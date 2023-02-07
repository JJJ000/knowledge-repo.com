---
title: What is the process of altering the header depending on an angularjs partial view?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the $scope.$on(`$routeChangeSuccess`, function(event, current, previous) { ... } event to dynamically update the header based on the current partial view.
---

**Contents**

[TOC]

# Section 1: Set Up 

1. Create an AngularJS application with two partial views. 
2. In the main view, include a header and a `<div>` element where the partial views will be loaded. 
3. In the partial views, include a title for each view. 

# Section 2: Create the Directive 

1. Create a directive to dynamically change the header based on the partial view. 
2. In the directive, use the `$route` service to get the current route. 
3. Use the `$route.current` object to get the title of the current route.
4. Use the `$scope` to set the title of the header to the title of the current route.

# Section 3: Use the Directive 

1. Add the directive to the header element in the main view. 
2. Pass the `$route` service as an argument to the directive. 
3. Pass the `$scope` as an argument to the directive. 

# Section 4: Test the Directive 

1. Test the directive by switching between the two partial views. 
2. Verify that the header changes to the title of the current partial view.
