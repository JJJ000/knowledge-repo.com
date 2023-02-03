---
title: What is the syntax for declaring a namespace in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: A namespace in JavaScript can be declared using the `namespace` keyword.
---

**Contents**

[TOC]

## Syntax
The syntax for declaring a namespace in JavaScript is as follows:

```js
var namespace = {
    // Declare properties and methods
};
```

## Example
Here is an example of declaring a namespace in JavaScript:

```js
var myNamespace = {
    foo: 'bar',
    baz: function() {
        // Do something
    }
};
```

## Accessing Properties
You can access the properties of the namespace using dot notation:

```js
myNamespace.foo // 'bar'
myNamespace.baz() // Executes the baz method
```

## Nested Namespaces
You can also nest namespaces within namespaces, like so:

```js
var myNamespace = {
    foo: 'bar',
    baz: {
        qux: 'quux'
    }
};

myNamespace.baz.qux // 'quux'
```
