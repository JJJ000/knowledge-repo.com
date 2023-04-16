---
title: Re-render the view in react when the browser window is resized
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: React components can be re-rendered on browser resize by using the window.onresize event handler.
---

**Contents**

[TOC]

#1 Listening for Resize Events

The first step to rerendering a React view on browser resize is to listen for the resize event. This can be done using the window.addEventListener() method. 

```javascript
window.addEventListener('resize', () => {
  // code to rerender view
});
```

#2 Updating State

The next step is to update the state of the component when the resize event is triggered. This can be done using the setState() method. 

```javascript
this.setState(prevState => ({
  width: window.innerWidth
}));
```

#3 Rerendering the View

Finally, the view must be rerendered when the state is updated. This can be done by using the render() method.

```javascript
render() {
  return (
    <div>
      <h1>The window width is {this.state.width}px</h1>
    </div>
  );
}
```

#4 Optimizing Performance

To optimize performance, it is recommended to debounce the resize event. This can be done using the Lodash debounce() method.

```javascript
window.addEventListener('resize', _.debounce(() => {
  // code to rerender view
}, 250));
```
