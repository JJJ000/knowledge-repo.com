---
title: How can I conditionally add a property to an object in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the ternary operator (?) to conditionally add a member to an object in JavaScript.
---

**Contents**

[TOC]

### Option 1: Using the Conditional (ternary) Operator

The conditional (ternary) operator can be used to conditionally add a member to an object in JavaScript. The syntax is as follows:

```
let objectName = {
    // existing members
}

condition ? objectName.newMember = value : null;
```

In the above code, if the condition is true, the new member will be added to the object with the specified value. If the condition is false, nothing will be added to the object.

### Option 2: Using the Object Literal Syntax

The object literal syntax can also be used to conditionally add a member to an object in JavaScript. The syntax is as follows:

```
let objectName = {
    // existing members
    ...(condition ? {newMember: value} : {})
}
```

In the above code, if the condition is true, the new member will be added to the object with the specified value. If the condition is false, nothing will be added to the object.
