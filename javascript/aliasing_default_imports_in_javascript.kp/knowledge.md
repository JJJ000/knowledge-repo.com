---
title: What is the syntax for assigning an alias to a default import in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can alias a default import in JavaScript by using the syntax `import <alias> from <module>`.
---

**Contents**

[TOC]

### Using Destructuring

Destructuring is a convenient way of creating variables from the properties of an object, or items from an array, without having to type out the full path.

For example, to alias a default import, you could do the following:

```javascript
import React, { Component as MyComponent } from "react";
```

This creates a new variable, `MyComponent`, which points to the `Component` property of the `react` package.

### Using Renaming

Another way to alias a default import is to use the `as` keyword. This allows you to rename the import while still keeping the same reference. For example:

```javascript
import React, { Component as MyComponent } from "react";
```

This creates a new variable, `MyComponent`, which points to the `Component` property of the `react` package.

### Using Aliases

You can also use aliases to alias a default import. This is done by specifying an alias in the `package.json` file. For example:

```json
{
  "name": "my-project",
  "version": "1.0.0",
  "dependencies": {
    "react": "^16.13.1"
  },
  "alias": {
    "react": "react-alias"
  }
}
```

This will allow you to use `react-alias` instead of `react` when importing the package.

### Using Imports

You can also use imports to alias a default import. This is done by importing the package under a different name. For example:

```javascript
import * as MyReact from "react";
```

This creates a new variable, `MyReact`, which points to the `react` package.
