---
title: "Day 16 Task: Docker for DevOps Engineers."
datePublished: Sun Jun 04 2023 16:52:44 GMT+0000 (Coordinated Universal Time)
cuid: clihnvqfj00000al2dmjtglbe
slug: day-16-task-docker-for-devops-engineers
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/HSACbYjZsqQ/upload/1818473e343c9b9a401e45e00d638724.jpeg
tags: linux, docker, aws, devops, jenkins

---

### Docker

Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime. Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.

### Why We Should Use This?

Docker is important and widely used in software development and deployment for several reasons:

1. **Containerization**: Docker allows applications and their dependencies to be packaged into lightweight, self-contained units called containers. Containers provide a consistent and isolated environment, ensuring that an application runs the same way across different systems, regardless of the underlying infrastructure.
    
2. **Portability**: Docker containers can run on any system that has Docker installed, whether it's a developer's laptop, a staging server, or a production environment. This portability enables easy deployment and scaling of applications, making them more flexible and adaptable.
    
3. **Efficiency**: Docker containers are highly efficient in terms of resource utilization. They are lightweight, sharing the host system's kernel and using fewer resources compared to traditional virtual machines. This allows for greater density of application instances on a single host and improves overall system efficiency.
    
4. **Version control**: Docker provides versioning and snapshot capabilities for containers, allowing developers to easily roll back to a previous version if issues arise. It also facilitates collaboration among team members by enabling them to share and reproduce the exact same development environment.
    
5. **DevOps integration**: Docker plays a crucial role in the DevOps workflow by promoting collaboration between developers and operations teams. Docker containers provide consistency between development, testing, and production environments, eliminating the "it works on my machine" problem and reducing deployment issues.
    
6. **Scalability**: Docker enables applications to be easily scaled horizontally by running multiple container instances across multiple hosts. With Docker's orchestration tools like Docker Swarm or Kubernetes, applications can be automatically scaled up or down based on demand, ensuring optimal performance and resource allocation.
    
7. **Security**: Docker provides built-in isolation between containers and the host system, reducing the attack surface for potential vulnerabilities. Containers can be configured to run with restricted permissions and limited access to system resources, enhancing application security.
    

Overall, Docker simplifies the software development lifecycle, improves deployment efficiency, enhances collaboration, and promotes consistency across different environments. These factors make Docker an essential tool for modern application development and deployment.

# Tasks

As you have already installed Docker in previous days' tasks, now is the time to run Docker commands.

* Use the `docker run` command to start a new container and interact with it through the command line. \[Hint: docker run hello-world\]
    
* Start a new container and interact with it through the command line. The `docker run` command followed by an image name or ID is used to run a container. For example, to run the "hello-world" image, you can use the following command:
    
    ```plaintext
    docker run hello-world
    
    Hello from Docker!
    This message shows that your installation appears to be working correctly.
    
    To generate this message, Docker took the following steps:
     1. The Docker client contacted the Docker daemon.
     2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
        (amd64)
     3. The Docker daemon created a new container from that image which runs the
        executable that produces the output you are currently reading.
     4. The Docker daemon streamed that output to the Docker client, which sent it
        to your terminal.
    
    To try something more ambitious, you can run an Ubuntu container with:
     $ docker run -it ubuntu bash
    
    Share images, automate workflows, and more with a free Docker ID:
     https://hub.docker.com/
    
    For more examples and ideas, visit:
     https://docs.docker.com/get-started/
    ```
    

This will download the "hello-world" image if it's not already available and run it in a new container.

* Use the `docker inspect` command to view detailed information about a container or image.
    
* View detailed information about a container or image. The `docker inspect` command followed by the container or image name or ID is used to retrieve detailed information. For example, to inspect a container named "my-container", you can use the following command:
    
    ```plaintext
    $ docker inspect my-container
    
    [    {        "Id": "abcd1234abcd1234abcd1234abcd1234abcd1234abcd1234abcd1234abcd1234",        
    "Created": "2023-06-03T10:24:39.94364818Z",        
    "Path": "/bin/bash",        
    ...        
    "NetworkSettings": {            ...        }    }]
    ```
    
* This will display a JSON-formatted output with detailed information about the container.
    
* Use the `docker port` command to list the port mappings for a container.
    
    List the port mappings for a container. The `docker port` command followed by the container name or ID displays the port mappings. For example, to list the port mappings for a container named "my-container", you can use the following command:
    
    ```plaintext
    $ docker port my-container
    
    8080/tcp -> 0.0.0.0:32768
    ```
    
    This will show the mapping between the exposed ports inside the container and the corresponding host ports.
    
* Use the `docker stats` command to view resource usage statistics for one or more containers.
    
    View resource usage statistics for one or more containers. The `docker stats` command provides real-time resource usage statistics for running containers. You can specify one or more container names or IDs to monitor their resource usage. For example, to view the resource usage of a container named "my-container", you can use the following command
    
    ```plaintext
    $ docker stats my-container
    
    CONTAINER ID   NAME          CPU %     MEM USAGE / LIMIT    MEM %     NET I/O       BLOCK I/O    PIDS
    abcd1234abcd   my-container  0.50%     100MiB / 1GiB        10.00%    2.34kB / 0B   24.6MB / 0B  15
    ```
    
    This will continuously display CPU, memory, network, and disk usage statistics for the specified container.
    
* Use the `docker top` command to view the processes running inside a container.
    
    View the processes running inside a container. The `docker top` command followed by the container name or ID displays the running processes within the container. For example, to view the processes running inside a container named "my-container", you can use the following command:
    
    ```plaintext
    $ docker top my-container
    
    PID   USER     TIME    COMMAND
    1     root     0:00    /bin/bash
    2     root     0:00    ls
    ```
    
    This will show the running processes, their process IDs (PIDs), CPU usage, and more
    
* Use the `docker save` command to save an image to a tar archive.
    
* Save an image to a tar archive. The `docker save` command followed by the image name or ID and the output file path is used to save an image to a tar archive. For example, to save an image named "my-image" to a tar file called "my-image.tar", you can use the following command:
    
    ```plaintext
    $ docker save my-image -o my-image.tar
    
    [Saving the image to my-image.tar]
    ```
    
    This will create a tar archive containing the image.
    
* Use the `docker load` command to load an image from a tar archive.
    
    Load an image from a tar archive. The `docker load` command followed by the input file path is used to load an image from a tar archive. For example, to load an image from a tar file called "my-image.tar", you can use the following command:
    
    ```plaintext
    $ docker load -i my-image.tar
    
    [Loading the image from my-image.tar]
    ```
    
    This will load the image from the tar archive and make it available for use in Docker.
    

These tasks involve simple operations that can be used to manage images and containers.