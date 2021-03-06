* HTTP sessions consist of three phases. 
    1. The client establishes a (usually) TCP connection.
    2. The client sends its request and waits for the answer.
    3. The server processes the request, sending back its answer, with a status code and data.
* DNS (Domain Name System)
    * The Domain Name System (DNS) is essentially a directory of names and IP addresses.  
    * The DNS translates domain names (www.revature.com) to numerical IP addresses (255.255.255) for locating and identifying computer services and devices over the web. 
    * The DNS also associates identifying data with the unique domain names assigned to each connected entity.
* HTTP Request LifeCycle
    * HTTP sessions consist of three basic phases: 
        1. The client establishes a TCP connection. 
        2. The client sends its Request and waits for the Response. 
        3. The server processes the request and sends back its Response with a status code and appropriate data
* Establish a connection
    1. The client establishes the connection.  
        * The HTTP default port is port :80. 
    2. The client sends its request and waits for the answer. 
        * The URL of a page to fetch contains both the domain name, and the port number.
    3.  The server processes the request, sending back its answer, providing a status code and appropriate data. 
    * The client-server model requires an explicit Request. 
    * Workarounds to this limitation are:  
        1. ping the server periodically via the XMLHTTPRequest, 
        2.  Fetch APIs,  
        3. using the WebSockets API
* Connecting and Sending A Request
    * The client always establishes the connection. The client-server model does not allow the server to send data to the client without an explicit Request.  
    * The HTTP default port is port :80.  
    * The URL of a page to fetch contains both the domain name, and the port number.
    * On connection, the web browser sends the request. A client request consists of text directives, separated by CRLF (Carriage Return, Line Feed), divided into three blocks: Line 1 - request method followed by the absolute URL doc path without the protocol or domain name and the HTTP protocol version.
    * An HTTP header gives the server: 
        * information about what type of data is appropriate (e.g., what language, what MIME types, etc) 
        * other data which informs and may alter its behavior (e.g., not sending an answer if it is already cached). 
* Response
    * The server processes the Request and returns a Response. A server Response is formed of text directives, separated by CRLF, divided into three blocks:
    * Line 1 (the status line) :an acknowledgment of the HTTP version used, and a request status code (and its meaning).  
    * Subsequent lines represent specific HTTP headers, giving the client information like data type and size, compression algorithm used, hints about caching, etc. It ends with an empty line.
* Request Methods
    * Request methods (HTTP verbs) indicate the desired action to be performed on a resource. The most common requests are GET and POST. There are also PUT, DELETE, TRACE, HEAD, CONNECT, OPTIONS. 
        * The POST method sends data to a server. POST is used mainly for HTML Forms. 
        * The GET method requests/retrieves data.
    * Get - Requests a representation of the specified resource. GET should only retrieve data.
    * Head - Asks for a response identical to that of a GET request, but without the response body.
    * Post - Used to submit an entity to the specified resource.
    * Put - Replaces all current representations of the target resource with the request payloa
    * Delete - Deletes the specified resource.
    * Connect - Establishes a tunnel to the server identified by the target resource.
    * Options - Describes the communication options for the target resource
* Response Status Codes
    * HTTP response status codes give the result of an HTTP request. Responses are grouped in five classes:
        1. Informational responses (100–199), 
        2. Successful responses (200–299), 
        3. Redirects (300–399), 
        4. Client errors (400–499), 
        5. and Server errors (500–599).
* Safe and Idempotent
    * An HTTP method is safe if it doesn't alter the state of the server. In other words, a method is safe if it leads to a read-only operation. Several common HTTP methods are safe: GET, HEAD, or OPTIONS. 
    *  All safe methods are also idempotent, but not all idempotent methods are safe. For example, PUT and DELETE are both idempotent but unsafe. 
    * idempotent - an identical request can be made once or several times in a row with the same effect while leaving the server in the same state. Implemented correctly, the GET, HEAD, PUT, and DELETE method are idempotent, but not the POST method. All safe methods are idempotent.
