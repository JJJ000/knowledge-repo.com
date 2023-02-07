---
title: What is the syntax for selecting an element by its name attribute in jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: In jQuery, an element can be selected by its name attribute using the syntax `$(`[name=`nameAttributeValue`]`)`.
---

**Contents**

[TOC]

### Selecting by Name Attribute

To select an element by its name attribute in jQuery, you can use the `[name='attributeName']` selector. For example, the following will select an element with the name attribute `myName`:

```javascript
$('[name="myName"]')
```

### Selecting Multiple Elements

You can also use the same selector to select multiple elements with the same name attribute. For example, the following will select all elements with the name attribute `myName`:

```javascript
$('[name="myName"]')
```

### Selecting Nested Elements

You can also use the same selector to select nested elements with the same name attribute. For example, the following will select all elements with the name attribute `myName`, even if they are nested within other elements:

```javascript
$('[name="myName"]')
```

### Limiting the Scope

You can also limit the scope of the selector by providing a context. For example, the following will select all elements with the name attribute `myName` within the element with the ID `myElement`:

```javascript
$('[name="myName"]', '#myElement')
```
