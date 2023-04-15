---
title: Is there a way for me to modify the serialization process of a list containing jaxb objects in order to output them as json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use a custom serializer with Jackson or GSON libraries to serialize the list of JAXB objects to customized JSON format.
---

**Contents**

[TOC]

## Prerequisites 

Before customizing the serialization of a list of JAXB objects to JSON, you will need the following:
- Java development environment
- JAXB library
- JSON library (Jackson or Gson)

## Convert JAXB objects to JSON

To convert a list of JAXB objects to JSON, first, you need to instantiate a JAXBContext object by providing the package name of the JAXB classes:

```
JAXBContext jaxbContext = JAXBContext.newInstance(“package.name”);
```

Then, create an instance of Marshaller and set the properties to format the output as JSON:

```
Marshaller marshaller = jaxbContext.createMarshaller();
marshaller.setProperty(Marshaller.JAXB_FORMATTED_OUTPUT, true);
marshaller.setProperty(MarshallerProperties.MEDIA_TYPE, "application/json");
marshaller.setProperty(MarshallerProperties.JSON_INCLUDE_ROOT, false);
```

After that, you can marshal the list of JAXB objects to an output stream to get the JSON string:

```
StringWriter writer = new StringWriter();
marshaller.marshal(objectList, writer);
String jsonString = writer.toString();
```

## Customizing JSON output

To customize the JSON output, you can create a custom serializer using a JSON library such as Jackson or Gson. Here's an example of how to do it using Jackson:

```
public class CustomSerializer extends JsonSerializer<JAXBObject> {

    @Override
    public void serialize(JAXBObject object, JsonGenerator gen, SerializerProvider serializers)
            throws IOException, JsonProcessingException {
        gen.writeStartObject();
        gen.writeFieldName("id");
        gen.writeString(object.getId().toString());
        gen.writeFieldName("name");
        gen.writeString(object.getName());
        gen.writeEndObject();
    }
}
```

In the above example, I have created a custom serializer for a JAXBObject. I have overridden the serialize method to write only the id and name fields to the JSON output.

## Use the custom serializer

Once you have defined the custom serializer, you can use it while serializing the list of JAXB objects to JSON. Here's how you can customize the serialization using the above serializer:

```
ObjectMapper mapper = new ObjectMapper();
SimpleModule module = new SimpleModule();
module.addSerializer(JAXBObject.class, new CustomSerializer());
mapper.registerModule(module);

String jsonString = mapper.writeValueAsString(objectList);
```

In the above example, I have created an ObjectMapper and registered our custom serializer with it. Then, I have serialized the objectList to a JSON string using the ObjectMapper's writeValueAsString() method. The output JSON will now only contain the id and name fields of the JAXBObject.
