---
title: Loading a JSON file into typescript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can import a JSON file in TypeScript by using the `import` keyword.
---

**Contents**

[TOC]

# Section 1: Importing JSON File

In TypeScript, importing a JSON file is done using the `import` statement. The syntax for importing a JSON file is as follows:

```
import * as data from './data.json';
```

Where `data` is the name of the variable that will hold the imported JSON file and `data.json` is the name of the JSON file to be imported.

# Section 2: Accessing Data

Once the JSON file has been imported, the data can be accessed using the `data` variable. For example, if the JSON file contains an array of objects, the data can be accessed like this:

```
data.forEach((item) => {
    console.log(item.name);
});
```

# Section 3: TypeScript Types

When importing a JSON file in TypeScript, it's important to define the types for the data being imported. This can be done using the `interface` keyword. For example, if the JSON file contains an array of objects with a `name` and `age` property, the interface would look like this:

```
interface Person {
    name: string;
    age: number;
}
```

# Section 4: Using the Interface

Once the interface has been defined, it can be used to type the imported data. The syntax for this is as follows:

```
const people: Person[] = data;
```

Where `people` is the variable that will hold the typed data and `Person` is the interface used to type the data.
