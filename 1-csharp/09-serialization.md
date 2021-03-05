* Serialization
    * Process of converting an object into a stream of bytes to store the object or transmit it to memory, a database, or a file
    * Save the state of the object for latter recreation (when needed)
    * Deserialization 
        * Process of unpacking serialized objects
    * Formats:
        * Custom binary (yeah, this is error prone, don’t do it)
        * Custom text (this has built in support in c#)
            * XML
            * JSON