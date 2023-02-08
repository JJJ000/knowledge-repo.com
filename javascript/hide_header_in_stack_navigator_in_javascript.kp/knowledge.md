---
title: Hide the header in a react navigation stack navigator
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: To hide the header in a Stack Navigator, set the header option to null.
---

**Contents**

[TOC]

## Solution 1

Using `headerMode: 'none'`:

```js
const Stack = createStackNavigator({
  Home: {
    screen: HomeScreen
  }
}, {
  headerMode: 'none'
});
```

## Solution 2

Using `navigationOptions`:

```js
const Stack = createStackNavigator({
  Home: {
    screen: HomeScreen,
    navigationOptions: {
      header: null
    }
  }
});
```
