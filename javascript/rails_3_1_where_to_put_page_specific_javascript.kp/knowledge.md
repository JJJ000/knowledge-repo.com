---
title: Where should you place your JavaScript code that is specific to a particular page when using rails 3.1?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Page specific JavaScript code should be placed in the corresponding view file in the Javascript folder.
---

**Contents**

[TOC]

1.  **Application.js**
   This is the primary file for adding global JavaScript code that will be used throughout the application.

2. **Views**
   Any JavaScript code that is specific to a particular view can be placed in the view file itself.

3. **Assets/Javascripts**
   For more complex JavaScript code, you can create a separate JavaScript file in the Assets/Javascripts folder and link to it in the view file.

4. **Vendor/Assets/Javascripts**
   If you are using third-party JavaScript libraries, they should be placed in the Vendor/Assets/Javascripts folder.
