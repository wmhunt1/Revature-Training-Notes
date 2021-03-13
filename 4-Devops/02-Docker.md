* it works on my machine dilmena
    * Applications need certain things to run on a machine (for example a runtime) When deploying an application, you would want your end users to have these basics set up to be able to run the app on their local machines But everyone’s machine is different!  We want to define a uniform environment in which our application runs on built with all the necessary configuration without having to inconvenience our end users
* Containerization vs Virtualization
    * Both containerization and virtualization provide solutions to creating a uniform environment across machines. This means that with either, you will be able to run your application in an environment that has the necessary artifacts. 
    * Difference 1: Containerization uses containers to achieve a uniform environment. Virtualization uses virtual machines (VMs). 
    * Difference 2: Containers virtualize the OS. VMs virtualize a machine. 
    * Difference 3: Containers allocate resources dynamically. VMs allocate resources statically.  
        * This means that with containers you only get assigned resources as needed. With VMs the resources are always there even if they aren’t being used.
* Docker
    * Docker is a containerization platform 
    * It’s a tool that allows you to wrap up your code into a deployable form (image) and run it anywhere using containers
    *  Very useful because you wouldn’t necessarily want users to download your code base if you want the general public to access your app
* Docker Packaging
    * Images 
        * filesystem, that contains everything needed to run an application - all dependencies, configuration, scripts, binaries, etc. 
        * This is what ensures that the environment is uniform throughout the containers
    * Containers
        *  A process that you run (on the filesystem you set up with an image) 
    * Registry
        *  A place that lets you distribute docker images
* Building an Image
    * Dockerfile 
        * a text document that contains all the commands a user could call on the command line to assemble an image 
    * Dockerignore 
        * Like gitignore but for building an image
        * This helps to avoid unnecessarily sending large or sensitive files and directories to the daemon (the engine that 