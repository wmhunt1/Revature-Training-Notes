* A dependency is anything that an object requires in order to function properly. The Dependency injection (DI) design pattern is a technique used to achieve Inversion of Control (IoC) between classes and their dependencies. 
* Dependencies Explained
    * IndexModel class depends on functionality provided by the MyDependency class.
    * An instance of the MyDependency class can be created in the IndexModel class to make WriteMessage() available to that class.
* Dependency Inversion – Overview
    * Code dependencies like this are problematic and should be avoided. To replace MyDependency with a different implementation, the class must be modified. If MyDependency has dependencies, they must be configured by the class.  The below implementation is difficult to unit test.
* Dependency Injection – A better way
    * Dependency injection helps provide services that classes need: By providing (through ASP.NET Core) a built-in service container called IServiceProvider.  By registering dependencies in the service container. By registering services through the Startup.ConfigureServices method. By using an interface (or base class) to abstract the dependency implementation. By injecting the service into the constructor of the class where it's used.  .NET framework takes on the responsibility of creating an instance of the dependency and disposing of it when it's no longer needed.
* Dependency Injection – Step by Step
    1. Create an interface where you declare a method that you want to make available through Dependency Injection.
    2. Define the method in a class that implements the Interface.
    3. Add the dependency to ConfigureServices() with services.[desiredScope]<[interface], [class]>()
    4. Inject the dependency into the constructor of the dependent class and assign it to a private variable of the interface type.
* [FromServices] AttributeAlternative to Constructor Injection
    * After registering a service with the service container, the [FromServices] attribute enables injecting the registered service directly into an Action Method without using constructor injection in the Controller. 
* .GetService<>()Alternative to Constructor Injection
    * When you are unable to obtain an instance of a needed service by Dependency Injection, .GetService<> can be used to get a service object. 
* Service Type Lifetimes
    * Transient services (AddTransient) are created each time they're requested from the service container. Best for lightweight, stateless services.
    * Scoped lifetime services (AddScoped) are created once per HTTP request (connection).
    * Singleton services (AddSingleton) are created the first time they're requested (or when Startup.ConfigureServices is run). Every subsequent request uses the same instance.
* Dependency Injection - .addDbContext
    * Entity Framework contexts are usually added to the service container using the scoped lifetime because web app database operations are normally scoped to the client request. The default lifetime is scoped if a lifetime isn't specified by an AddDbContext<TContext> overload when registering the database context. Services of a given lifetime shouldn't use a database context with a shorter lifetime than the service.
* Dependency Injection – Best Practices
    * Best design practices are to: 
        * Design services to use dependency injection to obtain their dependencies.
        * Avoid stateful, static classes and members. Design apps to use singleton services instead, which avoid creating global state. 
        * Avoid direct instantiation of dependent classes within services. Direct instantiation couples the code to a particular implementation.
        * Make classes small, well-factored, and easily tested. 
        * If a class seems to have too many injected dependencies, it’s a sign that the class has too many responsibilities and is violating the Single Responsibility Principle (SOLID). 
        * When services are resolved by IServiceProvider, constructor injection requires a public constructor. 
        * The built-in service container is designed to serve the needs of the framework and most consumer apps. It is recommended to use the built-in container unless you need a specific feature that the built-in container doesn't support. 
        * Dependency Injection is an alternative to static/global object access patterns. You may not be able to realize the benefits of DI if you mix it with static object access.
