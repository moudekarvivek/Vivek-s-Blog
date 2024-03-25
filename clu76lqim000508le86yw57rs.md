---
title: "🚢Day 19 - Exploring Docker Volume & Docker Network"
datePublished: Mon Mar 25 2024 16:47:51 GMT+0000 (Coordinated Universal Time)
cuid: clu76lqim000508le86yw57rs
slug: day-19-exploring-docker-volume-docker-network
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1711385061850/0ebe0205-167d-4f46-bc99-de718c570681.png
tags: docker, aws, devops, containers, containerization, dockerfile, devops-tools, docker-volume, 90daysofdevops, vivekmoudekar

---

### **Docker-Volume**

Docker allows you to create something called volumes. Volumes are stored outside the container's filesystem, which allows them to persist even if the container is stopped or deleted. You can also mount from the same volume and create more containers having same data.

You can create a volume using the docker volume create command:

```dockerfile
docker volume create vol
```

### **Docker Network**

A docker network is like a virtual bridge that allows Docker containers to communicate with each other and with the outside world. It provides a way for containers to Communicate to each other, even if they are running on different machines or hosts there are total 7 network type through which we can communicate.

### **Task-1: *Create a multi-container docker-compose file which will bring UP and bring DOWN containers in a single shot***

**It's simple example of a multi-container Docker Compose file that includes an application and a database container. This example uses Two-tier flask Application with MYSQL database.**

```yaml
version: '3'

services:
  web:
    image: python:3.9-slim
    volumes:
      - mysql-data: /var/lib/mysql
      - .message.sql: /docker-entrypoint-initdb.d/message.sql
    working_dir: /app
    command: ["python", "app.py"]
    ports:
      - "5000:5000"
    depends_on:
      - mysql

  mysql:
    image: MYSQL:5.7
    environment:
      MYSQL_HOST: mysql
      MYSQL_USER: root
      MYSQL_PASSWORD: test@123
    ports:
      - "3306:3306"
```

**To bring up the containers, run:**

```bash
docker-compose up -d
```

**To bring down the containers, run:**

```bash
docker-compose down
```

This will stop and remove all containers, networks, and volumes associated with the application.

---

### **Task-2: *Learn how to use Docker Volumes and Named Volumes to share files and directories between multiple containers.***

First we'll create two containers that read and write data to the same volume.

```bash
docker volume create shared_data
```

* <mark>Create two or more containers that read and write data to the same volume using the </mark> `docker run --mount` <mark> command.</mark>
    
    #### **Container 1**:
    
    ```bash
    docker run -d --name container1 --mount source=shared_data,target=/data busybox sh -c "echo 'Data from Container 1' > /data/file.txt && tail -f /dev/null"
    ```
    
    This command runs the first container named `container1`, mounting the `shared_data` volume to the `/data` directory inside the container. It writes data to a file named `file.txt` within the volume.
    
    #### Container 2:
    
    ```bash
    docker run -d --name container2 --mount source=shared_data,target=/data busybox sh -c "echo 'Data from Container 2' > /data/file2.txt && tail -f /dev/null"
    ```
    
    Similarly, this command runs the second container named `container2`, also mounting the `shared_data` volume to the `/data` directory inside the container. It writes different data to another file named `file2.txt` within the same volume.
    
      
    Now you have two containers (`container1` and `container2`) both reading and writing data to the same volume (`shared_data`). Any changes made by one container will be visible to the other container, as they are sharing the same volume.
    
* <mark>Verify that the data is the same in all containers by using the docker exec command to run commands inside each container</mark>
    
      
    To verify that the data is the same in all containers, you can use the `docker exec` command to run commands inside each container and check the content of the shared volume. Here's how you can do it:
    
    **1. *Verify Data in Container 1*:**
    
    ```bash
    docker exec container1 cat /data/file.txt
    ```
    
    This command will output the content of `file.txt` in `container1`
    
* **2\. Verify Data in Container 2:**
    
    ```bash
    docker exec container2 cat /data/file.txt
    ```
    
    Similarly, this command will output the content of `file.txt` in `container2`.
    
* <mark>Use the docker volume ls command to list all volumes and docker volume rm command to remove the volume when you're done.</mark>
    
* `docker volume ls` command to list all volumes and then the `docker volume rm` command to remove the specific volume. Here's how:
    
    ### **List all volumes**
    
    ```dockerfile
    docker volume ls
    ```
    
    This command will list all Docker volumes present on your system, including the `shared_data` volume we created earlier.
    

### **Remove the volume:**

```dockerfile
docker volume rm shared_data
```

This command will remove the `shared_data` volume. Make sure you are not actively using this volume in any running containers, as removing the volume will delete all data stored within it.

### **Conclusion**

In above task, we have learned to use Docker Volumes and Named Volumes to share files and directories between multiple containers. We created a Docker volume named `shared_data`, wrote data to a file inside the volume from one container, and then read the same file from another container. This demonstrates how Docker Volumes can be used to share data between containers, allowing them to access and modify the same files.

***😊Happy Learning : )***