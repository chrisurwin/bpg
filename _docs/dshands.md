---
layout: single
title: Rancher Deployment Strategies - Hub & Spoke
permalink: /deploymentstrategies/hands
sidebar:
  nav: "docs"
---
<img src="../media/image1.png" width="624" height="351" />
<p>In this deployment scenario, there is a single Rancher control plane managing compute resources across the globe. The control plane would be run in an HA configuration, and there would be impact due to latencies.</p>
<b>Pros:</b>
<p>
<li>Environments could have nodes and network connectivity across regions.</li>
<li>Single control plane interface to view/see all regions and environments.</li></p>
<b>Cons:</b>
<p>
<li>Subject to network latencies</li>
<li>If control plane goes out global provisioning of new services is unavailable until restored.</li></p>
