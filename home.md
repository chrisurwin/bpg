---
layout: page
title: Rancher Deployment Strategies
permalink: /home/
---
<p><strong>Hub and spoke</strong></p>
<p><img src="../media/image1.png" width="624" height="351" /></p>
<p>In this deployment scenario, there is a single Rancher control plane managing compute resources across the globe. The control plane would be run in an HA configuration, and there would be impact due to latencies.</p>
<p>Pros:</p>
<p>Environments could have nodes and network connectivity across regions.</p>
<p>Single control plane interface to view/see all regions and environments.</p>
<p>Cons:</p>
<p>Subject to network latencies</p>
<p>If control plane goes out global provisioning of new services is unavailable until restored.</p>
<p><strong>Regional Deployment Model</strong></p>
<p><img src="../media/image2.png" width="624" height="261" /></p>
<p>In the regional deployment model a control plane is deployed in close proximity to the compute nodes.</p>
<p>Pros:</p>
<p>Provisioning in regions stay functioning if a control plane in another region go down.</p>
<p>Cons:</p>
<p>Overhead of managing multiple Rancher installations.</p>