* LINQ
    * Stands for Language-Integrated Query is a uniform query syntax in C# and VB.NET to retrieve data from different sources and formats. It is integrated in C# or VB, thereby eliminating the mismatch between programming languages and databases, as well as providing a single querying interface for different types of data sources.
* LINQ QUERIES
    * Expressions that retrieve data from a data source 
    * 3 parts of a query operation:
        * Data Source 
        * Query 
        * Execution
* Linq Query Expression Basics
    * A query is a set of instructions that describes what data to retrieve from a given data source (or sources) and what type and organization the returned data should have. A query expression is a query expressed in query syntax.
    * The source data is organized logically as a sequence of elements of the same kind. For example: 
        * a SQL database table contains a sequence of rows. 
        * In an XML file, there is a "sequence" of XML elements 
        * An ‘in-memory’ collection contains a sequence of objects.
    * A query expression must begin with a from clause and must end with a select or group clause. Between the first from clause and the last select or group clause, it can contain one or more of: where, orderby, join, let and even more from clauses. You can also use the into keyword to enable the result of a join or group clause to serve as the source for additional query clauses in the same query expression. 
    * From an application's viewpoint, the specific type and structure of the original source data is not important. 
    * The application always sees the source data as an IEnumerable<T> or IQueryable<T> collection. 
* LINQ – Query Expression Examples
    * A query can: 
        * Retrieve a subset of the elements to produce a new sequence without modifying the individual elements. The query may then sort or group the returned sequence in various ways 
        * Retrieve a sequence of elements but transform them to a new type of object.
        *  Retrieve a singleton value about the source data, such as: 
            * The number of elements that match a certain condition.
            *  The element that has the greatest or least value.
            *  The first element that matches a condition, or the sum of values in a specified set of elements. 
* LINQ – Query Variables
    * A query variable is any variable that stores a query instead of the result of a query.  
    * A query variable is always an enumerable type that will produce a sequence of elements when it is iterated over in a foreach statement or a direct call to its IEnumerator.MoveNext method.
* Query Execution
    * By default, linq queries have deferred execution. This means that unless iterated via a foreach loop, the query isn’t going to retrieve data from the data source. You can force immediate execution by either using an aggregate function in the query such as count or by calling the ToList() or ToArray() methods.