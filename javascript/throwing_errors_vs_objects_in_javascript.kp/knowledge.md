---
title: What is the distinction between throwing a new error and throwing an object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The former throws an Error object, while the latter throws any arbitrary object.
---

**Contents**

[TOC]

####Error
`throw new Error` is used to throw an error object. The error object typically has a message property, which contains a string that provides a description of the error.

####Object
`throw someObject` is used to throw any other arbitrary object. The object can contain any kind of data, such as a string, a number, an array, or an object.
