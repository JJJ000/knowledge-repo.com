---
title: Store the result of a jquery getjson call in a variable
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Yes, the result of a jQuery getJSON request can be saved into a variable in JSON format.
---

**Contents**

[TOC]

1. Introduction

jQuery's getJSON() method is an AJAX method used to retrieve JSON data from a server using a GET HTTP request. The getJSON() method is used to make an asynchronous call to the server and returns the data in a JSON format. The returned data can then be saved into a variable in a JSON format.

2. Saving The JSON Data

The getJSON() method can be used to save the data into a variable in a JSON format. The following code shows an example of how to use the getJSON() method to save the data into a variable:

```javascript
$.getJSON(url, function(data) {
  var myData = data;
});
```

The url parameter is the URL of the server that the data is being requested from. The data parameter is the data returned from the server in a JSON format. The myData variable is the variable that the data is being saved into.

3. Accessing The Data

Once the data has been saved into a variable, it can be accessed using dot notation or bracket notation. The following code shows an example of how to access the data using dot notation:

```javascript
myData.name // returns the value of the "name" property
```

The following code shows an example of how to access the data using bracket notation:

```javascript
myData['name'] // returns the value of the "name" property
```

4. Conclusion

In conclusion, jQuery's getJSON() method can be used to save the data returned from a server into a variable in a JSON format. The data can then be accessed using dot notation or bracket notation.
