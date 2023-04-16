---
title: How to use vue.js to monitor nested data accurately
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To watch for nested data in Vue.js, you can use the Vue.js `$watch` method to observe changes in data properties.
---

**Contents**

[TOC]

## 1. Using the `$watch` Method

The `$watch` method is an instance method that can be used to watch for changes in a Vue instance's data. It takes two arguments, the first being the property to watch and the second being the callback function to be called when the property changes. For nested data, you can pass a dot-notated string to the `$watch` method to watch the nested property.

For example:

```javascript
this.$watch('myObject.myNestedProperty', (newValue, oldValue) => {
  // Do something when the nested property changes
});
```

## 2. Using the `watch` Option

The `watch` option is a component option that can be used to watch for changes in a Vue component's data. It takes an object that contains the properties to watch and the corresponding callback functions. For nested data, you can pass a dot-notated string to the `watch` option to watch the nested property.

For example:

```javascript
watch: {
  'myObject.myNestedProperty': (newValue, oldValue) => {
    // Do something when the nested property changes
  }
}
```

## 3. Using the `$watch` Deep Option

The `$watch` method also provides a `deep` option which can be used to watch for changes in deeply nested objects. When the `deep` option is set to `true`, the `$watch` method will recursively watch for changes in all properties of the watched object, including nested objects.

For example:

```javascript
this.$watch('myObject', (newValue, oldValue) => {
  // Do something when any property of the object changes
}, {
  deep: true
});
```

## 4. Using the `watch` Deep Option

The `watch` option also provides a `deep` option which can be used to watch for changes in deeply nested objects. When the `deep` option is set to `true`, the `watch` option will recursively watch for changes in all properties of the watched object, including nested objects.

For example:

```javascript
watch: {
  'myObject': (newValue, oldValue) => {
    // Do something when any property of the object changes
  },
  deep: true
}
```
