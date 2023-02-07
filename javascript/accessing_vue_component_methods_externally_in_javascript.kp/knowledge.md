---
title: Invoke a vue.js component method from outside the component
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can call a Vue.js component method from outside the component by using the vm.$refs reference to the component instance.
---

**Contents**

[TOC]

**1. Access the Component Instance**

The first step to calling a Vue.js component method from outside the component is to access the component instance. This can be done by referencing the component instance in the Vue instance's `$children` array.

**2. Call the Component Method**

Once the component instance is accessed, the component method can be called by referencing the method name on the component instance. For example, if the method name is `myMethod`, then the call would be:

```
componentInstance.myMethod();
```

**3. Pass Arguments**

If the method requires arguments, then these can be passed in the same way as for any other function call. For example:

```
componentInstance.myMethod(arg1, arg2);
```

**4. Access Return Value**

If the method returns a value, then this can be accessed in the same way as any other function call. For example:

```
let returnValue = componentInstance.myMethod();
```
