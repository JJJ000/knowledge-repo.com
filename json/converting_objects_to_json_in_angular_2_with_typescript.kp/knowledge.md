---
title: What is the correct way to convert an object to JSON in angular 2 using typescript?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: Use the built-in JSON.stringify() method to convert an object to JSON in Angular 2 with TypeScript.
---

**Contents**

[TOC]

1. Import the Angular JsonPipe

```typescript
import { JsonPipe } from '@angular/common';
```

2. Create a Pipe

```typescript
@Pipe({
  name: 'json'
})
export class JsonPipe implements PipeTransform {
  transform(value: any): string {
    return JSON.stringify(value);
  }
}
```

3. Use the Pipe

```typescript
let object = {
  name: 'John',
  age: 30
};

let jsonString = this.json.transform(object);
```

4. Output the JSON String

```typescript
console.log(jsonString);
// Outputs: {"name":"John","age":30}
```
