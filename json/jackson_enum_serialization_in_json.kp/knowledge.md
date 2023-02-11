---
title: Converting enumerations to JSON using jackson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Enums can be serialized with Jackson by annotating them with @JsonValue or @JsonCreator.
---

**Contents**

[TOC]

##### Serializing Enums

Enums can be serialized using Jackson in JSON by using the `@JsonValue` annotation. This annotation allows you to specify a custom serialization strategy for the enum, such as serializing it as a string or an integer. 

##### Example

For example, consider the following enum:

```java
public enum Color {
    RED,
    GREEN,
    BLUE
}
```

To serialize this enum as a string, you would add the `@JsonValue` annotation to the enum:

```java
public enum Color {
    @JsonValue
    RED("red"),
    @JsonValue
    GREEN("green"),
    @JsonValue
    BLUE("blue")

    private final String value;

    Color(String value) {
        this.value = value;
    }

    @Override
    public String toString() {
        return value;
    }
}
```

##### Deserializing Enums

Enums can also be deserialized using Jackson in JSON. To deserialize an enum, you need to specify a custom deserializer. This deserializer needs to take the incoming JSON string and convert it to the corresponding enum value.

For example, consider the following deserializer for the Color enum:

```java
public class ColorDeserializer extends StdDeserializer<Color> {
    public ColorDeserializer() {
        super(Color.class);
    }

    @Override
    public Color deserialize(JsonParser parser, DeserializationContext context) throws IOException {
        String value = parser.getValueAsString();
        if (value.equalsIgnoreCase("red")) {
            return Color.RED;
        } else if (value.equalsIgnoreCase("green")) {
            return Color.GREEN;
        } else if (value.equalsIgnoreCase("blue")) {
            return Color.BLUE;
        } else {
            throw new IllegalArgumentException("Unknown color: " + value);
        }
    }
}
```

Once the deserializer is defined, it needs to be registered with the ObjectMapper:

```java
ObjectMapper mapper = new ObjectMapper();
SimpleModule module = new SimpleModule();
module.addDeserializer(Color.class, new ColorDeserializer());
mapper.registerModule(module);
```

Now the ObjectMapper can deserialize the Color enum from JSON strings.
