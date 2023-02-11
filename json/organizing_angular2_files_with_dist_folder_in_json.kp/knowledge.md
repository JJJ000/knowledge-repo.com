---
title: Organize angular2 typescript files and JavaScript files into distinct directories, such as 'dist'
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Yes, it is recommended to separate Angular2 TypeScript files and JavaScript files into different folders, such as `dist` in JSON.
---

**Contents**

[TOC]

# Section 1: TypeScript Files

TypeScript files should be placed in a `src` directory. This directory should contain all TypeScript files that are used to create the Angular2 application. This includes the main TypeScript file, any components, services, and other files that are used to build the application.

# Section 2: JavaScript Files

JavaScript files should be placed in a `dist` directory. This directory should contain the compiled JavaScript files that are generated from the TypeScript files. The `dist` directory should also contain the necessary libraries and other resources that are required by the application.

# Section 3: JSON Files

JSON files should be placed in a `data` directory. This directory should contain any JSON files that are used by the application. This includes configuration files, data files, and other resources that are used by the application.

# Section 4: Other Resources

Any other resources that are required by the application should be placed in a `resources` directory. This includes images, fonts, and other assets that are used by the application.
