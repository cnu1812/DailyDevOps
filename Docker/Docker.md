## What problem Docker solves..?

Whenever a developer develops any product there are certain issues which are probably almost every time occurs. Well, that problem is whenever you are designing a project it works fine in your machine(the developer machine). But as soon as that project is moved on the production state may be on the servers (or) maybe somebody’s else computer in that case the project usually fails to work with the same performance (or) optimization when it is moved from one computer to another. So the classic problem is “it works on my machine”. Docker is designed to specifically address this exact problem “It works on my machine”.

### Virtual Machine

A virtual machine (VM) is a virtual environment that works like a computer within a computer. It runs on an isolated partition of its host computer with its own CPU power, memory, operating system, and other resources. End users can run applications on VMs and use them as they normally would on their workstation. For example you can use both windows and linux OS in same computer.

An application on a VM requires a guest OS and thus an underlying hypervisor to run.

### Container

![image](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQtjxqboLPLA4zC43dSFej0Fx61z2u1WC0t2w&usqp=CAU)

A container is a runnable instance of an image. This is where your application is running. In simple works it packages up code and all it's dependencies in a box called container.


## Containers VS Virual Machines


![Container Vs VM](https://user-images.githubusercontent.com/75531528/154963018-417e7334-47bb-4c18-9c97-1748eb73b1d2.png)

Hypervisor is used to create multiple machines on a host operating system and it manages virtual machines.


## What is docker?

Docker is a container platform which allows you to build, test and deploy applications quickly.

![Untitled-2022-02-21-1834](https://user-images.githubusercontent.com/75531528/154963216-873514ab-5d0d-4b79-b29b-c284c4f3b1ac.png)


### OCI (Open Container Initiative)

OCI was a process which defines two container related specifications:

- Image Spec
- Container runtime Spec.
- runc
- containerd

Docker uses these two specification in its different layers of Docker Engine Architecture.

### Docker Engine Architecture


![Untitled-2022-02-22-1748](https://user-images.githubusercontent.com/75531528/155137540-e4439bb8-cb70-421e-b46b-5fa4ce5e2e5a.png)

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

Docker can build images automatically by reading instructions from a DockerFile. A single image can be used to create multiple containers.


![Untitled-2022-02-21-1912](https://user-images.githubusercontent.com/75531528/154968456-4b3b3ce8-f6c0-4ef2-9bf9-a2c40be57fba.png)

[Dockerfile](https://github.com/cnu1812/DailyDevOps/blob/master/Docker/Dockerfile) commands explanation

- `From`: which tells us what image to base this off of. This is the multi-layered approach that makes Docker so efficient and powerful. In this instance, it’s using the php:5.6-apache Docker image, which again references a Dockerfile to automate the build process.
- `Run`:  Before building an image if want some configuration that needs to be present in the image. Basically any prerequities required to run an image.
- `Maintainer`: Gives the information about the author or manager who is managing this image.
- `Expose`: This command is used to specify the port number in which the container is running its process.
- `CMD`:  To run a command as soon as container is launched. CMD command is different from RUN because RUN is used at the time of building an image and CMD used to run command when container is started.
- `ENV`: This sets the environment variables, which can be used in the Dockerfile and any scripts that it calls. These are persistent with the container too, so they can be referenced at any time. In the case of the WordPress Dockerfile, we can see that it sets the version number, the upstream version number, and then the SHA1 hash of the download.
- `COPY`: It can copy a file (in the same directory as the Dockerfile) to the container. You can do this for things like custom configuration files or like in this instance, a file to run commands after the container has been set up.

## Docker Components

![image](https://dev-to-uploads.s3.amazonaws.com/i/o2dmqkdzcscl4atbhoj3.png)

## Docker Image

- Docker Image is run to create a docker container. Images are immutable. Once built, the files making up an image do not change. Images can be stored locally or remote locations like hub.docker.com.
- Images are built in layers. Each layer is an immutable file, but is a collection of files and directories. The last layer can be used to write out data to. Layers receive an ID, calculated via a SHA 256 hash of the layer contents.The Image ID listed by docker commands (ie ‘docker images’) is the first 12 characters of the hash. These hash values are referred to by ‘tag’ names.
- Command used to list hash values ` docker images -q --no-trunc`.

## Basic Commands

` docker ps`__ List all containers.

` docker run ImageName/ID `__ Runs the image. If image is not present locally then it will pull from docker hub.

` docker start ContainerName/ID`__ starts the container.

` docker kill ContainerName/ID`__ Stops a running container.

` docker rm ContainerName/ID`__ Deletes a stopped container.

` docker rm $(docker ps -a -q)`__ Delete all stopped containers.

`docker images -q --no-trunc`__ lista the hash value.

` docker pull ngnix:latest ` (latest is tag/version)__ Pulls the image from docke hub.

` docker images `__ Lists Docker Images.

` docker rmi image`__ deletes a Docker Image if no container is using it.

` docker rmi $(docker images -q)`__ deletes all Docker images.






