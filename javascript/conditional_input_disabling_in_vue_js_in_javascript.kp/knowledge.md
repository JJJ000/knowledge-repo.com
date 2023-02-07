---
title: Conditionally turn off user input in vue.js
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the v-if directive to conditionally disable an input element in Vue.js.
---

**Contents**

[TOC]

## Option 1: Using v-bind:disabled

This option uses the `v-bind:disabled` directive to conditionally disable an input. This directive binds the disabled attribute to a boolean value. When the boolean value is true, the input is disabled, and when it is false, the input is enabled.

```html
<input type="text" v-bind:disabled="isDisabled" />
```

```javascript
data() {
  return {
    isDisabled: true
  }
}
```

## Option 2: Using v-if

This option uses the `v-if` directive to conditionally render an input. This directive renders the input only if the boolean value is true. When the boolean value is false, the input is not rendered.

```html
<input type="text" v-if="isEnabled" />
```

```javascript
data() {
  return {
    isEnabled: false
  }
}
```
