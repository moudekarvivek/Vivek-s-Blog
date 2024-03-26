---
title: "🛠Day-22 : Getting Started with Jenkins"
datePublished: Tue Mar 26 2024 18:33:19 GMT+0000 (Coordinated Universal Time)
cuid: clu8pt86v000208jpf5lp9p7d
slug: day-22-getting-started-with-jenkins
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1711477882654/8bd4a367-c986-4154-b29e-e1b51e212682.png
tags: ubuntu, linux, aws, jenkins, ci-cd, jenkins-devops, 90daysofdevops, trainwithshubham, vivekmoudekar

---

### **🤵What is Jenkins?**

* Jenkins is an open source continuous integration-continuous delivery and deployment (CI/CD) automation software tool written in the Java programming language. It is used to implement CI/CD workflows, called pipelines.
    
* It allows all the developers to automate build, test and deploy process of software.
    
* Jenkins achieves Continuous Integration with the help of plugins. Plugins allow the integration of Various DevOps stages. If you want to integrate a particular tool, you need to install the plugins for that tool.
    

**✨Let us do discuss the necessity of this tool before going ahead to the procedural part for installation:**

1. **Automation of Software Development Processes**: Jenkins is a powerful automation tool primarily used for continuous integration and continuous delivery or deployment (CI/CD). It automates various stages of the software development lifecycle, including building, testing, and deploying applications. By automating these processes, Jenkins helps in reducing manual errors, improving efficiency, and speeding up the overall development cycle.
    
2. **Integration with Various Tools and Technologies**: Jenkins provides extensive support for integrating with a wide range of tools and technologies used in modern software development, such as version control systems (e.g., Git, SVN), build tools (e.g., Maven, Gradle), testing frameworks, deployment tools, and more.
    
3. **Continuous Integration and Testing**: Jenkins enables continuous integration practices by automatically triggering builds and running tests whenever changes are committed to the version control repository. This ensures early detection of integration issues and bugs, leading to faster feedback loops and higher software quality.
    
4. **Streamlined Deployment Process**: With Jenkins, teams can automate the deployment process, ensuring consistent and reliable deployments across different environments (e.g., development, staging, production).
    
5. **Scalability:** Jenkins can be scaled horizontally to handle large CI/CD workloads by distributing build jobs across multiple nodes. This scalability ensures that Jenkins can support the growth of your development team and projects.
    
6. **Customization:** Jenkins is highly customizable through its plugins and support for defining pipelines as code. This allows you to tailor Jenkins to fit your specific development and deployment requirements.
    
    Jenkins is a crucial tool for modern software development teams seeking to automate and streamline their CI/CD pipelines. By facilitating automation, integration, testing, deployment, scalability, and visibility, Jenkins helps teams deliver high-quality software faster and more efficiently, ultimately enhancing the overall development process and delivering greater value to end-users.
    

### **✔Task 1: What you understood in Jenkins?**

Jenkins is an automation server essential for modern software development. It enables continuous integration (CI) and deployment (CD), automating tasks like building, testing, and deploying code. Jenkins' key strength lies in its ability to create pipelines, defining the entire software delivery process as code. This automation helps teams catch bugs early, improve code quality, and accelerate software delivery. Jenkins is highly extensible, supporting integration with various tools and technologies through plugins. It empowers teams to build, test, and deploy software efficiently, making it a must-have for any development team striving for productivity and quality.

### ✔**Task 2: Create a freestyle pipeline to print "Hello World!!**

**<mark>Step 1</mark>**<mark>:</mark> First of all create a AWS EC2 instance and connect that instance with your Local machine using SSH client.

**<mark>Step 2</mark>**<mark>:</mark> For running jenkins You must have java install in your instance for that we will install java first.and after installing will check version using java version.

```bash
sudo apt update
sudo apt install fontconfig openjdk-17-jre
java -version
openjdk version "17.0.8" 2023-07-18
OpenJDK Runtime Environment (build 17.0.8+7-Debian-1deb12u1)
OpenJDK 64-Bit Server VM (build 17.0.8+7-Debian-1deb12u1, mixed mode, sharing)
```

<mark>Step 3</mark>: After the installation of Java version 17 will install jenkins LTS release for Ubuntu because we are using AMI as Ubuntu, and prefer to install stable version as weekly release can have updates, below Commands used to install.

```bash
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```

<mark>Step 4:</mark> To check jenkins active or not will use command, after doing that we have to copy the public url of instance and run it using :8080 but it will not run as we have not added port 8080 to security group.

```bash
systemctl status jenkins #it will show active means jenkins is up now on port 8080
```

<mark>Step 5:</mark> Go to Security group, edit inbound rules add `custom TCP` Select Port range `8080` & `anywhere-IPv4` Save it. Now it will work on this port

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1711475566541/c35f983d-59e0-46a6-8fd9-99a67b23a340.png align="center")

<mark>Step 6:</mark> Access your Jenkins through `your-public-IP: 8080`  
will get Jenkins dashboard,Initially jenkins is locked you have to copy the given path and paste it to your Local machine using Command `sudo cat <path>` this will show you a password copy and paste it in the dashboard and continue.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1711475758062/a364f8d4-fe84-42bd-bb9e-0b3b5ce61a0d.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1711476014663/fbb2d851-10c4-45bd-8ef7-3507a5180c39.png align="center")

<mark>Step 7: </mark> You will see Jenkins Dashboard go for Create a Job Option and enter a Item name -&gt; HelloWorld-Pipeline and select Free style Project.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1711476332546/ad3b9a78-1b85-49fa-a7f7-5d5e336f0f84.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1711476412321/744fbf51-9011-4983-9ebb-c581eebdaa15.png align="center")

<mark>Step 8:</mark> Configure the Job

1. In the job configuration page, go to the "Build" section.
    
2. Click on "Add build step" and select "Execute shell".
    
3. In the command box, type `echo "Hello World!!"`.
    
4. Save the Job Configuration.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1711476538669/f6dc1bbf-c290-4829-8705-e57da86e152b.png align="center")
    
    <mark>Step 9:</mark> Run the Job.
    
    1. Click on "Build Now" to run the job.
        
    2. Jenkins will execute the pipeline and print "Hello World!!" in the console output.
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1711476743350/3ef8ec1c-79b7-4d9d-a10a-f8fdf7cc8fb3.png align="center")
        
    
    ### **🚧Conclusion**
    
    Jenkins is a powerful and widely-used automation server that greatly facilitates the continuous integration and continuous delivery (CI/CD) process for software development teams. With its extensive plugin ecosystem, Jenkins offers flexibility and customization to suit various project requirements. By automating repetitive tasks such as building, testing, and deployment, Jenkins helps teams increase productivity, improve software quality, and accelerate the delivery of software updates. Its user-friendly interface, robust community support, and seamless integration with other development tools make Jenkins an indispensable tool for modern software development workflows.