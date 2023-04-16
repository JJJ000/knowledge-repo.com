---
title: What code is executed after react renders?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: After render code in Javascript would be any code that is executed after the React component has been rendered to the DOM.
---

**Contents**

[TOC]

## 1. ComponentDidMount
This method is invoked immediately after a component is mounted (inserted into the tree). 

## 2. ComponentDidUpdate
This method is invoked immediately after updating occurs. This method is not called for the initial render.

## 3. ComponentWillUnmount
This method is invoked immediately before a component is unmounted and destroyed. 

## 4. setState
This method is used to update the state of a component and re-render the component. It is called after the component has been updated.
