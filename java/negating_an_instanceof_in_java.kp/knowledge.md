---
title: How to reverse an instanceof statement
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the `not` operator (!) before the instanceof operator.
---

**Contents**

[TOC]

1. Using the `not` Operator
   The `not` operator can be used to negate the result of an instanceof check in Java. For example, the following code will check if a given `Object` is not an instance of the `String` class:
   
   ```
   if(!(object instanceof String)){
       // Do something
   }
   ```

2. Using the `instanceof` Operator with a Negated Boolean
   The `instanceof` operator can also be used with a negated boolean to check if a given `Object` is not an instance of a certain class. For example, the following code will check if a given `Object` is not an instance of the `String` class:
   
   ```
   if(object instanceof String != true){
       // Do something
   }
   ```

3. Using the `!=` Operator
   The `!=` operator can also be used to negate the result of an instanceof check in Java. For example, the following code will check if a given `Object` is not an instance of the `String` class:
   
   ```
   if(object instanceof String != true){
       // Do something
   }
   ```

4. Using the `!instanceof` Operator
   The `!instanceof` operator can also be used to negate the result of an instanceof check in Java. For example, the following code will check if a given `Object` is not an instance of the `String` class:
   
   ```
   if(!(object instanceof String)){
       // Do something
   }
   ```
