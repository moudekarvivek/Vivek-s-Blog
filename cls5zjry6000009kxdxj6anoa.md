---
title: "📦Day 7 :Understanding package manager and systemctl"
datePublished: Sat Feb 03 2024 11:23:11 GMT+0000 (Coordinated Universal Time)
cuid: cls5zjry6000009kxdxj6anoa
slug: day-7-understanding-package-manager-and-systemctl
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1706952721684/fb444eec-22a1-4d26-8e7b-04524a3d9adb.png
tags: devops, 90daysofdevops, shubhamlondhe, trainwithshubham, devopscommunity

---

## **INTRODUCTION:**

Welcome to the world of linux management ,where we will explore the package managers and systemctl (essential tools for handling software and services on your operating system). from scratch and how it's work?, Everything and will install docker and jenkins using package manager in our cloud terminal platform (AWS) .

## ⚙️**What is a package manager in Linux?**

In simpler words a package manager is a tool that allows users to install, remove, upgrade, configure and manage software packages on an operating system. When we talk about <mark>"packages"</mark> we mean bundles of software that include everything needed for an application to run, A package is essentially an archive file containing the binary executable, configuration file and sometimes information about the dependencies.

## ⚙️ **Different kinds of package managers**

package Managers differ based on packaging system but same packaging system may have more than one package manager.

For example, RPM has Yum and DNF package managers. For DEB, you have apt-get, aptitude command line based package managers.

Some of the Package Managers with Brief:

1. **🔧$apt(Advance Package Tool)**: It's a high-level package management tool used in Debian-based system like Ubuntu.
    
    ```plaintext
    sudo apt-get update
    sudo apt-get upgrade
    sudo apt-get install docker 
    ```
    
2. **🔧$yum (Yellowdog Updater, Modified): It** manage packages on Red Hat-based systems like centOS etc.
    
    ```plaintext
    sudo yum install nginx
    ```
    

# **<sup>🛠️Tasks:</sup>**

## **✨Docker Installation on your terminal using package managers.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1706954953228/5490ca06-c032-4cbb-9902-fd69459a99b7.jpeg align="center")

## 🐳Installing docker on Ubuntu:

1. Connect to your AWS EC2 instance
    
2. Open your terminal
    
3. Type: **sudo apt-get update**(This will Update your software list).
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1706957297121/845b9c89-c528-4908-8db1-5ddd82801d46.png align="center")
    
4. Now, Type: **sudo apt-get install docker.io** (This will install docker)**.**
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1706957530955/dbae19db-ecb7-4540-88a4-4288b5cf5ef6.png align="center")
    
    press "y" to proceed further.
    

To verify docker is installed or not use command **docker --version.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1706957717644/43b5ca58-12a7-4532-9ed6-091cc3ddfab4.png align="center")

This Indicates you have successfully installed Docker.

---

## ✨**Jenkins Installation on your terminal using package managers.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1706958235788/368bbcf6-8c2a-42f7-97c6-329259ede0c3.png align="center")

**Enable Jenkins Repository (If Not Available):**

If the `jenkins` package is not available in the default repositories, you may need to add the Jenkins repository. Follow these steps:

**a.** **Add the jenkins repository and then Add the Jenkins Repository to your sources list:**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1706958489423/66ab26d4-fe1d-41f8-b900-f7ff7ff79d98.png align="center")

**b. Install Jenkins:**

Now, you should be able to install Jenkins using:

sudo apt-get install jenkins

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1706958876635/fbb6c0b1-48a4-4203-a4d3-8ac70f8a1890.png align="center")

---

## **systemctl and systemd:**

Now, let's check out another tool called "systemctl." It helps us understand and control the state of services on our system, like Docker. systemctl is used to examine and control the state of “systemd” system and service manager. systemd is system and service manager for Unix like operating systems(most of the distributions, not all)

### Checking Docker Service Status:

After installing Docker, you can see its status by typing: `systemctl status docker` in your terminal. This tells you if Docker is running properly.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1706959016869/4c628edd-e605-44a8-a9c2-8dc8acd2de40.png align="center")

## **Conclusion:**

In summary, 🛠️ understanding Package Managers and Systemctl is crucial for effective system administration. These tools, governing software management and system control, are essential for maintaining stability, optimizing performance, and navigating the complexities of modern computing. Mastering these elements empowers administrators to streamline operations and enhance system security, ensuring a seamless and efficient computing environment. 🚀

***Happy Learning 😊***