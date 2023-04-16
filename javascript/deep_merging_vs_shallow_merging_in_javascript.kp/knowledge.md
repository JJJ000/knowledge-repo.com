---
title: What is the process for performing a deep merge instead of a shallow merge?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the spread operator (...) to deep merge objects in JavaScript.
---

**Contents**

[TOC]

### Using Lodash

The Lodash library provides a `_.merge()` method that can be used to perform a deep merge. This method takes two objects as parameters and recursively merges their properties.

Example:

```js
const obj1 = {
  a: {
    b: {
      c: 1
    }
  }
};
const obj2 = {
  a: {
    b: {
      d: 2
    }
  }
};

const result = _.merge(obj1, obj2);
// result = {
//   a: {
//     b: {
//       c: 1,
//       d: 2
//     }
//   }
// }
```

### Using Spread Operator

The spread operator (`...`) can also be used to perform a deep merge. This operator takes two objects as parameters and merges their properties.

Example:

```js
const obj1 = {
  a: {
    b: {
      c: 1
    }
  }
};
const obj2 = {
  a: {
    b: {
      d: 2
    }
  }
};

const result = { ...obj1, ...obj2 };
// result = {
//   a: {
//     b: {
//       c: 1,
//       d: 2
//     }
//   }
// }
```

### Using Object.assign()

The `Object.assign()` method can also be used to perform a deep merge. This method takes two objects as parameters and merges their properties.

Example:

```js
const obj1 = {
  a: {
    b: {
      c: 1
    }
  }
};
const obj2 = {
  a: {
    b: {
      d: 2
    }
  }
};

const result = Object.assign({}, obj1, obj2);
// result = {
//   a: {
//     b: {
//       c: 1,
//       d: 2
//     }
//   }
// }
```

### Using Recursion

Finally, a recursive approach can be used to perform a deep merge. This approach takes two objects as parameters and recursively merges their properties.

Example:

```js
const deepMerge = (obj1, obj2) => {
  const result = { ...obj1 };
  for (let key in obj2) {
    if (typeof obj2[key] === 'object') {
      result[key] = deepMerge(obj1[key], obj2[key]);
    } else {
      result[key] = obj2[key];
    }
  }
  return result;
};

const obj1 = {
  a: {
    b: {
      c: 1
    }
  }
};
const obj2 = {
  a: {
    b: {
      d: 2
    }
  }
};

const result = deepMerge(obj1, obj2);
// result = {
//   a: {
//     b: {
//       c: 1,
//       d: 2
//     }
//   }
// }
```
