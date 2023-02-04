---
title: Modifying state arrays in react.js correctly
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: State arrays in React.js should be modified using the setState() method.
---

**Contents**

[TOC]

**1. Updating State with setState**

The setState() method is used to update the state of a component in React. It takes two arguments, an object containing the properties to update, and a callback function. The object should contain only the properties that need to be updated. The callback function is optional and is used to notify the component when the state has been updated.

To update the state, we call the setState() method and pass in an object containing the properties we want to update. The state object is then merged with the existing state.

```js
this.setState({
  name: 'John',
  age: 25
});
```

**2. Replacing State with replaceState**

The replaceState() method is used to completely replace the state of a component in React. It takes two arguments, an object containing the properties to update, and a callback function. The object should contain only the properties that need to be updated. The callback function is optional and is used to notify the component when the state has been updated.

To replace the state, we call the replaceState() method and pass in an object containing the properties we want to update. The state object is then completely replaced with the new state.

```js
this.replaceState({
  name: 'John',
  age: 25
});
```

**3. Merging State with Object.assign**

The Object.assign() method is used to merge the state of a component in React. It takes two arguments, an object containing the properties to update, and a callback function. The object should contain only the properties that need to be updated. The callback function is optional and is used to notify the component when the state has been updated.

To merge the state, we call the Object.assign() method and pass in an object containing the properties we want to update. The state object is then merged with the existing state.

```js
this.state = Object.assign({}, this.state, {
  name: 'John',
  age: 25
});
```

**4. Resetting State with resetState**

The resetState() method is used to reset the state of a component in React. It takes no arguments, and a callback function is optional and is used to notify the component when the state has been reset.

To reset the state, we call the resetState() method. The state object is then reset to its initial state.

```js
this.resetState();
```
