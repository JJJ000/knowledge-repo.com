---
title: Logic used within a handlebars.js {{#if}} statement
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The logical operator used in a handlebars.js {{#if}} conditional is the JavaScript `&&` operator.
---

**Contents**

[TOC]

### AND Operator
The "AND" operator (&&) can be used to create a more complex condition within a handlebars.js {{#if}} conditional. The "AND" operator allows multiple conditions to be evaluated at once. For example:

```
{{#if (condition1 && condition2)}}
  // do something
{{else}}
  // do something else
{{/if}}
```

### OR Operator
The "OR" operator (||) can also be used to create a more complex condition within a handlebars.js {{#if}} conditional. The "OR" operator allows multiple conditions to be evaluated at once and will return true if one or more of the conditions are true. For example:

```
{{#if (condition1 || condition2)}}
  // do something
{{else}}
  // do something else
{{/if}}
```

### NOT Operator
The "NOT" operator (!) can be used to invert the evaluation of a condition within a handlebars.js {{#if}} conditional. This means that if the condition is true, the "NOT" operator will make it false, and vice versa. For example:

```
{{#if (!condition1)}}
  // do something
{{else}}
  // do something else
{{/if}}
```

### Nested Operators
It is also possible to nest multiple operators within a handlebars.js {{#if}} conditional. This allows for complex conditions to be evaluated and can be done by simply enclosing each condition within parentheses. For example:

```
{{#if ((condition1 && condition2) || (condition3 && condition4))}}
  // do something
{{else}}
  // do something else
{{/if}}
```
