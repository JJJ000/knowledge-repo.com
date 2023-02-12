---
title: Nested ng-repeats
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Nested ng-repeat is used to loop through elements in a JSON object.
---

**Contents**

[TOC]

### Section 1: Understanding ng-repeat

The ng-repeat directive is an AngularJS built-in directive that allows for looping through a collection of data. It can be used to iterate through an object or an array of objects and display the data in a view.

### Section 2: Nested ng-repeat

Nested ng-repeat is a way of looping through a collection of data within another collection of data. This can be useful when dealing with a JSON object that has multiple layers of data. For example, if you have a JSON object that contains an array of objects, you can use nested ng-repeat to loop through each object within the array.

### Section 3: Using ng-repeat with JSON

Using ng-repeat with JSON is fairly straightforward. All you need to do is define the ng-repeat directive in your HTML template, and then use the appropriate syntax to loop through the JSON data. For example, if you have a JSON object that contains an array of objects, you can use the following syntax to loop through the array:

```
<div ng-repeat="object in jsonObject.array">
  // content
</div>
```

### Section 4: Example

To illustrate how to use nested ng-repeat with JSON, let's consider the following example. Let's say we have a JSON object that contains an array of objects, each of which has a name and age property. We can use the following syntax to loop through the array and display the name and age for each object:

```
<div ng-repeat="person in jsonObject.people">
  <p>Name: {{ person.name }}</p>
  <p>Age: {{ person.age }}</p>
</div>
```

This will loop through the array of objects and display the name and age for each one.
