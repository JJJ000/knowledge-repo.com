---
title: Is it possible to trigger a reload/re-render in vue.js?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, Vue.js can be forced to reload/re-render by using the $forceUpdate() method.
---

**Contents**

[TOC]

Yes, you can force Vue.js to reload/re-render in Javascript. 

### Using `$forceUpdate()`

The `$forceUpdate()` method can be used to force a re-render of a component. This method is exposed on all Vue instances, and can be called to force the component to re-render itself.

### Using `$nextTick()`

The `$nextTick()` method can be used to queue a callback to be invoked after the next DOM update cycle. This can be used to ensure that the component is re-rendered after a certain state has been changed.

### Using `Vue.nextTick()`

The `Vue.nextTick()` method can be used to queue a callback to be invoked after the next DOM update cycle. This can be used to ensure that the component is re-rendered after a certain state has been changed.

### Using `Vue.set()`

The `Vue.set()` method can be used to set a property on an object and trigger a re-render. This is useful when the data being rendered is dynamic and needs to be updated to reflect the changes.
