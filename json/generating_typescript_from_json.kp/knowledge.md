---
title: Convert a JSON object into a typescript class instance
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: A TypeScript class instance can be created from a JSON object by using the `new` keyword and passing the JSON object as an argument.
---

**Contents**

[TOC]

## Section 1: Instantiating a TypeScript Class

To instantiate a TypeScript class, we must first define the class and its properties. For example, if we wanted to create a class called `Person`, we could define it as follows:

```typescript
class Person {
  name: string;
  age: number;
  constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
  }
}
```

## Section 2: Parsing JSON

Once we have the class definition, we can parse JSON into an instance of the class. To do this, we can use the `JSON.parse()` method, passing in the JSON string as an argument. For example, if we had the following JSON string:

```json
{
  "name": "John Doe",
  "age": 30
}
```

We could parse it into an instance of the `Person` class like this:

```typescript
let jsonString = '{"name": "John Doe", "age": 30}';
let person = JSON.parse(jsonString);
```

## Section 3: Creating an Instance of the TypeScript Class

Now that we have parsed the JSON string into an object, we can create an instance of the `Person` class using the `new` keyword. For example:

```typescript
let person = new Person(person.name, person.age);
```

## Section 4: Using the Instance of the TypeScript Class

Once we have an instance of the `Person` class, we can use it like any other object. For example, we could access the `name` and `age` properties of the `person` object like this:

```typescript
console.log(person.name); // John Doe
console.log(person.age); // 30
```
