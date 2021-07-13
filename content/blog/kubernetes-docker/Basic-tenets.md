---
title: 'Kubernetes - Lets learn the basic tenets '
date: 2021-05-18 13:00:00
category: 'Kubernetes / Docker'
draft: false
---

# <img src="https://img.shields.io/badge/kubernetes-326ce5.svg?&style=for-the-badge&logo=kubernetes&logoColor=white" style="vertical-align:middle" alt="react-badge"> - Let's Learn The Basic Tenets

# Introduction

Kubernetes is an open-source container orchestration tool that helps in managing containerized application services that consist of multiple containers, scheduling these containers across a cluster, scaling the containers, and manage their performance over time.

# What problems does <img src="https://img.shields.io/badge/kubernetes-326ce5.svg?&style=for-the-badge&logo=kubernetes&logoColor=white" style="vertical-align:middle" alt="react-badge"> solve?

If we consider microservices, which typically each run in their own containers, a containerized application might become hundreds or thousands of containers when building and operating a large-scale system. Significant complexity would be involved to manage these containers manually. Hence, this is where container orchestration can come in handy for making that operational complexity manageable for development and operations. Container orchestration technologies like Kubernetes automatically and continuously monitor the cluster of containers and make adjustments as required ensuring that there is no downtime in a production environment. For instance, if a container goes down, another container automatically takes its place without the end-user ever noticing.

# <img src="https://img.shields.io/badge/kubernetes-326ce5.svg?&style=for-the-badge&logo=kubernetes&logoColor=white" style="vertical-align:middle" alt="react-badge"> VS <img src="	https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white" style="vertical-align:middle" alt="react-badge">

Docker refers to a specific platform meant for building containerized applications, while Kubernetes is a container orchestration tool that aids in managing the container’s lifecycle. Docker Swarm is Docker’s own container orchestration tool that enables managing multiple containers deployed across multiple host machines.

<img src="https://editor.analyticsvidhya.com/uploads/85227PSLLpU1LQX8EY9LNae5tvSpq0BXn7DLhlI9VRp-rMxPxtqcbwa6EpAeQI6WFheKQZ4jtvJC2DgaSW9Ogs3ON5BksIKFgxNlczWKTrCI8k0WrBFMA2byFJElr3V-tfLDSV0C1eRE6.png" alt="Kubernetes vs docker" style="border-radius: 28px">
<a href="https://ubuntu.com/blog/kubernetes-versus-docker">image source</a>

# Basic Architecture of <img src="https://img.shields.io/badge/kubernetes-326ce5.svg?&style=for-the-badge&logo=kubernetes&logoColor=white" style="vertical-align:middle" alt="react-badge">

