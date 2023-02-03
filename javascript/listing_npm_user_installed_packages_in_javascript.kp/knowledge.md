---
title: What is the command to view npm packages installed by the user?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: To list npm user-installed packages in Javascript, use the command `npm list --depth=0 -g`.
---

**Contents**

[TOC]

1. Install the `npm-list-packages` Library

To list npm user-installed packages in Javascript, you first need to install the `npm-list-packages` library.

```
npm install npm-list-packages
```

2. Import the `npm-list-packages` Library

Once the library is installed, you need to import it into your Javascript file.

```
import listPackages from 'npm-list-packages';
```

3. List Packages

Once the library is imported, you can use the `listPackages()` function to list all the packages that are installed.

```
const packages = listPackages();
```

4. Log Packages

Finally, you can log the packages to the console to view the list of packages.

```
console.log(packages);
```
