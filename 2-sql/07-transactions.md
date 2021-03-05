* Transactions
    * unit of work that either succeeds completely or fails
    *  Used to describe a group of queries that are executed as a batch that should completely succeed or not have any effect on the database at all
    *  ACID Stands for atomicity, consistency, isolation, durability Describes the characteristics of a transaction
* AC
    * Atomic 
        * All or nothing 
        * Either the transaction completely succeeds without errors and persists to a non volatile data storage system or it fails
    * Consistent 
        * Guarantees committed transaction state 
        * Makes sure that your transaction is not half finished
        * Consistency is a property ensuring that only valid data following all rules and constraints is written in the database. When a transaction results in invalid data, the database reverts to its previous state, which abides by all customary rules and constraints.
* ID
    * Isolation	 
        * guarantees the individuality of each transaction, and prevents them from being affected from other transactions. It ensures that transactions are securely and independently processed at the same time without interference, but it does not ensure the order of transactions. 
        * Two transactions, affecting same data, one will have to wait 
    * Durable 
        * A transaction isn’t considered complete until it is persisted in a non volatile data storage; by that it means your device could turn off and the data would still be saved
* Degrees of Isolation
    * Isolation levels define the degree to which a transaction must be isolated from the data modifications made by any other transaction in the database system 
    * Ways other transactions can affect your transaction: 
        * Dirty Read when your transaction reads uncommitted updates done by another transaction 
        * Non Repeatable Read when your transaction reads committed updates done by another transaction
        *  Phantom Read some rows may be added or removed due to the updates done by another transaction  
    * So to protect your transactions from being affected by these different phenomena, you have isolation levels!
* Isolation Levels
    * Read uncommitted (zero isolation)
        *  Does not protect transaction from anything, your transaction can read uncommitted data from other transactions
        *  Useful for when you read and write all the time, like netflix, or if you’re tracking number of covid cases, you can just reload 
    * Read committed 
        * Protects transaction from dirty read but not from non repeatable read. Meaning you can still read committed data from other transactions. 
        * Locks updates unless committed
    * Repeatable read 
        *  Protects transaction from non repeatable read but not from phantom read.  
        * When querying batches of data you’d still be able to get a different set of rows when you query the table before and after updates from another table occur 
        * Locks row  
    * Serializable 
        * Protects transaction from phantom read. Congratulations. You’ve reached the highest isolation level.  
        * This guarantees total isolation. 
        * It’s essentially locking the data set you’re working with from other transactions.