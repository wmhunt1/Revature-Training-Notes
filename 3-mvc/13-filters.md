* Filters in ASP.NET Core allow code to be run before or after specific stages in the request processing pipeline. Filters help developers encapsulate cross-cutting concerns, like exception handling or authorization.
* Filters – Overview
    * Built-in NET filters handle tasks like Authorization and Response caching. 
    * Custom filters can be created to handle cross-cutting concerns like error handling, caching, configuration, authorization, and logging. 
    * Filters run within the ASP.NET Core Action Invocation Pipeline. The Action Invocation Pipeline begins running after ASP.NET Core selects the Action method to execute.
* Filter Types
    1. Authorization Filter - Runs first. Used to determine if the user is authorized for the request. Authorization filters stop the pipeline if the request is not authorized.
    2. Resource Filter - Runs after authorization and encapsulates all other filters. OnResourceExecuting() runs code before model binding and OnResourceExecuted() runs after the pipeline has completed.
    3. Action Filter - Runs OnActionExecuting() immediately before an Action method and OnActionExecuted() immediately after an Action method runs. These filters can change both the arguments passed into an Action and the Result returned from the Action.
    4. Exception Filter - Applies global policies to unhandled exceptions that occur before the response body has been written to.
    5. Result Filter - Runs immediately before and after the execution of Action results. They run only after the Action method has executed successfully
* Filter Interaction in the Filter Pipeline
    * Resource filters work like middleware in that they surround the execution of everything that comes later in the pipeline. Filters differ from middleware in that they're part of the runtime, which means that they have access to context and constructs. Even if you don't have any filters, middleware, try-catch, etc, ASP.NET Core will itself catch any exceptions within the pipeline of Controller, Action method, filters, View, etc.  An exception in the Startup class will probably crash the whole app, but that doesn’t happen with exceptions anywhere else. They'll be caught and typically an HTTP 500 will be sent.
* Filter Order-of-Execution and Scope
    * Filters are nested inside each other during different stages of the data lifecycle of an application. How filters are nested determines their scope. Global filters surround class (Controller) filters, which surround method (Action) filters. As a result of filter nesting, the ‘On…Executed()’ filter method runs in the reverse order of the ‘On…Executing()’ filter method. 
* Authorization Filter
    * Authorization filters: Are the first filters to run in the filter pipeline. Control access to Action methods. Have a OnExecuting() method, but no OnExecuted() method.
    * The built-in Authorization filter: Calls the authorization system. Does not authorize requests. cannot handle thrown exceptions.
* Resource Filters
    * Resource filters: Runs after the Authorization filter. Implement either the IResourceFilter or IAsyncResourceFilter interface. It wraps most of the rest of the filter pipeline.
    * Resource filter example: DisableFormValueModelBindingAttribute Prevents model binding from accessing the form data. Used for large file uploads to prevent the form data from being read into memory.
* Action Filters
    * Action filters: Implement either the IActionFilter or IAsyncActionFilter interface. Their execution surrounds the execution of Action methods.
* Action Filter - ActionExecutingContext
    * The ActionExecutingContext provides the following properties: ActionArguments - enables reading the inputs to the Action method. Access to various Controller Properties like HttpContext, ModelState, etc. These enable direct manipulation of the Controller instance and properties inherited from Controller class. Result – This gets or sets the ActionResult returned by the Action method. Setting Result to anything not-null skips execution of the Action method and subsequent Action filters.
* Action Filter
    * After the Action method executes, the ActionExecutedContext provides Controller access, Result, and the properties Canceled and Exception. Canceled is set to True if Action execution was short-circuited by another filter. Exception is Non-null if the Action or a previously run Action filter threw an exception.  Setting Exception to null: Effectively handles the exception. Result is executed as if it was returned from the Action method
* Exception Filter
    * Exception filters: handle exceptions thrown at any previous step Are an alternative to error-handling middleware (e.g. UseExceptionHandler), which is put in Startup.cs and is global Implement IExceptionFilter or IAsyncExceptionFilter. Can be used to implement common error handling policies.
* Result Filter
    * Result filters: Only execute when an Action produces an Action result. Implement an interface: IResultFilter or IAsyncResultFilter IAlwaysRunResultFilter or IAsyncAlwaysRunResultFilter Run before and then after preparing the result to be sent and sending it a [HttpPost] attribute. Provides access to the Canceled and Exception properties
