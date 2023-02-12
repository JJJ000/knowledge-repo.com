---
title: What is the best way to set the mime type header when using @responsebody in spring mvc?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: You can set the mime type header when using @ResponseBody in Json by adding the @ResponseBody annotation to the method and specifying the `content-type` attribute with the desired mime type.
---

**Contents**

[TOC]

1. Setting the Mime Type Header

The mime type header can be set using the @RequestMapping annotation. This annotation can be used to specify the mime type of the response. The following example shows how the mime type can be set to application/json:

@RequestMapping(value="/example", method=RequestMethod.GET, produces="application/json")
public @ResponseBody String example(){
  // Return JSON data
}

2. Configuring the Content Negotiation Manager

The Content Negotiation Manager in Spring MVC can be configured to automatically set the mime type header based on the requested file extension. This can be done by configuring the ContentNegotiationManagerFactoryBean in the application context. The following example shows how to configure the ContentNegotiationManagerFactoryBean to set the mime type header for JSON requests:

<bean class="org.springframework.web.accept.ContentNegotiationManagerFactoryBean">
  <property name="favorPathExtension" value="true"/>
  <property name="defaultContentType" value="application/json"/>
  <property name="mediaTypes">
    <map>
      <entry key="json" value="application/json"/>
    </map>
  </property>
</bean>

3. Setting the Content Type Header

The Content Type header in the response can be set using the @ResponseHeader annotation. The following example shows how to set the Content Type header to application/json:

@RequestMapping(value="/example", method=RequestMethod.GET)
@ResponseHeader(name="Content-Type", value="application/json")
public @ResponseBody String example(){
  // Return JSON data
}

4. Setting the Content Type Header in the Response Body

The Content Type header can also be set in the response body using the @ResponseBody annotation. The following example shows how to set the Content Type header to application/json in the response body:

@RequestMapping(value="/example", method=RequestMethod.GET)
public @ResponseBody String example(){
  // Return JSON data with Content-Type: application/json
}
