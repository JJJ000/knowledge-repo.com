---
title: Example of jquery ajax post using php
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: jQuery`s $.post() method can be used to send an AJAX POST request to a PHP script.
---

**Contents**

[TOC]

**Section 1: HTML Form**

```html
<form action="process.php" method="post">
  <input type="text" name="name" placeholder="Name">
  <input type="text" name="email" placeholder="Email">
  <input type="submit" value="Submit">
</form>
```

**Section 2: process.php**

```php
<?php
  // get the data from the form
  $name = $_POST['name'];
  $email = $_POST['email'];

  // process data
  // (save to database, etc.)

  // return a response
  echo json_encode(array('success' => true));
?>
```

**Section 3: JavaScript**

```javascript
$('form').on('submit', function(e) {
  e.preventDefault();
  var formData = $(this).serialize();
  $.ajax({
    type: 'POST',
    url: 'process.php',
    data: formData,
    success: function(data) {
      // do something with the response
    }
  });
});
```

**Section 4: jQuery Ajax POST Example**

```javascript
$.ajax({
  type: 'POST',
  url: 'process.php',
  data: {name: 'John', email: 'john@example.com'},
  success: function(data) {
    // do something with the response
  }
});
```
