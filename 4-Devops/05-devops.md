* Devops
    * Marriage of development and operations 
    * A culture 
    * It's the concept of the development team and the operations team working together to bring the latest features and versions of software to the customer as fast as possible
    * a set of practices that allows us to roll out new features from the dev team and environment to production with quick response to any failures 
* CI
    * Stands for Continuous Integration 
    * All about automating building and testing code (using a pipeline) whenever you commit to a vcs (or make a pull request) to see if the code you just made passes the checks that have been set up
    * Drives the ongoing merging and testing of code, which leads to finding defects early (2018, Guckenheimer) 
    * Tools involved with CI: 
        * Pipelines (like Azure Pipelines, Github Actions, Jenkins, AWS Code Pipeline) 
        * Code Analysis tools like Sonar Cloud (more on this later) 
* CD
    * Stands for either Continuous Deployment or Continuous Delivery 
    * Continuous Delivery is when someone (obviously a authority figure) manually deploys the code to prod after much deliberation
    *  Continuous Deployment is when everything is automated to even the deployment of code to prod 
    * Of course CD is not only limited to releasing code to production, using the idea of CD to other environments before production like testing helps find bugs that might come up in an environment different from dev
* Achieving DevOps
    1. CI/CD 
    2. Utilizing VCS 
    3. Agile planning
    4.  Monitoring and Logging 
    5. Designing for scale 