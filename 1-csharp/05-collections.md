* Collections
    * A collection is a data structure that can hold one or more items.
    * In C# there are two major types of collections: generic and non generic
    * All collections provide methods for adding, removing, or finding items in the collection. 
* Collections Hierarchy
    * Note that arrays belong in the System namespace and is not included in the hierarchy. 
    * All collections that directly or indirectly implement the ICollection interface or the ICollection<T> interface share these features:
        * The ability to enumerate the collection
        * The ability to copy the collection contents to an array
        * Capacity and Count properties
        * A consistent lower bound
    * The IEnumerable interface exposes an enumerator, which supports a simple iteration over a non-generic/generic collection
* Arrays
    * The basic data structure to store a group of objects
    * A collection of objects of the same data type stored in a contiguous space in memory
    * Array types:
        * Single dimensional 
        * Multidimensional
        * Jagged 
            * Array of arrays
    * Note that array sizes are immutable
* Non Generic Collections
    * Non generic collections are used to store data when the size is unknown. This makes sure that you only take up the memory space you need!
    * Some common non generic collections:
        * Arraylist
        * Hashtable
        * Stack
        * Queue
    * Note that non generic collections store data as objects, this means that you can store multiple data types in one collection. To be able to have a homogenous data set, you’ll have to set up some type checking before storing in a non generic collection.
* Generic Collections
    * Leveraging generics you are able to have a type safe collection
    * Because you’re not casting things to an object, you’ll be able to save on overhead
    * Some common generic collections:
        * List<T>
            * list of objects that can be accessed by index
            * An ever expanding array
        * Dictionary<T>
            * Represents a collection of key/value pairs that are organized based on the key.
        * Stack<T>
            * LIFO
        * Queue<T>
            * FIFO
