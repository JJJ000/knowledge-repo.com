---
title: Attempting to utilize jquery to present data on an html page by loading a local JSON file
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: You can use the jQuery $.getJSON() function to read and display data from a local JSON file in an HTML page.
---

**Contents**

[TOC]

# Intro
JSON data is an easy and efficient way to retrieve and store data. JQuery is a widely used JavaScript library that simplifies many functions within JavaScript. This combination of technologies can be very powerful for displaying data in HTML pages.

# Steps
1. First create a JSON file with sample data, name it `data.json`. This file could contain data in the following format:

```json
{
   "employees": [
      {
         "firstName": "John",
         "lastName": "Doe",
         "age": 28
      },
      {
         "firstName": "Jane",
         "lastName": "Doe",
         "age": 31
      },
      {
         "firstName": "Jim",
         "lastName": "Carrey",
         "age": 59
      }
   ]
}
```

2. Next, create an HTML file and include a link to JQuery. In the below steps, we'll assume the name of the file to be `index.html`.

```html
<!DOCTYPE html>
<html>
<head>
   <title>Local JSON data display</title>
   <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
</head>
<body>
   <div id="employees"></div>
</body>
</html>
```

3. In order to display data from the `data.json` file, use the `.getJSON()` method in JQuery. This method takes two parameters; the first one refers to the file path and the second one is a callback function to process the data.

```js
$(document).ready(function() {
   $.getJSON('data.json', function(data) {
      console.log(data); // Just to view the data
   });
});
```

4. Finally, let's modify the callback function to show the data on the webpage. The `appendTo()` function in JQuery is used to append data to an element in the HTML page.

```js
$(document).ready(function() {
   $.getJSON('data.json', function(data) {
      $.each(data.employees, function (i, employee) {
         $('<div>').appendTo($('#employees'))
            .html('<p>Name: '+ employee.firstName + ' ' + employee.lastName +'</p><p>Age: ' + employee.age + '</p>');
      });
   });
});
```

# Conclusion
With the steps outlined above, it is very easy to load and display local JSON data in an HTML page using JQuery. So go ahead and experiment with the code to see how you can modify it to suit your needs.
