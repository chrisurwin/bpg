---
layout: single
author_profile: true
title: Kubernetes Setup & Management - Deployment Migrations
permalink: /k8s/migrations
sidebar:
  nav: "docs"
---

Any deployment plan may be migrated to any other deployment plan. For resilient deployment targets, this involves no downtime. If your desired migration is not listed, we don’t officially support it – but it is possible. Contact Rancher for further instruction. <br>
Standalone to Overlapping-Planes
<li>Add 2 more hosts to the environment. The deployment automatically scales up.<li>
Overlapping-Planes to Separated-Planes
<li>Add 3+ hosts to the environment. Ensure resource requirements are satisfied and create host labels as defined in the Separated-Planes deployment instructions</li>
<li>For etcd containers not on etcd=true hosts, migration is necessary. Delete one data sidekick container of an etcd. Ensure it is recreated on a correct host and becomes healthy (green circle) before continuing. Repeat this process as is necessary</li>
<li>For kubernetes, scheduler, controller-manager, kubectld, rancher-kubernetes-agent, rancher-ingress-controller containers not on the orchestration=true host, delete the containers</li>
<li>Make note of etcd=true and orchestration=true hostnames. From kubectl, type kubectl delete node <hostname> to remove the hosts from the Compute Plane. Wait until all pods on etcd=true, orchestration=true hosts are deleted. At this point, delete kubelet and proxy containers from these hosts</li>


