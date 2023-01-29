---
title: Sending emails on an Android device using the javamail API without relying on the pre-installed application
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: It is possible to send emails in Android using JavaMail API without using the default/built-in app by creating a custom application.
---

**Contents**

[TOC]

### Introduction

Email is one of the most commonly used communication tools. Android provides an easy way to send emails from an application using the JavaMail API. This API allows for emails to be sent without having to use the default/built-in app.

### Setup

Before sending emails from an Android application, the following setup needs to be completed:

1. Download the JavaMail API from the JavaMail project website (https://java.net/projects/javamail/pages/Home).

2. Add the JavaMail API .jar file to the project's classpath.

3. Create a new mail session with the mail server's hostname and port.

4. Configure the mail session with the necessary authentication information.

### Sending the Email

Once the setup is complete, sending an email is a simple process. The following code snippet shows how to send an email using the JavaMail API:

```java
//Create a new session with the mail server
Session session = Session.getDefaultInstance(properties, null);

//Create the message
MimeMessage message = new MimeMessage(session);
message.setFrom(new InternetAddress("from@example.com"));
message.addRecipient(Message.RecipientType.TO, new InternetAddress("to@example.com"));
message.setSubject("Subject");
message.setText("Message body");

//Send the message
Transport.send(message);
```

### Conclusion

Using the JavaMail API, it is possible to send emails from an Android application without having to use the default/built-in app. The setup is straightforward and the code required to send an email is relatively simple.
