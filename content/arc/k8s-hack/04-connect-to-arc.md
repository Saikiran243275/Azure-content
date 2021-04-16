---
title: "Connect to Arc"
description: "Connect clusters to Azure Arc."
slug: connect-to-arc
menu:
  side:
    parent: arc-k8s-hack
    identifier: arc-k8s-connect-arc
series:
 - arc-k8s-hack
weight: 4
---

## Background

*Persona: Cluster Administrator*

You want to add Azure Arc to a number of clusters to give a centralised management approach for tagging and deployment of resources.

It is important to consider the structure of subscription/resource groups, how tags are applied and appropriate Role-based access control (RBAC)

**TODO: Update this to Flux v2**

Azure Arc for Kubernetes is based upon the CNCF incubation project Flux (version 1) by Weaveworks.

An agent runs within your cluster and reconciles desired vs actual state.

## Challenge

Connect Kubernetes clusters to Azure Arc.

You will need several key components in order to connect your cluster to Azure Arc.

* Access to the Azure CLI
* Access to your Kubernetes cluster(s)
* The correct extensions and providers registered in your Azure subscription

When connected to Arc, what information can you get from the Resource Graph?

**TODO**: Get some standard, useful information from resource graph

For example:
```
resources
| where type == 'microsoft.kubernetes/connectedclusters'
```

**Stretch** How would you automate onboarding of clusters to Arc?

## Success Criteria

* An Azure Arc enabled Kubernetes resource exists in Azure Resource Manager
* Cluster metadata appears on the Azure Arc enabled Kubernetes resource as metadata
  * Distribution
  * Kubernetes version
* Show some metadata from the Resource Graph

## References

* [Accessing a Kubernetes cluster](https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/#set-the-kubeconfig-environment-variable)
* [Connect an existing Kubernetes cluster to Azure Arc](https://docs.microsoft.com/azure/azure-arc/kubernetes/quickstart-connect-cluster)
* [Flux concepts](https://fluxcd.io/docs/concepts/)