---
title: Obtain JSON from response body using retrofit 2
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the Retrofit2 Call<T> object`s execute() or enqueue() methods to get the JSON from the response body.
---

**Contents**

[TOC]

## Section 1: Create Retrofit Instance

Retrofit is a type-safe HTTP client for Android and Java. To create a Retrofit instance, you need to define a base URL and configure the converter, which is used to parse the response into the desired object.

```java
Retrofit retrofit = new Retrofit.Builder()
        .baseUrl(BASE_URL)
        .addConverterFactory(GsonConverterFactory.create())
        .build();
```

## Section 2: Create an Interface

Next, you need to create an interface that defines the endpoints. The interface should have methods that define the HTTP methods and the relative URL.

```java
public interface ApiService {
    @GET("/user")
    Call<User> getUser();
}
```

## Section 3: Create an Instance of ApiService

Now you can create an instance of the ApiService using the Retrofit instance.

```java
ApiService service = retrofit.create(ApiService.class);
```

## Section 4: Make the Request

Finally, you can make the request by calling the method on the ApiService instance.

```java
Call<User> call = service.getUser();
call.enqueue(new Callback<User>() {
    @Override
    public void onResponse(Call<User> call, Response<User> response) {
        if (response.isSuccessful()) {
            // Get the JSON from the response body
            String json = response.body().toString();
        }
    }

    @Override
    public void onFailure(Call<User> call, Throwable t) {
        // Handle error
    }
});
```
