---
title: Big Picture
linktitle: Big Picture
type: book
date: "2022-03-26T00:00:00+01:00"
tags:
  - Docker
  - Kubernetes
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 10
---

What is Kubernetes - Big picture

<!--more-->
### Overview

![k8s-ship](/images/uploads/k8s-ship.PNG)

Unless you have been hiding behind a 🗿 for the last few years "Breaking down the monolith" has been a theme across Software industry.  More than often application architectures evolved like below and Kubernetes has been heart and center of this evolution.

<img align="center" width="400" height="400" src="/images/uploads/monolith.PNG">

<center>To</center>

<img align="center" width="400" height="400" src="/images/uploads/k8s-microservices.png">  


**What is Kubernetes?**

Kubernetes is a portable, extensible, open-source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation.
> As per Kubernetes.io

---

### Architecture

When you deploy Kubernetes, you get a **cluster**.
A Kubernetes cluster consists of a set of worker machines, called **nodes**, that run containerized applications. Every cluster has at least one worker node. The worker node(s) host the Pods that are the components of the application workload. The **control plane** manages the worker nodes and the Pods in the cluster.

![k8s-cluster](/images/uploads/k8s-cluster.png)

Next we will look under the hood at a high level.

---

#### Control Plane

<img align="right" width="400" height="400" src="/images/uploads/k8s-master.png">

The **Control Plane** components make global decisions about the cluster (for example, scheduling, maintaining desired state). Can be setup as a Multi-Master H/A control plane. The master node does not run any containers in general. Let's breakdown further:

**Kube-ApiServer**

- Front-end to the control plane
- Exposes the API (REST)
- Consumes JSON/YAML

**Cluster Store (K-V)**

- Persists cluster state and config
- Based on etcd
- Performance is critical
- Have recovery plans in place

**Kube-ControllerManager**

- Controller of controllers
  - Node controller
  - Deployment controller
  - Endpoints/EndpointSlice controller…
- Watch loops
- Reconciles observed state with desired state

**Kube-Scheduler**

Watches API Server for new work tasks
- Assigns work to cluster nodes
- Affinity/Anti-affinity
- Constraints
- Taints
- Resources…

---

#### Nodes

<img align="right" width="400" height="400" src="/images/uploads/k8s-node.png">

**Node** components run on every node, maintaining running pods and providing the Kubernetes runtime environment

**Kubelet**

- Main Kubernetes agent
- Registers node with cluster
- Watches API Server for work tasks (Pods)
- Executes Pods
- Reports back to Masters

**Container Runtime**

- Can be Docker
- Pluggable: Implements Container Runtime Interface (CRI)
  - Docker, containerd, CRI-O, Kata…
- Low-level container intelligence

**Kube-Proxy**

- Networking component
- Pod IP addresses

---

### Concepts

#### Declarative Model and Desired State

Describe what you want **(Desired state)** in a manifest file.
It's **Declarative** since it does not specify the **HowTo** part, leaving that for Kubernetes to figure out.
<img align="center" width="400" height="400" src="/images/uploads/k8s-declarative-desired-state.png">

Internally within the Control Plane the following events would occur to get and maintain the **Desired** state.
![k8s-operation](/images/uploads/k8s-operation.png)

* **Client/Kubectl** calls **ApiServer{}** with your **Desired** state,
* **ApiServer{}** persists that in the **K-V** store,
* **Scheduler** schedules work to the Worker nodes to create **Desired** state,
* **Controller** would run **Watch/Reconciliation** loops to maintain **Desired** state.

---

#### Atomic unit

The Atomic unit of scheduling/scaling in the Kubernetes world is the **Pod**. Meaning you cannot run your containerized workload directly, it needs to be wrapped in a **Pod**.

So what does a **Pod** give?

* It gives a **Shared Execution Environment** for the Containers.
  <img align="center" width="400" height="500" src="/images/uploads/k8s-pods.png">

* Unless you have a Specialist Use Case where a <hlpr> container enhances the <app> container functionality, it's best practice to keep the containers loosely coupled, i.e in all typical application use cases you would connect them via  Networking.
  ![k8s-coupling](/images/uploads/k8s-pods-coupling.png)

* Scaling in Kubernetes happens by adding/removing **Pods**, not **Containers**
  ![k8s-scaling](/images/uploads/k8s-pods-scaling.png)


#### Stable Networking with Services

#### Deployments

#### K8s API and API Server
