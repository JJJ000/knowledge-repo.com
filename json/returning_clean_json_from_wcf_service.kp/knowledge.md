---
title: What is the best way to get a formatted JSON response from a wcf service?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Return a response with the content type set to `application/json`.
---

**Contents**

[TOC]

# Section 1: Create a Data Contract
In order to return clean JSON from a WCF Service, you need to create a Data Contract. A Data Contract is a formal agreement between a service and a client that abstractly describes the data to be exchanged. 

# Section 2: Implement a Serialization Method
Once the Data Contract is created, you need to implement a serialization method. This will allow you to serialize the data into a JSON format. There are several different serialization methods available, such as DataContractJsonSerializer, JavaScriptSerializer, and Newtonsoft.Json. 

# Section 3: Configure the Service
After the serialization method is implemented, you need to configure the service to return JSON. This can be done by adding a behavior to the service configuration in the web.config file. The behavior should specify that the response format should be JSON. 

# Section 4: Test the Service
Finally, you should test the service to ensure that it is returning clean JSON. This can be done by sending a request to the service and verifying that the response is in the correct format.
