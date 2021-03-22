* Rest
    * Stands for REpresentational State Transfer Architectural style to design your services 
    * Guiding Principles of REST: Client-Server Stateless Cacheable Uniform Interface Layered System Code on Demand
* Uniform Interface
    * Your service would have an interface defined by four interface constraints:  
        * Identification of resources  
            * You’ll be able to identify what resource you’re trying to access
        * Manipulation of resources through representations  Using the appropriate action verb to access and manipulate your resources
        * Self-descriptive messages 
            *  Including in the response any necessary information to process the data, such as the format of the data (if the body is JSON, HTML, XML, etc...) otherwise the client would process it as text 
        * Hypermedia as the engine of application state (HATEOAS)
            *  Not really implemented as implementing this is very tedious
* Client Server & Layered System
    * Client Server 
        * The client app must evolve separately from the server app without any dependency on each other 
        * Decoupling your services from each other 
        * Services should be independent from each other, even if they call upon each other
    * Layered System 
        * Constraining the interactions of your components to the ones in the next layer 
        * Ex: You have an Authorization Service, a subsystem of BL Services, and another subsystem of DL Services. The layers would be UI>Auth & BL>DL, UI components can interact with the authorization service, after being authorized, it should be able to call some of the BL components, but it can never access the DL services
* Stateless & Cacheable
    * Stateless
        * Server isn’t responsible for storing client state 
        * The server will not store anything about the latest HTTP request the client made 
        * It will treat every request as new 
        * No session, no history 
    * Cacheable 
        * Resources from the server can be cached if applicable, these resources themselves must declare themselves cacheable 
        * Example of a cacheable request:
            * Get requests 
        * Example of a non cacheable requests:
            * Delete requests
* Code on demand (optional)
    * Allows client functionality to be extended by downloading and executing code in the form of applets or scripts
    * We usually send out static resources in the form of JSON or XML, but for example, the server can send executable script on the client side to render a part of the UI 
* Richardson Maturity Model
    * A way to describe how REST compliant your service is  
    * Grades your API according to the constraints of REST according to levels 
    * Level 0 Uses HTTP, single URI, one method (usually post) 
    * Level 1 Uses HTTP, multiple URIs, still one method (POST) Unique URI for each unique resource  
    * Level 2 Uses HTTP, multiple URIs, various http methods Operations depend on the action method used 
    * Level 3 Uses HTTP, multiple URIs, various http methods, and HATEOAS
* Rest vs Soap
    * Rest
        * HTTP 
        * Any format, JSON is easier to parse and is lightweight 
        * Stateless 
        * Good caching support 
        * Just https, not truly end to end security 
        * Simpler, easy to get up and running because http is everywhere and you don’t have to deal with XML 
        * Contract based on HTTP standards & conventions & is either hypermedia or an API description language 
        * Errors: 4xx, 5xx, status codes 
        * Gets told by the client what it wants to do to a resource via http verb
    * Soap
        * Any protocol over HTTP, just uses POST
        * XML
        * Could be stateful 
        * Supports caching but not at the http level 
        * Lots of security support 
        * Contract based on WSDL document 
        * Errors: faults 
        * Gets told by the client what it wants to do to a resource via articulating it in the soap message