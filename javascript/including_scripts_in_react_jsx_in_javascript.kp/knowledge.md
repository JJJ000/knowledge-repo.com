---
title: Including a script tag within a react/jsx component
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: In React/JSX, you can add a script tag by using the JSX syntax of <script>{/* JavaScript code here */}</script>.
---

**Contents**

[TOC]

1. Adding a Script Tag to React/JSX

To add a script tag to React/JSX, you must use the dangerouslySetInnerHTML prop. This prop takes an object with a __html key, whose value is a string containing the HTML you want to render.

2. Syntax

The syntax for adding a script tag in React/JSX looks like this:

`<div dangerouslySetInnerHTML={{__html: '<script>Your script here</script>'}} />`

3. Example

For example, if you wanted to add a script tag to a React component, you could do the following:

```
class MyComponent extends React.Component {
  render() {
    return (
      <div dangerouslySetInnerHTML={{__html: '<script>Your script here</script>'}} />
    );
  }
}
```

4. Security Considerations

When using the dangerouslySetInnerHTML prop, it is important to be aware of potential security issues. Malicious code can be injected into your application if you are not careful. It is best to use this prop only when absolutely necessary.
