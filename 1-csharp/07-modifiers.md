* Non-Access Modifiers
    * AKA keywords, modifiers, etc.
    * They are used to modify the declaration of types and type members
* Abstract
    * Applied to: classes and class members
    * Enables you to create classes and class members that are incomplete and must be implemented in a derived class.
    * This keyword cannot be used with the static keyword
    * Abstract methods are:
        * Implicitly virtual (implicitly overridable)
        * Only declared in abstract classes
        * Have no method body (just a method signature)
* Const
    * Applied to: fields
    * Constant fields and locals aren't variables and may not be modified. 
    * Constants can be numbers, Boolean values, strings, or a null reference. 
    * Don’t create a constant to represent information that you expect to change at any time. 
* Read-only
    * Applied to: fields, structs, and struct members
    * Read-only fields:
        * indicates that assignment to the field can only occur as part of the declaration or in a constructor in the same class. 
        * A read-only field can't be assigned after the constructor exits
    * Read-only struct:
        * indicates that the structure type is immutable. 
* Read-only vs const
    * THE READONLY KEYWORD IS DIFFERENT FROM THE CONST KEYWORD.
    * CONST FIELDS ARE INITIALIZED ON DECLARATION. THE INITIALIZATION OF READONLY FIELDS CAN BE ACCOMPLISHED AT A LATER POINT
    * A CONST FIELD IS A COMPILE-TIME CONSTANT, THE READONLY FIELD CAN BE USED FOR RUN-TIME CONSTANTS.
* Sealed
    * Applied to: classes, class members
    * Sealed classes cannot be inherited by other classes
    * Sealed methods and properties aren’t overridable in any classes that inherit those members
    * Similar to the final keyword in java
* Static
    * Applied to: classes and class members
    * Used to create class members which belongs to the type itself rather than to a specific object
        * This means that all instances of the type would have the share the same variable value for static fields
        * You wouldn’t need to instantiate an object of the type to access a static method
    * A static class can only have static members
* Virtual
    * Applied to: methods, properties, indexers, events
    * Used to modify a method, property, indexer, or event declaration and allow for it to be overridden in a derived class. 
    * By default, methods are non-virtual. You cannot override a non-virtual method.
    * You cannot use the virtual modifier with the static, abstract, private, or override modifiers. 
* Override
    * Applied to: methods, properties, indexers, events
    * Required to extend or modify the abstract or virtual implementation of an inherited method, property, indexer, or event.