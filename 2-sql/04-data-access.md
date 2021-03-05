* Select Statement
    * Used for retrieving data from the database 
    * The select statement has several clauses:
        *  Select - Specifies what columns to have in the result set 
        * From  - Specifies what table to query 
        * Where - Defines a condition, filtering out rows that don’t match 
        * Group by - Aggregates multiple rows into one, if they have the same values for all the expressions in the group by list 
        * Having - defines a condition for filtering after group by
        *  Order by - specifies the sort order of the result set
    * Logical order of operations to the select statement: from, where, group by, having, select, order by
* Join
    * Combine data back together in a query that was spread out into many tables by the DB’s design 
    * Kinds: 
        * Full 
        * Inner 
        * Left
        * Right
        * Cross join - implements the cartesian product 
* Set operations
    * Used to combine the results of select queries 
    * Union  
        * Gives you all rows that are found in either query, without duplicates
    * Union All
        * Gives you all rows found in either query, period, including duplicates * Faster to run, potentially more data 
    * Intersect 
        * All rows that are in both queries
        *  No duplicates 
    * Except
        * Set difference 
        * All rows in the first query but not in the second query
* Subqueries
    * Sometimes, the most natural way to express a query is with a condition based on another query 
    * Operators in subqueries: IN, NOT IN, EXISTS, ANY, ALL