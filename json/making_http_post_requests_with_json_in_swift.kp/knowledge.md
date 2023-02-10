---
title: What is the process for sending an http post request with a JSON body in swift?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: You can make an HTTP Post request with a JSON body in Swift using the URLSession.shared.dataTask(withrequest) method.
---

**Contents**

[TOC]

### Section 1: Making the Request

To make an HTTP Post request with a JSON body in Swift, you can use the URLSession class. The URLSession class provides methods for creating and managing HTTP requests.

### Section 2: Encoding the JSON

To encode the JSON body, you can use the JSONEncoder class. The JSONEncoder class provides methods for encoding objects into JSON format.

### Section 3: Setting the Request Body

Once you have encoded the JSON body, you can set it as the request body by creating a URLRequest object and setting the httpBody property to the encoded JSON.

### Section 4: Sending the Request

Finally, you can send the request by creating a URLSessionDataTask object and passing the URLRequest object to its constructor. The URLSessionDataTask object can then be used to send the request.
