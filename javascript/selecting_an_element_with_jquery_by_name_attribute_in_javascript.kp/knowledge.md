---
title: What is the syntax for selecting an element by its name attribute using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can select an element with its name attribute in jQuery using the syntax `$(`[name=nameAttribute]`)`.
---

**Contents**

[TOC]

## Using Attribute Selectors

The following syntax can be used to select an element with its name attribute in jQuery:

```javascript
$('[name="nameAttribute"]')
```

Where `nameAttribute` is the value of the name attribute of the element.

## Using the Attr Method

The `attr()` method can also be used to select an element with its name attribute in jQuery:

```javascript
$('element').attr('name')
```

Where `element` is the element to be selected and `name` is the name attribute of the element.

## Using the Name Method

The `name()` method can also be used to select an element with its name attribute in jQuery:

```javascript
$('element').name()
```

Where `element` is the element to be selected and `name` is the name attribute of the element.

## Using the Get Method

The `get()` method can also be used to select an element with its name attribute in jQuery:

```javascript
$('element').get(0).name
```

Where `element` is the element to be selected and `name` is the name attribute of the element.
