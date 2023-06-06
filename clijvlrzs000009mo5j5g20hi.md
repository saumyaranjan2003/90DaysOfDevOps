---
title: "Day 17 Task: Docker Project for DevOps Engineers."
datePublished: Tue Jun 06 2023 06:04:29 GMT+0000 (Coordinated Universal Time)
cuid: clijvlrzs000009mo5j5g20hi
slug: day-17-task-docker-project-for-devops-engineers
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1686029580032/31aa287d-c0e9-459a-8283-bf372feb7bae.png
tags: docker, aws, python, reactjs, devops

---

### Dockerfile

Docker is a tool that makes it easy to run applications in containers. Containers are like small packages that hold everything an application needs to run. To create these containers, developers use something called a Dockerfile.

A Dockerfile is like a set of instructions for making a container. It tells Docker what base image to use, what commands to run, and what files to include. For example, if you were making a container for a website, the Dockerfile might tell Docker to use an official web server image, copy the files for your website into the container, and start the web server when the container starts.

Here are some of the most commonly used commands in a Dockerfile:

**FROM**: Specifies the base image that the new image will be built on top of. For example, you might use an official Node.js image as the base for an application that runs on Node.js.

**RUN**: Executes a command in the image. This command is run during the image build process. For example, you might use the RUN command to install necessary packages or dependencies for your application.

**COPY**: Copies files from the host machine to the image. For example, you might use the COPY command to copy the files for your application into the image.

**ENV:** Sets an environment variable in the image. For example, you might use the ENV command to set a variable that holds the version of your application.

**EXPOSE**: Specifies the ports that should be exposed on the container. For example, you might use the EXPOSE command to specify that port 8000 should be exposed on the container.

**CMD**: Specifies the command that should be run when a container is created from the image. For example, you might use the CMD command to specify that your application should be started when the container is created.

```plaintext
FROM ubuntu:18.04
COPY . /app
RUN make /app
CMD python /app/app.py
```

Each instruction creates one layer:

* `FROM` creates a layer from the `ubuntu:18.04` Docker image.
    
* `COPY` adds files from your Docker client’s current directory.
    
* `RUN` builds your application with `make`.
    
* `CMD` specifies what command to run within the container.
    

Once the image is created from the Dockerfile, you can use it to create as many containers as you want. Each container will be the same and will run the same way.

task:

* Create a Dockerfile for a simple web application (e.g. a Node.js or Python app)
    
* we are writing a docker file for react-django-app
    
    ```plaintext
    FROM python:3.9 
    COPY . . 
    RUN pip install -r requirements.txt 
    CMD ["python","manage.py","runserver","0.0.0.0:8000"]
    ```
    
* Build the image using the Dockerfile and run the container
    
    ```plaintext
    docker build . -t react-django-app:latest
    ```
    
* Verify that the application is working as expected by accessing it in a web browser
    
* ```plaintext
    docker run -d -p 8000:8000 react-django-app:latest
    ```
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686030555282/1ce9fcaf-b931-4ce1-828d-9ab1d2018327.png align="center")
    
    after the docker run -d -p command if you are using any cloud-vm so kindly add the port to the security group. for aws -&gt; edit bound (TCP-Port-num-anywhere ipv4)-&gt;ok
    
* copy the ip paste it into the browser. then your ip:port-num