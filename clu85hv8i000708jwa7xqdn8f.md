---
title: "🐳Day 21 - Docker Important Interview Questions"
datePublished: Tue Mar 26 2024 09:04:37 GMT+0000 (Coordinated Universal Time)
cuid: clu85hv8i000708jwa7xqdn8f
slug: day-21-docker-important-interview-questions
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1711443778506/9a05fa7a-408a-4778-a459-6c20e7bb91cd.png
tags: docker, devops, docker-images, devops-articles, devops-journey, 90daysofdevops, trainwithshubham, vivekmoudekar

---

### **Introduction**

Docker is a good topic to ask in DevOps Engineer Interviews, mostly for freshers. One must surely try these questions in order to be better in Docker.

1. ### <mark>What is the Difference between an Image, Container and Engine?</mark>
    
    **Image**:
    
    * An image is a lightweight, standalone, executable package that includes everything needed to run a piece of software, including the code, runtime, libraries, and dependencies.
        
    * Images are often built from a Dockerfile, which contains instructions for assembling the image layer by layer.
        
    * Images are immutable, meaning once built, they remain unchanged.
        
    
    **Container**:
    
    * A container is a runtime instance of an image.
        
    * It's a lightweight, isolated, and portable environment that packages an application and its dependencies together, ensuring consistency across different environments.
        
    * Containers run on top of a host operating system and share the kernel with other containers.
        
    * Containers are ephemeral, meaning they can be started, stopped, and destroyed without affecting the host system or other containers.
        
    
    **Engine**:
    
    * The engine, often referred to as the container engine, is the underlying software responsible for creating, managing, and running containers.
        
    * In the context of Docker, the Docker Engine is the core component that enables containerization.
        
    * It includes the Docker daemon, which runs on the host system, and the Docker client, which allows users to interact with the daemon through commands.
        
    * The engine orchestrates the building of images, the creation and management of containers, networking, storage, and more.
        
    
    In summary, an image is a static, read-only blueprint for a piece of software, a container is a runnable instance of that image, and the engine is the software responsible for managing and orchestrating containers on a host system. Together, they form the foundation of containerization technology, enabling efficient and scalable deployment of applications.
    
2. ### <mark>What is the Difference between the Docker command COPY vs ADD?</mark>
    
    \-&gt; The Dockerfile commands `COPY` and `ADD` are both used to copy files and directories from the host machine into the Docker image being built.but there are some differences.
    
    **COPY**:
    
    * The `COPY` command is straightforward and primarily used for copying local files and directories into the container.
        
    * It has a simple syntax: `COPY <src> <dest>`, where `<src>` is the source file or directory on the host, and `<dest>` is the destination path in the image.
        
    * `COPY` only copies the files and directories specified in `<src>` to `<dest>`. It does not perform any extra processing or decompression.
        
    
    **ADD**:
    
    * The `ADD` command is more versatile and can do more than just copying files. It can also extract files from local or remote tar files, as well as URLs.
        
    * Its syntax is: `ADD <src> <dest>`, similar to `COPY`.
        
    * In addition to copying files, `ADD` has some extra functionality:
        
        * It can handle URLs and automatically download files from them.
            
        * It can also handle compressed files (e.g., .tar, .gz) and automatically extract them into the destination directory.
            
    * Because of this extra functionality, `ADD` is slightly more complex and can sometimes lead to unexpected behavior if not used carefully.
        
        In summary, while both `COPY` and `ADD` can be used to copy files into Docker images, `COPY` is generally preferred for simple file copying operations, while `ADD` can be useful for more advanced scenarios involving URLs or compressed files.
        
    
3. ### <mark>What is the Difference between the Docker command CMD vs RUN?</mark>
    
      
    The Dockerfile commands `CMD` and `RUN` serve different purposes and are used at different stages of the Docker image build process:
    
    **RUN**:
    
    * The `RUN` command is used to execute commands during the image build process. These commands are executed in the container's filesystem at build time.
        
    * It is typically used to install dependencies, run package managers, download files, or perform any other actions required to set up the environment inside the image.  
        
        **CMD**:
        
        * The `CMD` command is used to specify the default command to run when a container is started from the image. It defines the primary command that will be executed when the container is run, although it can be overridden at runtime.
            
        * If the Dockerfile contains multiple `CMD` instructions, only the last one will take effect.
            
        * The `CMD` instruction can be specified in two formats:
            
            * Exec form: `CMD ["executable", "param1", "param2"]`
                
            * Shell form: `CMD command param1 param2`
                
        * If a Docker container is started without specifying a command (e.g., `docker run <image>`), the command specified by `CMD` will be executed.
            
    
    In summary, `RUN` is used to execute commands during the image build process to set up the environment inside the image, while `CMD` is used to specify the default command to run when a container is started from the image.
    
      
    
4. ### <mark>How Will you reduce the size of the Docker image?</mark>
    
    Reducing the size of a Docker image is crucial for optimizing performance, minimizing resource usage, and enhancing overall efficiency. Here are several strategies to achieve this:
    
    **1\. Use Alpine Linux or other lightweight base images**: Use Alpine Linux rather than a full-fledged operating system like Ubuntu, Alpine Linux is known for its small size and efficiency.
    

