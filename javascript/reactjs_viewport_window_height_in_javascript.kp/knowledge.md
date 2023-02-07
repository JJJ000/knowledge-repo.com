---
title: How to obtain the viewport/window height in reactjs
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The viewport/window height in ReactJS can be accessed using the `window.innerHeight` property.
---

**Contents**

[TOC]

## 1. Using the DOM API

The DOM API provides access to the window object which can be used to get the viewport/window height.

```javascript
const vh = window.innerHeight;
```

## 2. Using the Dimensions Module

The Dimensions module from React Native can also be used to get the viewport/window height.

```javascript
import { Dimensions } from 'react-native';
const vh = Dimensions.get('window').height;
```

## 3. Using the BrowserRouter

The BrowserRouter component from React Router can also be used to get the viewport/window height.

```javascript
import { BrowserRouter } from 'react-router-dom';
const vh = BrowserRouter.getViewportHeight();
```

## 4. Using the useWindowSize Hook

The useWindowSize hook from React Resize Detector can also be used to get the viewport/window height.

```javascript
import { useWindowSize } from 'react-resize-detector';
const { height: vh } = useWindowSize();
```
