---
layout: single
title: Rancher Proof of Concept/Home Lab/Hello World Environments
permalink: /scaling/poc
sidebar:
  nav: "docs"
---

<p><img src="../media/image005.png" width="624" height="351" /></p>

<p>Run server and agent on a single node to running 5-10 agent nodes. A 4GB multi core VM/server should be used for the Rancher server agent combo node. Other nodes can be tailored to your needs. <p>
<p>If you plan to use a single server and more then 1 or 2 environments with a few hosts each, it would be best to create an external Database. This can be an RDS instance or another VM that runs MySQL. Alternatively, you could use more memory and give the MySQL directory its own block device/volume. The disk supporting MySQL should be as fast as possible.<p>
<p>In this type of environment, you would want your Rancher server to have a minimum:
<li>1GB of Ram</li>
<li>1xCPU core</li>
</p><p>
If you are running an agent on the server it is recommended to use at least to account for additional workload added by user containers:
<li>2GB of Ram</li>
<li>2xCPU cores</li>

