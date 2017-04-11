---
layout: single
title: Rancher Deployment Strategies - Hub & Spoke
permalink: /deploymentstrategies/hands
sidebar:
  nav: "docs"
---
<p><img src="/media/image1.png" width="624" height="351" /></p>
<p>In this deployment scenario, there is a single Rancher control plane managing compute resources across the globe. The control plane would be run in an HA configuration, and there would be impact due to latencies.</p>
<p>Pros:</p>
<p>Environments could have nodes and network connectivity across regions.</p>
<p>Single control plane interface to view/see all regions and environments.</p>
<p>Cons:</p>
<p>Subject to network latencies</p>
<p>If control plane goes out global provisioning of new services is unavailable until restored.</p>
