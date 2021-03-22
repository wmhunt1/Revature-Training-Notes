* No App is an Island
    * Web services provide a means of being able to access functionality of different applications online via their interfaces! Its language agnostic! You can use web services that are coded in other languages! To be able to use a web service, you only need to know the endpoint and what type of request to send (i.e. what format requests the service expects)
* SOAP (the service)
    * Stands for Simple Object Access Protocol 
    * Technically, a messaging protocol specification for exchanging structured information in the implementation of web services in computer networks. 
    *  Describes services that uses SOAP to communicate with other applications 
    * Protocol Independent , you can send soap messages via SMTP, HTTP, HTTPS, etc 
    * Platform and language independent
    *  Works on a basis of dumb endpoints, smart pipelines 
    * Well documented
* WSDL
    * Stands for Web Service Definition Language
    *  Describes a web service, specifies endpoints and methods 
    * User guide for your soap service 
    * If your web service was a restaurant, the WSDL is your takeout menu 
    * Contains the ABCs (Address, Binding, Contract) of your SOAP service
* Contract First vs Contract Last
    * SOAP services are highly documented, what is written in your WSDL is what you get 
    * In creating a soap service, you could either create the WSDL first (contract first) or create the service first and then generate the WSDL after
    * Some IDEs provide support to generate a WSDL file for your web service 
* SOAP message
    * If the WSDL is the menu, the message is your actual order 
    * An ordinary XML document containing the following elements: 
    * An envelope element that identifies the XML document as a soap message 
    * A header that would contain header information 
    * A body element that contains call and response info 
    * A fault element containing errors and status info
* XML namespace
    * SOAP services rely heavily on XML 
    * To be able to format messages to an input expected by the service, you would utilize XML namespaces to declare the tag structure the service would be expecting 
    * Can be used to describe the tag structure of an object 
    * A standardized tag structure would help in parsing data