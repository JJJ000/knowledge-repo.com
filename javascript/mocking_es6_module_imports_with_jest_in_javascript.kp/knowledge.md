---
title: What is the best way to use jest to simulate an es6 module import?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use jest.mock() to mock an ES6 module import in Javascript.
---

**Contents**

[TOC]

## Step 1: Install Dependencies

In order to mock an ES6 module import using Jest, you will need to install the following dependencies:

- [jest](https://jestjs.io/)
- [@babel/preset-env](https://babeljs.io/docs/en/babel-preset-env)
- [babel-jest](https://www.npmjs.com/package/babel-jest)

## Step 2: Configure Babel

Next, configure Babel to compile your ES6 modules by adding a `.babelrc` file to your project root. Inside the `.babelrc` file, add the following:

```json
{
  "presets": ["@babel/preset-env"]
}
```

## Step 3: Configure Jest

Next, configure Jest to use Babel by adding a `jest.config.js` file to your project root. Inside the `jest.config.js` file, add the following:

```javascript
module.exports = {
  transform: {
    '^.+\\.js$': 'babel-jest'
  }
};
```

## Step 4: Mock Module

Finally, you can mock your ES6 module import in Jest by using the `jest.mock` function. For example, if you wanted to mock a module called `MyModule`, you could do the following:

```javascript
jest.mock('MyModule', () => {
  return {
    doSomething: jest.fn()
  };
});
```
