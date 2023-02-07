---
title: What is the method for determining the active route in angular?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The active route can be determined by using the Router service`s `url` property.
---

**Contents**

[TOC]

## 1. Using the Router

The Router service can be used to determine the active route. This can be done by injecting the Router service into the component and then calling the router's routerState.snapshot.url property. 

## 2. Using the ActivatedRoute

The ActivatedRoute service can also be used to determine the active route. This can be done by injecting the ActivatedRoute service into the component and then calling the ActivatedRoute's snapshot.url property.

## 3. Using the Location Service

The Location service can be used to determine the active route. This can be done by injecting the Location service into the component and then calling the Location service's path() method.

## 4. Using the Router State

The RouterState service can also be used to determine the active route. This can be done by injecting the RouterState service into the component and then calling the RouterState's url property.
