---
layout: single
author_profile: true
title: Kubernetes Setup & Management - Restoring Backups
permalink: /k8s/restoringbackups
sidebar:
  nav: "docs"
---
Backup restoration will only work for Resilient Separated-Planes deployments. If all hosts running etcd fail, follow these steps:
<li>Change your environment type to <i>Cattle</i>. This will tear down the Kubernetes system stack. Pods (the Compute plane) will remain intact and available</li>
<li>Delete reconnecting/disconnected hosts and add new hosts if you need them</li>
<li>Ensure at least one host is labelled <i>etcd=true</i></li>
<li>For each <i>etcd=true</i> host, mount the network storage containing backups - see <a href="./remotebackups">Configuring Remote Backups</a> section for details. Then run these commands:</li>
```#configure this to point to the desired backup in /var/etcd/backups```<br>
```target=2016-08-26T16:36:46Z_etcd_1```<br>
```don’t touch anything below this line```<br>
```docker volume rm etcd docker volume create --name etcd docker run -d -v etcd:/data --name etcd-restore busybox docker cp /var/etcd/backups/$target etcd-restore:/data/data.current docker rm etcd-restore```
> Note - you must be logged in as a user with read access to the remote backups. Otherwise, the docker cp command will silently fail
<li>Change your environment type back to Kubernetes. The system stack will launch and your pods will be reconciled. Your backup may reflect a different deployment topology than what currently exists; pods may be deleted/recreated</li>


