---
layout: single
author_profile: true
title: Kubernetes Setup & Management - Remote Backups
permalink: /k8s/tearingdown
sidebar:
  nav: "docs"
---

After tearing a down a Kubernetes stack, persistent data is left behind. A user may choose to manually delete this data if they wish to repurpose/reuse the hosts.
<li>A named volume etcd will exist on all hosts which ran etcd at some point. Run docker volume rm etcd on each host to delete it</li>
<li>Backups are enabled by default and stored to /var/etcd/backups on hosts running etcd. Run rm -r /var/etcd/backups/* on one host (if network storage was mounted) or all hosts (if no network storage was mounted) to delete the backups</li>



