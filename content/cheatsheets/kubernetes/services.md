---
title: Services
linktitle: Services
type: book
date: "2022-03-26T00:00:00+01:00"
tags:
  - Docker
  - Kubernetes
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 30
---

Kubernetes Networking with Services

<!--more-->
### Overview

Kubernetes **Service** object is the way in Kubernetes to expose applications, both on the network and to the outside world. Exposing the app could be ```external``` like from a web browser and ```internal``` like accessing it from maybe another Pod or application on the same cluster that's talking to it.

🥁 Services nail both these scenarios. 

![k8s-services-apiserver](/images/uploads/k8s-services-apiserver.png)

It is a high‑level stable abstraction point for multiple Pods.
![k8s-services-clusterIP](/images/uploads/k8s-services-clusterIP.png)
![k8s-services-internal-access](/images/uploads/k8s-services-internal-access.png)
![k8s-services-nodeport](/images/uploads/k8s-services-external-access-nodeport.png)
![k8s-services-loadbalancer](/images/uploads/k8s-services-external-access-loadbalancer.png)
