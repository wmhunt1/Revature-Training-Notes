* MSA
    * What is MSA? How does it differ from monolithic apps? From SOA? 
    * When do you want to implement MSA?
    *  What are the benefits of MSA? Monolithic architecture? SOA? 
    * MSA vs SOA?
    * What are the drawbacks of MSA? Monolithic architecture? SOA?
    * What are some MSA development practices that help in implementation/production?
* K8
    * What is container orchestration? 
        * A tool that helps in  deployment, scaling, networking, and monitoring of your containers and helps by abstracting details
    * What is k8s? 
        * A container orchestration tool. It provides tools that help deploy and manage containers that run over a network.  It lets us build application services that span multiple containers, schedule containers across a cluster, scale those containers, and manage their health over time.  
    * What is a cluster? Node? Pod? 
        * a set of node machines for running containerized applications (foundation) (control plane plus nodes)
        * the worker machines are nodes
        * a unit of replication
    * Explain the k8s architecture 
        * Cluster Node Pod Containers
    * What is the object config file?
        * A file that defines the configuration for a Kubernetes object
    * What is a deployment?
       * A Kubernetes Deployment is used to tell Kubernetes how to create or modify instances of the pods that hold a containerized application.
    * What are services?
        * A Kubernetes service is a logical abstraction for a deployed group of pods in a cluster (which all perform the same function)