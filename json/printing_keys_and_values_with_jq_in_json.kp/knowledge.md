---
title: Print the key and value for each item in an object using jq
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: For each entry in an object in JSON, you can print the key and value by using the `Object.keys()` and `Object.values()` methods.
---

**Contents**

[TOC]

#### Section 1: Accessing an Object

To access an object in JSON, you can use the dot notation or the bracket notation.

#### Section 2: Dot Notation

Using dot notation, you can access the key and value of each entry in an object by using the following syntax: 

`objectName.keyName` 

For example, if you have an object called 'person' with a key called 'name', you can access the value of 'name' by using the following syntax: 

`person.name` 

#### Section 3: Bracket Notation

Using bracket notation, you can access the key and value of each entry in an object by using the following syntax: 

`objectName["keyName"]` 

For example, if you have an object called 'person' with a key called 'name', you can access the value of 'name' by using the following syntax: 

`person["name"]` 

#### Section 4: Printing Key and Value

Once you have access to the key and value of each entry in an object in JSON, you can print them with the following syntax: 

`console.log("Key: " + keyName + " Value: " + objectName[keyName]);`

For example, if you have an object called 'person' with a key called 'name', you can print the key and value by using the following syntax: 

`console.log("Key: name Value: " + person["name"]);`
