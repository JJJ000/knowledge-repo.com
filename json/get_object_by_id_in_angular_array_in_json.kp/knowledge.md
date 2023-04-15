---
title: Retrieve an object from an array in angular based on its unique identifier
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the find method to retrieve an object from an array by its id in Angular.
---

**Contents**

[TOC]

## Introduction
Angular is a popular open-source web application framework that is commonly used for building dynamic user interfaces. One of the common use cases in an Angular application is to retrieve a specific object from an array of objects based on its ID value. In this article, we will discuss the steps involved in implementing this functionality in an Angular application.

## Step 1: Import HttpClientModule
To retrieve data from a remote server, you need to import HttpClientModule in the app.module.ts file. This module provides HTTP services for communicating with the server.

```typescript
import { HttpClientModule } from '@angular/common/http';

@NgModule({
  imports: [
    BrowserModule,
    HttpClientModule
  ],
  declarations: [AppComponent],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

## Step 2: Fetch Data from Server
The next step is to fetch data from the server using HttpClient's GET method. In this example, we will assume that we have an array of objects stored in a JSON file named 'data.json'. We will use HttpClient to fetch this data and store it in a variable called 'items'.

```typescript
import { Component, OnInit } from '@angular/core';
import { HttpClient } from '@angular/common/http';

interface Item {
  id: number;
  name: string;
}

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent implements OnInit {
  items: Item[];

  constructor(private http: HttpClient) {}

  ngOnInit() {
    this.http.get<Item[]>('assets/data.json').subscribe(data => {
      this.items = data;
    });
  }
}
```

## Step 3: Retrieve Object by ID
Once the data is fetched from the server and stored in the 'items' variable, we can retrieve a specific object from the array by its ID value. To do this, we can use the find() method on the array and pass a callback function that matches the object's ID value with the given ID.

```typescript
getObjectById(id: number): Item {
  return this.items.find(item => item.id === id);
}
```

## Conclusion
In this article, we discussed how to retrieve a specific object from an array of objects based on its ID value in an Angular application. We first imported HttpClientModule to fetch data from the server and then used HttpClient's GET method to retrieve data from a JSON file. Finally, we used the find() method on the array to retrieve the object by its ID value.
