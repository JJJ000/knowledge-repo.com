---
title: What is the syntax for using an angular 2 pipe with multiple arguments?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can call an Angular 2 pipe with multiple arguments in Javascript by using the transform method on the pipe instance.
---

**Contents**

[TOC]

### Step 1: Create the Pipe in the Component

In the component where the pipe will be used, create the pipe. To do this, import the pipe from the module and add it to the `declarations` array.

```typescript
import { MyPipe } from './my-pipe.pipe';

@Component({
  selector: 'app-my-component',
  templateUrl: './my-component.component.html',
  styleUrls: ['./my-component.component.css'],
  declarations: [MyPipe]
})
```

### Step 2: Use the Pipe in the Template

In the template, use the pipe with the arguments. The arguments should be passed in as an array.

```html
<div>{{ value | myPipe: [arg1, arg2, arg3] }}</div>
```

### Step 3: Use the Pipe in the Component

In the component, use the pipe with the arguments. The arguments should be passed in as an array.

```typescript
import { MyPipe } from './my-pipe.pipe';

@Component({
  selector: 'app-my-component',
  templateUrl: './my-component.component.html',
  styleUrls: ['./my-component.component.css'],
  declarations: [MyPipe]
})
export class MyComponent {
  value = 'some value';
  args = [arg1, arg2, arg3];

  constructor(private myPipe: MyPipe) {}

  transform() {
    return this.myPipe.transform(this.value, this.args);
  }
}
```

### Step 4: Use the Result of the Pipe

In the template, use the result of the pipe.

```html
<div>{{ transform() }}</div>
```
