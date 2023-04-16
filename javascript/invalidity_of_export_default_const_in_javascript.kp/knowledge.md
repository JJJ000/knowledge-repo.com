---
title: What is the reason that 'export default const' is not valid?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Export default const is invalid in Javascript because const declarations are not hoisted, and therefore cannot be used before they are declared.
---

**Contents**

[TOC]

# Syntax

Export default const is invalid in Javascript because it does not follow the syntax for exporting in Javascript. The syntax for exporting in Javascript is `export default <value>` where <value> is the value being exported. The keyword `const` is not a valid value, so the statement is invalid.

# Semantics

Export default const is invalid in Javascript because it does not make sense semantically. The keyword `const` is used to declare a constant variable, which cannot be changed or reassigned. However, when exporting a value, the value can be changed or reassigned. Therefore, the statement does not make sense semantically.

# Alternatives

The correct syntax for exporting a constant in Javascript is `export const <name> = <value>`. This syntax declares a constant with the given name and value, and then exports it. This syntax is valid in Javascript and is semantically meaningful.
