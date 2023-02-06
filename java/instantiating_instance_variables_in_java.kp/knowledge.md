---
title: Should I assign values to instance variables when I declare them or in the constructor?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: It is best to instantiate instance variables in the constructor.
---

**Contents**

[TOC]

### Declaration
It is possible to declare and instantiate instance variables in the same statement. This is a valid approach for simple objects that do not require any additional processing when instantiating the variable.

### Constructor
Using the constructor to instantiate instance variables is a better practice than declaring and instantiating in the same statement. This allows for additional processing to be done when the variable is created, such as performing calculations or validating the value of the variable. It also allows for the instance variable to be set using a parameter passed into the constructor.
