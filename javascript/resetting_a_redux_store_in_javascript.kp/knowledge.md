---
title: What is the process for restoring a redux store to its initial state?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To reset the state of a Redux store, dispatch an action with a type property set to `RESET`.
---

**Contents**

[TOC]

1. Unsubscribe from Store Listeners 

If you have any listeners that are subscribed to the store, you will want to unsubscribe them before resetting the store. This will ensure that any listeners are not called when the store is reset.

2. Reset the Store

To reset the store, you will need to call the `dispatch()` method on the store, passing in an action with a type of `RESET`. This action can be defined in your reducers, and will reset the state of the store to its initial state.

3. Re-subscribe to Store Listeners 

Once the store has been reset, you will need to re-subscribe any listeners that were unsubscribed in the first step. This will ensure that any listeners are called when the store is updated.

4. Dispatch Initial Actions

Finally, you will need to dispatch any initial actions that your application needs to run properly. This could include actions such as fetching data from an API or setting up authentication.
