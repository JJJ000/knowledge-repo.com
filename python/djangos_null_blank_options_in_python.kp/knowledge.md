---
title: How do null=true and blank=true differ in django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Null=True indicates that the field can be left blank, while blank=True indicates that the field is allowed to be blank in forms.
---

**Contents**

[TOC]

#### Null
Null indicates that the field in the database can be left blank and will not be given a value. This is generally used when the value is unknown or when it is not necessary to have a value for the field.

#### Blank
Blank indicates that the field can be left blank in the form when submitting data. This is generally used when the value is optional and not required.
