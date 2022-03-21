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

![Untitled-2022-02-25-1155](https://user-images.githubusercontent.com/75531528/157451578-b8449549-9746-46c4-982f-86965525b57b.png)


The control plane consists of components that make global decisions about the cluster. These components are the:

- **kube-apiserver:** Gatekeeper for the entire cluster. CRUD operations for servers go through the API. API server configures the API objects such as pods, services, replication controllers () and deployments. It exposes API for almost every operation. How to interact with this API? Using a tool called kubectl aka kubecontrol. It talks to the API server to perform any operations that we issue from cmd. In most cases, the master node does not contain containers. It just manages worker nodes, and also makes sure that the cluster of worker nodes are running healthy and successfully.

- **kube-scheduler:**It is responsible for physically scheduling Pods across multiple nodes. Depending upon the constraints mentioned in the configuration file, scheduler schedules these Pods accordingly. For example, if you mention CPU has 1 core, memory is 10 GB, DiskType is SSD, etc. Once this artifact is passed to API server, the scheduler will look for the appropriate nodes that meet these criteria & will schedule the Pods accordingly.

- **kube-controlmanager:** The component that handles controller processes. It ensures that the desired configuration is propagated to resources

- **etcd:** Distributed key-value lightweight database. Central database to store current cluster state at any point of time. Any component of Kubernetes can query etcd to understand the state of the cluster so this is going to be the single source of truth for all the nodes, components and the masters that are forming Kubernetes cluster.

- **kubelet:**  The agent that runs on every node and notifies the kube- apiserver that this node is part of the cluster.

- **kubeproxy:** Responsible for maintaining the entire network configuration. It maintains the distributed network across all the nodes, across all the pods, and all containers. Also exposes services to the outside world. It is the core networking component inside Kubernetes. The kube-proxy will feed its information about what pods are on this node to iptables. iptables is a firewall in Linux and can route traffic. So when a new pod is launched, kube-proxy is going to change the iptable rules to make sure that this pod is routable within the cluster.

## kubectl and minikube installation
- Before installing kubectl and minikube, you have to install either docker desktop or any virtual machine. Docker desktop is recomended.
- kubectl is command line tool can install [here](https://kubernetes.io/docs/tasks/tools) download the latest release for your according operating system.
- Then install the [minikube](https://minikube.sigs.k8s.io/docs/start/)  and set your path-variables so that your system can recognize kubectl commands.
- Use this commands to get started

       minikube version
       minikube start --driver=docker
       minikube status
       kubectl cluster-info
       get node
- Stuck anywhere you can refer [this](https://www.youtube.com/watch?v=xhxmExC9N1U&t=1305s)

## Example pod, deployment


