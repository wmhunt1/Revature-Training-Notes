* HTTP Request
    * Send from client to server
    *  3 parts: 
        * Start line 
            * Method - describes action to be performed 
            * Target - describes where to send the request
        *  Header 
            * Meta data 
            * Ex: content type - what data type the body has
        *  Body 
            * Data you want the server to process
* HTTP Verbs/Methods
    * Describes what action the client wants the server to perform on a given resource 
    * Common Verbs: 
        * GET Show resource 
        * POST Create a new resource 
        * PUT Update resource 
        * DELETE Delete resource
        * HEAD Returns just the headers of a get response
* Safe & Idempotent
    * Safe methods 
        * A method is said to be safe if it does not change the state of the resource 
        * Basically it should not affect the resource in any way 
        * GET, HEAD
    * Idempotent methods 
        * A method is said to be idempotent if the state of the resource is only affected once by any changes implemented by this method 
        * Aside from the initial change, the resource should not be affected by any subsequent calls to the same method with the same inputs 
        * For example, if you delete a resource, you can call the delete action on the same resource multiple times, but it will only get deleted once 
        * DELETE, PUT, HEAD, GET
* HTTP Response
    * From server to client
    *  3 parts: 
        * Status line 
            * Contains HTTP status codes of describing what happened when interacting with the server 
        * Headers
        * Body
* HTTP Status Codes
    * Status codes give a short description of whether an interaction is successful or not. 
    * Status codes are grouped by their number: 
        * 1xx - informational 
        * 2xx - communicating success 
        * 3xx - redirection 
        * 4xx - errors that are the client’s fault, client side errors 
        * 5xx - errors that are the server’s fault, server side errors
* Common Status
    * 100 Continue 200 Ok, for get requests 201 Created, for post 204 No content, for put and delete 301 Moved permanently 302 Found, moved temporarily, commonly used in redirection 400 Bad request, generic error message 402 Payment Required 404 Not found 405 Method not allowed (if server does not support method) 418 I’m a teapot, if you’re trying to make coffee in a teapot 451 Unavailable for Legal Reasons, based on Fahrenheit 451 500 Internal Server Error, try again later we’re having problems right now 501 Not Implemented, if a method isn’t implemented (if it’s under construction) 502 Bad Gateway
* DNS
    * The Domain Name System (DNS) is the phonebook of the Internet. 
    * Humans access information online through domain names, like nytimes.com or espn.com. Web browsers interact through Internet Protocol (IP) addresses. 
    * DNS translates domain names to IP addresses so browsers can load Internet resources.