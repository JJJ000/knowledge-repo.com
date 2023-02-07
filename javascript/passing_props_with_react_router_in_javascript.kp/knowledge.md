---
title: Provide props to a handler component using react-router
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Pass props to the handler component by using the `render` method of the Route component.
---

**Contents**

[TOC]

**Section 1: Using the render Prop**

The render prop is a function that is passed to a component, which allows the component to pass back the props it receives. This can be used to pass props to a handler component in React Router. To do this, you can use the `<Route>` component and pass the props to the render prop. 

For example: 

```jsx
<Route
  path="/my-handler"
  render={props => <MyHandler {...props} myProp="myValue" />}
/>
```

**Section 2: Using the component Prop**

The component prop is another way to pass props to a handler component in React Router. This prop takes a React component as an argument, and the props are passed to the component as an argument. 

For example:

```jsx
<Route
  path="/my-handler"
  component={props => <MyHandler {...props} myProp="myValue" />}
/>
```

**Section 3: Using the children Prop**

The children prop is yet another way to pass props to a handler component in React Router. This prop takes a function as an argument, and the props are passed to the function as an argument. 

For example:

```jsx
<Route
  path="/my-handler"
  children={props => <MyHandler {...props} myProp="myValue" />}
/>
```

**Section 4: Using the withRouter Higher-Order Component**

The `withRouter` higher-order component is a function that wraps a component and passes the props from React Router to it. This can be used to pass props to a handler component in React Router. 

For example:

```jsx
import { withRouter } from 'react-router'

const MyHandlerWithProps = withRouter(props => (
  <MyHandler {...props} myProp="myValue" />
))

<Route path="/my-handler" component={MyHandlerWithProps} />
```
