* Typescript
    * Superset of JS, which means that all valid JS is valid TS 
    * JS flavor that imposes type checking and “compile” time errors
    * Statically typed (not strongly typed!) 	 
    * CANNOT IN ITSELF BE RUN IN THE BROWSER HAS TO BE TRANSPILED BEFORE IT’S EXECUTED (using node.js and tsc) 
    * Still JS under the hood
* Types in TS
    * All valid JS types are TS types 
    * Some special types TS introduced: 
        * Any - literally any type, when you assign something to any, you are resigning to JS’s type inference system (i.e. letting JS take the wheel and infer the type for you)
        * Unknown – a type safe any. Ensures someone using the type declares what the type is 
        * Void – a function that returns undefined or no return value. Like how you’d use void as a return type in C#
* STRUCTURAL TYPING
    * A core principle of TypeScript is that type checking focuses on the shape (structure) that objects have. 
    * This is called “Structural Typing” (or “Duck Typing”).  
    * The compiler only checks that at least the variable names required are present in args passed and that they match the types required.  
    * You use interfaces for these in TS 
        * Weird I know
* INTERFACES
    * The “contract” aspect of interfaces in TS refers to the structure of the object. So all objects of the interface type must follow the structure and type composition of that interface. 
    * In a nutshell: because interfaces are contracts and must be followed, in TS, the contract you’re setting is with regards to object structure. 
    * Note that interfaces in TS are the same as interfaces in C#, you use them to impose a structure to any class (or object) that would want to implement them
* COMPOSING TYPES
    * Note: TS is still JS under the hood
    * You can have multiple types for a single variable, you do these using union or the | sign 
    * So if you have a property that could be null or string, you can just say let x : null | string
* CLASSES
    * Same as JS classes, but TS classes has access modifiers Public, private, and protected. Works the same way as C#.
    * So TS developers can work in a more OOP way.
* Modules in TS
    * Works like a JS module but has some additional support 
    * Being able to alias your imports, import multiple modules from a single script file, only import types (type safe way of importing) 
    * This helps in organizing your code in their own files and using them in different places 
    * So you expose something for use using the export keyword and you use that something in another file using the import keyword 
    * Any declaration (variable, function, class, type alias, interface) can be exported by adding the export keyword before the type keyword.