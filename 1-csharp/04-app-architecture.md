* Seperation of Concerns
    * The concept of organizing your code such that logic that follows a certain theme or have some dedicated functionality are grouped together
    * In a nutshell: Leveraging classes and other grouping mechanisms to group data and logic that belong with each other
    * We want to avoid having spaghetti code! We want lasagna! 
    * This is the first step in writing readable, extendable, and maintainable code
* Classes
    * Building blocks of your program
    * They are the blueprints to the actual objects that you process in your program
    * Besides being used to structure data, you also use classes to encapsulate logic and the data that go together.
* Namespace
    * Logical grouping of types that follow a certain theme of functionality.
    * To utilize the classes located in a different namespace, use the using keyword
    * Analogous to Java packages.
    * Note: If namespaces are the logical grouping of types, the physical grouping are called assemblies. 
* Project
    * A project contains all files that are compiled into an executable, library, or website.
        * Those files can include source code, icons, images, data files, and so on.
    * A project also contains compiler settings and other configuration files that might be needed by various services or components that your program communicates with.
    * The project file is an XML document that contains all the information and instructions that MSBuild needs in order to build your project, including the content, platform requirements, versioning information, web server or database server settings, and the tasks to perform.
    * Note that the file extension describes what kind of project you’re compiling: .csproj for a csharp project, .vbproj for a vb.net project