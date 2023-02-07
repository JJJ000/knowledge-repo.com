---
title: What are some valid applications for the "with" statement in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, the `with` statement can be used to reduce the amount of typing needed when accessing properties of an object.
---

**Contents**

[TOC]

Yes, there are legitimate uses for JavaScript's "with" statement. 

Advantages
----------------
The "with" statement has the advantage of allowing developers to reduce the amount of code they need to write. By using the "with" statement, developers can avoid having to repeatedly type the same object's name when referencing its properties. This can make code more readable and easier to maintain.

Disadvantages
----------------
The "with" statement can also be used to hide the source of variables, making code harder to debug. Additionally, the "with" statement can make code slower, as the JavaScript engine must scan the entire object each time the "with" statement is used. This can be especially problematic in large applications.

Conclusion
----------------
The "with" statement can be a useful tool for developers, but it should be used with caution. Developers should weigh the advantages and disadvantages of using the "with" statement before deciding whether or not to use it in their code.
