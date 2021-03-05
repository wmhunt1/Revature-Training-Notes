* The 4 OOP Pillars
    * Abstraction
    * Polymorphism
    * Inheritance
    * Encapsulation
* Abstractions
    * a technique for dealing with complexity by providing users with a simplified interface which hides the complex details of an operation
    * Separation between the needed functionality and implementation details
    * Hide the implementation details of how data is being processed, of how logic is  executed, show your end user the properties/methods available to them for use
    * Implemented in C# using interfaces and abstract classes
* Interfaces
    * Contains definitions for a group of related functionalities that a non-abstract class or a struct must implement
    * May not declare instance data such as fields, auto-implemented properties, or property-like events.
    * All method stubs declared within interfaces are implicitly abstract
    * May define static methods, which must have an implementation
    * Does not have constructors
    * Cannot be instantiated at all
    * Beginning with C# 8.0, an interface may define a default implementation for members
* Abstract Classes
    * Denoted using abstract keyword
    * Can have constructors 
        * These are used to initialize fields in the abstract class
    * Often contains unimplemented method stubs
    * May have abstract and non abstract methods
    * May have fields
* Polymorphism
    * Literally means “many forms”
    * When you present the same interface but the inputs/data types being utilized would different
    * Ability to substitute different implementation details for different needs
    * Ability of an object to take on many forms
* Implementations
    * Ad hoc: defines a common interface for an arbitrary set of individually specified types
    * Parametric: when a type can be declared abstractly so that aspects of its implementation can be declared at runtime through the use of a parameterized type
    * Inclusion (Sub-Typal): when a name denotes instances of many different classes related by some common superclass
* Inheritance
    * The mechanism of basing an object or class upon another object or class, retaining similar implementation
        * Establishes an “is-a” relationship between objects
    * Promotes code reusability
    * In C# the constructors are inherited from parent to child
    * You can inherit from multiple interfaces but you can only inherit from one class
* Composition, Aggregation, Association
    * Composition describes a relationship between two or more objects where one object maintains instances of the other object(s). (has-a)
        * The composite object is responsible for the lifecycle of all constituent instances
        * Example: An order has multiple line items.
    * Aggregation describes a relationship between two or more objects where one object contains multiple instances of other objects. (has-a)
        * The lifecycle of the contained objects are independent of the aggregate object’s
        * Example: A department has multiple employees
    * Association describes a relationship between two objects where one object uses a separate instance of another object as a part of its functionality. (uses-a)
        * The lifecycles of the two objects are entirely separate from one another
        * Example: A computer uses a keyboard.
* Encapsulation
    * Treat related data/behavior as a single unit/capsule
    * This means that the validation and any processing of the data in your data classes would be done in the class itself. 
    * Implemented via data hiding (using access modifiers) and wrapping (grouping logic in classes, assemblies, and namespaces)
    * Wrapping focuses on encapsulating the complex data in order to present a simpler view for the user. On the other hand, data hiding focuses on restricting the use of data, intending to assure the data security.