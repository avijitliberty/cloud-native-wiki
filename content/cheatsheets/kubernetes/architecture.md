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

<img align="left" width="350" height="350" src="/images/uploads/monolith.PNG">
<img align="right" width="400" height="400" src="/images/uploads/k8s-microservices.png">  

**What is Kubernetes?**

Kubernetes is a portable, extensible, open-source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation.
> As per Kubernetes.io

### Architecture


When you deploy Kubernetes, you get a **cluster**.
A Kubernetes cluster consists of a set of worker machines, called **nodes**, that run containerized applications. Every cluster has at least one worker node. The worker node(s) host the Pods that are the components of the application workload. The **control plane** manages the worker nodes and the Pods in the cluster.

![k8s-cluster](/images/uploads/k8s-cluster.png)

Next we will look under the hood at a high level.

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
