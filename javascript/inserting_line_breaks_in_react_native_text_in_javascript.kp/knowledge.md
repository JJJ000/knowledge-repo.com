---
title: What is the best way to add a line break to a <text> component in react native?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the \n character to insert a line break into a <Text> component in React Native.
---

**Contents**

[TOC]

**1. Inserting a Line Break using the \n Character**

The simplest way to insert a line break in a React Native <Text> component is to use the \n character. This character will create a new line whenever it is encountered.

**2. Using the React Native Text Component's Prop**

The React Native Text component also has a prop called numberOfLines, which can be used to specify the number of lines of text that should be displayed before it is truncated. This prop can be set to 0 in order to allow the text to be displayed on multiple lines.

**3. Using the React Native StyleSheet**

The React Native StyleSheet can also be used to add line breaks to a <Text> component. The StyleSheet can be used to set the lineHeight property, which will specify the height of each line of text. This can be used to add extra space between lines of text, which will create a line break.

**4. Using the React Native Dimensions Module**

The React Native Dimensions module can also be used to add line breaks to a <Text> component. The Dimensions module provides access to the device's width and height, which can be used to set the lineHeight property in the React Native StyleSheet. This will allow the text to be displayed on multiple lines.
