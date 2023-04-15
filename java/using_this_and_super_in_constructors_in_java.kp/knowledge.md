---
title: What is the reason for requiring that this() and super() be the first statement in a constructor?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Because they are used to call the parent class constructor, which must be called before any other code in the constructor.
---

**Contents**

[TOC]

### Reason
The reason why this() and super() have to be the first statement in a constructor in Java is because they are used to invoke another constructor in the same class or its superclass.

### this()
The this() keyword is used to call the constructor of the same class. It is used to reuse the code and to reduce the complexity of the program. When this() is used, the constructor of the current class is invoked with the given arguments.

### super()
The super() keyword is used to call the constructor of the superclass. It is used to reuse the code and to reduce the complexity of the program. When super() is used, the constructor of the superclass is invoked with the given arguments.

### Necessity
Since this() and super() are used to invoke another constructor, they must be the first statement in a constructor. This is because the first statement of a constructor is executed first and any other statements will be executed after that. Therefore, if this() and super() are not the first statement, then the other constructor will be invoked first and the code will not execute properly.
