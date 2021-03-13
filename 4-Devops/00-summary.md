* SDLC
    * What is the SDLC? 
        * software development life cycle
    * Phases in the SDLC?  
        * Planning => Analysis => Design => Implementation => Maintenance =>  back to planning
    * What are some implementations of the SDLC? 
        * Create unit tests and data, create builds and deploy
    * What is Agile? How is it related to scrum?
        * Agile is a general philosophy regarding software production, Scrum is an implementation of that philosophy pertaining specifically to project management. Guidelines vs Rules
    * What makes the waterfall model "rigid"?
        * Linear, one phase ends and one begins
    * How is scrum flexible?
        * Scrum facilitates flexibility through transparency, inspection, and adaptation to ultimately achieve the most valuable business outcomes. Scrum provides an adaptive mechanism for project delivery in which a change in requirements can be accommodated without significantly impacting overall project progress.
    * What is a burn down chart?
        * Basically a project tracker
    * What is the scrum master?
        * The scrum master is the team role responsible for ensuring the team lives agile values and principles and follows the processes and practices that the team agreed they would use. Clear obsticles, good environment and team dynamic, good relationship between team and customer, protect from distractions. The cat herder
    * What are user stories?
        * The end goal from user persepective
* Docker
    * Why is it important to have similar environments? 
        * So programs work that same 
    * What is containerization? How is it different from virtualization?
        * the process of packaging an application along with its required libraries, frameworks, and configuration files together so that it can be run in various computing environments efficiently.
        * containers vs VM
        * virtualize OS vs MAchine
        * allocate dynamics vs statically
    * What is docker?
        * Docker is a containerization platform 
    * What are images? Containers? How are they related? 
        * filesystem, that contains everything needed to run an application - all dependencies, configuration, scripts, binaries, etc. 
        * A process that you run (on the filesystem you set up with an image) 
        * Images can exist without containers, whereas a container needs to run an image to exist.
    * What is a docker file?
        * a text document that contains all the commands a user could call on the command line to assemble an image 
    * What is the docker daemon?
        * a persistent background process that manages the containers on a single host.
* Git
    * What are branches? Why should we branch? 
        * PArrelel versions of programs
        * Used in Version control and software management to maintain stability while isolated changes are made to code
    * What are pull requests? Why are they good practice?
        * Updated branchs, so you don't get to far behind or ahead 
    * What are merge conflicts? How can we resolve them?
        * When a branch has differences, by going through them
* Cloud
    * What is the cloud? What is cloud computing? 
        * A collection of servers owned by some service provider
    * What are the major service providers of cloud computing? 
        * AWS by Amazon Azure by Microsoft GCP by Google
    * What are the benefits of utilizing cloud services?
        * Cost, Scaling, and Security 
    * What are the different types of scaling? 
        * Horizontal (add or remove servers) 
        * Vertical (make servers worse or better)
    * What are the different service types provided by the cloud? 
        * Iaas: Infrastructure as a service (IaaS) is an instant computing infrastructure, provisioned and managed over the internet. You configure it the same way you’d configure your servers. 
        * Paas: Platforms as a service remove the need for organizations to manage the underlying infrastructure (usually hardware and operating systems) and allow you to focus on the deployment and management of your applications. 
        * SaaS: Software as a Service provides you with a completed product that is run and managed by the service provider.
* Cloud Deployment Models
    * What are regions? Availability zones? SLAs? 
        * Each Region is a separate geographic area. Availability Zones are multiple, isolated locations within each Region. Service-level agreements (SLAs) describe Microsoft's commitments for uptime and connectivity. 
    * What are the different cloud deployment models?
        * Private (certain org), Public (everyone), Hybrid (private resources but public hosting)
* DevOps
    * What are the respective goals of the dev and ops teams? 
        * Make stuff vs maintain stuff
    * What is DevOps? Why is DevOps important?
        * the combination of practices and tools designed to increase an organization's ability to deliver applications and services faster than traditional software development processes.
    * What’s CI/CD? 
        * Continues Integration/Deployment Automatic deployment vs manual 
    * What tools are involved in CI?
        Pipelines (Azure) and Code Anaylsis (sonar)
    * What other practices help in achieving devops? 
        * VSC, agile, monitoring and logging, and scale
* Code Analysis 
    * What is code analysis? 
        * Code analysis is the analysis of source code that is performed without actually executing programs. It involves the detection of vulnerabilities and functional errors in deployed or soon-to-be deployed software.
    * Why is it important? 
        * Improves the quality of the source code and security, as security data leaks have been reported more often. It can identify vulnerabilities in runtime as well, depending upon which type of code analysis your testing team implements. It also improves the coding standards among developers.
    * In a CI/CD pipeline, when should code analysis be performed?
        * Commit stage