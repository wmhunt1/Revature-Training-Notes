* Object Relational Mapper (ORM)
    * Note that in DBs, data is stored in tables, in rows and columns
    *  Dilemma: converting data from DB into something c# would understand (objects) 
    * ORMs are used (as you’ve probably guessed it) to answer this problem!  
    * ORMs maps data from DB to an object in your program
    *  The ORM we’ll be using is Entity Framework Core
* EF Core
    * ORM for .Net Core
    * 2 ways to connect your DB to your c# code: 
        * DB first The DB structure already exists, classes are created based on the existing structure 
        * Code first You create the DB structure based on the classes in the code
* Artifacts we’ll be working with
    * DBContext
        *  A DbContext instance represents a session with the database and can be used to query and save instances of your entities 
        * We need to make our own implementation of this that is specific to our application
    *  Connection String 
        * Used to connect to your db 
        * Contains information about the database you’ll be connecting to 
    * Startup project 
        * the one that the tools build and run
    *  Project 
        * also known as the target project because it's where the commands add or remove files.  
        * By default, the project in the current directory is the target project.
* Before you begin
    * Install the following packages in your data layer : 
        * Microsoft.EntityFrameworkCore.Design
        *  Microsoft.EntityFrameworkCore.Tools 
        * Npgsql.EntityFrameworkCore.PostgreSQL 
    * Install the package Microsoft.EntityFrameworkCore.Design in your startup project 
    * Install EF Core globally using the command dotnet tool install --global dotnet-ef 
        * So you can run ef commands
* Code First EF Core
    * Create Entities/Models Make sure to use naming convention  to ease the migration process 
    * Create implementation of the DBContext 
    * Run dotnet ef migrations add <name of migration> -c <implemented db-context>  --startup-project <location of startup project> 
    * Run dotnet ef database update --startup-project <location of startup project> 
    * Repeat steps 3-4 for any changes to your db
* Migration
    * Basically a snapshot of the database schema given the current state of your models 
    * Changes made to the schema based on changes made on your models/entities
    *  To apply the changes of the latest migration to your database, run dotnet ef database update
* DB first EF Core
    * Have a data access library project separate from the startup application project With a project reference from the latter to the former 
    * Install Microsoft Entity Framework Core Design and PostgreSQL to both projects 
    * Run the (extremely) long scaffold code 
        *  Dotnet ef dbcontext scaffold -c <connection-string-in-quotes> Npgsql.EntityFrameworkCore.PostgreSQL --startup-project <path to project folder>--force--output-dir Entities
    *  Edit the DBContext.OnConfiguring method from scaffolded code
    *  Any time you change the structure of the tables, go to step 3