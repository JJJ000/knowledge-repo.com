---
title: Send a post request using resttemplate in JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: RestTemplate can be used to send a JSON-formatted POST request.
---

**Contents**

[TOC]

1. Setup

- Add the following dependencies to the project:
  - `org.springframework.web`
  - `org.springframework.boot`
  - `com.fasterxml.jackson.databind`

2. Create a RestTemplate

- Create an instance of `RestTemplate`:
  ```java
  RestTemplate restTemplate = new RestTemplate();
  ```

3. Create a JSON Object

- Create an instance of `ObjectMapper`:
  ```java
  ObjectMapper objectMapper = new ObjectMapper();
  ```

- Create a `Map` containing the JSON data:
  ```java
  Map<String, Object> jsonData = new HashMap<>();
  jsonData.put("key1", "value1");
  jsonData.put("key2", "value2");
  ```

4. Make the Request

- Convert the `Map` to a JSON string:
  ```java
  String jsonRequest = objectMapper.writeValueAsString(jsonData);
  ```

- Make the POST request:
  ```java
  HttpHeaders headers = new HttpHeaders();
  headers.setContentType(MediaType.APPLICATION_JSON);
  HttpEntity<String> request = new HttpEntity<>(jsonRequest, headers);
  ResponseEntity<String> response = restTemplate.postForEntity("http://example.com/endpoint", request, String.class);
  ```
