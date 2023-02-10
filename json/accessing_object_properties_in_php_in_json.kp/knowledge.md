---
title: What is the syntax for accessing an object property in PHP when the property name is stored in a variable?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use array notation with the variable as the key, i.e. $object[$variable].
---

**Contents**

[TOC]

#Section 1: Accessing Object Properties

In PHP, you can access object properties using the syntax `$object->property`. For example, if you have an object `$person` with a property `name`, you can access the value of the property by using `$person->name`.

#Section 2: Accessing Properties with Variables

When accessing object properties with variables, you must use the syntax `$object->{$variable}`. This will allow you to use the value of the variable as the property name. For example, if you have a variable `$prop` with the value `name`, you can access the value of the property `name` of the object `$person` using `$person->{$prop}`.

#Section 3: Accessing Properties in JSON

When accessing object properties in JSON, you must use the syntax `object[property]`. This will allow you to access the value of the property using the property name as a string. For example, if you have an object `person` with a property `name`, you can access the value of the property by using `person["name"]`.

#Section 4: Accessing Properties with Variables in JSON

When accessing object properties with variables in JSON, you must use the syntax `object[variable]`. This will allow you to use the value of the variable as the property name. For example, if you have a variable `prop` with the value `name`, you can access the value of the property `name` of the object `person` using `person[prop]`.
