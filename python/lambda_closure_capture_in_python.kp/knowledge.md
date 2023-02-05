---
title: How do lambda functions store information?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Lambda function closures capture the values of the variables in the enclosing scope of the lambda function at the time of its creation.
---

**Contents**

[TOC]

#### Captured Variables 
Lambda function closures capture variables from the enclosing scope. These variables are then bound to the function and can be used in the function body. 

#### Non-Local Variables
Lambda function closures also capture non-local variables, which are variables that are not defined in the function's local scope. These variables are also bound to the function and can be used in the function body. 

#### Free Variables
Lambda function closures also capture free variables, which are variables that are not bound to the function, but are referenced in the function body. These variables are also bound to the function and can be used in the function body. 

#### Mutable Variables
Lambda function closures also capture mutable variables, which are variables that can be changed. These variables are also bound to the function and can be used in the function body.
