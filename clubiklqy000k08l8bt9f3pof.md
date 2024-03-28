---
title: "⚙Day 24- Complete Jenkins CI/CD Project"
datePublished: Thu Mar 28 2024 17:33:58 GMT+0000 (Coordinated Universal Time)
cuid: clubiklqy000k08l8bt9f3pof
slug: day-24-complete-jenkins-cicd-project
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1711647139384/60eea908-4081-4174-8716-9b302e41e0c4.png
tags: docker, jenkins, dockerfile, cicd-cjy1vtdk2005kjjs17n8couc3, docker-images, 90daysofdevops, trainwithshubham, vivekmoudekar

---

We have made it through Day 23 of our Jenkins CI/CD journey. Today is all about putting your knowledge into practical Application, by completing a Jenkins CI/CD project for your Node.js application. This project will not only streamline your development process but also Plus point to your resume. So, get ready to build a robust CI/CD pipeline.

Let's make a beautiful CI/CD Pipeline for your Node JS Application 😍

## **<mark>🍴Task-01:</mark> Fork Repository and Integrate GitHub**

### **Step 1: Fork the Repository**

To start with Jenkins CI/CD project, start by forking the provided repository on GitHub. This will creates a personal copy of the repository under your GitHub account, which will allow you to freely experiment without impacting the original codebase.

### **Step 2: Connecting Jenkins to GitHub Repository**

After forking the repository, establish a connection between Jenkins and GitHub. Jenkins can automatically build and deploy your application whenever changes are pushed to the repository. This integration streamlines the development process and ensures that your CI/CD pipeline is triggered.

### **Step 3: GitHub WebHooks and CI/CD**

These are mechanisms allow GitHub to notify external services, like Jenkins about events in your repository. Configure WebHooks to enable automatic triggering of the CI/CD pipeline whenever changes occur in your GitHub repository.

## **<mark>🍴Task-02:</mark> Running the Application with Docker Compose**

### **Step 1: Execute Shell Script in Jenkins**

Inside your Jenkins job configuration, Under Build Steps Option select Execute Shell. This step will be responsible for executing commands within the Jenkins environment. In this case, it will run your Node.js application using Docker Compose.

### **Step 2: Create a Docker Compose File**

Create a Docker Compose file tailored to your Node.js application. This file should define the services, networks, volumes, and other configurations required for your application to run smoothly in a Dockerized environment.

### **Step 3: Run the Project and Celebrate**

Once your Jenkins job is configured and your Docker Compose file is ready, execute the job. Watch as Jenkins automatically builds and deploys your Node.js application using the defined CI/CD pipeline.

Happy Learning :)