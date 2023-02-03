---
title: What does "export default" mean in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Export default is a keyword used to export a single module or value from a JavaScript file.
---

**Contents**

[TOC]

# Definition 

"Export default" is a feature of JavaScript ES6 modules that allows developers to export a single value from a module. It is used to create a default export for a module, meaning that a module can have multiple named exports, as well as a default export.

# Syntax 

The syntax for exporting a default value from a module is as follows: 

```
export default <value>;
```

# Usage 

This feature can be used to export a single class, function, or primitive from a module. For example, a module might look like this: 

```
// myModule.js

class MyClass {
    // ...
}

function myFunction() {
    // ...
}

const myVariable = "foo";

export default myVariable;
```

In this example, the default export is the variable `myVariable`, while the `MyClass` and `myFunction` are named exports. 

# Advantages 

Using the "export default" feature of JavaScript ES6 modules has several advantages. First, it makes it easier to keep track of exports from a module, since there is only one default export. Second, it allows developers to export a single value from a module without having to use a named export. Finally, it allows for more concise import statements, since the default export does not need to be named when imported.
