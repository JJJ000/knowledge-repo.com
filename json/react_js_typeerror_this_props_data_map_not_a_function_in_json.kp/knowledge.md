---
title: An uncaught typeerror was encountered when attempting to use the map function on this.props.data in react js
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: The data being mapped needs to be an array, not an object.
---

**Contents**

[TOC]

**Overview**

React JS is a JavaScript library used for building user interfaces. It is used to create single page applications. When working with React JS, you may encounter an error such as “Uncaught TypeError: this.props.data.map is not a function”. This error occurs when you are attempting to map over an object that does not have a map method.

**Cause of Error**

This error occurs when you are attempting to map over an object that does not have a map method. The map method is only available on arrays, not objects. This means that if you are trying to map over an object, you will get this error.

**Solution**

The solution to this error is to make sure that you are mapping over an array and not an object. If you are trying to map over an object, you can use the Object.keys() method to convert it into an array. Once you have converted the object into an array, you can then map over it without getting the error.

**Conclusion**

When you encounter the “Uncaught TypeError: this.props.data.map is not a function” error in React JS, it means that you are attempting to map over an object which does not have a map method. The solution to this error is to make sure that you are mapping over an array and not an object. If you are trying to map over an object, you can use the Object.keys() method to convert it into an array. Once you have converted the object into an array, you can then map over it without getting the error.
