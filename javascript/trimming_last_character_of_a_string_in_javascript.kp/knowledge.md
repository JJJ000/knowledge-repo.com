---
title: What is the most efficient way to remove the last character from a string using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the built-in String.prototype.slice() method, passing in 0 for the start index and -1 for the end index.
---

**Contents**

[TOC]

**1. Using the Substring Method**

The `substring()` method can be used to remove the last character from a string.

Syntax:
```
string.substring(0, string.length - 1);
```

Example:
```
let str = "Hello World!";

str = str.substring(0, str.length - 1);

console.log(str); // Output: "Hello World"
```

**2. Using the Slice Method**

The `slice()` method can also be used to remove the last character from a string.

Syntax:
```
string.slice(0, -1);
```

Example:
```
let str = "Hello World!";

str = str.slice(0, -1);

console.log(str); // Output: "Hello World"
```

**3. Using the Replace Method**

The `replace()` method can also be used to remove the last character from a string.

Syntax:
```
string.replace(/.$/, "");
```

Example:
```
let str = "Hello World!";

str = str.replace(/.$/, "");

console.log(str); // Output: "Hello World"
```

**4. Using the Split Method**

The `split()` method can also be used to remove the last character from a string.

Syntax:
```
string.split("").slice(0, -1).join("");
```

Example:
```
let str = "Hello World!";

str = str.split("").slice(0, -1).join("");

console.log(str); // Output: "Hello World"
```
