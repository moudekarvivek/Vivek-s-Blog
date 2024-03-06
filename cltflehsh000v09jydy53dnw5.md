---
title: "☁Project 1: Deploying a Node.js App on AWS ECS Fargate and ECR🖥"
datePublished: Wed Mar 06 2024 09:24:34 GMT+0000 (Coordinated Universal Time)
cuid: cltflehsh000v09jydy53dnw5
slug: project-1-deploying-a-nodejs-app-on-aws-ecs-fargate-and-ecr
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1709705925474/c4b7b519-672b-40c6-bd5c-8cd6ab1ffacd.png
tags: ec2, linux, docker, aws, github, aws-ecs, aws-iam, linux-commands, aws-ecr, awswithtws-7daysofaws, vivekmoudekar

---

### <mark>👓</mark>**<mark>INTRODUCTION</mark>**

Automate the deployment of a Node.js Application on Serverless AWS ECS fargate with the image repository on ECR and the cloudwatch login integrated with proper IAM roles and configuration.

1. In the Above Cover Image First we will Bring our application code from Github to the EC2 Instance of AWS Using `Git clone` command.
    
2. Now, We have to make docker image of Application and Push that on ECR(Elastic Container Registry) Services it is used to store docker images,for that your EC2 instance must have the acess of ECR.
    
3. To give Acess of ECR to EC2 Instance we will use IAM(Identity Acess Management) service. In which we will give acess of ECR full acess,for that we have to create a user and make policy for that.
    
4. After Giving acess we are able to push docker image on ECR. and from there we can run our Image on ECS(Elastic Container Service).
    
5. And from Cloudwatch we can acess the logs of Application.
    

### **<mark>✔Pre-requisites</mark>**

Before diving into deployment, let's ensure you have everything you need:

* **Dockerfile Familiarity**: We assume you're comfortable with writing a Dockerfile to containerize your Node.js application.
    
* **Access to AWS Management Console**: Make sure you have access to the AWS Management Console to perform necessary configurations.
    
* **Basic EC2 Instance Knowledge**: Understanding the basics of setting up an EC2 instance.
    

### **<mark>📁Project Steps</mark>**

#### **Cloning the Source Code from GitHub**

1. **Source Code Retrieval**: Head over to your GitHub repository and copy the URL of your Node.js application's source code.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709711536501/dfbc32bc-109e-4264-b56f-be840f074790.png align="center")
    

**EC2 Instance Creation**: Using the AWS Management Console, create an EC2 instance where you'll clone the repository.

1) Create a instance connect the instance with ssh Client method to local machine.

2) After connecting our instance first update your terminal using Command `sudo apt-get update`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709711982669/9f316029-3e53-4012-996a-842aea86c847.png align="center")

3) Our System got up-to-date now bring your application code from github to local machine using command `git clone <URL>` .

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709712574469/b318f5b3-aeea-4743-b907-69fd1ef7c6e0.png align="center")

---

### **<mark>⚙Configuring Image in AWS ECR</mark>**

1. **ECR Repository Creation**: Navigate to AWS ECR and create a repository to store your Docker images. Customize the repository settings as per your requirements.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709712983035/096a15cf-29d3-4602-90e1-3a369e2654da.png align="center")
    
    We have Created a repository on ECR naming node-app to store the docker images. But in that repository there is no docker images available in that.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709713232347/c542b3ba-17d8-4aa8-8e4d-e05f3c8bf528.png align="center")
    
    Click on view Push commands so that we can push images here.
    
2. GO on Local terminal first install docker using command
    
    `sudo apt install docker.io` , When we are installing docker this means we are building the docker image on this EC2 instance.
    
3. Now, will try docker command `docker ps` But it will denied the permission of docker,user don't have permission of docker.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709714702655/99b71664-7e00-4478-824a-4376d2e462fd.png align="center")
    
4. Add user to the docker group using command
    
    `sudo usermod -aG docker $USER` our user added to the docker group now reboot system `sudo reboot` ,To implement changes.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709714818703/120bda58-787a-43b9-bdca-87ad4f10affa.png align="center")
    
