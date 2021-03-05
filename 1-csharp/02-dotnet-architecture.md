* .NET is a free, open-source development platform for building many kinds of apps.
    * Development platform means it’s a collection of libraries and languages that you can use to develop applications as well as runtime implementations to run your applications on
* Components of Components of a .NET implementation:
    * One or more runtimes. Examples: .NET Framework CLR, .NET 5 CLR.
    * A class library. Examples: .NET Framework Base Class Library, .NET 5 Base Class Library.
    * Optionally, one or more application frameworks. Examples: ASP.NET, Windows Forms, and Windows Presentation Foundation (WPF) are included in the .NET Framework and .NET 5.
    * Optionally, development tools. 
* .Net Standard
    * A set of APIs that are implemented by the Base Class Library of a .NET implementation
    * The base class library (BCL) provides classes and types that are helpful in performing day to day operation e.g. dealing with string and primitive types, database connection, IO operations.
* CLR
    * .NET provides a run-time environment, called the common language runtime, that runs the code and provides services that make the development process easier.
    * Some of those services include: memory management, JIT compliation, Exception handling support
* The compilation process
    * See Diagram
* Managed Code
    * Code whose execution is managed by a runtime.
    * The CLR is in charge of taking the managed code, compiling it into machine code and then executing it. On top of that, runtime provides several important services such as automatic memory management, security boundaries, type safety etc
* Unmanaged Code
    * Code that is developed outside .NET is unmanaged code.
        * Code that isn’t managed by the CLR
        * Does not leverage CLR features such as memory management
    * Executed by the help of wrapper classes
* Garbage Collection
    * CLR provides automatic memory management of your heap memory
        * When the garbage collector performs a collection, it checks for objects in the managed heap that are no longer being used by the application and performs the necessary operations to reclaim their memory.
    * Sometimes we utilize resources that are outside the scope of the CLR. We need to clean this up ourselves. 
    * Luckily, there is the IDisposable interface with the dispose() method that can be used to clean up these external resources.
        * Types that utilize these unmanaged resources inherit from the IDisposable Interface
    * You can also use using blocks and statements for clean up.