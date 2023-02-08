---
title: What is the process for converting a JSON object to a typescript class?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the `new` keyword to create a new instance of the TypeScript class, then assign the JSON object to the instance.
---

**Contents**

[TOC]

**Section 1 - Install Typescript Compiler**

1. Install the Typescript compiler by running the following command in the terminal: 

`npm install -g typescript`

**Section 2 - Create a Typescript Class**

1. Create a Typescript class with the properties that you want to use from the JSON object. For example: 

```
class MyClass {
  public id: string;
  public name: string;
  public age: number;
}
```

**Section 3 - Convert JSON Object to Typescript Class**

1. Use the Typescript compiler to convert the JSON object to the Typescript class. For example: 

```
let myObj = {
  "id": "123",
  "name": "John Doe",
  "age": 42
};

let myClass: MyClass = JSON.parse(JSON.stringify(myObj));
```

**Section 4 - Use Typescript Class**

1. Now you can use the Typescript class as you would any other object. For example: 

```
console.log(myClass.name); // John Doe
console.log(myClass.age); // 42
```
