---
title: Changing the type of an interface property defined in a typescript d.ts file
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: No, it is not possible to override an interface property type defined in a Typescript d.ts file in Javascript.
---

**Contents**

[TOC]

##### Section 1:
It is possible to override an interface property type defined in a Typescript d.ts file in Javascript.

##### Section 2:
The process involves creating a custom type definition file that overrides the interface property type. This file should be named the same as the original d.ts file, and should be placed in the same directory.

##### Section 3:
The custom type definition file should contain the same interface, but with the property type that needs to be overridden. The type should be specified using the correct JavaScript syntax.

##### Section 4:
Once this is done, the interface should be imported into the JavaScript file where it will be used. This will ensure that the overridden property type will be used instead of the one defined in the d.ts file.
