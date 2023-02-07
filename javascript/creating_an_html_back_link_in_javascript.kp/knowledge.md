---
title: What is the process for creating an html back link?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: In Javascript, an HTML back link can be created using the `document.write()` method.
---

**Contents**

[TOC]

### Creating the HTML Link

The HTML link can be created using the `<a>` tag in Javascript. The `<a>` tag is used to create a hyperlink to another web page. To create an HTML back link, the `href` attribute should be set to the URL of the previous page. 

```
<a href="http://www.previouspage.com">Back</a>
```

### Adding the onClick Event

The onClick event can be used to trigger a function when the user clicks on the link. This can be used to execute a function that will take the user back to the previous page. The onClick event can be added to the `<a>` tag as follows: 

```
<a href="http://www.previouspage.com" onClick="goBack()">Back</a>
```

### Creating the goBack() Function

The goBack() function can be created using the window.history object's `go()` method. This method takes an integer as an argument, which is the number of pages to go back. The goBack() function can be defined as follows:

```
function goBack() {
    window.history.go(-1);
}
```

### Adding the goBack() Function to the HTML

The goBack() function can be added to the HTML page by using the `<script>` tag. The `<script>` tag should be placed between the `<head>` and `<body>` tags. The goBack() function should be placed inside the `<script>` tag as follows:

```
<html>
    <head>
        <script>
            function goBack() {
                window.history.go(-1);
            }
        </script>
    </head>
    <body>
        <a href="http://www.previouspage.com" onClick="goBack()">Back</a>
    </body>
</html>
```
