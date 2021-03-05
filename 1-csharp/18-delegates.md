* What is a delegate?
    * A delegate is a reference type variable that holds the reference to a method.
    * Delegates are used for implementing events and the callback methods. 
    *  All delegates are implicitly derived from the System.Delegate class.
    * Delegates in C# are similar to the function pointer in C/C++.
* Why Do We Use Delegates?
    * Programmers often need to pass a method as a parameter of other methods. For this purpose, delegates are created and used. This ability to refer to a method as a parameter makes delegates ideal for defining callback methods. Ex: You can write a method that compares two objects in your application. That method can be used in a delegate for a sort algorithm. Because the comparison code is separate from the library, the sort method can be more general. 
* How to Define and Use Delegates
    * To use delegates, we use these three steps:
        * 