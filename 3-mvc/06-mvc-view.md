* In the Model-View-Controller (MVC) pattern, the view handles the app's data presentation and user interaction. A view is an HTML template with embedded Razor markup. 
* Views - Overview
    * In ASP.NET Core MVC, Views are .cshtml files that use C# in Razor markup. Usually, View files are grouped into folders named for each of an app’s Controllers. The folders are stored in a Views folder at the root of the app  
    * The Home Controller is represented by a Home folder inside the Views folder.  
    * This Home folder contains the Views for the About, Contact, and Index webpages. When a user requests one of these three webpages, Controller Actions in the Home Controller determine which of the three Views is used to Render (build and return) a webpage to the user.
* Views - Benefits
    * Views separate the user interface from other parts of the app.  
    * This helps with Separation of Concerns. The app is easier to maintain because it's better organized.  
    * The parts of the app are loosely coupled. Build and update the app’s Views separate from the business logic and data access components. 
* Views – How Controllers Specify Views
    * Views are typically returned from actions as a ViewResult, which is a type of ActionResult. Your action method can create and return a ViewResult (not common). Since most controllers inherit from Controller, you simply use the View helper method to return the ViewResult:
* Views – Return Options
    * The View helper method has several overloads.
* Dynamic Views
    * Views that don't declare a model type using @model but that have a model instance passed to them (for example, return View(Address);) can reference the instance's properties dynamically. This feature offers flexibility but doesn't offer compilation protection or IntelliSense. If the property doesn't exist, webpage generation fails at runtime.
* Partial Views
    * A partial view is a Razor markup file (.cshtml) that renders HTML output within another markup file's rendered output.
    * Partial view file names often begin with an underscore (_).  Partial views are an effective way to break up large markup files into smaller components and reduce the duplication of common markup content across markup files. 
    * Partial views shouldn't be used to maintain common layout elements (use _Layout.cshtml) or where complex rendering logic or code execution is required to render the markup. 
    * The Partial Tag Helper renders content asynchronously and uses an HTML-like syntax:
* Views – Passing Data
    * Strongly typed - Viewmodel
        * Specify a model (aka, viewmodel) type in the view and pass it from the action method. 
        * This allows the view to have strong type checking(and Intellisense!). Strong typing (or strongly typed) means every variable and constant has an explicitly defined type (string, int, or DateTime). The validity of types used in a view is checked at compile time. 
    * Weakly typed ViewData and ViewBag
        * Weak types (or loose types) means that you don't explicitly declare the type of data you're using. You can use the collection of weakly typed data for passing small amounts of data in and out of controllers and views.
    * Weakly typed – ViewData, ViewDataAttribute, and ViewBag
        * Weakly typed means that you don't explicitly declare the type of data you're using. You can use the collection of weakly typed data for passing small amounts of data in and out of controllers and views.
* ViewData and ViewBag Differences
    * ViewData()
        * Derives from ViewDataDictionary, so it has dictionary properties that can be useful, such as ContainsKey, Add, Remove, and Clear.
        * Keys in the dictionary are strings, so whitespace is allowed. Example: ViewData["Some Key With Whitespace"] 
        * Any type other than a string must be cast in the view to use ViewData.
    * ViewBag()
        * Derives from DynamicViewData, so it allows the creation of dynamic properties using dot notation (@ViewBag.SomeKey = <value or object>), and no casting is required. The syntax of ViewBag makes it quicker to add to controllers and views. 
        * Simpler to check for null values. Example: @ViewBag.Person?.Name 
        * ViewBag isn't available in the Razor Pages.
* Views – TempData
    * The TempData property stores data until it's read in another request. It is a Dictionary of string to object. Data is removed after the request that reads it.  The Keep(String) and Peek(string) methods can be used to examine the data without deletion at the end of the request. Keep() marks all items in the dictionary for retention. 
    * TempData is useful for 1) redirection when data is required for more than a single request and 2) when implemented by TempData providers using either cookies or session state.   
    * TempData is: 
        * Useful for redirection when data is required for more than a single request. 
        * Implemented by TempData providers using either cookies or session state.