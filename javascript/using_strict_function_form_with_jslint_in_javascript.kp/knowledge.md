---
title: Jslint is now indicating that you should use the "use strict" function instead
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the `use strict` function to enable strict mode in JavaScript, which helps to enforce better coding practices.
---

**Contents**

[TOC]

# What is JSLint?

JSLint is a static code analysis tool used to find potential errors and problems in JavaScript code. It is designed to help developers write more reliable and secure code.

# What is "Use the Function Form of 'use strict'"

"Use the function form of 'use strict'" is a JSLint warning that suggests using the function form of the "use strict" directive when writing JavaScript code. The "use strict" directive is a way to opt-in to a stricter version of JavaScript, which helps developers write more secure and reliable code.

# Why is it Important?

Using the function form of the "use strict" directive is important for two reasons. First, it ensures that the "use strict" directive is applied to the entire function, rather than just the first line of the code. This helps ensure that all of the code within the function is being checked for potential errors and problems. 

Second, it helps to ensure that the code is written in a consistent manner. Many developers use the "use strict" directive to ensure that their code is written in a consistent and reliable manner, and the function form of the directive helps to ensure that this is the case.

# How to Use it

To use the function form of the "use strict" directive, simply add the directive at the beginning of the function definition, like so:

```
function myFunction() {
  "use strict";
  // code here
}
```

This will ensure that the "use strict" directive is applied to the entire function, rather than just the first line.
