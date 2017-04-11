---
layout: single
title: Kubernetes Setup & Management - Failure Recovery
permalink: /k8s/failurerecovery
sidebar:
  nav: "docs"
---
If a host enters reconnecting/disconnected state, attempt to re-run the agent registration command. Wait 3 minutes. If the host hasn’t re-entered active state, add a new host with similar resources and host labels. Delete the old host from the environment. Containers will be scheduled to the new host and eventually become healthy.


