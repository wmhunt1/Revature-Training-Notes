* Data Types
    * A typical C# program uses types from the class library and user-defined types that model the concepts that are specific to the program's problem domain.
    * You use data types to structure the data that you process in your program. They’re very important in app design! 
    * Setting a data type is also a form of validation that leverages the strong typing of C#.
    * Fun Fact! All types inherit from the System.Object base class. (Which is just a fancy way of saying all types are objects!)
    * There are two major types:
        * Value Types
        * References
    * Examples
        * String
        * Number
        * Boolean
        * Array
        * Object
        * Date
        * Bytes
        * File
        * Null
* Common Type System (CTS)
    * The CTS is a standard definition of the types in .NET compliant languages.
    * Note that there are two major types: Value & Reference
    * Cool .NET feature: Language interoperability
        * Basically, in one solution, your projects can be written in multiple .NET compliant language.
        * You can have a project written in VB.NET and reference that same project in a project written in C#
* Value Types
    * Analogous to java’s primitives
    * Types that derive from System.Value. 
    * Stored in the stack and not the heap. 
        * This means that when accessing the value of a variable set to a value type, you get the value directly and not a reference to where the value is stored in heap. (Because variables are stored in stack and the actual objects they reference are stored in heap)
        * There's no separate heap allocation or garbage collection overhead for value-type variables.
    * Two categories:
        * Structs – used to create custom value types
        * Enums - defines a set of named integral constants 
* Reference Types
    * A type that is defined as a class, delegate, array, or interface is a reference type. 
    * At run time, when you declare a variable of a reference type, the variable contains the value null until you explicitly create an object by using the new operator or assign it an object that has been created elsewhere.
    * Note that reference types are stored in the heap. The stack holds the reference to a place in heap that contains the actual value of the object. 
