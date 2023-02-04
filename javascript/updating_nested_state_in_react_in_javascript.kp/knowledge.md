---
title: What is the process for changing nested state values in react?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the spread operator (...) to create a new state object with the updated nested properties.
---

**Contents**

[TOC]

# Section 1: Accessing Nested State Properties

In order to update nested state properties in React, you must first access the nested state properties. This can be done using the `setState` method.

# Section 2: Using the setState Method

The `setState` method takes in an object as an argument and allows you to update the state with the new values. For example, if you wanted to update the nested state property `name` in the following state:

```
state = {
  user: {
    name: 'John',
    age: 30
  }
}
```

You would use the `setState` method like so:

```
this.setState({
  user: {
    name: 'Jane'
  }
})
```

# Section 3: Updating Nested State Properties

If you want to update a nested state property, you can use the `Object.assign` method to create a new object with the updated values. For example, if you wanted to update the nested state property `name` and `age` in the following state:

```
state = {
  user: {
    name: 'John',
    age: 30
  }
}
```

You would use the `Object.assign` method like so:

```
this.setState(Object.assign({}, this.state, {
  user: {
    name: 'Jane',
    age: 32
  }
}))
```

# Section 4: Conclusion

Updating nested state properties in React is a relatively simple process. By using the `setState` method and the `Object.assign` method, you can easily update the nested state properties in your React application.
