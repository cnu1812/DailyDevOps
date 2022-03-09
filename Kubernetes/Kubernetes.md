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




## What is kubernetes in nutshell?

Let’s say you created an application(e.g Pokemon go) and decided to share it with the world. How can you do that? by deploying it to the internet. So you deployed this application into 5 different servers using docker. And your application starts getting massive traffic even you are not imagined. Millions of users started using. You are happy on one side simultaneously you are sad because you have to scale up the servers because 5 are not enough for such massive traffic. Now you need to scale up fast and make sure all containers restart if they die. And you will be gone out of control.
This is where Kubernetes comes into play.

## What is Kubernetes?

Kubernetes is an open-source container orchestration system for automating software deployment, scaling, and management.

## kubectl and minikube installation

## Example pod, deployment


