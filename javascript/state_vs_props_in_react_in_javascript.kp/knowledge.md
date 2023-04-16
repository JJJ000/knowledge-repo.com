---
title: How do state and props differ in react?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Props are data passed from a parent component to a child component, while state is data managed within a component.
---

**Contents**

[TOC]

## State
State is an object that holds data specific to a component. It is a way for a component to maintain information about itself. It is mutable, meaning it can change over time. The state of a component can be changed by user interaction, system events, or API calls.

## Props
Props are immutable pieces of data that are passed down from a parent component to a child component. They are used to pass data from one component to another, and are typically used to customize the appearance or behavior of a child component. Props are read-only, meaning they cannot be changed by the child component.
