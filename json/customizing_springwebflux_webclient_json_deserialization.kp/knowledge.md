---
title: What are the steps to modify the JSON deserialization of a springwebflux webclient?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: You can customize the JSON deserialization of SpringWebFlux WebClient by configuring a custom Jackson ObjectMapper.
---

**Contents**

[TOC]

1. Configure the WebClient

First, configure the WebClient to use a custom ObjectMapper. This can be done by adding a custom ClientHttpRequestInterceptor to the WebClient.Builder.

```
WebClient.Builder builder = WebClient.builder();
builder.interceptors(new CustomObjectMapperInterceptor());
WebClient webClient = builder.build();
```

2. Create a Custom ObjectMapper Interceptor

Next, create a custom ClientHttpRequestInterceptor that will inject a custom ObjectMapper for JSON deserialization. This interceptor should be added to the WebClient.Builder.

```
public class CustomObjectMapperInterceptor implements ClientHttpRequestInterceptor {
    @Override
    public ClientHttpResponse intercept(HttpRequest request, byte[] body, ClientHttpRequestExecution execution) throws IOException {
        ObjectMapper objectMapper = new ObjectMapper();
        // configure objectMapper here
        request.getHeaders().add("Content-Type", "application/json");
        request.getHeaders().add("Accept", "application/json");
        request.getHeaders().add("X-ObjectMapper", objectMapper.writeValueAsString(objectMapper));
        return execution.execute(request, body);
    }
}
```

3. Configure the ObjectMapper

Finally, configure the ObjectMapper to customize the JSON deserialization. This can be done by adding custom deserializers, configuring the date format, or any other custom configuration.

```
ObjectMapper objectMapper = new ObjectMapper();
objectMapper.registerModule(new JavaTimeModule());
objectMapper.configure(DeserializationFeature.FAIL_ON_UNKNOWN_PROPERTIES, false);
objectMapper.setDateFormat(new SimpleDateFormat("yyyy-MM-dd'T'HH:mm:ss.SSSZ"));
```
