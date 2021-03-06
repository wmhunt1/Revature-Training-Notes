* MVC - Model
    * The Model in an MVC application represents the state of the application. Business logic should be encapsulated in the model, along with any implementation logic for persisting the state of the application.
* Model Overview
    * The model is the central component of the MVC pattern. 
    * It is the application's dynamic data structure. The model receives user input from the view through the controller. The model directly manages the data, logic and rules of the application.
* Model - Examples
    * A Model is a class that holds data in public properties that the program uses as a template for entities in the DB and, through model binding, are connected to user input pages (views), controllers, and the DataBase. 
    * Model classes reside in the Model folder in MVC folder structure.
* Binding
    * Controllers work with data that comes from HTTP requests. The HTTP request could provide a record key or posted form fields may provide values for the properties of the model. Writing code to retrieve each of these values and convert them from strings to .NET types would be tedious and error-prone. Model binding automates this process.  
    * The model binding system: 
        * Retrieves data from various sources such as route data, form fields, and query strings.
        * Provides the data to controllers as method parameters and public properties. 
        * Converts string data to .NET types. 
        * Updates properties of complex types.
* Model Binding
    * Model binding goes through the following steps after the routing system selects the action method: 
    1. Finds the first parameter of GetByID, an integer named id. 
    2. Looks through the available sources in the HTTP request and finds id = "2" in route data. 
    3. Converts the string "2" into integer 2. 
    4. Finds the next parameter of GetByID, a boolean named dogsOnly. 
    5. Looks through the sources and finds "DogsOnly=true" in the query string. Name matching is not case-sensitive. 
    6. Converts the string "true" into boolean true.
    7.  Calls the GetById method, passing in 2 for the id parameter, and true for the dogsOnly parameter.
* Model Binding Targets
    * Model binding tries to find values for 3 kinds of targets: 
        1. Parameters of the controller action method that a request is routed to.
        2.  Parameters of the Razor Pages handler method that a request is routed to. 
        3. Public properties of a controller or PageModel class, if specified by attributes. 
    * The [BindProperty] attribute can be applied to a public property of a controller or PageModel class to cause model binding to target that property. 
        1. Apply [BindProperties] to a controller class to tell model binding to target all public properties of the class:
        2. Apply [BindProperty] to a public property of a controller to cause model binding to target that property.
* Attributes for Complex Data Types
    * There are various different Annotation attributes for controlling model binding of complex types. These attributes affect model binding when posted form data is the source of values.
    * A complex type must have a public default constructor and public writable properties to bind. 
    * For binding to a parameter, the prefix is the parameter name. Some attributes have a Prefix property that lets you override the default usage of parameter or property name.
        * [BindRequired] - Applied only to model properties. Causes model binding to add a model state error if binding cannot occur for a model's property.
        * [BindNever] - Can only be applied to model properties. Prevents model binding from setting a model's property.
        * [Bind] - Can be applied to a class or a method parameter. Specifies which properties of a model should be included in model binding.
* Model State
    * The ModelState Class encapsulates the state of model binding to a property of an action-method argument or to the argument itself. 
    * If a source is found but can't be converted into the target type, model state is flagged as invalid. The target parameter or property is set to null or a default value. In an API controller that has the [ApiController] attribute, invalid model state results in an automatic HTTP 400 response. 
    * Otherwise, ModelState can be checked manually.
* Model Validation
    * Both model binding and model validation occur before the execution of a controller action. For web apps, if the controller doesn’t have the [ApiController] attribute, it's the app's responsibility to inspect ModelState.IsValid and react appropriately. Web apps typically redisplay the page with an error message. 
    * Validation attributes let you specify validation rules for model properties. Attributes are placed on the properties of the model.
* Build in Attributes: CreditCard etc
* Passing Data to Views - ViewModel
    * You can pass Strongly-Typed data and Weakly-Typed data to views. Strongly-typed views typically use ViewModel types designed to contain the data to display on that view. The controller creates and populates these ViewModel instances from the model.
    * Strongly-typed - Viewmodel
        * Specify a model (aka, viewmodel) type in the view and pass it from the action method. 
        * This allows the view to have strong type checking(and Intellisense!). Strong typing (or strongly typed) means every variable and constant has an explicitly defined type (string, int, or DateTime). The validity of types used in a view is checked at compile time. 
* Passing Data to ViewsViewData and ViewBag
    * Weakly typed ViewData and ViewBag
        * Weak types (or loose types) means that you don't explicitly declare the type of data you're using. You can use the collection of weakly typed data for passing small amounts of data in and out of controllers and views.
        * Weakly typed – ViewData, ViewDataAttribute, and ViewBag
        * Weakly typed means that you don't explicitly declare the type of data you're using. You can use the collection of weakly typed data for passing small amounts of data in and out of controllers and views.
        * ViewData()
            * Derives from ViewDataDictionary, so it has dictionary properties that can be useful, such as ContainsKey, Add, Remove, and Clear.
            * Keys in the dictionary are strings, so whitespace is allowed. Example: ViewData["Some Key With Whitespace"] 
            * Any type other than a string must be cast in the view to use ViewData.
        * ViewBag()
            * Derives from DynamicViewData, so it allows the creation of dynamic properties using dot notation (@ViewBag.SomeKey = <value or object>), and no casting is required. The syntax of ViewBag makes it quicker to add to controllers and views. 
            * Simpler to check for null values. Example: @ViewBag.Person?.Name 
            * ViewBag isn't available in the Razor Pages.