Like other distributed computing platforms, a kubernetes cluster has at least one master and multiple commpute nodes. The master node is the node that works on exposing the **_Application Program Interface_** (API), scheduling the deployments, and managing the overall cluster. Each of the worker nodes runs a container runtime, such as docker, along with an agent that communicates with master. The nodes can either be virtual machines(VM's) running in a cloud or physical servers runnin within a data center.

<img src="https://editor.analyticsvidhya.com/uploads/56634Picture1.png" style="width: 100%">

<a href="https://platform9.com/blog/kubernetes-enterprise-chapter-2-kubernetes-architecture-concepts/">image source</a>

# <img src="https://img.shields.io/badge/kubernetes-326ce5.svg?&style=for-the-badge&logo=kubernetes&logoColor=white" style="vertical-align:middle" alt="react-badge"> Master Node :

The master node receives input from a CLI or UI via an API. This input can be the commands that a developer provides to Kubernetes. For example, which container images are to be run, which ports are to be exposed, parameters of the desired state of the applications running in the cluster are defined by the developer/

1. **API Server:** Both internal & external components communicate through API server.

2. **Key-Value Store (etcd):** The key-value store acts as the single source of truth for all components present in the Kubernetes cluster. The master node asks the etcd for retriving parameters of the state of the nodes and containers.

3. **Controller:** A controller checks the state of the cluster and makes changes attempting to move it from current state to the desired state.

4. **Scheduler:** A scheduler looks for requests coming from the API Server and is responsible for assigning them to healthy nodes. It assesses the quality of the nodes and deploys pods to the best suited node.

# <img src="https://img.shields.io/badge/kubernetes-326ce5.svg?&style=for-the-badge&logo=kubernetes&logoColor=white" style="vertical-align:middle" alt="react-badge"> Worker Node:

Worker Nodes are responsible for executing the work assignments from the master Node are and reporting back the results to the master node.

1. **Kubelet:** Every node of the cluster has a ‘Kubelet’ which is the primary Kubernetes agent. Kubelet watches for tasks from the master node, executes them and then reports back the results to the master node. Additionally, it monitors the pods and reports back to the Master if a pod is dysfunctional.

2. **Container Runtime:** A container runtime executes containers and manages containers images on a node. For example, Docker is a popular container runtime.

3. **Kube-Proxy:** The Kube-proxy maintains network rules on each node and ensures that each node has anIP.

4. **Pob:** A pod constitutes one or more containers and includes shared storage (volumes), IP address, and information about how to run them.

# Running <img src="https://img.shields.io/badge/kubernetes-326ce5.svg?&style=for-the-badge&logo=kubernetes&logoColor=white" style="vertical-align:middle" alt="react-badge"> on Local Machine:

We can run Kubernetes on our local system, instead of a cloud service. For this, we would need to install two programs – <a href="https://minikube.sigs.k8s.io/docs/start/">Minikube</a> and <a href="https://kubernetes.io/docs/tasks/tools/">Kubectl</a>. Minikube allows us to **run a single-node Kubernetes cluster on our local computer**. Kubectl is a command-line tool for Kubernetes.

Minikube uses a hypervisor driver that varies by the operating system. This link has the list of drivers that one could use for setting up Minikube- <a href="https://minikube.sigs.k8s.io/docs/drivers/">https://minikube.sigs.k8s.io/docs/drivers/</a>

We will be using Docker as the hypervisor drive in this illustration. The hypervisor drive acts as an abstraction layer to separate the virtual machine from the system hardware.

<img src="https://editor.analyticsvidhya.com/uploads/20466Picture2.png" style="width: 95%; border-radius: 100px">

<a href="https://www.padok.fr/en/blog/minikube-kubeadm-kind-k3s">image source</a>

# Starting the cluster

To start the cluster, we can run the following command from the terminal with administrative access:

```
minikube start

```

In case Minikube fails to start, you can choose some other appropriate driver for setting up a compatible container or virtual machine manager.

As in the output, Minikube has used the docker driver for our case.

<img src="https://editor.analyticsvidhya.com/uploads/34131Picture4.png" alt="mike-kube output">

# Interacting with the cluster

We can interact with the created Kubernetes cluster using kubectl by running the following command

```
kubectl get po -A

```

This displays all the components of the Kubernetes cluster that have been created like etcd – minikube, Kube-apiserver-minikube, Kube-controller-manager-minikube, Kube-scheduler-minikube, etc. These, as the name indicates, are the components that we had discussed in the previous sections.

<img src="https://editor.analyticsvidhya.com/uploads/79054Picture5.png" alt="cluster interaction">

# Creating a sample deployment

We can use the following commands to create a deployment that manages a pod. This pod manages a container based on the Docker image provided

```
kubectl create deployment hello-world --image=k8s.gcr.io/echoserver:1.4

```

We can view the deployment using the command below:

```
kubectl get deployments

```

To run pods, we can run this command:

```
kubectl get pods

```

<img src="https://editor.analyticsvidhya.com/uploads/64891Picture6.png" alt="pods">

We can expose the deployment on a port:

```
kubectl expose deployment hello-world --type=NodePort --port=8080

```

To access the deployment, we can run the following command:

```
kubectl port-forward service/hello-world 7080:8080

```

<br><br><br>

**_Orchestration is the automated configuration, management, and coordination of computer systems, applications, and services._**