2\. **Multi-stage builds**: This allows you to compile dependencies and build artifacts in one stage and copy only the necessary files into the final image, reducing the overall image size.

3.**Minimize layers**: Minimize the number of layers in your Dockerfile by combining multiple commands into a single RUN instruction and cleaning up unnecessary files and dependencies within the same layer.

4.**Use specific package versions**: To avoid unnecessary dependencies from being pulled into the image

5.**Compress files where appropriate**: Compress files and assets where applicable, especially if they are large and don't need to be uncompressed during runtime.

6.**Remove unnecessary dependencies**: Identify and remove any unnecessary dependencies or packages that are not required for the application to function properly.

5. ### <mark>Why and when to use Docker?</mark>
    
    Docker is a powerful tool used for containerization, providing a way to package, distribute, and run applications in isolated environments called containers. Here are several reasons why and when to use Docker:
    
    **Consistency across environments**: Docker ensures consistency between development, testing, and production environments by packaging applications and their dependencies into portable containers. This minimizes the risk of "it works on my machine" issues and streamlines the deployment process.
    
    **Isolation**: Containers provide isolation for applications, allowing them to run independently of the underlying host system and other containers. This isolation improves security, as each container has its own filesystem, network, and process space.
    
    **Efficiency**: Docker containers are lightweight and share the host system's kernel, resulting in faster startup times and lower resource overhead compared to traditional virtual machines.
    
    **Portability**: Docker containers are portable across different platforms and environments, including local development machines, cloud providers, and on-premises servers.
    
    **Scalability**: Docker enables horizontal scaling of applications by allowing multiple instances of a container to run simultaneously.
    
    **Microservices architecture**: Docker facilitates the adoption of microservices architecture by providing a lightweight and scalable way to deploy and manage individual services as containers.
    
    In summary, Docker is beneficial for its ability to provide consistency, isolation, efficiency, portability, scalability, and support for modern software development and deployment practices.
    

6. ### <mark>Explain the Docker components and how they interact with each other.</mark>
    
      
    Docker is composed of several key components that work together to enable containerization and manage containerized applications.
    
    **Docker Engine**:
    
    * At the core of Docker is the Docker Engine, which is responsible for building, running, and managing containers.
        
    * The Docker Engine consists of two main components:
        
        * **Docker Daemon**: This is a persistent background process that manages Docker objects, such as images, containers, networks, and volumes. The daemon listens for Docker API requests and handles container lifecycle operations.
            
        * **Docker Client**: This is a command-line tool that allows users to interact with the Docker daemon via the Docker API. Users can use the Docker client to build, run, and manage containers using simple commands.
            
        
        **Images**:
        
        * Images are read-only templates that contain the filesystem and configuration needed to run a containerized application.
            
        * Images are built from a Dockerfile, which contains instructions for creating the image layer by layer.
            
        * Docker images can be stored locally or pushed to a registry, such as Docker Hub or a private registry, for sharing and distribution.
            
        
        **Containers**:
        
        * Containers are lightweight, portable, and isolated runtime environments that run instances of Docker images.
            
        * Each container encapsulates an application and its dependencies, ensuring consistency and isolation from the host system and other containers.
            
        * Containers are created from Docker images and can be started, stopped, paused, and deleted using Docker commands.
            
        
        **Docker Compose**:
        
        * Docker Compose is a tool for defining and running multi-container Docker applications.
            
        * It uses a YAML configuration file (docker-compose.yml) to define services, networks, and volumes for an application.
            
        * Docker Compose simplifies the process of managing complex multi-container applications by allowing users to define the entire application stack in a single file and manage it with a few simple commands.
            
    
7. ### <mark>In what real scenarios have you used Docker?</mark>
    
    used by developers to create isolated development environments for building, testing, and debugging applications. Docker containers provide consistency across development, testing, and production environments, ensuring that applications behave the same way in different environments.
    
    Docker is used to package individual services as containers, allowing each service to be deployed, scaled, and managed independently also known as Microservices.
    
8. ### <mark>Docker vs Hypervisor?</mark>
    
    * **Docker**:
        
        * Uses containerization.
            
        * Lightweight and shares host OS kernel.
            
        * Ideal for microservices and cloud-native applications.
            
    * **Hypervisor**:
        
        * Uses virtualization.
            
        * Creates complete virtual machines.
            
        * Ideal for running multiple operating systems on a single physical machine.
            
    
    In essence, Docker containers are lightweight, share the host OS kernel, and are great for microservices, while hypervisors create complete virtual machines and are suitable for running multiple operating systems on one physical machine.
    
