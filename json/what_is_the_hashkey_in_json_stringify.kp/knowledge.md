---
title: What does the $$hashkey represent in my json.stringify output?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The $$hashKey is an AngularJS-specific property used to track the order of objects within an array.
---

**Contents**

[TOC]

# What is $$hashKey?
$$hashKey is a unique identifier generated by AngularJS for each item in an ng-repeat directive. It is used to track the items in an ng-repeat loop, and is used internally by AngularJS to keep track of the items in the loop.

# Why is $$hashKey added to my JSON.stringify result?
When JSON.stringify is used to convert an object to a string, AngularJS adds the $$hashKey property to the object that is being converted. This is done to ensure that the object is properly tracked in AngularJS and that the data is not lost when the object is converted to a string.

# How does $$hashKey work?
The $$hashKey property is a unique identifier that is generated by AngularJS for each item in an ng-repeat directive. This key is used to track the items in the loop and is used internally by AngularJS to keep track of the items in the loop.

# What is the purpose of $$hashKey?
The purpose of the $$hashKey is to ensure that the data is not lost when the object is converted to a string. It also helps AngularJS to track the items in an ng-repeat loop, and is used internally by AngularJS to keep track of the items in the loop.