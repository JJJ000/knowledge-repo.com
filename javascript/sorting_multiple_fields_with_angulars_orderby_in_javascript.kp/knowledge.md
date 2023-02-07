---
title: Sort by multiple fields in angular
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the Angular pipe `orderBy` with an array of strings representing the fields to sort by.
---

**Contents**

[TOC]

### Method 1:

This can be done using the `orderBy` filter in Angular. The `orderBy` filter takes an array of objects and orders them by one or more of their fields.

To order by multiple fields, pass an array of field names to the `orderBy` filter. The order of the fields in the array determines the order of sorting. For example:

```
$scope.items = $filter('orderBy')($scope.items, ['field1', 'field2']);
```

### Method 2:

Another method of ordering by multiple fields is to use the `sort` function. The `sort` function takes a comparison function as an argument, which is used to determine the order of the elements in the array.

For example, to sort an array of objects by two fields, `field1` and `field2`, the comparison function could be written as follows:

```
function compare(a, b) {
  if (a.field1 < b.field1)
    return -1;
  if (a.field1 > b.field1)
    return 1;
  if (a.field2 < b.field2)
    return -1;
  if (a.field2 > b.field2)
    return 1;
  return 0;
}
```

The array can then be sorted using the `sort` function:

```
$scope.items.sort(compare);
```

### Method 3:

A third method of ordering by multiple fields is to use the `Array.prototype.sort` method. This method takes a comparison function as an argument, which is used to determine the order of the elements in the array.

For example, to sort an array of objects by two fields, `field1` and `field2`, the comparison function could be written as follows:

```
function compare(a, b) {
  if (a.field1 < b.field1)
    return -1;
  if (a.field1 > b.field1)
    return 1;
  if (a.field2 < b.field2)
    return -1;
  if (a.field2 > b.field2)
    return 1;
  return 0;
}
```

The array can then be sorted using the `Array.prototype.sort` method:

```
$scope.items.sort(compare);
```

### Method 4:

A fourth method of ordering by multiple fields is to use the `lodash` library. The `lodash` library provides a `orderBy` function that takes an array of objects and orders them by one or more of their fields.

To order by multiple fields, pass an array of field names to the `orderBy` function. The order of the fields in the array determines the order of sorting. For example:

```
$scope.items = _.orderBy($scope.items, ['field1', 'field2']);
```
