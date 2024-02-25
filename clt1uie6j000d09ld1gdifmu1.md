---
title: "🐳Day 18 - Docker Compose for DevOps Engineers"
datePublished: Sun Feb 25 2024 18:30:46 GMT+0000 (Coordinated Universal Time)
cuid: clt1uie6j000d09ld1gdifmu1
slug: day-18-docker-compose-for-devops-engineers
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1708857832062/35de1784-e6be-48a1-b37d-09258306b26f.png
tags: docker, yaml, containers, docker-compose, docker-images, 90daysofdevops, trainwithshubham, vivekmoudekar

---

## 📚**Docker Compose**

Docker Compose is a tool provided by Docker that allows you to define and run multi-container Docker applications. It enables you to describe your application's infrastructure (including networks, volumes, and services) in a single YAML file called `docker-compose.yml`.

With Docker Compose, you can define the services that make up your application, their dependencies, ports they expose, volumes they use, networks they are connected to, and other configurations. Once you have defined your application stack in the `docker-compose.yml` file, you can use the `docker-compose` command-line tool to start, stop, and manage your entire application with a single command.  
*Docker Compose simplifies the process of managing multi-container Docker applications, especially in development and testing environments, by providing a convenient way to define, manage, and scale complex applications. It abstracts away many of the complexities of managing individual containers and their interactions, allowing developers to focus on building and testing their applications.*

## 📜What is YAML?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708857964111/af1d57cb-683c-4df2-b944-bf026772bef3.png align="center")

YAML, pronounced as "YAML" or sometimes "YAML" (rhymes with "camel"), stands for "YAML Ain't Markup Language." It's a human-readable data serialization language that's often used for configuration files, data exchange, and representing structured data in a way that's easy for both humans and computers to understand.

Imagine you have a recipe for making a sandwich. In a recipe book, the steps might be written in a format that's easy for humans to read and follow. YAML is like a format for writing down instructions or information in a clear and simple way that computers can also understand.

```yaml
sandwich:
  name: Grilled Cheese
  ingredients:
    - bread
    - cheese
    - butter
  steps:
    - Take two slices of bread.
    - Place cheese between the slices.
    - Spread butter on the outsides of the bread slices.
    - Heat a skillet over medium heat.
    - Cook the sandwich on the skillet until golden brown on both sides.
    - Serve hot.
```

In this example:

* We have a "sandwich" object with properties like "name," "ingredients," and "steps."
    
* Under "ingredients," we have a list of items needed to make the sandwich.
    
* Under "steps," we have a list of instructions to follow.
    

Just like in a recipe book, YAML organizes information in a structured and easy-to-read format, making it great for configuration files, storing data, and defining settings for software applications.

## ✔TASKS

### **<mark>Task-1 </mark> :** Learn how to use the docker-compose.yml file, to set up the environment, configure the services and links between different containers, and also to use environment variables in the docker-compose.yml file.

* Let's break down how to use a `docker-compose.yml` file.
    

## 1) **Setting up the Environment:**

1. **Create a** `docker-compose.yml` **File**: Begin by creating a `docker-compose.yml` file in the root directory of your project.
    
2. **Define Version:** Specify the version of Docker Compose syntax you're using. For example:
    
    ```yaml
    version: '3.8'
    ```
    
    1. **Define Services:** Declare the services (containers) that comprise your application under the `services` key.
        
    
    ## **Configuring Services:**
    
    1. **Configure Each Service:** Define each service with its specific configuration options. This includes specifying the Docker image, volumes, ports, networks, environment variables, and any other settings needed for that service.
        
        ```yaml
        services:
          web:
            image: nginx:latest
            ports:
              - "8080:80"
            volumes:
              - ./html:/usr/share/nginx/html
        ```
        
        ## **Establishing Links between Containers:**
        
        1. **Link Containers (Deprecated):** Docker Compose provides service-to-service links, but this feature is deprecated. Instead, rely on Docker networks for inter-service communication.
            
        
        ## **Using Environment Variables:**
        
        1. **Define Environment Variables:** You can use environment variables in your `docker-compose.yml` file to inject dynamic values into your services. Define them under the `environment` key within each service.
            
            ```yaml
            services:
              web:
                image: nginx:latest
                environment:
                  NGINX_PORT: 8080
            ```
            
            1. **Use Environment Variables in Configuration:** You can reference these environment variables within the configuration settings for the service. For instance, in the `ports` configuration, you could use an environment variable instead of hardcoding the port.
                
                ```yaml
                services:
                  web:
                    image: nginx:latest
                    ports:
                      - "${NGINX_PORT}:80"
                    environment:
                      NGINX_PORT: 8080
                ```
                
                This way, you can have dynamic configurations based on the environment variables passed into your Docker Compose setup.
                
    
    **Example Summary:**
    
    Here's a simple example of a `docker-compose.yml` file that sets up a web server using Nginx, with a dynamic port configuration using environment variables:
    
    ```yaml
    version: '3.8'
    
    services:
      web:
        image: nginx:latest
        ports:
          - "${NGINX_PORT}:80"
        environment:
          NGINX_PORT: 8080
    ```
    

### <mark>TASK-2 </mark> :

### ◼ **Pull the Docker Image:**

```dockerfile
docker pull nginx
```

### **◼ Create a new user and give it permission to run Docker commands**:

```dockerfile
sudo useradd -m newuser
sudo usermod -aG docker newuser
sudo reboot
```

## ◼️**Run the container as the new user**:

```dockerfile
sudo su - newuser #login new user
docker run --name mynginx -d -p 8080:80 nginx #run the container
```

## ◼️**Inspect the container's running processes and exposed ports**:

```dockerfile
docker inspect mynginx
```

## ◼️**View the container's log output**:

```dockerfile
docker logs mynginx
```

## ◼️**Stop and start the container**:

```dockerfile
docker stop mynginx
docker start mynginx
```

## ◼️**Remove the container**:

```dockerfile
docker rm mynginx
```

***Note***: Make sure to replace `newuser` with the actual username you want to use, and adjust the Docker image and container names as needed.

## **How to run Docker commands without sudo?**

To run Docker commands without using `sudo`, you need to add your user to the Docker group. Here are the steps:

### ◼️**Add your user to the docker group:**

```dockerfile
sudo usermod -aG docker $USER
```

### ◼️**Log out and log back in**:

```dockerfile
su - $USER
```

### ◼️**Verify Docker command without sudo**:

```dockerfile
docker ps
```

◼️**Reboot the machine (optional)**: While not strictly necessary, rebooting the machine can ensure that all changes are applied correctly. But for safe side you can do that.

Happy Learning😊