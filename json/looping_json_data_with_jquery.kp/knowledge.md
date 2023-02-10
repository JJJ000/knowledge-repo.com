---
title: Iterate through JSON data using a $.each loop in jquery
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: $.each can be used to loop through a JSON object to access and manipulate its data.
---

**Contents**

[TOC]

### Section 1: Introduction

jQuery is a popular JavaScript library that provides powerful features for traversing and manipulating the Document Object Model (DOM). One of the most useful features of jQuery is its ability to loop through JSON data. The $.each() function allows developers to quickly iterate through an array or object and perform a specific action on each item.

### Section 2: Syntax

The syntax for the $.each() function is as follows:

```
$.each( arrayOrObject, function( index, value ) {
  // code to be executed
});
```

The arrayOrObject parameter is the array or object to loop through. The index parameter is the index of the current item in the array or object. The value parameter is the value of the current item in the array or object.

### Section 3: Example

The following is an example of how to use the $.each() function to loop through a JSON array:

```
var myArray = [1,2,3,4,5];
 
$.each(myArray, function(index, value) {
  console.log(index + ': ' + value);
});
```

This will output the following to the console:

```
0: 1
1: 2
2: 3
3: 4
4: 5
```

### Section 4: Conclusion

The $.each() function is a powerful tool for looping through JSON data in jQuery. It allows developers to quickly iterate through an array or object and perform a specific action on each item. The syntax is simple and straightforward, and the example provided shows how to loop through an array.
