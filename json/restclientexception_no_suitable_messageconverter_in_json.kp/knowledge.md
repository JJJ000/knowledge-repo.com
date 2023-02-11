---
title: No suitable converter was found to translate the response from the server
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: No suitable converter was found to convert the JSON response into an object.
---

**Contents**

[TOC]

## Overview
RestClientException is an exception that is thrown when an error occurs while attempting to make a REST call. This exception is thrown when there is no suitable HttpMessageConverter found in JSON. 

## Causes
The most common cause of this exception is when the client is attempting to make a REST call and the server is expecting a different format than what is being sent. For example, if the server is expecting JSON but the client is sending XML, this exception will be thrown. Additionally, this exception can be thrown if the client is attempting to make a call to a server that does not support the requested format. 

## Solutions
The best way to resolve this issue is to ensure that the client and server are both using the same format. If the client is sending XML and the server is expecting JSON, the client should be updated to send JSON instead. Additionally, the server should be configured to accept the format that the client is sending. 

Another solution is to use a different HttpMessageConverter such as Jackson or Gson to convert the data into the desired format. This can be done by adding the appropriate dependency to the project and then configuring the client to use the appropriate converter. 

Finally, it is also possible to use a custom HttpMessageConverter to convert the data into the desired format. This requires writing custom code to convert the data, but can be a useful solution if the other approaches are not feasible.
