---
title: Retrieving the redux state within an action creator?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: In an action creator, the Redux state can be accessed using the getState() method of the store object.
---

**Contents**

[TOC]

### Accessing the Store

To access the Redux store from an action creator, you need to pass in the store as an argument. This can be done by wrapping the action creator in a function that takes in the store as an argument. 

```js
const mapDispatchToProps = (dispatch, ownProps) => {
  return {
    exampleActionCreator: (store) => {
      // Access store here
    }
  };
};
```

### Retrieving State from the Store

Once you have access to the store, you can use the `getState()` method to retrieve the current state. This will return an object containing the entire state tree.

```js
const mapDispatchToProps = (dispatch, ownProps) => {
  return {
    exampleActionCreator: (store) => {
      const state = store.getState();
      // Do something with state here
    }
  };
};
```

### Accessing Specific State Values

Once you have the state object, you can access specific values using the `state` object. For example, if you have a state value called `user`, you can access it by using `state.user`.

```js
const mapDispatchToProps = (dispatch, ownProps) => {
  return {
    exampleActionCreator: (store) => {
      const state = store.getState();
      const user = state.user;
      // Do something with user here
    }
  };
};
```

### Updating State Values

In addition to retrieving state values, you can also update them using the `dispatch()` method. This will take in an action object, which contains the type and payload of the action.

```js
const mapDispatchToProps = (dispatch, ownProps) => {
  return {
    exampleActionCreator: (store) => {
      const action = {
        type: 'UPDATE_USER',
        payload: { name: 'John' }
      };
      store.dispatch(action);
    }
  };
};
```
