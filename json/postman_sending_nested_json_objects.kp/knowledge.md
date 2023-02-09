---
title: Postman transmitting a JSON object with multiple levels of nesting
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: Send the nested JSON object as a stringified JSON object in the request body.
---

**Contents**

[TOC]

## Creating a Nested JSON Object

In order to create a nested JSON object, you must first create the parent object. This can be done by creating a JSON object and adding a key-value pair for each child object. For example, if you wanted to create a nested JSON object for a person, you could create a JSON object with the key "person" and the value being an object containing the person's name, age, etc.

## Adding Nested Objects

Once the parent object is created, you can add the nested objects. This is done by adding a new key-value pair to the parent object, with the key being the name of the nested object and the value being the object itself. For example, if you wanted to add a nested object for the person's address, you could add a key-value pair with the key "address" and the value being an object containing the address details.

## Sending the Nested JSON Object

Once the nested JSON object is created, it can be sent to the desired destination. This can be done by using an API call or by using a library such as Axios or Fetch. For example, if you wanted to send the nested JSON object to an API endpoint, you could use Axios to make a POST request to the endpoint with the nested JSON object as the payload.

## Validating the Nested JSON Object

Before sending the nested JSON object, it is important to ensure that it is valid and conforms to the expected format. This can be done by using a library such as JSON Schema or by validating the object manually. For example, if you wanted to validate the nested JSON object manually, you could check that all of the required keys are present and that the values are of the expected types.
