---
title: Using react useeffect, what is the syntax to call a loading function only once?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Call the loading function in the React useEffect hook`s dependency array as an empty array to ensure that it is only called once.
---

**Contents**

[TOC]

### Step 1: Declare the useEffect Hook

At the start of the component, declare the useEffect hook and pass in the loading function as a parameter.

```js
useEffect(() => {
  loading();
}, []);
```

### Step 2: Pass an Empty Array as a Dependency

When the useEffect hook is declared, pass an empty array as a dependency. This ensures that the loading function is only called once.

### Step 3: Add the Loading Function

Add the loading function to the component. This should be called when the component is mounted.

```js
const loading = () => {
  // Perform loading tasks here
};
```

### Step 4: Call the Loading Function

Finally, call the loading function within the useEffect hook. This will ensure that the loading function is only called once.

```js
useEffect(() => {
  loading();
}, []);
```
