## What problem Docker solves..?

Whenever a developer develops any product there are certain issues which are probably almost every time occurs. Well, that problem is whenever you are designing a project it works fine in your machine(the developer machine). But as soon as that project is moved on the production state may be on the servers (or) maybe somebody’s else computer in that case the project usually fails to work with the same performance (or) optimization when it is moved from one computer to another. So the classic problem is “it works on my machine”. Docker is designed to specifically address this exact problem “It works on my machine”.

### Virtual Machine

A virtual machine (VM) is a virtual environment that works like a computer within a computer. It runs on an isolated partition of its host computer with its own CPU power, memory, operating system, and other resources. End users can run applications on VMs and use them as they normally would on their workstation. For example you can use both windows and linux OS in same computer.

An application on a VM requires a guest OS and thus an underlying hypervisor to run.

### Container

![image](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQtjxqboLPLA4zC43dSFej0Fx61z2u1WC0t2w&usqp=CAU)

A container is a runnable instance of an image. This is where your application is running. In simple works it packages up code and all it's dependencies in a box called container.


## Containers VS Virual Machines

Hypervisor is used to create multiple machines on a host operating system and it manages virtual machines.


## What is docker?

Docker is a container platform which allows you to build, test and deploy applications quickly.

### Runtime
- runc
- containerd

## Docker Architecture

![image](https://dev-to-uploads.s3.amazonaws.com/i/dmgpglab3k1z23g02cr5.png)

## Docker daemon

It listens to the API requests being made through the Docker client and manages Docker objects such as images, containers, networks, and volumes.

## Docker client

This is what you use to interact with Docker. When you run a command using docker, the client sends the command to the daemon, which carries them out. The Docker client can communicate with more than one daemon.

## Docker registries

This is where Docker images are stored. Docker Hub is a public registry that anyone can use. When you pull an image, Docker by default looks for it in the public registry and saves the image on your local system on DOCKER_HOST. You can also store images on your local machine or push them to the public registry.

## Dockerfile

Describes steps to create a Docker image. It’s like a recipe with all ingredients and steps necessary in making your dish. This file can be used to create Docker Image. These images can be pulled to create containers in any environment. These images can also be store online at docker hubs. When you run docker image you get docker containers. The container will have the application with all its dependencies.

Dockerfile commands explanation

- `Run`:  Before building an image if want some configuration that needs to be present in the image. Basically any prerequities required to run an image.
- `Maintainer`: Gives the information about the author or manager who is managing this image.
- `Expose`: This command is used to specify the port number in which the container is running its process.
- `CMD`:  To run a command as soon as container is launched. CMD command is different from RUN because RUN is used at the time of building an image and CMD used to run command when container is started.





