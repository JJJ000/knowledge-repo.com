---
title: What is the best way to divide an angularjs project into multiple controller files?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Create a separate .js file for each controller and include it in the HTML page.
---

**Contents**

[TOC]

1. Create the Controller File

- Create a new file in your project folder and name it appropriately.
- Add the following code to the file:

```javascript
angular.module('myApp')
  .controller('MyController', function($scope) {
    // controller code goes here
  });
```

2. Include the Controller File

- Add a `<script>` tag to the HTML page that contains the AngularJS application, referencing the controller file.

```html
<script src="myController.js"></script>
```

3. Use the Controller

- Add the controller name to the `ng-controller` directive in the HTML page.

```html
<div ng-controller="MyController">
  <!-- HTML markup and AngularJS code goes here -->
</div>
```

4. Test the Controller

- Open the HTML page in a browser and test the controller code.
