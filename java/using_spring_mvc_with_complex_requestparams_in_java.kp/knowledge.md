---
title: Requesting a complex object as a @requestparam in spring mvc
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: It is possible to use @RequestParam to pass a complex object as a GET request parameter in Spring MVC, provided the object is converted to a String representation first.
---

**Contents**

[TOC]

# Section 1: Overview
Spring MVC is a popular Java web development framework and is often used to create complex web applications. It is based on the Model-View-Controller architecture and is designed to simplify the development process. One of the features of Spring MVC is the ability to accept complex objects as GET @RequestParam parameters. This allows developers to pass complex objects from the client-side to the server-side, enabling more complex interactions between the two.

# Section 2: Setup
In order to use complex objects as GET @RequestParam parameters, the object must first be defined in the controller. This is done by creating an instance of the object and then annotating it with the @ModelAttribute annotation. This allows the object to be used in the controller method as a parameter. Additionally, the object must also be specified in the URL as a query parameter.

# Section 3: Example
For example, consider a controller with a method that accepts a complex object as a parameter. The controller method might look something like this:

```java
@RequestMapping("/getData")
public ResponseEntity<Object> getData(@ModelAttribute ComplexObject complexObject) {
    // code to process the complex object
    return new ResponseEntity<>(object, HttpStatus.OK);
}
```

The URL for this controller method would then be something like this:

```
http://localhost:8080/getData?complexObject.field1=value1&complexObject.field2=value2
```

# Section 4: Conclusion
By using complex objects as GET @RequestParam parameters, developers are able to pass complex data from the client-side to the server-side, enabling more complex interactions between the two. This is a powerful feature of Spring MVC that can be used to create more sophisticated web applications.
