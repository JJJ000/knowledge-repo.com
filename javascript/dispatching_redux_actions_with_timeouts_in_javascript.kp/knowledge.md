---
title: What is the process for sending a redux action after a specified amount of time has passed?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Dispatch a Redux action with a timeout by using the setTimeout() function.
---

**Contents**

[TOC]

### 1. Create the Action

Create a Redux action with the necessary payload.

```javascript
const action = {
    type: 'ACTION_TYPE',
    payload: {
        data: 'data'
    }
}
```

### 2. Create the Timeout

Create a timeout using `setTimeout()` and dispatch the action after the specified time.

```javascript
setTimeout(() => {
    store.dispatch(action);
}, 5000);
```

### 3. Cancel the Timeout

If needed, create a function to cancel the timeout.

```javascript
let timeoutId;

function cancelTimeout() {
    clearTimeout(timeoutId);
}
```

### 4. Execute the Timeout

Execute the timeout and store the returned ID for later use.

```javascript
timeoutId = setTimeout(() => {
    store.dispatch(action);
}, 5000);
```
