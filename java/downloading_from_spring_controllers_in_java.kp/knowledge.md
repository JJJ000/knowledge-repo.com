---
title: Obtaining a file from spring controllers
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To download a file from a Spring Controller in Java, use the ResponseEntity class to return the file as an HttpEntity object.
---

**Contents**

[TOC]

### Setting up the Controller

To download a file from a Spring Controller, we need to set up the controller to accept the request and return a response. This can be done by creating a controller class and adding an @GetMapping annotation to the desired method.

```
@GetMapping("/download")
public ResponseEntity<Resource> downloadFile() {
    // ...
}
```

### Creating the Resource

Next, we need to create the Resource object that will be returned in the response. This can be done by using the Resource class and passing in the file path as an argument.

```
Resource resource = new ClassPathResource("/path/to/file.txt");
```

### Setting the Response Headers

The response headers need to be set in order to ensure that the file is downloaded correctly. This can be done by using the HttpHeaders class and setting the appropriate headers.

```
HttpHeaders headers = new HttpHeaders();
headers.add(HttpHeaders.CONTENT_DISPOSITION, "attachment; filename=\"file.txt\"");
```

### Returning the Response

Finally, we need to return the response with the resource and the headers. This can be done by using the ResponseEntity class and passing in the resource and headers as arguments.

```
return ResponseEntity.ok()
        .headers(headers)
        .contentLength(resource.contentLength())
        .body(resource);
```
