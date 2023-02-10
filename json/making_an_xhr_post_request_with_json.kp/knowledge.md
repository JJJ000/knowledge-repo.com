---
title: Send a post request with JSON data using xmlhttprequest
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Send an XmlHttpRequest with the POST method, setting the Content-Type header to `application/json` and the body to the JSON data.
---

**Contents**

[TOC]

**Section 1: Create the Request**

To create an XMLHttpRequest POST using JSON in JavaScript, you need to create a new XMLHttpRequest object, open it, and set the request type and headers.

```javascript
var xhr = new XMLHttpRequest();
xhr.open("POST", url, true);
xhr.setRequestHeader("Content-Type", "application/json");
```

**Section 2: Create the JSON Data**

Next, you need to create the JSON data that you want to send. The data needs to be in the form of a JavaScript object.

```javascript
var data = {
  name: "John Doe",
  age: 25
};
```

**Section 3: Send the Request**

Finally, you need to send the request with the JSON data.

```javascript
xhr.send(JSON.stringify(data));
```

**Section 4: Handle the Response**

Once the request is sent, you need to handle the response. This can be done by adding an event listener for the "load" event.

```javascript
xhr.addEventListener("load", function() {
  // Handle the response here
});
```
