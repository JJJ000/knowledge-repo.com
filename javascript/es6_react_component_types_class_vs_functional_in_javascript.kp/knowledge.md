---
title: What are the advantages and disadvantages of using es6 class-based react components compared to functional es6 react components?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Functional ES6 React components should be used when the component is mainly concerned with rendering UI, while ES6 class based React components should be used when the component needs to have a state or lifecycle methods.
---

**Contents**

[TOC]

## Advantages of Class-Based Components
1. Class-based components provide the ability to use additional features such as local state and lifecycle methods.
2. Class-based components can be extended from other components, allowing for code reuse and inheritance.
3. Class-based components can also contain their own methods, which can be used for more complex logic.

## Advantages of Functional Components
1. Functional components are typically easier to read and understand than class-based components.
2. Functional components are less verbose and require less code to get the same result as class-based components.
3. Functional components are more performant than class-based components, as they have less overhead.

## Conclusion
When deciding whether to use class-based or functional components in React, it is important to consider the complexity of the component and the desired features. If the component requires more complex logic or features such as local state or lifecycle methods, then a class-based component is likely the better choice. However, if the component is simple and does not require any additional features, then a functional component is likely the better choice.
