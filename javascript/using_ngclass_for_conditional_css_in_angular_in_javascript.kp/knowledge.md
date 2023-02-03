---
title: Using *ngclass to add conditionally applied classes in angular
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: *ngClass can be used to conditionally apply a class to an element in Angular based on a boolean expression.
---

**Contents**

[TOC]

#### Section 1 - Syntax
The syntax for using *ngClass with a conditional class in Angular is as follows:

```
<div [ngClass]="{'class-name': condition}">...</div>
```

#### Section 2 - Example
For example, to add a class of 'highlight' to a div element when the condition of `isHighlighted` is true, the syntax would be:

```
<div [ngClass]="{'highlight': isHighlighted}">...</div>
```

#### Section 3 - Multiple Classes
It is also possible to add multiple classes to an element when a condition is true. To do this, the syntax is as follows:

```
<div [ngClass]="{'class-name-1': condition-1, 'class-name-2': condition-2}">...</div>
```

#### Section 4 - Combining Syntax
It is also possible to combine the syntax for adding a single class and multiple classes. For example, to add the classes 'highlight' and 'bold' when the condition of `isHighlighted` is true, the syntax would be:

```
<div [ngClass]="{'highlight': isHighlighted, 'bold': isHighlighted}">...</div>
```