5. check `docker ps` command now no error as we have added docker to usergroup.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709714865878/bb276538-6013-42dd-a172-367491999e7e.png align="center")
    
6. Go to google install AWS CLI unzip that in terminal.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709714994755/efd14811-b79c-413e-85b9-5be76042846b.png align="center")
    
7. Below are the push commands that we have to run on our local terminal to push our image on this repo. but to push images on ECR we want to make sure that vivek user which we have created in IAM have permission of ECR<mark>.</mark>
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709714299042/28f66dcb-3838-4e3f-a6ec-75437e6f8e49.png align="center")
    

---

### **<mark>🔍Configuring IAM</mark>**

1. **IAM User Creation**: Create an IAM user in the AWS Management Console with appropriate permissions to access ECR.
    
2. **Policy Attachment**: Attach policies granting necessary permissions for ECR access to the IAM user.
    
3. **AWS CLI Installation**: Install the AWS Command Line Interface (CLI) on your EC2 instance.
    
4. **AWS CLI Configuration**: Connect your EC2 instance to the AWS Management Console using the AWS CLI for seamless interaction.
    

---

### **🏹Pushing the Image to ECR**

1. **ECR Push Commands**: Access the AWS ECR console to obtain push commands for your Docker image.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709715331494/4b4501f0-14b2-4b1f-b384-dc3ed1e9f5f0.png align="center")
    

Now, Follow this above command and run it one by one

2. **Execution**: Execute the provided commands on your EC2 instance to push the Docker image to ECR, ensuring a secure and efficient process.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709715616541/3a3c0fd6-ebca-4610-96da-19c9e28e71a5.png align="center")
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709715633986/674d582f-bac1-4670-9c12-19a60b222cf2.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709715786224/3c3c001f-8465-469a-b47c-53ce93590f27.png align="center")

We can now see after following above push commands we have successfully pushed docker images on ECR.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709715925862/9206759b-9887-4d92-b898-ff68c70016cf.png align="center")

---

### **<mark>⚙Configuring AWS ECS</mark>**

1. **ECS Cluster Creation**: Navigate to the ECS repository in the AWS Console and create a new cluster.
    
2. **Configuration Details**: Provide necessary details such as cluster name, VPC, and subnet settings to tailor the cluster to your requirements.
    
3. **Launch Type Selection**: Opt for AWS Fargate as the launch type for your cluster to leverage its serverless capabilities.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709716397296/7dcf78b2-1b02-4fb1-954a-d6633738b71d.png align="center")
    

### **<mark>🌱Using AWS Fargate</mark>**

1. **Task Definition Creation**: Define a task for your cluster, specifying container image details and required ports.
    
2. **Resource Configuration**: Configure CPU and memory resources based on anticipated application load to ensure optimal performance.
    
3. **Task Deployment**: Review the details and create the task, followed by deployment and execution on the cluster using Fargate's automated management.
    
4. The task is now deployed to the cluster.
    
5. #### **Open Port in the Security Group**
    
6. **Security Group Configuration**: Navigate to the ENI ID associated with your task and access the corresponding security group.
    
7. **Inbound Rule Modification**: Open Port 80 (HTTP) in the inbound rule and restrict access to your IP for enhanced security.
    

---

### **<mark>🖥Project Live Execution</mark>**

1. **Accessing Task Details**: Navigate to the task created earlier and retrieve the public IP.
    
2. **Application Access**: Access your live Node.js application using the provided IP address, witnessing your deployment in action.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709716743074/561a2997-40df-419c-8d8f-c8a9f256e160.png align="center")
    
    ### **<mark>🚧Conclusion</mark>**
    
    Congratulations on successfully deploying your Node.js application on AWS ECS Fargate and ECR! By following this detailed guide, you've not only achieved deployment but also gained valuable insights into AWS cloud services. Enjoy exploring the endless possibilities of cloud deployment and have a fantastic day!