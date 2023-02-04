---
title: The difference between 'change' and 'ngmodelchange' in angular is that 'change' is triggered when a value of an element changes, while 'ngmodelchange' is triggered when the value of a two-way binding changes
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: ngModelChange is an event emitted by an Angular component when a data-bound input property changes, while change is a DOM event that is fired when an element`s value changes.
---

**Contents**

[TOC]

#### ngModel

`ngModel` is an Angular directive that binds an input, select, textarea, or custom form control to a property on the scope using NgModelController, which is created and exposed by this directive. It binds the view into the model, which other directives such as input, textarea or select require.

#### Change

The `change` event is fired when the value of an <input>, <select>, or <textarea> element has been changed. This event is limited to <input> elements, <textarea> boxes and <select> elements.

#### ngModelChange

The `ngModelChange` event is an Angular event that is emitted when the value of an `ngModel` bound input field changes. This event is triggered when the user changes the value of the input field and then tab out of the field or clicks away from the field.

#### Difference

The main difference between `change` and `ngModelChange` is that the `change` event is triggered when the value of an input field changes, whereas the `ngModelChange` event is triggered when the value of an `ngModel` bound input field changes. The `ngModelChange` event is triggered after the `change` event.
