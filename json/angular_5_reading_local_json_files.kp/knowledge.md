---
title: Service for reading a local .json file in angular 5
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Angular 5 provides the HttpClient service for reading local .json files.
---

**Contents**

[TOC]

# Section 1: Creating the Service

Creating a service in Angular 5 is simple. The first step is to generate the service using the Angular CLI. To do this, run the following command in the terminal:

`ng generate service my-service`

This will create a new service called `my-service` in the `src/app` directory.

# Section 2: Reading the JSON File

The next step is to read the local JSON file. To do this, the `HttpClient` module must be imported into the service. To do this, open `my-service.service.ts` and add the following line to the top of the file:

`import { HttpClient } from '@angular/common/http';`

Next, inject the `HttpClient` into the service's constructor. To do this, add the following line to the constructor:

`constructor(private http: HttpClient) {}`

Finally, use the `get` method of the `HttpClient` to read the local JSON file. To do this, add the following line to the service:

`this.http.get('/path/to/my/file.json').subscribe(data => { ... });`

# Section 3: Parsing the JSON File

Once the JSON file has been read, it must be parsed. To do this, add the following line to the `subscribe` callback:

`let jsonData = JSON.parse(data);`

This will parse the JSON file and store the data in the `jsonData` variable.

# Section 4: Returning the Data

Finally, the data must be returned from the service. To do this, add the following line to the service:

`return jsonData;`

This will return the parsed JSON data from the service.
