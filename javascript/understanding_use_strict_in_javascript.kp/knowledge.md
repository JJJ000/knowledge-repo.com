---
title: What is the purpose of the "use strict" directive in javascript, and why is it important?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: In JavaScript, `use strict` is a directive that enables strict mode, which helps to prevent errors and insecure coding practices by enforcing stricter syntax rules.
---

**Contents**

[TOC]

### What is "use strict"?
"use strict" is a directive in JavaScript that enables strict mode. Strict mode is a way to opt-in to a restricted variant of JavaScript. It enables a set of rules that enforce a more secure programming style.

### What Does "use strict" Do?
When "use strict" is enabled, it prevents certain actions from being taken and throws more exceptions. These actions include using a variable without declaring it, using an object that has been deleted, writing to a read-only property, and using a function that has been deleted. Additionally, "use strict" prevents the use of global variables, and requires the use of proper syntax.

### Benefits of "use strict"
The main benefit of "use strict" is that it helps to prevent errors and makes code more secure. By preventing certain actions, it ensures that code is not inadvertently changed or corrupted. Additionally, it helps to make code more readable, as it enforces a more consistent coding style.

### When to Use "use strict"
It is recommended that "use strict" be used in all JavaScript files. This will ensure that code is secure and consistent across the entire project. Additionally, "use strict" should be used in any code that is shared or distributed, as it helps to ensure that the code will work as expected.
