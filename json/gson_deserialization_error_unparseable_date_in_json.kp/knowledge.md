---
title: Attempting to convert a millisecond-format date received from a server into a readable date using gson resulted in an unparseable date 1302828677828
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Gson cannot deserialize an unparseable date in millisecond format.
---

**Contents**

[TOC]

### Gson Deserialization

Gson is a Java library used for serializing and deserializing Java objects from and to JSON. To deserialize a millisecond-format date received from a server in JSON, the Gson library must be used.

### Unparseable Date Error

When attempting to deserialize a millisecond-format date received from a server in JSON, an error may occur if the date is unparseable. An unparseable date is a date that cannot be interpreted correctly by the Gson library. In this case, the unparseable date is "1302828677828".

### Troubleshooting

To troubleshoot this issue, it is important to first identify the exact format of the date. Once the format is determined, the Gson library can be used to parse the date correctly. Additionally, it may be necessary to convert the date to a different format in order to successfully deserialize it.

### Conclusion

In conclusion, Gson is a Java library used for serializing and deserializing Java objects from and to JSON. When attempting to deserialize a millisecond-format date received from a server in JSON, an error may occur if the date is unparseable. To troubleshoot this issue, it is important to first identify the exact format of the date and then use the Gson library to parse the date correctly. Additionally, it may be necessary to convert the date to a different format in order to successfully deserialize it.
