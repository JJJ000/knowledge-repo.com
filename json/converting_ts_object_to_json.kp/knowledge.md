---
title: Convert a typescript object to a JSON string
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JSON.stringify() method to convert a TypeScript object into a JSON string.
---

**Contents**

[TOC]

### Step 1: Import the Necessary Module

In order to convert a TypeScript object into a JSON string, we must first import the `JSON` module from the `typescript` library.

```typescript
import { JSON } from "typescript";
```

### Step 2: Create the TypeScript Object

Next, we must create the TypeScript object that we wish to convert into a JSON string. For the purposes of this example, we will create a simple object containing two key-value pairs.

```typescript
let tsObject = {
  name: "John Doe",
  age: 25
}
```

### Step 3: Convert the Object to a JSON String

Finally, we can use the `stringify()` method from the `JSON` module to convert the TypeScript object into a JSON string.

```typescript
let jsonString = JSON.stringify(tsObject);
```

### Step 4: Print the JSON String

To print the JSON string, we can simply use the `console.log()` method.

```typescript
console.log(jsonString);
```

The output should be a JSON string that looks like this:

```json
{"name":"John Doe","age":25}
```
