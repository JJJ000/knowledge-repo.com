---
title: It is not possible to make changes to the state of a react component that has been unmounted
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The best practice is to check if the component is mounted before performing the update.
---

**Contents**

[TOC]

## What is React State Update?
React state update is a feature of React that allows components to update their state based on user input or changes in the application. It is used to keep track of the current state of a component and to update it when necessary.

## What is an Unmounted Component?
An unmounted component is a component that has been removed from the DOM tree and is no longer rendered. This can happen when a component is removed from the application or when the application is closed.

## Why Can't React State Update be Performed on an Unmounted Component?
React state updates are performed on components that are rendered in the DOM. When a component is unmounted, it is no longer rendered in the DOM and therefore cannot be updated. This is because React state updates rely on the component being rendered in order to correctly update the state.

## How Can React State Updates be Performed on an Unmounted Component?
React state updates cannot be performed on an unmounted component, but there are some workarounds that can be used. One workaround is to use the componentWillUnmount lifecycle method to save the state before the component is unmounted. This allows the state to be saved and then used when the component is re-mounted. Another workaround is to use a state management library such as Redux or MobX to store the state in a global store. This allows the state to be accessed even when the component is unmounted.
