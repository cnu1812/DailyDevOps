## Monolithic Applications

Imagine a team develops a booking application using a monolithic approach. In this case, the UI is the website that the user interacts with. The business logic contains the code that provides the booking functionalities, such as search, booking, payment, and so on. These are written using one programming language (e.g. Java or Go) and stored in a single repository. The data layer contains functions that store and retrieve customer data. All of these components are managed as a unit, and the release is done using a single binary.


![mono](https://user-images.githubusercontent.com/75531528/157446111-70946705-a5a7-40a7-ac3f-b5d068ea0773.png)

In a monolithic architecture, application tiers can be described as:

- part of the same unit
- managed in a single repository
- sharing existing resources (e.g. CPU and memory)
- developed in one programming language
- released using a single binary

## Microservices

Now, let's imagine the team develops a booking application using a microservice approach.

In this case, the UI remains the website that the user interacts with. However, the business logic is split into smaller, independent units, such as login, payment, confirmation, and many more. These units are stored in separate repositories and are written using the programming language of choice (e.g. Go for the payment service and Python for login service). To interact with other services, each unit exposes an API. And lastly, the data layer contains functions that store and retrieve customer and order data. As expected, each unit is released using its own binary.

![micro](https://user-images.githubusercontent.com/75531528/157449331-4518deb2-797c-44e4-aa9a-3045fb7638c9.png)


In a microservice architecture, application tiers are managed independently, as different units. Each unit has the following characteristics:

- managed in a separate repository
- own allocated resources (e.g. CPU and memory)
- well-defined API (Application Programming Interface) for connection to other units
- implemented using the programming language of choice
- released using its own binary




## What is kubernetes in nutshell?

Let’s say you created an application(e.g Pokemon go) and decided to share it with the world. How can you do that? by deploying it to the internet. So you deployed this application into 5 different servers using docker. And your application starts getting massive traffic even you are not imagined. Millions of users started using. You are happy on one side simultaneously you are sad because you have to scale up the servers because 5 are not enough for such massive traffic. Now you need to scale up fast and make sure all containers restart if they die. And you will be gone out of control.
This is where Kubernetes comes into play.

## What is Kubernetes?

Kubernetes is an open-source container orchestration system for automating software deployment, scaling, and management.

A container orchestrator framework is capable to create, manage, configure thousands of containers on a set of distributed servers while preserving the connectivity and reachability of these containers. In the past years, multiple tools emerged within the landscape to provide these capabilities, including Docker Swarm, Apache Mesos, CoreOS Fleet, and many more. However, Kubernetes took the lead in defining the principles of how to run containerized workloads on a distributed amount of machines.

Kubernetes is widely adopted in the industry today, with most organizations using it in production. Kubernetes currently is a graduated CNCF project, which highlights its maturity and reported success from end-user companies. This is because Kubernetes solutionizes portability, scalability, resilience, service discovery, extensibility, and operational cost of containers.

## Kubernetes Architecture

![image](https://video.udacity-data.com/topher/2020/December/5fdfdd93_screenshot-2020-12-20-at-23.25.47/screenshot-2020-12-20-at-23.25.47.png)

A Kubernetes cluster is composed of a collection of distributed physical or virtual servers. These are called nodes. Nodes are categorized into 2 main types: master and worker nodes. The components installed on a node, determine the functionality of a node, and identifies it as a master or worker node.

### Control Plane (Master Node)

image

The control plane consists of components that make global decisions about the cluster. These components are the:

kube-apiserver
kube-scheduler
kube-controlmanager
etcd
kubelet
kubeproxcy

## kubectl and minikube installation

## Example pod, deployment


