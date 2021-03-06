* MVC – Controller
    * MVC controllers are responsible for responding to requests made against an ASP.NET MVC website. Each browser request is mapped to a particular controller.
* ASP.NET URL Routing
    * The default route in an ASP.NET Core application maps the first segment of a URL to a controller name, the second segment of a URL to a controller action, and the third segment to a parameter named id. The below Url equates to calling Product.Index(3)  
    * The routing configuration includes defaults for all three parameters. If a controller is not supplied, the controller defaults ‘Home’. If an action is not supplied, the action defaults to ‘Index’. If there’s no id, the id parameter defaults to an empty string.
* Controllers
    * If the URL, http://localhost/Product/Index/3, is entered into the browser, a controller named ProductController is invoked. The ProductController is responsible for generating the response to the browser request. Convention (and default) is to name the controller the same as the Url.
    * A controller is a regular C# class that derives from the base System.Web.Mvc.Controller class. 
    * The controller inherits useful methods from the Controller base class.
* Controller Actions
    * An action is a method on a controller class that gets called when you enter a URL with the action specified. If you make a request for URL, http://localhost/Product/Index/3,  the product controller is called and the Index action is invoked with the parameter “3”.
    * A controller action must be a public method of a controller class. Any public method in a controller class is exposed as a controller action. A method used as a controller action cannot be overloaded
* ActionResults
    * When a browser makes a request, a controller action returns a response in the form of an ActionResult. All ActionResults inherit from the ActionResult Class. Conventionally, an ActionResult is returned through a method of the Controller base class instead of returning an action result directly.