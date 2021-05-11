* Dynamic Web Design
    * What’s the difference between a dynamic and a responsive web design? 
        * info that changes depending on viewer etc vs Adapting to the device
    * What does it mean if your web page is dynamic? 
        A web page is dynamic if it reacts to user interaction
    * What does is mean if your web page is responsive?
        * changing based on device
    * Can a web page be dynamic but not responsive? 
        * yes
    * Can a web page be responsive but not dynamic? 
        * yes
    * What are events?
        interaction with webpage
    * What is the DOM?
        Document object model,  html as a tree
* Response Request
    * Big picture of the request/response lc? 
        * A request is sent and a response is sent
    * What are the parts of a http request? 
        * Start Line, header, body
    * What are http methods? What http methods are safe? 
        * Action for server to perform - Get Post Delete
    * Idempotent?
        * only what you want to change changes
    *  What are the parts of a http response? 
        * status line, header, body
    * How are status codes grouped? 
        * 1xx - info
        * 2xx - comm suc
        * 3xx - redirection 
        * 4xx - clients fault
        * 5xx - servers fault
    * Difference between a 405 and a 501?
        * not allowed vs not implemented
* MVC
    * What is the Model? View? Controller?
        * State of application and BL/DL
        * Presents content
        * handle user input, work with model, choose view
    * why use ASP MVC
        * seperate different aspects while losely coupling them
    * What is binding?
        * Retrieves and provides data to controllers. The GetElementbyId stuff
    * What if ViewData? ViewBag? TempData
        * View Data Dictionary and properties
        * Creation of dynamic properties using dot notation
        * Stored until next request
    * How does routing work?
        * chooses 
* Http request lifecycle
    * What are the 3 parts?
        * connection, request, response
* Dependancy Injection
    * What is it?
        * A dependency is anything that an object requires in order to function properly. The Dependency injection (DI) design pattern is a technique used to achieve Inversion of Control (IoC) between classes and their dependencies. 
    * How does it work?
        *  1. Create an interface where you declare a method that you want to make available through Dependency Injection.
        2. Define the method in a class that implements the Interface.
        3. Add the dependency to ConfigureServices() with services.[desiredScope]<[interface], [class]>()
        4. Inject the dependency into the constructor of the dependent class and assign it to a private variable of the interface type.
* Filters
    * What are they?
        * Built-in NET filters handle tasks like Authorization and Response caching. 
    * What are the types?
        * Authorization - Are you allowed?
        * Resource - 
        * Action
        * Exception
        * Result
* Routing
    * What is it?
        * ASP.NET Core controllers use Routing middleware to match the URLs of incoming requests and map them to actions. Route templates are: 	-defined in startup code or attributes, 	-describe how URL paths are matched to actions, and 	-are used to generate URLs for links. Actions are either conventionally routed or attribute routed. 
        * Decides URL path based on actions and is in the start up config
