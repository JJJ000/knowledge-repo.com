---
title: What are the advantages of using ng-if instead of ng-show/ng-hide?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Ng-if should be used when an element needs to be completely removed from the DOM, while ng-show/ng-hide should be used when an element needs to be hidden but remain in the DOM.
---

**Contents**

[TOC]

**When to use ng-if** 

- When the element needs to be completely removed from the DOM: ng-if is the best choice when the element needs to be completely removed from the DOM. This is because ng-if will add or remove the element from the DOM depending on the condition, whereas ng-show/ng-hide will only hide the element from view. 

- When the condition requires complex logic: ng-if is also the best choice when the condition requires complex logic. This is because ng-if allows for more complex expressions to be evaluated, whereas ng-show/ng-hide only supports simple boolean expressions. 

**When to use ng-show/ng-hide** 

- When the element needs to remain in the DOM: ng-show/ng-hide is the best choice when the element needs to remain in the DOM. This is because ng-show/ng-hide will only hide the element from view, whereas ng-if will add or remove the element from the DOM depending on the condition. 

- When the condition is a simple boolean expression: ng-show/ng-hide is also the best choice when the condition is a simple boolean expression. This is because ng-show/ng-hide only supports simple boolean expressions, whereas ng-if allows for more complex expressions to be evaluated.
