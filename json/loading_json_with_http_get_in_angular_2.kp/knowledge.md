---
title: Retrieve JSON data from a local file using http.get() in angular 2
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-03 00:00:00
updated_at: 2023-03-03 00:00:00
tldr: The http.get() method can be used to read a local JSON file in Angular 2.
---

**Contents**

[TOC]

# Section 1: Overview

Angular 2 provides the http.get() method to allow developers to easily retrieve JSON content from a local file. This method is part of the HttpClient service, which is part of the @angular/common/http package. The http.get() method takes a URL as an argument and returns an Observable, which can be subscribed to in order to retrieve the data.

# Section 2: Setup

To use the http.get() method, the @angular/common/http package must be installed and imported into the project. This can be done with the following command: 

`npm install @angular/common/http`

The HttpClient service must also be imported into the component where it will be used:

`import { HttpClient } from '@angular/common/http';`

# Section 3: Usage

The http.get() method can be used to retrieve JSON content from a local file by providing the file's URL as an argument. For example, the following code will retrieve a local file named "data.json":

`this.http.get('/assets/data.json').subscribe(data => {
  // Do something with the data
});`

# Section 4: Conclusion

The http.get() method is a convenient way to retrieve JSON content from a local file in Angular 2. This method is part of the HttpClient service, which must be imported and set up before it can be used. Once set up, the http.get() method can be used to retrieve the content of a local file by providing its URL as an argument.
