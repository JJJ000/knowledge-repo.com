---
title: How do I reset localstorage in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: localStorage.clear() can be used to clear all data from localStorage.
---

**Contents**

[TOC]

#### Using the localStorage.clear() Method
The `localStorage.clear()` method is the most straightforward way to clear all entries in localStorage.

```
localStorage.clear();
```

#### Iterating Through localStorage Entries
It is also possible to iterate through all entries in localStorage and remove them one by one.

```
for (var key in localStorage) {
  if (localStorage.hasOwnProperty(key)) {
    localStorage.removeItem(key);
  }
}
```

#### Setting localStorage Entries to Null
Another approach is to set the value of each entry to `null`.

```
for (var key in localStorage) {
  if (localStorage.hasOwnProperty(key)) {
    localStorage.setItem(key, null);
  }
}
```

#### Setting localStorage Entries to an Empty String
The last approach is to set the value of each entry to an empty string.

```
for (var key in localStorage) {
  if (localStorage.hasOwnProperty(key)) {
    localStorage.setItem(key, "");
  }
}
```