9. ### <mark>What are the advantages and disadvantages of using docker?</mark>
    
    **Advantages**:
    
    1. **Portability**: Easy to package and deploy applications consistently across different environments.
        
    2. **Isolation**: Applications run independently without interfering with each other or the host system.
        
    3. **Efficiency**: Lightweight containers result in faster startup times and better resource utilization.
        
    4. **Scalability**: Easily handle varying levels of traffic by running multiple container instances.
        
    5. **DevOps Enablement**: Facilitates collaboration and automation between development and operations teams.
        
    6. **Version Control**: Versioned images allow for easy management and rollback of application changes.
        
        **Disadvantages**:
        
        1. **Learning Curve**: Initial learning curve for beginners.
            
        2. **Security Concerns**: Misconfigurations or vulnerabilities may pose security risks.
            
        3. **Complex Networking**: Networking setup can be complex, especially for multi-container applications.
            
        4. **Resource Overhead**: Running multiple containers may consume significant memory and CPU.
            
        5. **Persistence**: Managing persistent data requires additional configuration and consideration.
            
    
10. ### <mark>What is a Docker namespace?</mark>
    
    In Docker, a namespace is a feature of the Linux kernel that provides process isolation by allowing multiple instances of the same resource to coexist without interfering with each other. Docker utilizes namespaces to provide isolation for containers, ensuring that each container operates in its own environment without impacting other containers or the host system.
    
    Some of the namespaces used by Docker include:
    
    **PID (Process ID) Namespace**: Each container has its own isolated process tree, with its own set of process IDs (PIDs). This prevents processes in one container from interacting with processes in another container or the host system.
    
    **Network Namespace**: Each container has its own isolated network stack, including network interfaces, IP addresses, routing tables, and firewall rules. This ensures that network communication within a container is isolated from other containers and the host system.
    
    By leveraging namespaces, Docker provides lightweight and efficient process isolation, ensuring that containers remain independent and secure while sharing the same underlying host system resources. This enables Docker to achieve high levels of resource utilization and scalability while maintaining a high degree of isolation and security.
    
11. ### <mark>What is a Docker registry?</mark>
    
    A Docker registry is a storage and distribution system for Docker images. It serves as a central repository where Docker users can store, share, and retrieve container images. Users can push images to the registry to store them and pull images from the registry to use them in their Docker environment. Docker registries support versioning, access control, and authentication mechanisms to ensure security and manageability. Popular examples include Docker Hub, Docker Trusted Registry (DTR), Amazon Elastic Container Registry (ECR), Google Container Registry (GCR), and Azure Container Registry (ACR).
    
12. ### <mark>What is an entry point?</mark>
    
    An instruction in a Dockerfile defining the default command to execute when a container starts.
    
13. ### <mark>How to implement CI/CD in Docker?</mark>
    
    Implementing CI/CD (Continuous Integration/Continuous Deployment) with Docker involves automating the build, test, and deployment processes of Dockerized applications.
    
    here's a simplified approach to implementing CI/CD with Docker:
    
    1. **Version Control**: Store code in Git for tracking changes.
        
    2. **Dockerfile**: Write a Dockerfile to build the application image.
        
    3. **CI Pipeline**:
        
        * Use CI tool (e.g., Jenkins, GitLab CI) to trigger builds on code changes.
            
        * Build Docker image and run tests.
            
        * Push image to Docker registry.
            
    4. **CD Pipeline**:
        
        * Pull image from registry.
            
        * Deploy to target environment (e.g., staging, production).
            
    5. **Monitoring & Rollback**:
        
        * Monitor application health.
            
        * Automate rollback if issues arise.
            
    6. **Feedback & Improvement**:
        
        * Continuously improve pipelines based on feedback.
            
        * Optimize for faster, more reliable deployments.
            
    
14. ### <mark>Will data on the container be lost when the docker container exits?</mark>
    
    In most cases, data stored within a Docker container is ephemeral, meaning it will be lost when the container exits. Docker containers are designed to be lightweight, portable, and stateless, with the assumption that they can be stopped, started, and destroyed without impacting data persistence.
    
    In summary, by default, data stored within a Docker container is lost when the container exits. However, Docker provides mechanisms such as volumes, bind mounts, and restart policies to enable data persistence and ensure that data can be shared and retained across container lifecycles.
    
15. <mark>What is a Docker swarm?</mark>  
    Docker Swarm is Docker's native clustering and orchestration tool used to manage a cluster of Docker hosts and deploy and scale containerized applications across them. It enables users to treat multiple Docker hosts as a single, virtualized system, providing high availability, fault tolerance, and scalability for containerized applications.
    
16. ### **<mark>Common Docker Commands:</mark>**
    
    ◼️ **View running containers:** docker ps
    
    ◼️ **Run a container with a specific name:** docker run --name container\_name
    
    ◼️ **Export a Docker container:** docker export container\_id &gt; filename.tar
    
    ◼️ **Import an existing Docker image:** docker import filename.tar
    
    ◼️ **Delete a container:** docker rm container\_id
    
    ◼️ **Remove all stopped containers, unused networks, build caches, and dangling images:** docker system prune.
    

### **Conclusion**

These Docker interview questions cover important topics, giving you a good understanding of Docker. Mastering these concepts will help you in interviews and also in real-world projects.