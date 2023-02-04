---
title: What is the best way to assign multiple classes to a reactjs component?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: To add multiple classes to a ReactJS Component, use the className attribute and pass in a string of space-separated class names.
---

**Contents**

[TOC]

### Using the ClassName Property

The `className` property is used to add multiple classes to a React component. It accepts a string of class names separated by spaces.

```jsx
<MyComponent className="class1 class2 class3" />
```

### Using the Spread Operator

The spread operator (`...`) can be used to add multiple classes to a React component. This approach is useful when you need to add classes conditionally.

```jsx
const classes = ["class1", "class2", "class3"];

<MyComponent className={`${classes.join(" ")}`} />
```

### Using an Array

An array of class names can also be used to add multiple classes to a React component.

```jsx
const classes = ["class1", "class2", "class3"];

<MyComponent className={classes} />
```

### Using the Classnames Package

The [classnames](https://www.npmjs.com/package/classnames) package can also be used to add multiple classes to a React component. This package provides a simple syntax for conditionally joining class names together.

```jsx
const classes = {
  "class1": true,
  "class2": false,
  "class3": true
};

<MyComponent className={classnames(classes)} />
```
