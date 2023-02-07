---
title: What is the process for executing gulp tasks in a sequential order?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To run Gulp tasks sequentially, use the gulp.series() method to specify the order of the tasks.
---

**Contents**

[TOC]

# Section 1: Install Required Dependencies

In order to run Gulp tasks sequentially, you will need to install the `run-sequence` package. This package allows tasks to be run in a specific order.

# Section 2: Create a Gulpfile

Create a `gulpfile.js` in the root of your project. This is where your Gulp tasks will be defined.

# Section 3: Define Tasks

In the `gulpfile.js`, define the tasks that you want to run in sequence. Here is an example of how to define two tasks:

```javascript
gulp.task('task1', function () {
  // Task 1 logic here
});

gulp.task('task2', function () {
  // Task 2 logic here
});
```

# Section 4: Run Tasks Sequentially

Finally, use the `run-sequence` package to run the tasks sequentially. Here is an example of how to do this:

```javascript
var runSequence = require('run-sequence');

gulp.task('default', function () {
  runSequence('task1', 'task2');
});
```

Now when you run the `gulp` command, the tasks will be run in the order that you specified.
