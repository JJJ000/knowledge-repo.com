---
title: Selecting elements in jquery using html5 custom data attributes
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: jQuery selectors can be used to access custom data attributes in HTML5 using the syntax `[data-attributeName=`attributeValue`]`.
---

**Contents**

[TOC]

## Using Attribute Selectors

We can use the attribute selector to select elements with custom data attributes. This selector is written as `[attribute=value]`. For example, if we have an element with a custom data attribute called `data-example`, we can select it using `[data-example=value]`.

## Using jQuery

jQuery provides a few methods for selecting elements with custom data attributes. The most common is the `.data()` method, which allows us to select elements based on their data attribute values. For example, if we have an element with a custom data attribute called `data-example`, we can select it using `$('[data-example=value]')`.

## Using HTML5

HTML5 provides a few methods for selecting elements with custom data attributes. The most common is the `dataset` property, which allows us to select elements based on their data attribute values. For example, if we have an element with a custom data attribute called `data-example`, we can select it using `document.querySelectorAll('[data-example=value]')`.

## Using JavaScript

JavaScript also provides a few methods for selecting elements with custom data attributes. The most common is the `getElementsByAttribute()` method, which allows us to select elements based on their data attribute values. For example, if we have an element with a custom data attribute called `data-example`, we can select it using `document.getElementsByAttribute('data-example', 'value')`.
