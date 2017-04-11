---
layout: single
title: Kubernetes Setup & Management
permalink: /k8s/planes
sidebar:
  nav: "docs"
---

<p><img src="../../media/image013.png" width="624" height="351" /></p>

For production deployments, it is best practice that each plane runs on dedicated physical or virtual hosts. For development, multi-tenancy may be used to simplify management and reduce costs.
Data Plane
Comprised of one or more Etcd nodes which persist state regarding the Compute Plane. Resiliency is achieved by adding 3 hosts to this plane.
Orchestration Plane
Comprised of stateless Kubernetes/Rancher components which orchestrate and manage the Compute Plane:
•	apiserver
•	scheduler
•	controller-manager
•	kubectld
•	rancher-kubernetes-agent
•	rancher-ingress-controller) Resiliency is achieved by adding 2 hosts to this plane.
Compute Plane
Comprised of the real workload (Kubernetes pods), orchestrated and managed by Kubernetes.

