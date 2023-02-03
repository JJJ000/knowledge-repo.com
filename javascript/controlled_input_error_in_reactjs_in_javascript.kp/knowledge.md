---
title: Converting an uncontrolled input of type text to a controlled one in reactjs using a component
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The component should set the value of the input in its state, and use the value from state as the value of the input.
---

**Contents**

[TOC]

## Overview
In ReactJS, a component changing an uncontrolled input of type text to be controlled can result in an error. An uncontrolled input is one that is not bound to the state of a React component, while a controlled input is bound to the state. This error can be caused by a variety of issues, including improper syntax, an incorrect data type, or an incorrect event handler.

## Syntax Error
A syntax error can occur when the code for the uncontrolled input is incorrect. For example, if the uncontrolled input is written as `<input type="text" />` instead of `<input type="text" value={this.state.value} onChange={this.handleChange} />`, then an error will occur when the component attempts to change the uncontrolled input to a controlled input.

## Incorrect Data Type
Another potential cause of the error is if the data type of the uncontrolled input is incorrect. For example, if the uncontrolled input is written as `<input type="text" value={this.state.value} onChange={this.handleChange} />` but the value of the state is an array instead of a string, then an error will occur when the component attempts to change the uncontrolled input to a controlled input.

## Incorrect Event Handler
Finally, an incorrect event handler can also cause the error. If the uncontrolled input is written as `<input type="text" value={this.state.value} onChange={this.handleChange} />` but the `handleChange` event handler is incorrect, then an error will occur when the component attempts to change the uncontrolled input to a controlled input.
