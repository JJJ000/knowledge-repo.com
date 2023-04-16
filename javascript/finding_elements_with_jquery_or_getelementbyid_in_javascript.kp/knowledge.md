---
title: What is preventing jquery or a dom method like getelementbyid from locating the element?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The element may not exist in the DOM yet, or the selector used may not match the element.
---

**Contents**

[TOC]

## HTML not Loaded

One reason jQuery or a DOM method such as getElementById may not find an element in Javascript is because the HTML has not been loaded yet. In order for Javascript to access an element on the page, the HTML must first be loaded. This can be done by using the `window.onload` event, which will fire after the page has been loaded.

## Selector Incorrect

Another reason jQuery or a DOM method such as getElementById may not find an element in Javascript is because the selector used to find the element is incorrect. If the selector is not specific enough, or if it is targeting the wrong element, then the element will not be found. It is important to ensure that the selector is accurate and specific before attempting to find an element using jQuery or a DOM method.

## Element Not Present

A third reason jQuery or a DOM method such as getElementById may not find an element in Javascript is because the element is not present on the page. If the element does not exist, then it cannot be found by the Javascript code. It is important to ensure that the element exists before attempting to find it with jQuery or a DOM method.

## Element Hidden

A fourth reason jQuery or a DOM method such as getElementById may not find an element in Javascript is because the element is hidden. If the element is hidden, it will not be visible to the Javascript code and therefore cannot be found. It is important to ensure that the element is visible before attempting to find it with jQuery or a DOM method.
