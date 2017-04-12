---
layout: single
author_profile: true
title: Kubernetes - Resilient Separated Planes
permalink: /k8s/resilientsp
sidebar:
  nav: "docs"
---


<b>Characteristics</b><br>
<li>Data Plane resilient to minority of hosts failing</li>
<li>Orchestration Plane resilient to all but one host failing</li>
<li>Compute Plane resiliency depends on the deployment plan</li>
<li>High-performance, production-ready environment</li>
<br>
<b>Instructions<b>
<ol>
<li>Create a Cattle environment</li>
<li>Add 3 hosts with 1 CPU, >=1.5GB RAM, >=20GB DISK. Label these hosts etcd=true <ol type="i"><li> If you care about backups, see <a href="./remotebackups">Configuring Remote Backups</a> now.</li>
<li>If you don’t want pods scheduled on these hosts add label nopods=true.</li></ol></li>
<li>Add 2 hosts with >=1 CPU and >=2GB RAM. Label these hosts orchestration=true <ol type="i"><li>If you don’t want pods scheduled on these hosts, add label nopods=true</li></ol></li>
<li>Add 1+ hosts without any special labels. Resource requirements vary by workload.</li>
<li>Navigate to Catalog > Library. On the Kubernetes catalog item, click View Details. Select your desired version, optionally update configuration options, and click Launch.
</li>
</ol>
<b>Instructions (Rancher v1.1.X and older)</b>
<ol>
<li>Create a Cattle environment.</li>
<li>Add 3 hosts with 1 CPU, >=1.5GB RAM, >=20GB DISK. Label these hosts etcd=true <ol type="i"><li>If you care about backups, see Configuring Remote Backups now</li>
<li>If you don’t want pods scheduled on these hosts add label nopods=true.</li></ol></li>
<li>Add 2 hosts with >=1 CPU and >=2GB RAM. Label these hosts orchestration=true <ol type="i"><li>If you don’t want pods scheduled on these hosts, add label nopods=true</li></ol></li>
<li>Add 1+ hosts without any special labels. Resource requirements vary by workload.</li>
<li>Edit the environment and select Kubernetes</li>
</ol>	

