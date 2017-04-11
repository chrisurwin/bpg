---
layout: single
title: Kubernetes - Resilient Separated Planes
permalink: /k8s/resilientsp
sidebar:
  nav: "docs"
---

Characteristics
•	Data Plane resilient to minority of hosts failing
•	Orchestration Plane resilient to all but one host failing
•	Compute Plane resiliency depends on the deployment plan
•	High-performance, production-ready environment
Instructions (Rancher v1.2+)
1.	Create a Cattle environment.
2.	Add 3 hosts with 1 CPU, >=1.5GB RAM, >=20GB DISK. Label these hosts etcd=true.
i.	If you care about backups, see Configuring Remote Backups now.
ii.	If you don’t want pods scheduled on these hosts add label nopods=true.
3.	Add 2 hosts with >=1 CPU and >=2GB RAM. Label these hosts orchestration=true.
i.	If you don’t want pods scheduled on these hosts, add label nopods=true.
4.	Add 1+ hosts without any special labels. Resource requirements vary by workload.
5.	Navigate to Catalog > Library. On the Kubernetes catalog item, click View Details. Select your desired version, optionally update configuration options, and click Launch.
Instructions (Rancher v1.1.X and older)
1.	Create a Cattle environment.
2.	Add 3 hosts with 1 CPU, >=1.5GB RAM, >=20GB DISK. Label these hosts etcd=true.
i.	If you care about backups, see Configuring Remote Backups now.
ii.	If you don’t want pods scheduled on these hosts add label nopods=true.
3.	Add 2 hosts with >=1 CPU and >=2GB RAM. Label these hosts orchestration=true.
i.	If you don’t want pods scheduled on these hosts, add label nopods=true.
4.	Add 1+ hosts without any special labels. Resource requirements vary by workload.
5.	Edit the environment and select Kubernetes.
