* DDL
    * Concerned with designing the structure of your database
    * Used in creating, altering, and deleting tables 
    * Commands: 
        * CREATE 
        * ALTER
        * DROP
* Constraints
    * In creating tables, columns can have constraints
    * Used for setting guidelines in what data belongs to a column
    * Types:
        * Data type 
        * Not Null
        * Unique
        * Check
        * Exclusion 
        * Primary Key - unique and not null
        *  Foreign Key
* Keys
    * Keys are used to uniquely identify a data set, and also to establish relationships between entities
    *  Candidate key 
        * Minimal set of columns in a table that every other column depends on 
        * The values of any candidate key can uniquely identify a row 
    * Primary key 
        * Unique identifier for a row in a table 
        * In implementation we choose one candidate key to identify the row 
    * Foreign Key 
        * A set of columns which hold the values of some primary key to establish a relationship to another row
    *  Composite Key 
        * Any key that’s more than one column
* Referential integrity
    * Refers to the accuracy and consistency of data within a relationship
    * whenever a foreign key value is used it must reference a valid, existing primary key in the parent table
* DTR in SQL
    * Relationships in SQL are defined by multiplicity 
    * 1:1 
        * This means that two sets of data are unique to each other
        * Ex: A wizard can only have one apprentice, and an apprentice can only follow one wizard 
    * 1:m 
        * This means that one set of data can have many instances of the other data set
        * Ex: A wizard can have many apprentices, but apprentices can only follow one wizard 
    * m:m 
        * This means that both data sets can have many instances of each other
        * Ex: in a wizard school, a wizard can teach many apprentices, and apprentices can learn from multiple wizards
* Implementation of SQL Relationships
    * 1:1 Put both entities in the same table or separate the entities in two tables with a FK reference that is Unique and Not Null 
    * 1:m  Two tables, FK that is not unique
    * m:m  3 tables one of which is a join/junction table
* ER Diagram
    * shows the relationships of entity sets stored in a database 
    * Visual representation of your DB design
* Why separate out data? 
    * Can’t insert some data without also having some other data
    * Forced to delete some data in order to delete some other data 
    * Redundancy can mean accidental consistency when updating
* Normalization
    * Designing a database in a certain way to ease data management
    * Normal Forms: 
        * 1NF 
            * Atomic Values
            * No repeating groups of columns
            * No duplicate rows 
        * 2NF 
            * Has to be 1NF
            * NO partial dependencies 
            * No composite keys mean you’re 2NF by default 
        * 3NF 
            * Has to be 2NF
            * NO transitive dependencies
    * The data in a table must depend on the key (1NF), the whole key (2NF), and nothing but the key (3NF).”