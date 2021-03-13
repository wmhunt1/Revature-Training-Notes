* Intro to .NET
    * What is .Net?
        * Free, and open source development platform
    * What is C#?
        * An object-oriented and type-safe coding language.
    * What is the starting point of a program?
        * The entry point 
    * What is OOP?
        * Breaking code down into classes for reusability
    * What is type safety
        * Prevents type errors but not allowing you to switch data types.
* .Net Architecture
    * What is an SDK?
        * Software development kit like VSC
    * What's the role of the CLR?: Common language runtime
        * converts managed code into native code and run the program
    * What's the role of BCL?
        * Base class library: Provides built in data types and functions
    * What is managed code?
        * Code that is managed by a run time
    * What is unmanaged code?
        * Code made outside
    * What's the garbage collection process?
        * Automatic memory management. Checks for items in the managed heap (where reference type objects are allocated) that are no longer needed and gets rid of them to clear out memory
* Data Types
    * What is a data type?
        * Defined by values it can take, language, or operations that can be performed
    * What are the different data types in C#?
        * String, number, boolean, array
    * Value types vs reference types?
        * Directly stores data vs storing reference
    * What is CTS?
        * Common type System - The CTS is a standard definition of the types in .NET compliant languages.
    * What is language interoperability?
        * ability for languages to interact
    * What is CLS? How is it related to CTS?
        * Common language specification 
* App Architecture
    * What does seperation of concerns mean?
        * Organizing Code logically to group related items to make lasagna instead of sphagetti
    * What are classes?
        * Blue prints
    * What is the difference between a namescape and an assembly?
        * The main difference between namespace and assembly is that a namespace is a logical group of related classes that can be used by the languages targeted by Microsoft .NET framework, while Assembly is a building block of .NET Framework applications that form the fundamental unit of deployment, version control, reuse, activation scoping, and security permissions.
    * What is the difference between projects and namescapes?
        * Group of namescapes vs groups of classes
    * How many projects can be included in a solution?
        * Unlimited but no more than 15-20
* Collections
    * What are collections?
        * A class used to represent a set of similar data types as one unit and are used to group and manage related objects. For example, lists, queues, arrays, stacks.
    * What is the root interface of the collections hierarchy?
        * The Collection interface
    * What is the IEnumerable for?
        * is an interface defining a single method GetEnumerator() that returns an IEnumerator interface. It is the base interface for all non-generic collections that can be enumerated.
    * Arrays vs ArrayList vs List<T>?
        * Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.
        * ArrayList is a non-generic collection of objects whose size increases dynamically. It is the same as Array except that its size increases dynamically.
        * A list is an object which holds variables in a specific order.
    * What is a dictionary?
        * Dictionary is a generic collection which is generally used to store key/value pairs.
    * Stack vs queue?
        * Life list but FIFO and LIFO
* Exception Handling
    * What are exceptions? How are they different from errors?
        * An exception is a problem that arises during the execution of a program
        * Exceptions are those which can be handled at the run time whereas errors cannot be handled.
    * Why handle exceptions?
        * The exceptions should be handled to prevent any abnormal termination of a program. The program should keep running even if it gets interrupted in between.
    * How do you handle exceptions?
        * Try (IDs block), Catch (catchs exemption), and Finally (executes statements), and Throw (throws exception when problem appears)
    * Why throw exceptions?
        * ensure that failures do not go unnoticed
    * What is the exception hierarchy?
        * Tries catches in order until one is caught
* Modifiers
    * What are modifiers? Are they only limited to access modifiers?
        * Modifiers are C# keywords used to modify declarations of types (class, struct, interface, enum) and type members (fields, properties, methods, indexers, ...). The remaining sections explain these modifiers.
        * No they include modifiers like override or void
    * What are access modifiers?
        * Access modifiers are keywords used to specify the declared accessibility of types and type members
        * They are public (access not restricted), internal (current project), proected (limited to project, class, and subclasses), private (containing type)
    * What is the difference between const and readonly?
        * readonly is a constant defined at runtime. const is used to create a constant at compile time. readonly field value can be changed after declaration. const field value cannot be changed after declaration
    * Where can I apply the sealed keyword to?
        * You can also use the sealed modifier on a method or property that overrides a virtual method or property in a base class. This enables you to allow classes to derive from your class and prevent them from overriding specific virtual methods or properties.
    * How do I make something overridable? How do I override it?
        * virtual and then override modifier
* Serialization
    * What is serialization? Why is it important?
    * What are some use cases of serialization?
* Variance
    * What is variance? How is it related to polymorphism?
    * What are the different type variances?
    * What are the different ways to type cast?
    * What are the different ways to check a type?
    * Why is type checking important? 
* OOP Pillars
    * What are the 4 OOP pillars?
    * What is the difference between encapsulation and abstraction?
    * What are some use cases for abstraction? Polymorphism? Inheritance? Encapsulation?
    * Besides having an is-a relationship, what other object relationships are there?
* Unit Testing
    * What is unit testing?
    * Why is unit testing important?
    * What are parts of a unit test?
    * What is test driven development? When have you applied TDD? 
* Application monitering
    * Why are breakpoints important? What’s the use of breakpoints?
    * What is logging?
    * Why is logging important?
    * What are some use cases for logging in a production environment?
    * What are the logging levels? Why are there logging levels?
* Regular Expression
    * What are regular expressions?
    * When can we use them?
* Passing by reference
    * What does it mean to pass by reference?
    * What are some use cases for passing by reference?
    * What are the key differences between ref and out parameters?
* SOLID
    * What is SOLID? 
    * Give a brief explanation of each concept 
    * How do I implement SRP? OCP? LSP? ISP? DIP? 