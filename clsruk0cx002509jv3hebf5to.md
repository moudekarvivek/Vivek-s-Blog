---
title: "🐋Day 16 - Docker for DevOps 
                         Engineers."
datePublished: Sun Feb 18 2024 18:34:20 GMT+0000 (Coordinated Universal Time)
cuid: clsruk0cx002509jv3hebf5to
slug: day-16-docker-for-devops-engineers
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1708280644765/c0ca6389-7e25-4b10-8845-2e01bf1d4e4e.png
tags: docker, devops, docker-compose, docker-images, 90daysofdevops, shubhamlondhe, trainwithshubham, devopscommunity, vivekmoudekar

---

## 🐳Docker

Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime. Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.

## **🐳Getting Started with Docker Commands**

Before diving into Docker commands,we are assuming that Docker is installed on your system. Once installed, follow these tasks.

1. **<mark>Use the </mark>** `docker run` **<mark> command to start a new container and interact with it through the command line. [Hint: docker run hello-world]</mark>**
    

```bash
docker run -it hello-world
```

*This command will pull the docker image of "Hello-world" from docker Registry and run the "hello-world" image, and you'll be able to interact with it through the command line.*

---

1. **<mark>Use the </mark>** `docker inspect` **<mark> command to view detailed information about a container or image.</mark>**
    
    To view detailed information about a container or image using the `docker inspect` command, follow these steps:
    
    **1) For a Container**:
    
    If you want to inspect a specific container, first, you need to know its ID or name. You can get a list of all running containers with `docker ps`, or you can specify a container's name or ID directly. Then, run:
    
    ```bash
    docker inspect <container_id_or_name>
    ```
    

Replace `<container_id_or_name>` with the actual ID or name of the container you want to inspect.

For example:

```bash
docker inspect my-container
```

*This command will display detailed information about the specified container, including its configuration, network settings, volumes, and more.*

---

1. **<mark>Use the </mark>** `docker port` **<mark> command to list the port mappings for a container.</mark>**
    

  
To list the port mappings for a specific container using the `docker port` command, follow these steps:

**1) 👓Identify the Container**:

First, you need to know the ID or name of the container for which you want to list the port mappings. You can get a list of all running containers with `docker ps`, or you can specify a container's name or ID directly.

2) 🏃‍♂️**Run the Command**:

Once you have identified the container, run the following command:

```bash
docker port <container_id_or_name>
```

Replace `<container_id_or_name>` with the actual ID or name of the container you want to inspect.

*The output of the* `docker port` *command will display the container's port mappings in the format* `<port_inside_container>/<protocol> -> <host_ip>:<host_port>`*. This information can be useful for understanding how ports are exposed and mapped between the container and the host system.*

---

1. **<mark>Use the </mark>** `docker stats` **<mark> command to view resource usage statistics for one or more containers.</mark>**
    

```bash
docker stats <container_id_or_name> [<container_id_or_name> ...]
```

Replace `<container_id_or_name>` with the actual ID(s) or name(s) of the container(s) you want to inspect.

*The* `docker stats` *command is a useful tool for monitoring the resource usage of containers in real-time, which can help you identify performance issues, optimize resource allocation, and manage your Docker environment more effectively.*

---

1. **<mark>Use the </mark>** `docker top` **<mark> command to view the processes running inside a container</mark>**
    

```bash
docker top <container_id_or_name>
```

The output of the `docker top` command provides a snapshot of the processes currently running inside the container. It can be helpful for troubleshooting or monitoring the behavior of applications running within Docker containers.

---

1. **<mark>Use the </mark>** `docker save` **<mark> command to save an image to a tar archive.</mark>**
    
    ```bash
    docker save -o my_image.tar <image_name>
    ```
    
    Replace `[my_name.tar]` with the desired name for the output tar archive file, and `<image_name>` with the name of the image you want to save.
    

---

1. **<mark>Use the </mark>** `docker load` **<mark> command to load an image from a tar archive</mark>**
    
    ```bash
    docker load -i <my_name.tar>
    ```
    
    Replace `[my_name.tar]` with the name of the tar archive file containing the image you want to load.
    

---

## **🐳Conclusion**

In conclusion, mastering Docker commands such as `docker save` and `docker load` is essential for efficient Docker image management. By leveraging `docker save` and `docker load`, Docker users can streamline workflows, enhance productivity, and ensure smooth operations in containerized environments. Whether deploying applications, archiving images, or sharing with team members, understanding these commands is key to maximizing the benefits of Docker and optimizing development processes.

Happy Learning😊