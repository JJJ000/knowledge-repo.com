---
title: Can a JSON file be incorporated when using typescript with a tsconfig.json file?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Yes, you can include a JSON file in a tsconfig.json file by adding it to the `files` or `include` array.
---

**Contents**

[TOC]

## Yes

TypeScript supports the use of JSON files through the `"include"` option in the `tsconfig.json` file. This option allows you to specify a list of files or folders to be included in the compilation process. The `"include"` option takes an array of strings, each of which should be a relative path to the JSON file.

For example, if you have a file called `data.json` in the same directory as your `tsconfig.json` file, you can include it in the compilation process by adding the following line to your `tsconfig.json`:

```json
{
  "include": [
    "data.json"
  ]
}
```

## How to Access the Data

Once the JSON file is included in the compilation process, you can access the data from it in your TypeScript code. This can be done by importing the JSON file as a module. For example, if you have a file called `data.json` in the same directory as your `tsconfig.json` file, you can access the data from it in your TypeScript code by adding the following line to the top of your TypeScript file:

```typescript
import * as data from "./data.json";
```

Once imported, you can access the data from the `data` object.

## Caveats

When including a JSON file in the compilation process, there are a few caveats to be aware of. First, the JSON file must be valid JSON. If the JSON file is not valid, the compilation will fail. Second, the JSON file will be treated as a module and the data in it will be immutable. This means that any changes you make to the data in the JSON file will not be reflected in the compiled code. Finally, the JSON file will be treated as a module and the data in it will not be accessible outside of the module.
