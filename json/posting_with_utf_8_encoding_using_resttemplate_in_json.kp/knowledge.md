---
title: What is the syntax for telling resttemplate to post with utf-8 encoding?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Set the charset of the request to UTF-8 when creating the request entity.
---

**Contents**

[TOC]

1. Setting the Character Encoding

The RestTemplate class provides a setRequestFactory() method that allows you to set the character encoding used for requests. By default, the RestTemplate will use ISO-8859-1. To set the character encoding to UTF-8, use the following code:

```
RestTemplate restTemplate = new RestTemplate();
HttpComponentsClientHttpRequestFactory requestFactory = new HttpComponentsClientHttpRequestFactory();
requestFactory.setBufferRequestBody(false);
requestFactory.setCharset(StandardCharsets.UTF_8);
restTemplate.setRequestFactory(requestFactory);
```

2. Setting the Request Header

The RestTemplate class also provides a setRequestHeader() method that allows you to set additional headers on the request. To set the Content-Type header to application/json; charset=UTF-8, use the following code:

```
HttpHeaders headers = new HttpHeaders();
headers.setContentType(MediaType.APPLICATION_JSON_UTF8);
HttpEntity<String> entity = new HttpEntity<String>(headers);
restTemplate.exchange(url, HttpMethod.POST, entity, String.class);
```

3. Setting the Json Encoding

The RestTemplate also provides a setJsonEncoding() method that allows you to set the encoding for the JSON data that is sent in the request body. To set the encoding to UTF-8, use the following code:

```
MappingJackson2HttpMessageConverter converter = new MappingJackson2HttpMessageConverter();
converter.setJsonEncoding(StandardCharsets.UTF_8);
restTemplate.getMessageConverters().add(converter);
```

4. Setting the Message Converter

The RestTemplate class also provides a setMessageConverter() method that allows you to set the message converter used to serialize and deserialize JSON data. To use a UTF-8 encoding, use the following code:

```
MappingJackson2HttpMessageConverter converter = new MappingJackson2HttpMessageConverter();
converter.setObjectMapper(new ObjectMapper().setDefaultCharset(StandardCharsets.UTF_8));
restTemplate.setMessageConverter(converter);
```
