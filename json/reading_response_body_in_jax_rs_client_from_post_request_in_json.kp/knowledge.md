---
title: Retrieve the response body from a post request in a jax-rs client
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The response body can be read using the Response.readEntity() method.
---

**Contents**

[TOC]

## Creating the JAX-RS Client

The first step in reading the response body from a post request in Json is to create a JAX-RS client. This can be done by creating a Client object and configuring it with the desired settings.

```
Client client = ClientBuilder.newClient();
```

## Making the Post Request

Once the client is created, the next step is to make the post request. This can be done by creating a WebTarget object and using the request() method to make the post request.

```
WebTarget target = client.target("http://example.com/endpoint");
Response response = target.request().post(Entity.json(jsonObject));
```

## Reading the Response Body

Once the post request is made, the response body can be read by using the readEntity() method on the Response object.

```
String responseBody = response.readEntity(String.class);
```

## Closing the Client

Finally, the client should be closed when it is no longer needed to free up resources. This can be done by using the close() method on the Client object.

```
client.close();
```
