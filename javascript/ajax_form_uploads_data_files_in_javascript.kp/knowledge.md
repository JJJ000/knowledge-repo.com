---
title: Submitting both data and files in one form via ajax?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Ajax can be used to send both data and files in one form by using FormData objects to store the data and files.
---

**Contents**

[TOC]

# Section 1: HTML Form

To upload both data and files in one form, first we need to create an HTML form that contains the necessary input elements for the data and files. The form should look something like this:

```html
<form id="myForm" action="myScript.php" method="post" enctype="multipart/form-data">
    <input type="text" name="name" placeholder="Name">
    <input type="text" name="email" placeholder="Email">
    <input type="file" name="photo" accept="image/*">
    <input type="submit" value="Submit">
</form>
```

# Section 2: JavaScript

Once the form is created, we can use JavaScript to submit the form data via an AJAX request. To do this, we need to use the XMLHttpRequest object to create an AJAX request. We can use the `FormData` object to get the form data and attach the files to the request. The JavaScript code should look something like this:

```js
// Get the form element
var form = document.getElementById('myForm');

// Listen for the form submit event
form.addEventListener('submit', function(e) {
    e.preventDefault();

    // Create a new FormData object
    var formData = new FormData(form);

    // Create an AJAX request
    var xhr = new XMLHttpRequest();
    xhr.open('POST', form.action, true);
    xhr.onload = function() {
        if (xhr.status === 200) {
            alert('Form data and files uploaded successfully!');
        } else {
            alert('Error submitting the form!');
        }
    };
    xhr.send(formData);
});
```

# Section 3: PHP Script

Finally, we need to create a PHP script that will receive the form data and files. The script should look something like this:

```php
<?php
    // Get the form data
    $name = $_POST['name'];
    $email = $_POST['email'];
    
    // Get the file data
    $fileName = $_FILES['photo']['name'];
    $fileData = $_FILES['photo']['tmp_name'];
    $fileType = $_FILES['photo']['type'];
    $fileSize = $_FILES['photo']['size'];
    
    // Do something with the data (e.g. save to a database, etc.)
    // ...
?>
```

# Section 4: Conclusion

In conclusion, to upload both data and files in one form using AJAX in JavaScript, we need to create an HTML form, use JavaScript to submit the form data via an AJAX request, and create a PHP script to receive the form data and files.
