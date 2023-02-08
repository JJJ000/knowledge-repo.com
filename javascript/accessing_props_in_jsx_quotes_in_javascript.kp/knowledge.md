---
title: Access props within double curly braces in react jsx
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can access props inside quotes in React JSX by using the curly braces syntax, e.g. {props.example}.
---

**Contents**

[TOC]

**Section 1: Using Props in Quotes**

Props can be used inside quotes in React JSX. This allows you to use props as part of a string, such as when creating a heading or other text element. To do this, you must wrap the prop in curly braces and use single quotes around the entire string. For example:

```
<h1>{'Welcome ' + this.props.name + '!'}</h1>
```

**Section 2: Using Props with Template Literals**

Template literals can also be used to include props inside quotes in React JSX. This allows for more complex strings than using the plus operator. To do this, wrap the template literal in backticks and use curly braces to include the prop. For example:

```
<h1>{`Welcome ${this.props.name}!`}</h1>
```

**Section 3: Using Props with Variables**

You can also use props with variables in React JSX. To do this, assign the prop to a variable, then use the variable inside the quotes. For example:

```
const name = this.props.name;
<h1>{`Welcome ${name}!`}</h1>
```

**Section 4: Using Props with Expressions**

Props can also be used with expressions in React JSX. To do this, wrap the expression in curly braces and use single quotes around the entire string. For example:

```
<h1>{`Welcome ${this.props.name.toUpperCase()}!`}</h1>
```
