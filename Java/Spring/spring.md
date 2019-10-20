# Spring 

## What is it ?

The Spring Framework is an application framework and inversion of control container for the Java platform

Current version 5 : Builded upon Reactive Streams compatible Reactor Core


Framework leger car utillise des plain java object POJO.


##Spring Boot
- Tomcat embarque
- AutoConfiguration


## Content negociation
Bean ContentNegociatingViewResolver :

 - Used by Spring MVC to determine view handler to use
 - Auto Configured by SpringBoot
 - The Content Negociating View Resolver will determine the view to use to render the data of the model
   to the client
   
   
Content type in the header : application/json, application/xml, text/html => For request body interpretation
Accept : for type we want in return






## Http Status
406 : Not acceptable (for instance content type is not found)



##Libraries

*JAXB API, stands for Java Architecture for XML Binding, 
using JAXB annotation to convert Java object to / from XML file

* Jackson Jackson is a pure JSON/Java data mapper 



## Spring REST Docs
Tool for generating API Documentation
Spring REST Docs hooks into controller tests to generate documentation snippets
Test Clients Supported :
 -Spring MVC Test
 -WebTestClient (Webflux)
 -REST Assured
 
 
Spring REST Docs support following testing framework :
 -JUnit 5
 -JUnit 4
 -Spock
 -TestNG