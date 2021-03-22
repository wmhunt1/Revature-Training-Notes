* Monolithic Architecture
    * Just like our ASP.NET MVC application where the view is tightly coupled to the logic, a monolithic architecture describes applications that have everything built into it. The UI, BL, and DL are all wrapped up in a package. 
* The ASP.NET MVC Dilemma:The unhealthy codependency of the UI and BL
    * WITH ASP.NET MVC, THE VIEW IS TIGHTLY COUPLED TO THE PROCESSING LOGIC
    * THIS MEANS THAT THE CLIENT WILL HAVE TO WAIT FOR ITS REQUEST TO BE PROCESSED AND ALSO FOR THE VIEW THAT THE SERVER EVENTUALLY RETURNs
* The Solution
    * Break up the unhealthy codependency! Decoupling the logic that processes the data (aka your backend logic) from the logic that presents your data (aka your front end logic) Put those into two different servers 
* Service Oriented Architecure
    * SOA for short 
    * Architecture style for building software applications that use services available in a network such as the web 
    * Services are an implementation of a well defined business functionality 
    * So what we want to do is to delegate the whole business logic with the data layer associated with it as a service that returns to the client the necessary data it would need to present to the end user, how to present that data is wholly up to the client
* SOA Principles
    * Standardized Service Contract 
    * Loose Coupling 
    * Service Abstraction
    * Service Reusability 
    * Service Autonomy 
    * Service Statelessness 
    * Service Discoverability 
    * Service Composability 
    * Service Interoperability