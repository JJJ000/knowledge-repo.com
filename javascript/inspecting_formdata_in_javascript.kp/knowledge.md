---
title: What is the process for examining formdata?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: FormData can be inspected by looping through its entries using the forEach() method.
---

**Contents**

[TOC]

# 1. Using the `entries()` Method

The `entries()` method of the FormData interface returns an iterator allowing to go through all key/value pairs contained in this object.

Syntax:
```
formData.entries();
```

Example:
```
let formData = new FormData();
formData.append('name', 'John');
formData.append('age', '30');

for (let pair of formData.entries()) {
   console.log(pair[0]+ ', ' + pair[1]); 
}
// Output: name, John 
//         age, 30
```

# 2. Using the `forEach()` Method

The `forEach()` method of the FormData interface iterates over all key/value pairs contained in this object and calls a callback function for each of them.

Syntax:
```
formData.forEach(callback);
```

Example:
```
let formData = new FormData();
formData.append('name', 'John');
formData.append('age', '30');

formData.forEach(function(value, key){
   console.log(key + ', ' + value);
});
// Output: name, John 
//         age, 30
```

# 3. Using the `get()` Method

The `get()` method of the FormData interface returns the first value associated with a given key from within a FormData object.

Syntax:
```
formData.get(name);
```

Example:
```
let formData = new FormData();
formData.append('name', 'John');
formData.append('age', '30');

console.log(formData.get('name')); 
// Output: John
```

# 4. Using the `has()` Method

The `has()` method of the FormData interface returns a boolean stating whether a FormData object contains a certain key or not.

Syntax:
```
formData.has(name);
```

Example:
```
let formData = new FormData();
formData.append('name', 'John');
formData.append('age', '30');

console.log(formData.has('name')); 
// Output: true
