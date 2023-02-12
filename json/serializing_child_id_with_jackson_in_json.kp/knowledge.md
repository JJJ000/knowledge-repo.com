---
title: What is the Jackson syntax for serializing only the id of a child object?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the @JsonIdentityInfo annotation to serialize only the ID of a child with Jackson in JSON.
---

**Contents**

[TOC]

1. Add @JsonIdentityInfo Annotation 

Jackson provides the @JsonIdentityInfo annotation to serialize an object by id. This annotation can be used to prevent an infinite loop when serializing an object with a bidirectional relationship.

2. Set Serializer 

The annotation must be used in conjunction with a custom serializer. The custom serializer should extend the StdSerializer class and override the serialize method. In the serialize method, the id of the object should be returned instead of the full object.

3. Annotate Object 

The @JsonIdentityInfo annotation should be added to the object that needs to be serialized by id. The annotation should include the custom serializer class and an id field.

4. Serialize Object 

Finally, the object can be serialized with the Jackson ObjectMapper. The ObjectMapper will serialize the object with the id instead of the full object.
