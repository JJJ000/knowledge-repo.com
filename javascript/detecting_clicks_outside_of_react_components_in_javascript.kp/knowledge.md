---
title: Determine when a click occurs outside of a react component
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use a ref to detect clicks outside a React component and call a function to handle the click event.
---

**Contents**

[TOC]

### 1. Using React Refs

Using React refs, you can detect a click outside of a React component by setting a ref on the outermost element of your component and then using the `addEventListener` method to detect a click outside of the component.

### 2. Using Higher Order Components

You can also detect a click outside of a React component using Higher Order Components (HOC). HOCs are functions that take a component as an argument and return a new component with additional functionality. In this case, the HOC would take a component as an argument and return a new component that has the ability to detect a click outside of itself.

### 3. Using Render Props

You can also detect a click outside of a React component using render props. Render props are functions that are passed as props to a component and are used to render other components. In this case, the render prop would be passed a function that is used to detect a click outside of the component. 

### 4. Using React Hooks

Finally, you can detect a click outside of a React component using React hooks. React hooks are functions that allow you to access state and lifecycle methods inside a functional component. In this case, you can use the `useEffect` hook to detect a click outside of the component and set the state accordingly.
